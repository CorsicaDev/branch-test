branch-test
===========

Testing branch structure

`test addition from feedback`

#Branch structure

This is the breakdown of branches that will exist:

- Any number of feature branches
- Master branch
- Staging branch
- Stable branch

## Feature branches
All dev work is done in feature branches. This would include things like bug fixes, 
new features, or basically any discrete changeset that needs to be made. When your feature
or change is ready to be merged into master, it should be code reviewed from your branch first.
When a feature or change is "done", the branch can be closed. The feature branch should be named something
indicative of the work that is being done in the branch. If multiple people are working on one feature, 
it is fine for them to all be working in the same feature branch.

TL;DR: if you need to make a new change, it should be done in a new feature branch. 

## Master branch
The master branch is what everyone should be in sync with, and is what feature branches 
are merged into. While working on a feature you should be constantly taking merges in from 
the master branch to stay in sync with everyone else. This prevents merge nightmares later on.
No commits that aren't merges should ever be made directly to the master branch or any branches outside
the feature branches. This way we can guarantee that syncing with the master branch won't break the build
for other people on the team.

## Staging branch
The staging branch is the intermediary between the master and the stable branch. Changes that are proposed
to be added to the stable branch should first go to the staging branch, where a full set of tests are run.

## Stable branch
The stable branch represents what we are currently shipping to the public.
