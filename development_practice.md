# Development Practice

## Routine / Project work

### Selecting an issue

We work primarily from project boards in zenhub. Most [applications](/applications.md) have their own board, and we also create boards specific to projects for features that span multiple applications or that we expect will require multiple work cycles to complete. The `ready` column of a given board should have issues ordered roughly by priority. Always assign yourself to an issue before starting to work on it, and move it to the `in progress` column.

### Pairing

Our team considers ourselves "pairing-friendly." Several of us very much like to pair, and we all do pair at least sometimes. We've tried various ways of formalizing our pairing arrangements in the past. What currently works best is to invite someone to pair with you if you'd like. Pairing on code-review has also been a helpful practice on occasion.

### Submitting code

* Ensure code is arranged in logical, unitary commits unless you want it squash-merged.
* Ensure any new or modified code has test coverage. Many of us practice test-driven development, but at the least a test should be confirmed to be failing before the code change is applied.
* Run Rubocop to enforce code style agreed upon by our team.
* Open a pull request in Github
  * Reference the relevant issues, using [github keywords](https://docs.github.com/en/enterprise/2.16/user/github/managing-your-work-on-github/closing-issues-using-keywords) if the issue will be resolved
* Make adjustments as-needed according to code review.
* If your PR isn't getting reviewed, freely post it in slack.
* If your PR is approved and passes CI checks you may merge your own pull request. Usually this happens when it's reviewed before CI is finished.
* Ensure the issue is closed if no further work is required.

### Reviewing code

* Review other pull requests over the course of the day, either within the sub-team you're working with for that work cycle, or for any PR that may come along ad-hoc.
* We generally follow the [Samvera Code Review](https://samvera.github.io/review.html) guidelines
* Ask the author of the code to pair with you on the review if desired / required.

## Maintenance Mondays

We have recently begun focusing on software maintenance tasks on Mondays.  Tasks are triaged as GitHub issues on the [Maintenance Board](https://github.com/orgs/pulibrary/projects/4).  Maintenance tasks can be spread out over a series of Mondays if needed, and work cycles should still be scheduled for maintenance tasks that are time-consuming and/or require heavy collaboration with other teams.

## Dependabot

We have set up our github repositories to use Dependabot, which generates PRs to upgrade dependencies based on security warnings. Based on our experience with these PRs it is important to test a deployment to a staging server before merging them even if the tests are all passing. Also, in some of our projects our tests do not fully cover our javascript code. In those cases when javascript dependencies are updated it can be helpful to do a bit of QA before merging.

If the PR has been open for a while, or you've just merged another PR, use the `@dependabot rebase` comment to trigger a rebase before deploying. This can take a few minutes.
