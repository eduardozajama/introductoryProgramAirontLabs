# 4. Merge,Rebase,Squash.
## What is Merging?


>In general, merging means combining something into a single entity.

When version controlling your code with git, there are generally three choices when merging feature branches into main.
Rebase
It rewrites history on top of a branch. This provides a linear history, meaning context is lost of where a feature branched off. You may also have to force push changes (since you are rewriting history) if you have already pushed to a remote.

## Merge
It will create a merge commit that joins two branches together. With the fast-forward-only flag ff-only, git will attempt to merge without a merge commit, but this isn't possible if the branches have diverged (i.e., there has been a commit to the parent branch that's not on the feature branch).

## Squash + Merge
 Acts like merge but creates a single new squashed commit that encompasses all commits in the feature branch.


 
![](/merge-rebase-squash/squashrebasemerge.jpeg)

## Git Merge Vs Git Rebase


|Merge	|Rebase
|-------------|----------
| Git merge is a command that allows you to merge branches from Git.	|Git rebase is a command that allows developers to integrate changes from one branch to another.
In Git Merge logs will be showing the complete history of the merging of commits.	|Logs are linear in Git rebase as the commits are rebased 
All the commits on the feature branch will be combined as a single commit in the master branch. |All the commits will be rebased and the same number of commits will be added to the master branch.
|Git Merge is used when the target branch is shared branch	|Git Rebase should be used when the target branch is private branch


To summarise, we can use Git Rebase, when we are working on branches, which cannot be seen by other developers. And we use Git Merge when the target and source branch can be viewed by other developers.
### Resources

>[Blog]( https://www.edureka.co/blog/git-rebase-vs-merge/)  
 
>[Atlassian](https://www.atlassian.com/git/tutorials/merging-vs-rebasing) 

>[Blog](https://rietta.com/blog/github-merge-types/)

> [Medium](https://medium.datadriveninvestor.com/git-rebase-vs-merge-cc5199edd77c)