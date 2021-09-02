## How to be the runner

Each week one person from the team is assigned to be the "runner". This person watches honeybadger for all our projects and responds to new errors as they occur.

The Friday before:
- Ensure your notifications are on for all projects.

Each morning:
- Look through new errors from the weekend / night before.

Friday during:
- Add an agenda item for the most impactful ticket to resolve for discussion at
the end of the week. You will work this ticket the next week.

Week after:
- Work the ticket from the week before.

When a new error comes in:
- Quickly take a look at it to determine whether it is indicative of an incident
  that requires immediate response.

Over the course of the week:
- For each notification do your best to create a ticket in Github for it. Rename
the title of the ticket to be descriptive and copy the long stack-trace into it,
as well as any relevant environment information.
- Keep tabs on which tickets come up a lot and would be most impactful for you
to fix the following week.
- The general goal is for each error to either have an associated PR, an associated issue describing what happened and what we might be able to do about it, or be resolved (often network issues can simply be resolved).

### Notes for new runners
The first time that you are a runner you might spend more time than a regular runner going through the notifications and troubleshooting. This is normal, particularly since there will be projects that you have never seen before.

### Errors of certain kinds
- Staging errors are often due to development / testing. But it could be an opportunity to catch an error before we see it in production. If you're not sure, check in with the team.
- Errors that look like attack probes should be ticketed in princeton_ansible for lack of a better place. Operations will use them to look at Signal Sciences configuration.
- Errors that look like SIGHUP from closing a console on a box can be set to "ignore"
