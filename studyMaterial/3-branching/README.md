3. Branching

## Branches in a nutshell

Nearly every VCS has some form of branching support. Branching means you diverge from the main line of development and continue to do work without messing with that main line. 
The way Git branches is incredibly lightweight, making branching operations nearly instantaneous, and switching back and forth between branches generally just as fast. Understanding and mastering this feature gives you a powerful and unique tool and can entirely change the way that you develop.
 In modern software development, speed and agility are crucial when it comes to developing and releasing software. However, when you have a large team of developers working simultaneously, branching and merging code can become messy fast. 
Therefore, teams need to have a process in place to implement multiple changes at once. This is where having an efficient branching strategy becomes a priority for these teams.


## What is a branching strategy?

Branches are primarily used as a means for teams to develop features giving them a separate workspace for their code. These branches are usually merged back to a master branch upon completion of work. In this way, features (and any bug and bug fixes) are kept apart from each other allowing you to fix mistakes more easily.
This means that branches protect the mainline of code and any changes made to any given branch don’t affect other developers.
A branching strategy, therefore, is the strategy that software development teams adopt when writing, merging and deploying code when using a version control system.
It is essentially a set of rules that developers can follow to stipulate how they interact with a shared codebase.
 

 ## Why do you need a branching strategy?

Having a branching strategy is necessary to avoid conflicts when merging and to allow for the easier integration of changes into the master trunk.
A branching strategy aims to:
Enhance productivity by ensuring proper coordination among developers
Enable parallel development
Help organize a series of planned, structured releases
Map a clear path when making changes to software through to production
Maintain a bug-free code where developers can quickly fix issues and get these changes back to production without disrupting the development workflow







   ## How are Git branches created?
You create branches by using the branch command. Branch creates a reference in Git for the new branch and a pointer back to the parent commit so Git can keep a history of changes as you add commits to the branch.
When you're working with a branch that someone else shared, Git keeps an upstream tracking relationship. The relationship associates the branch on the local repo with the corresponding branch on the remote repo.

Upstream tracking makes it simple to sync changes with others using push and pull.

![](/studyMaterial/3-branching/branch%20create.png)


In this screenshot, you can see a new branch that was created from the main branch. Work continues on both branches and commits are added to both branches.
Git always adds new commits to the current local branch. Check what branch you're working on before you commit so that you don't commit changes to the wrong branch.
Swap between local branches using the checkout command. Git will change the files on your computer to match the latest commit on the checked out branch.
When your work in the branch is ready to share with the rest of the team, you push the changes to update the remote branch.






A common mistake is to make some changes and commit them, realize you're on an incorrect branch, then checkout to the correct branch.
Your most recent changes will no longer be on the filesystem since each branch has its own version of code.
Git brings the files' state back to the last commit on the branch you swapped into, not the previous branch where you made your changes.
You'll need to either cherry-pick the commits from the branch or merge the changes into the correct branch.


## What are some common Git branching strategies?

<!-- UL -->
* GitFlow
 <!-- UL -->
* GitHub Flow
<!-- UL -->
* GitLab Flow
< !-- UL -->
* Trunk-based development








## GitFlow
Considered to be a bit complicated and advanced for many of today’s projects, GitFlow enables parallel development where developers can work separately from the master branch on features where a feature branch is created from the master branch.
Afterwards, when changes are complete, the developer merges these changes back to the master branch for release.
This branching strategy consists of the following branches:
Master 
Develop
Feature- to develop new features that branches off the develop branch 
Release- help prepare a new production release; usually branched from the develop branch and must be merged back to both develop and master
Hotfix- also helps prepare for a release but unlike release branches, hotfix branches arise from a bug that has been discovered and must be resolved; it enables developers to keep working on their own changes on the develop branch while the bug is being fixed.
 
 
 ![](/studyMaterial/3-branching/gitflow-branching-strategy.png)

 
 
 
 
The main and develop branches are considered to be the main branches, with an infinite lifetime, while the rest are supporting branches that are meant to aid parallel development among developers, usually short-lived. 
 
 
   

 
## GitHub Flow
GitHub Flow is a simpler alternative to GitFlow ideal for smaller teams as they don’t need to manage multiple versions.
Unlike GitFlow, this model doesn’t have release branches. You start off with the main branch then developers create branches, feature branches that stem directly from the master, to isolate their work which are then merged back into main. The feature branch is then deleted.
The main idea behind this model is keeping the master code in a constant deployable state and hence can support continuous integration and continuous delivery processes.
 
 ![](/studyMaterial/3-branching/github-flow-branching-model.jpeg)
 

## GitLab Flow
GitLab Flow is a simpler alternative to GitFlow that combines feature-driven development and feature branching with issue tracking.
With GitFlow, developers create a develop branch and make that the default while GitLab Flow works with the main branch right away.
GitLab Flow is great when you want to maintain multiple environments and when you prefer to have a staging environment separate from the production environment. Then, whenever the main branch is ready to be deployed, you can merge back into the production branch and release it.
Thus, this strategy offers propers isolation between environments allowing developers to maintain several versions of software in different environments.
While GitHub Flow assumes that you can deploy into production whenever you merge a feature branch into the master, GitLab Flow seeks to resolve that issue by allowing the code to pass through internal environments before it reaches production, as seen in the image below.

![](/studyMaterial/3-branching/gitlab_flow_environment_branches.png)
 

 ## Trunk-based development
Trunk-based development is a branching strategy that in fact requires no branches but instead, developers integrate their changes into a shared trunk at least once a day. This shared trunk should be ready for release anytime.
The main idea behind this strategy is that developers make smaller changes more frequently and thus the goal is to limit long-lasting branches and avoid merge conflicts as all developers work on the same branch. In other words, developers commit directly into the trunk without the use of branches.
Consequently, trunk-based development is a key enabler of continuous integration (CI) and continuous delivery (CD)  since changes are done more frequently to the trunk, often multiple times a day (CI) which allows features to be released much faster (CD).
This strategy is often combined with feature flags. As the trunk is always kept ready for release, feature flags help decouple deployment from release so any changes that are not ready can be wrapped in a feature flag and kept hidden while features that are complete can be released to end-users without delay. 

![](/studyMaterial/3-branching/gitlab_flow_environment_branches.png)

 
## What is the best branching strategy?
The answer to which Git branch strategy is the best depends on you and your team’s environment, product and your specific development needs.

There is not a one-size-fits-all Git branch strategy, and regardless of which you end up selecting, it’s likely you can optimize it with further modifications. In order to improve the quality of your code make sure to use Branch Policies 

### Resources

 https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell 
 https://www.flagship.io/glossary/trunk-based-development/
https://www.gitkraken.com/learn/git/best-practices/git-branch-strategy 
https://learn.microsoft.com/en-us/azure/devops/repos/git/repository-settings?view=azure-devops&tabs=browser#branch-policies 





