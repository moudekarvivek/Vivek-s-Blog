---
title: "🐙Day 8 - Basic Git & GitHub for DevOps Engineers"
datePublished: Sun Feb 04 2024 18:08:38 GMT+0000 (Coordinated Universal Time)
cuid: cls7th11w000309jrdivk7tyw
slug: day-8-basic-git-github-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1707068620328/6e51f15d-089e-4d4e-bd9c-f52869b98dd6.png
tags: github, git, devops, git-commands, 90daysofdevops, trainwithshubham, git-github-version-control-linux-git-commands-github-repositories-cheat-sheet-git-branching-git-workflow-collaboration-git-history-git-commit-git-merge-git-rebase-git-pull-request-git-fork-git-stash-git-remote-git-ignore-git-hooks-github-issues-github-actions-github-pages-github-security-git-for-beginners-advanced-git-techniques-github-collaboration-git-integration-git-flow-git-best-practices, 90daysofdevopschallenge, devopscommunity, vivekmoudekar

---

# 🐙What is Git?

Git is a version control system that allows you to track changes to files and co-ordinate work on those files among multiple people. It is commonly used for software development, but it can be used to track changes to any set of files.

With Git, you can keep a record of who made changes to what part of a file, and you can revert back to earlier versions of the file if needed. Git also makes it easy to collaborate with others, as you can share changes and merge the changes made by different people into a single version of a file

# 🐙What is GitHub?

GitHub is a web-based platform that provides hosting for version control using git. It is a subsidiary of Microsoft, and it offers all of the distributed version control and source code management (SCM) functionality of Git as well as adding its own features. GitHub is a very popular platform for developers to share and collaborate on projects, and it is also used for hosting open-source projects. similarly there are other hosting platform like this i.e- bitbucket, gitlab ,etc.

# 🐙What is Version Control?

Version control is a system that tracks changes to file or set of files over time so that you can recall specific versions later. It allows you to revert files back to a previous state, revert the entire project back to a previous state, compare changes over time.

There are 2 Types of version control systems:

1. **Centralized Version Control Systems (CVCS):** uses a central server to store all the versions of a project's files. Developers "check out" files from the central server, make changes, and then "check in" the updated files. Examples of CVCS include Subversion and Perforce.
    
2. **Distributed Version Control Systems(DVCS):** allows developers to "clone" an entire repository, including the entire version history of the project. This means that they have a complete local copy of the repository, including all branches and past versions. Developers can work independently and then later merge their changes back into the main repository
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1707068828962/40c57b30-2584-4612-97a7-e0c22b44cfb5.jpeg align="center")

## 🐙Why we use distributed version control over centralized version control?

1. **Better collaboration:** In a DVCS, every developer has a full copy of the repository, including the entire history of all changes. This makes it easier for developers to work together, as they don't have to constantly communicate with a central server to commit their changes or to see the changes made by others.
    
2. **Improved speed:** Because developers have a local copy of the repository, they can commit their changes and perform other version control actions faster, as they don't have to communicate with a central server.
    
3. **Greater flexibility:** With a DVCS, developers can work offline and commit their changes later when they do have an internet connection. They can also choose to share their changes with only a subset of the team, rather than pushing all of their changes to a central server.
    
4. **Enhanced security:** In a DVCS, the repository history is stored on multiple servers and computers, which makes it more resistant to data loss. If the central server in a CVCS goes down or the repository becomes corrupted, it can be difficult to recover the lost data.
    

# 🛠️TASK:

* **1\. Install Git:**
    
    To Install git on your local machine first you have to visit the official website for git i.e.- [https://git-scm.com/downloads](https://git-scm.com/downloads) .
    
* Choose the version for your operating system whether it is one of this (Windows,
    
    macOS, Linux) download and install.
    
* #### **2\. To Create a GitHub Account:**
    
    If you don't have a GitHub account, creating one is pretty fast.
    
    * Visit GitHub website and signup as a new user.
        
    * Enter your desired email address and password.
        
    * Complete the account creation process.
        
    
    ### **Happy Learning 😊:)**