# Git Interview Questions

+ [Difference between git commit and git push command.](#difference-between-git-commit-and-git-push-command)
+ [Difference between git pull and fetch.](#difference-between-git-pull-and-fetch)
+ [What is Git stash?](#what-is-git-stash)
+ [Explain git status command.](#explain-git-status-command)
+ [Explain git revert command.](#explain-git-revert-command)
+ [How to view the commit history in git?](#how-to-view-the-commit-history-in-git)
+ [Difference between git merge vs rebase.](#difference-between-git-merge-vs-rebase)
+ [What is cherry-pick in GIT?](#what-is-cherry-pick-in-git)

## Difference between git commit and git push command.

git commit records changes to the local repository while git push updates the changes 
to the remote repository and the changes be visible to the other users.

## Difference between git pull and fetch.

Git fetch gathers any commits from the target branch that do not exist in your current branch and stores them in 
your local repository. However, it does not merge them with your current branch.

Git pull update your current HEAD branch with the latest changes from the remote server. 
This means that pull not only downloads new data and also directly integrates it into your current working copy files.

## What is Git stash?

git stash temporarily shelves (or stashes) changes you have made to your working copy so you can work on something else, 
and then come back and re-apply them later on.

## Explain git status command.

The git status command displays the state of the working directory and the staging area. 
It lets you see which changes have been staged, which haven't, and which files aren't being tracked by Git.

## Explain git revert command.

The git revert command is used for undoing changes to a repository's commit history. 
Git revert expects a commit ref passed in. To revert the latest commit use git revert HEAD command.

git revert simply creates a new commit that is the opposite of an existing commit. 
So a git push need to be followed to update in remote repository.

## How to view the commit history in git?

git log command lists the commits made in that repository in reverse chronological so that most recent commits show up first.

## Difference between git merge vs rebase.

Both does the same thing (integrate branches) in slightly different way.

The major benefit of rebasing is that you get a much cleaner project history. 
First, it eliminates the unnecessary merge commits required by git merge.
Rebasing is the process of moving or combining a sequence of commits to a new base commit.

## What is cherry-pick in GIT?

Cherry picking means to choose a specific commit from one branch and apply it onto another.

It is a 2 step process where you need to check-out to the branch where you want to apply the commit 
and then apply the commit by its commit-hash.
```
git checkout master
git cherry-pick <commit-hash>
```


