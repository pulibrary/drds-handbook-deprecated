# Development Practice

- Daily:
  - Self-assign an issue from the ready column for the project you're working
    on. Work individually or in a pair.
  - Ensure new / modified code has test coverage.
  - Run Rubocop to enforce code style agreed upon by our team.
  - Do not merge your own pull request. If your PR isn't getting reviewed, freely post it in slack.
  - Review other pull requests over the course of the day.
    - We generally follow the [Samvera Code Review](https://samvera.github.io/review.html) guidelines
  - Sometimes pair code review is helpful.
  - Open issues in Github as needed (check if there is a similar issue to avoid duplicates).

## Maintenance Mondays

We have recently begun focusing on software maintenance tasks on Mondays.  Tasks are triaged as GitHub issues on the [Maintenance Board](https://github.com/orgs/pulibrary/projects/4).  Maintenance tasks can be spread out over a series of Mondays if needed, and work cycles should still be scheduled for maintenance tasks that are time-consuming and/or require heavy collaboration with other teams.

## Dependabot

We have set up our github repositories to use Dependabot, which generates PRs to
upgrade dependencies based on security warnings. Based on our experience with
these PRs it is important to test a deployment to a staging server before
merging them even if the tests are all passing. Also, in some of our projects
our tests do not fully cover our javascript code. In those cases when javascript
dependencies are updated it can be helpful to do a bit of QA before merging.

If the PR has been open for a while, or you've just merged another PR, use the `@dependabot rebase` comment to trigger a rebase before deploying. This can take a few minutes.
