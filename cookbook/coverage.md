# Code Coverage

We want to maintain high test coverage for all our software, and a good way to 
ensure we do that is to measure it regularly. All DRDS projects should measure
test coverage as part of the CI process, and if test coverage drops then a PR 
should fail. 

There are two ways we enforce test coverage:

## 1. Coveralls

[Coveralls](https://coveralls.io/github/pulibrary) is an automated tool for measuring
and reporting test coverage. It is easy to integrate with CircleCI, the CI system
we use most often. 

To add coveralls: 

1. Go to https://coveralls.io/github/pulibrary and add the github repository of the 
project you want to add. 
2. Follow the coveralls installation instructions.
3. Add the coveralls API key as an environment variable in CircleCI as `COVERALLS_REPO_TOKEN`
4. Edit the CircleCI config to run the tests like this:
```ruby
COVERALLS_REPO_TOKEN=$COVERALLS_REPO_TOKEN bundle exec rspec spec
```

## 2. Not coveralls

Although many of our applications use coveralls, some applications have achieved 
100% code coverage and the team would prefer not to pay the performance penalty 
that comes with calculating coverage via coveralls. Once a project has 100% test
coverage, you can instead set it up like this: 

1. To `.circleci/config.yml`, add a stanza under `jobs` for `coverage_report`:
```
coverage_report:
  executor: abid-executor
  steps:
    - attach_workspace:
        at: '~/abid'
    - run: gem install simplecov
    - run:
        name: Inspect coverage report
        command: |
          RAILS_ENV=test ruby ./scripts/report_coverage.rb
    - store_artifacts:
        path: ~/abid/coverage
        destination: coverage
```
1. Add a section to `workflows` to ensure that `coverage_report` is run:
```
workflows:
  build_accept:
    jobs:
      - build
      - rubocop:
         requires:
          - build
      - test:
         requires:
          - build
      - coverage_report:
         requires:
          - test
```
1. Add this file to `scripts/report_coverage.rb` in the project:
```ruby
  # frozen_string_literal: true

  require "simplecov"

  class SimpleCovHelper
    def self.report_coverage(base_dir: "./coverage")
      SimpleCov.configure do
        minimum_coverage(100)
      end
      new(base_dir: base_dir).inspect_results
    end

    attr_reader :base_dir

    def initialize(base_dir:)
      @base_dir = base_dir
    end

    def results_file
      Pathname "#{base_dir}/.resultset.json"
    end

    def inspect_results
      results = SimpleCov::Result.from_hash(JSON.parse(File.read(results_file))).first
      results.format!
      covered_percent = results.covered_percent.round(2)
      min_coverage = SimpleCov.minimum_coverage
      min_coverage = min_coverage[:line].to_f if min_coverage.is_a? Hash
      return unless covered_percent < min_coverage
      $stderr.printf("Coverage (%.2f%%) is below the expected minimum coverage (%.2f%%).\n", covered_percent, SimpleCov.minimum_coverage[:line])
      Kernel.exit SimpleCov::ExitCodes::MINIMUM_COVERAGE
    end
  end

  SimpleCovHelper.report_coverage
```
1. Remove the `coveralls` gem from the Gemfile and `spec/spec_helper.rb`
