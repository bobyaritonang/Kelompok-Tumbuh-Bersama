# **Exercise 01 Creatting markdown on Github**

## **What is Git**
<center> <img src="https://www.technotification.com/wp-content/uploads/2018/04/git-commands.jpg" width="150" height="100"/></center>
<br>
By far, the most widely used modern version control system in the world today is Git. Git is a mature, actively maintained open source project originally developed in 2005 by Linus Torvalds, the famous creator of the Linux operating system kernel. A staggering number of software projects rely on Git for version control, including commercial projects as well as open source. Developers who have worked with Git are well represented in the pool of available software development talent and it works well on a wide range of operating systems and IDEs (Integrated Development Environments).

Having a distributed architecture, Git is an example of a DVCS (hence Distributed Version Control System). Rather than have only one single place for the full version history of the software as is common in once-popular version control systems like CVS or Subversion (also known as SVN), in Git, every developer's working copy of the code is also a repository that can contain the full history of all changes.

In addition to being distributed, Git has been designed with performance, security and flexibility in mind.

## How To Install Git

### 1. On windows

 1. [Download](https://git-scm.com/download/win) the latest Git for Windows installer.

 2. When you've successfully started the installer, you should see the Git Setup wizard screen. Follow the Next and Finish prompts to complete the installation. The default options are pretty sensible for most users.

 3. Open a Command Prompt (or Git Bash if during installation you elected not to use Git from the Windows Command Prompt).

 4. Run the following commands to configure your Git username and email using the following commands, replacing Emma's name with your own.

### 2. On Linux(ubuntu)

 1. From your shell, install Git using apt-get:
   > $ sudo apt-get update

   > $ sudo apt-get git
 2. Verify the installation was successful by typing git _--version_:


## Configuration & set up: git config

### - Git Remote

Once you have a remote repo setup, you will need to add a remote repo url to your local git config, and set an upstream branch for your local branches. The git remote command offers such utility.

 > $ git remote add <remote_name> <remote_repo_url>

 This command will map remote repository at  to a ref in your local repo under . Once you have mapped the remote repo you can push local branches to it.
 
 > $ git push -u <remote_name> <local_branch_name>

Define the author name to be used for all commits in the current repository. Typically, you’ll want to use the --global flag to set configuration options for the current user.

 > $ git config --global user.name <name>
 > $ git config --global user.email <email>

### - Git Init

This page will explore the git init command in depth. By the end of this page you will be informed on the core functionality and extended feature set of git init. 

> $ git init

### - git clone

Here we'll examine the git clone command in depth. git clone is a Git command line utility which is used to target an existing repository and create a clone, or copy of the target repository. In this page we'll discuss extended configuration options and common use cases of git clone. Some points we'll cover here are:

 * Cloning a local or remote repository
 * Cloning a bare repository
 * Using shallow options to partially clone repositories
 * Git URL syntax and supported protocols

#### Cloning to a specific folder

 > git clone <repo> <directory>
  
Clone the repository located at ＜repo＞ into the folder called ~＜directory＞! on the local machine.

#### Cloning a specific tag

 > $ git clone ssh://john@example.com/path/to/my-project.git 

Clone the repository located at ＜repo＞ and only clone the ref for ＜tag＞.

#### Git Alias

It is important to note that there is no direct git alias command. Aliases are created through the use of the git config command and the Git configuration files. As with other configuration values, aliases can be created in a local or global scope.
 * example:

 >  $ alias = checkout
 >  $ git config --global alias.co checkout

 > $ alias graph="git log --all --decorate --oneline  --graph"

## Git Branch
If --list is given, or if there are no non-option arguments, existing branches are listed; the current branch will be highlighted in green and marked with an asterisk. Any branches checked out in linked worktrees will be highlighted in cyan and marked with a plus sign. Option -r causes the remote-tracking branches to be listed, and option -a shows both local and remote branches.

> git branch [--name]

> git branch [--track[=(direct|inherit)] | --no-track]  [-f] [--recurse-submodules] <branchname> [<start-point>]

 > git branch (--set-upstream-to=<upstream> | -u <upstream>) [<branchname>]

>  git branch --unset-upstream [<branchname>]

>  git branch (-m | -M) [<oldbranch>] <newbranch>

 > git branch (-c | -C) [<oldbranch>] <newbranch>

 > git branch (-d | -D) [-r] <branchname>…​

 > git branch --edit-description [<branchname>]
## Git Repository

In Git, the repository is like a data structure used by VCS to store metadata for a set of files and directories. It contains the collection of the files as well as the history of changes made to those files. Repository in Git is considered as your project folder. A repository has all the project-related data. Distinct projects have distinct repositories.

> $ git init  

## Git Flow

### Develop and main branches

Instead of a single main branch, this workflow uses two branches to record the history of the project. The main branch stores the official release history, and the develop branch serves as an integration branch for features. It's also convenient to tag all commits in the main branch with a version number.

<center> <img src="https://wac-cdn.atlassian.com/dam/jcr:34c86360-8dea-4be4-92f7-6597d4d5bfae/02%20Feature%20branches.svg?cdnVersion=638" width="400" height="500"/></center>
