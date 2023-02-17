# Git Practicals

## Git Pull Request
Pull Requests are a GitHub and BitBucket specific feature that offers an easy, web-based way to submit your work, alternately called "patches" to the project.
The Git pull command is a combination of Git merge and Git fetch, meaning that the source code will get downloaded, and if this code’s reference is indicated, all changes will be combined.

![git pull request](https://github.com/dharmit27/git_practice/blob/main/screenshots/PR.png)
![git pull request merged](https://github.com/dharmit27/git_practice/blob/main/screenshots/PR%20Merge.png)

## Git Merge
A merge request is simply a request from a user to merge their code from one branch to another, typically to the master branch. Like the Git pull request, the Git merge request allows the team members to discuss the suggested changes and merges, offering feedback and possibly adding new commits to make the process smoother.

```
# Creating a New Branch
git checkout -b branch1

# Adding Some Files
touch new-file3.js

# Staging the Changes
git add .

# Committing the Change
git commit -m "Feature Changes"

# Switching to Main Branch
git switch main

# Merging the Branch1 with the Main Branch
git merge branch1
```

![merged branch](https://github.com/dharmit27/git_practice/blob/main/screenshots/MergeBranch.png)

## Git Rebase
Rebasing is the process of moving or combining a sequence of commits to a new base commit. Rebasing is most useful and easily visualized in the context of a feature branching workflow. The primary reason for rebasing is to maintain a linear project history.
Commands : 
```
# Create a new feature branch
git checkout -b feature1

# Commit changes to the feature branch
touch new-file.js
git add .
git commit -m "New Feature Added"

touch new-file2.js
git add .
git commit -m "Made Some changes to earlier feature"
```
![commits to feature branch](https://github.com/dharmit27/git_practice/blob/main/screenshots/Commits%20to%20Feature%20Branch.png)

```
# Switch Back to Main branch
git switch main

# Rebase with the Feature Branch
git rebase feature1
```
![rebase with feature branch](https://github.com/dharmit27/git_practice/blob/main/screenshots/Rebase%20with%20Feature%20Branch.png)

## Change Commit Message
Git provides an interactive rebase to change the commit messages. The latest commit message can be changed by applying git commit --amend. But for the earlier commit messages the change can be done using interactive rebase.

```
# List of all the commit messages
git log --oneline
```
![all commit messages](https://github.com/dharmit27/git_practice/blob/main/screenshots/Commit%20Messages%20Before%20Edit.png)

```
# Change the Last Commit Message
git commit --amend -m "Commit Message Changed"
```
![commit message changed](https://github.com/dharmit27/git_practice/blob/main/screenshots/CommitMessageChanged.png)

## Git Cherry Pick
git cherry-pick is a powerful command that enables arbitrary Git commits to be picked by reference and append to the current working HEAD. For example, if a commit is made in a wrong branch then we can switch to the correct branch and pick the commit from the wrong branch.

```
# Switch to Main branch
git switch main

# Cherry Pick Commit from Feature Branch
git cherry-pick <Hash of Commit>
```

![cherry pick commit](https://github.com/dharmit27/git_practice/blob/main/screenshot/CheeryPickCommit.png)


## Git Drop Commit
For dropping some commits from the branch we have to reset the HEAD or we can squash some commits into only one commit. This can be done using the interactive rebase.
Squashing commits into one single commit.

```
# Get All Commit Messages
git log --online

# To Delete the Last Commit
git reset --hard HEAD~1

# To Delete Multiple Commit Messages and Merge them into one commit
# Using Interactive rebase
git rebase -i HEAD~n
```
![all commits](https://github.com/dharmit27/git_practice/blob/main/screenshots/All%20Commits.png)
![cherry pick commit](https://github.com/dharmit27/git_practice/blob/main/screenshot/rebaseInteractive.png)
![merged some commits](https://github.com/dharmit27/git_practice/blob/main/screenshots/Deleted%20some%20Commits.png)


