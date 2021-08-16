## Tension

The quicker we discover bugs, the quicker they'll be resolved. Without a process for grooming them, the more likely it is that our users will find bugs before we do.

We use Sentry to track issues but GitHub is where our Sprint work lives. 

Not all bugs require immediate attention. We need a process that makes the team aware of the important ones without inundating everyone with low-priory issues.

## Proposal

Each week, a Product team member is assigned the role of Bug Squasher. A pinned check-in agenda item reminds us of the rotation.

The Bug Squasher does the following:

- A few times during the week, go to [Sentry](https://sentry.io/organizations/parabol/issues/?project=107196&query=+level%3Afatal+timesSeen%3A%3E5+is%3Aunassigned&statsPeriod=14d), click "Issues" and enter the following in the custom search: `level:fatal timesSeen:>5 is:unassigned is:unresolved`
    - This will filter for bugs that have crashed the app on more than 5 occasions, are currently unassigned and haven't been ignored
    - While the Bug Squasher should focus on creating or linking issues that show up in the above custom search, It's worth checking `level:fatal timesSeen:>5` too incase any assigned or ignored bugs are still popping up
- If the Sentry issue is a duplicate (it has the same name and url), merge the duplicate issues by clicking the checkboxes and click "Merge"
- If you know that it's a duplicate issue but it's not displayed in the custom search or if the bug is affecting very few users (e.g. 1 user has encountered the bug 5 times over 9 months), you can also click "Ignore" and add a comment to the issue
- If the Sentry issue is a new bug, create a new GitHub issue by clicking on the issue and then "Link GitHub issue"
- If the Sentry issue is not an exact duplicate but it is a known bug, link it to the existing GitHub issue
- After creating / linking the GitHub issue, assign the Sentry issue to #parabol
    - Note: Sentry are [working on](https://forum.sentry.io/t/advanced-sentry-search/4736/14) being able to search for issues that are not linked to Jira / GitHub. When this is live, we won't need to assign them to #parabol.
- If there is a critical bug, the Bug Squasher messages the Product team in Slack so that it can be resolved asap. A critical bug is subjective but it's likely to be an update in a latest release that breaks core functionality. The PM will assign non-critical bugs to developers during the Sprint.

Even with the new proposal, I suggest that we keep the Sentry alert in `t_product_devops` as a pesky reminder of fatal bugs that have affected 5+ users.