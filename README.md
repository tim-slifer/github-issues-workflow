# github-issues-workflow

This is a simple(ish) label-driven workflow approach for Github Issues. If more complex (and expensive) project management tooling is either not available or not needed for a project, this approach allows a team to leverage Github Issues in an organized fashion by using Labels to track various aspects of Issues.

Unlike actual lifecycle tools, however, this approach works on the honor system. There is no enforcement of workflow rules like the "real" lifecycle tools. This is open-ended and flexible, which for some teams can be beneficial. 

https://github.com/tim-slifer/github-issues-workflow/labels

A naming convention and color scheme allow for issues to be separated into various groups. These groups represent workflow state and other important information about an Issue. This approach requires that only one label from any given group be used at any one time (with limited exceptions).

The group names are intended to be as self-explanatory as possible. Some group names are intentionally prefixed with a "z" in order to maintain a certain ordering to the labels as they are shown on the Issues list, allowing the labels from the primary groups to be shown first. 

Making use of Milestones in Github is highly recommended alonside the use of these labels. Combined with Label filtering, a team can quickly and easily gain insight to the quantity and status of remaining work within the release/sprint/iteration/etc.

# Guidelines

The open-ended approach allows for labels to be added and changed as needed during the life of an Issue. Some useful guidelines for consideration...

- `Type` and `Stage` are added when an Issue is created. If `Type` is `BUG`, a `Severity` can be added also, or added if/when the Issue is triaged. `Priority` can be added at creation, but can wait until the Issue is added to a Milestone when a work cycle is being planned.
- `Stage` labels have an implied natural progression, but can be updated in whichever order makes sense for the team and the work at hand. `NEW` is a typical initial Stage, but on some issues with little to no pre-code design to be done, `DEVELOPMENT` is just a valid of option at creation.
- `Status` labels will cycle for each `Stage` and also have an implied progression, but can just the same be applied in the order that makes the most sense. `OPEN` is standard for an Issue that has progressed to a new Stage, has been assigned, and remains in queue to be worked. `REWORK` is standard for a `Type.BUG` that has been returned for additional correction, and should be accompanied by changing to `Stage.DEVELOPMENT`. Once an Issue is complete and moved to `Stage.READY`, the `Status` group is no longer needed.
- `Cause` and `Discovery` are groups made to accompany `Type.BUG`. Usage is obviously encouraged, but is not essential if the team is not tracking when defects are identified, or performing any Root Cause Analysis. The actual labels in these groups are simply a guide. A team can (and should) adapt, change, or expand these groups to suit the needs of the team.
- `Meta` is intended as a more free-style group of labels that are less directly related to the lifecycle progression of an issue. Unlike the other groups, `Meta` allows one or several labels from the group to be used at a given time.
