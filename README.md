## Git Pull Request
Pull Requests are a GitHub and BitBucket specific feature that offers an easy, web-based way to submit your work, alternately called "patches" to the project.
The Git pull command is a combination of Git merge and Git fetch, meaning that the source code will get downloaded, and if this code’s reference is indicated, all changes will be combined.

## Git Merge
A merge request is simply a request from a user to merge their code from one branch to another, typically to the master branch. Like the Git pull request, the Git merge request allows the team members to discuss the suggested changes and merges, offering feedback and possibly adding new commits to make the process smoother.

## Git Rebase
Rebasing is the process of moving or combining a sequence of commits to a new base commit. Rebasing is most useful and easily visualized in the context of a feature branching workflow. The primary reason for rebasing is to maintain a linear project history.
Commands : `git rebase <feature_branch>`, `git push -f`

## Change Commit History
Git provides an interactive rebase to change the commit messages. The latest commit message can be changed by applyging git commit --amend. But for the earlier commit messages the change can be done using interactive rebase.

## Git Cherry Pick
git cherry-pick is a powerful command that enables arbitrary Git commits to be picked by reference and append to the current working HEAD. For example, if a commit is made in a wrong branch then we can switch to the correct branch and pick the commit from the wrong branch.

## Git Drop Commit
For dropping some commits from the branch we have to reset the HEAD or we can squash some commits into only one commit. This can be done using the interactive rebase.
Squashing commits into one single commit.
