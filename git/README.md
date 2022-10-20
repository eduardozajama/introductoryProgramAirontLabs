# 2. Git 

## Git vs Github
Git is a Version Control System (VCS) that was created by Linus Torvalds in 2005, and has been maintained by Junio Hamano since then.It makes developing easier. We can think of it as making versions of your application and saving versions of your application. Git lives on your localhost machine.
 Let’s say for example you create a project, you initialize a project, you have the folder, you have the files. You do git init inside your localhost environment and that initializes the git repository (repo). What happens next is that Git start to track changes to new and newly modified files, it tracks content by taking snapshots of the given file. If you want to have a new change and you changed something in a file, for example: the header of an html file. It will go ahead and stage that content in the index, ready for inclusion in the next commit. Every time you commit, you commit one change. If you change something else and then commit again, you commit another change. 
Git keeps track of all the changes, the reason why we do this is that later on we can go back and refer to those changes, or we could go back and revert to those changes if something was to go wrong.
Github works directly with Git, meaning it’s basically a Git repository but remotely (online).

## How do they work?

Let’s say you have your project on Git on your computer. Now what you do is you go ahead and upload that project, that Git repo project into Github. The reason why we upload to Github is so that later on, your team can actually look at that project and pull that project into their computers. This means that a lot of team members, as you upload a project, are able to see your changes and can use it as well. They can download that project using git clone to work on a local copy, also do git push to push it up to Github and use many other commands to work collectively.
All these features  make it easy to visualize your project, save your files and changes made, reverse those changes if needed. working collaboratively in a team.

## Working in a project
Working in a project
A Git project consists of three major sections: the working directory, the staging area, and the git directory.
The working directory is where you add, delete, and edit the files. Then, the changes are staged (indexed) in the staging area. After you commit your changes, the snapshot of the changes will be saved into the git directory.
For all of these to be possible we have a set of commands.
## Basic Git Commands

Here are some basic GIT commands you need to know:
<!-- UL -->
* git init will create a new local GIT repository. The following Git command will create a repository in the current directory:
<!-- Code Blocks -->
```
git init
 ```


<!-- UL -->
* Alternatively, you can create a repository within a new directory by specifying the project name:<!-- Code Blocks -->
```
git init [project name]
```
<!-- UL -->
* git clone is used to copy a repository. If the repository lies on a remote server, use:
<!-- Code Blocks -->
```
      git clone username@host:/path/to/repository
``` 
<!-- UL -->
* Conversely, run the following basic command to copy a local repository:
<!-- Code Blocks -->
```
git clone /path/to/repository
```
git add<!-- UL -->
*  is used to add files to the staging area. For example, the basic Git following command will index the temp.txt file:
<!-- Code Blocks -->
```
git add <temp.txt>
```
<!-- UL -->
* git commit will create a snapshot of the changes and save it to the git directory.
<!-- Code Blocks -->
```
git commit –m “Message to go with the commit here”
```
<!-- UL -->
* git config can be used to set user-specific configuration values like email, username, file format, and so on. To illustrate, the command for setting up an email will look like this:
<!-- Code Blocks -->
```
 git config --global user.email youremail@example.com
 ```
<!-- UL -->
* The –global flag tells GIT that you’re going to use that email for all local repositories. If you want to use different emails for different repositories, use the command below:
<!-- Code Blocks -->
```
git config --local user.email youremail@example.com
```
<!-- UL -->
* git status displays the list of changed files together with the files that are yet to be staged or committed.
<!-- Code Blocks -->
```
git status
```
<!-- UL -->
* git push is used to send local commits to the master branch of the remote repository. Here’s the basic code structure:
<!-- Code Blocks -->
```
git push origin <master>
```
## Git Branch
A branch is a version of the repository that diverges from the main working project. It is a feature available in most modern version control systems. A Git project can have more than one branch. These branches are a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug, you spawn a new branch to summarize your changes. So, it is complex to merge the unstable code with the main code base and also facilitates you to clean up your future history before merging with the main branch.

![](/git/branch.png)

## Operations on Branches
We can perform various operations on Git branches. The git branch command allows you to create, list, rename and delete branches. Many operations on branches are applied by git checkout and git merge command. So, the git branch is tightly integrated with the git checkout and git merge commands.
 
## Git Tags
Tags make a point as a specific point in Git history. Tags are used to mark a commit stage as relevant. We can tag a commit for future reference. Primarily, it is used to mark a project's initial point like v1.1.
Tags are much like branches, and they do not change once initiated. We can have any number of tags on a branch or different branches. The below figure demonstrates the tags on various branches.

![](/git/tags.png)


In the above image, there are many versions of a branch. All these versions are tags in the repository.

### When to create a Tag:

<!-- UL -->
* When you want to create a release point for a stable version of your code.
 <!-- UL -->
* When you want to create a historical point that you can refer to reuse in the future.


## Git Commit
It is used to record the changes in the repository. It is the next command after the git add. Every commit contains the index data and the commit message. Every commit forms a parent-child relationship. When we add a file in Git, it will take place in the staging area. A commit command is used to fetch updates from the staging area to the repository.

The staging and committing are co-related to each other. Staging allows us to continue in making changes to the repository, and when we want to share these changes to the version control system, committing allows us to record these changes.
Commits are the snapshots of the project. Every commit is recorded in the master branch of the repository. We can recall the commits or revert it to the older version. Two different commits will never overwrite because each commit has its own commit-id. This commit-id is a cryptographic number created by SHA (Secure Hash Algorithm) algorithm.


>  A Git Tag is used to label and mark a specific commit in the git commit history.

## Git Stash
Sometimes you want to switch the branches, but you are working on an incomplete part of your current project. You don't want to make a commit of half-done work. Git stashing allows you to do so. The git stash command enables you to switch branches without committing the current branch.
The below figure demonstrates the properties and role of stashing concerning repository and working directory.

![](/git/stash.png)

Generally, the stash's meaning is "store something safely in a hidden place." The sense in Git is also the same for stash; Git temporarily saves your data safely without committing.
Stashing takes the messy state of your working directory, and temporarily save it for further use.

Git Hooks
Git hooks provide a way to fire off custom scripts that run automatically every time a particular event occurs in a Git repository. They let you customize Git’s internal behavior and trigger customizable actions at key points in the development life cycle.

. There are two types of hooks present in Git:

<!-- UL -->
* Client-Side hooks

<!-- UL -->
* Server-Side hooks


![](/git/hooks.png)



Git hooks are scripts that run automatically every time a particular event occurs in a Git repository. They let you customize Git’s internal behavior and trigger customizable actions at key points in the development life cycle.
 
Common use cases for Git hooks include encouraging a commit policy, altering the project environment depending on the state of the repository, and implementing continuous integration workflows. But, since scripts are infinitely customizable, you can use Git hooks to automate or optimize virtually any aspect of your development workflow.

### Resources
> [Javatpoint](https://www.javatpoint.com/git)

> [Git](https://git-scm.com/)

> [W3schools](https://www.w3schools.com/git/git_intro.asp?remote=github)

> [Atlassian](https://www.atlassian.com/git/tutorials/git-hooks)






