## How to be the runner

Each week one person from the team is assigned to be the "runner". This person watches honeybadger for all our projects and responds to new errors as they occur.

The Friday before:
- Ensure your notifications are on for all projects.

Each morning:
- Look through new errors from the weekend / night before.

When a new error comes in:
- Quickly take a look at it to determine whether it is indicative of an incident
  that requires immediate response.

Over the course of the week:
- For each notification, spend up to 30 minutes investigating / diagnosing the error. If it can be resolved in that time, submit a PR resolving it. Otherwise, do your best to diagnose the problem and create a ticket for it. These tickets will default to the "inbox" pipelines in zenhub and be reviewed for priority by technical liaisons / product owners.
- Staging errors are probably due to development / testing. But it could be an opportunity to catch an error before we see it in production. If you're not sure, check in with the team.
- The general goal is for each error to either have an associated PR, an associated issue describing what happened and what we might be able to do about it, or be resolved (often network issues can simply be resolved).

### Notes for new runners
The first time that you are a runner you might spend more time than a regular runner going through the notifications and troubleshooting. This is normal, particularly since there will be projects that you have never seen before.
