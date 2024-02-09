---
title: "🧬Day 10 - Advance Git & GitHub for DevOps Engineers: Part - I"
datePublished: Fri Feb 09 2024 07:50:23 GMT+0000 (Coordinated Universal Time)
cuid: clsecl7yt000a08jnfazj6n14
slug: day-10-advance-git-github-for-devops-engineers-part-i
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1707464215146/2bd56a56-4e02-42b6-99c1-14545f2fb027.png
tags: devops, 90daysofdevops, shubhamlondhe, trainwithshubham, devopscommunity

---

# 🔃Git Branching

Git branching is a brilliant function of git in which if a user want to add some new functionality or fix Bugs without altering the main or primary branch, we can create different versions of our projects. To create a branch we use `git branch` command.

Brief of how branching works in git:

1. **Creating Branch**: To create a new branch user have to use `git branch` command followed by the branch name.
    
    ```plaintext
    git branch <Branch_name>
    ```
    
2. **Switching Branch**: For switching to other feature branch we will use `git checkout` command followed by the branch that has to be used as new commit branch.
    
    ```plaintext
    git checkout <Branch_name>
    ```
    
3. **Commit Changes**: Currently our pointer is on new branch now we can make changes to our code and commit the code using `git add` and after adding to the staging area we can now commit the code.
    
    ```plaintext
    git add . (# here "." indicates all the file present in that branch add them to staging area)
    
    git commit -m "First version of my code" (This meassage is not compusory)
    ```
    
4. **Merging Branches**: When we finished working on our functionality or bugs, we can merge the changes back into the `main` branch using the `git merge` command. For example:
    
    ```plaintext
    git checkout main
    git merge <new_brach_name>
    ```
    
5. **Delete Branches**: After merging a branch and if no longer needed we can delete using `-d` flag.
    
    ```plaintext
     git branch -d <branch_name>
    ```
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1707464541479/38920969-1bb2-4364-8e30-e4dbd8b8e72a.webp align="center")

---

# ⏮️Git **Revert and Reset**

Two commonly used tools that git users will encounter are those of git reset and git revert . The benefit of both of these commands is that you can use them to remove or edit changes you’ve made in the code in previous commits. But both have the different purpose to serve.

1. ## **Git Revert**:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1707464850548/47277b41-d315-4005-b1a0-798e4e06379e.png align="center")
    
    This is used to revert back the specific changes which have already made in previous commits.
    

* To revert back the specific commit we have the unique Hash ID of every commit through which we can track them to quote that we use `git log` command, copy the Hash Id of the commit which want to be revert.
    

Now, use command `git revert` followed by the Hash\_Id.

```plaintext
git revert <Unique_Hash_ID>
```

This will create a new commit that undo the changes introduced by the specific

commit.

1. ## **Git Reset**:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1707464817935/45325235-d36e-46bc-9661-33a38f6f219f.png align="center")
    

This is used to reset the commit or undo the commit to previous changes where we have to commit again to track that changes. It is safety for you that in case you do not want to reset your commit and it was done accidentally you can again add the files to staging area and commit those using `git add .` and `git commit -m "commit Message"` commands. video for reference: https://youtu.be/OGk5rvYw8c0?si=0pPAEovq20qM\_pLt

There are different reset modes and let see the flags for them:

1) **Hard Reset (--hard)**: Resets both the index and working directory to the specified commit. This is the most aggressive mode, to shift pointer to the previous commit completely now head will be on previous commit completely.

```plaintext
git reset e3df726 --hard
```

2) **Soft Reset (--soft)**: Moves the HEAD to the specified commit but keeps changes in the index and working directory, or we can say normal reset.

```plaintext
git reset f2gh776 --soft
```

3) **Mixed Reset (--mixed)**: Default mode. Resets the index to the specified commit but keeps changes in the working directory.

```plaintext
git reset i7r89yu --mixed
```

---

# 🔀Git Rebase and Merge

1. ### What Is Git Rebase?
    

Command that lets users integrate changes from one branch to another, and the logs are modified once the action is complete. Git rebase was developed to overcome merging’s shortcomings, specifically regarding logs. this is used to keep neat and easy to find commits.

```plaintext
git rebase <base_branch> #Git Rebase
```

1. ### **What is Git Merge?**
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1707464964382/805e1a4d-5d88-4ccb-8af7-c84f0b553c49.png align="center")
    
    Imagine you're working on a group project with your friends. Each of you has a copy of the project files, and you're all making changes independently. When you're done with your changes and want to combine everyone's work, you merge.
    
    \- Git merge is like combining different versions of a project into one. It takes the changes from one branch (like your work) and applies them to another branch (like the main project). This creates a new commit, which represents the combined work of everyone involved.
    
    \- **Example:** Let's say you have a branch called "feature" where you've been adding new features to the project. When you're finished, you merge the "feature" branch into the "master" branch to incorporate your changes into the main project.
    

```plaintext
git merge <source_branch> # Git Merge
```

Suppose you have a Git repository with two branches: `master` and `feature` :

```plaintext
# Checkout the feature branch
git checkout feature

# Make some changes to the files
# Add, commit your changes
git add .
git commit -m "Implemented new feature"

# Switch back to the master branch
git checkout master

# Merge the changes from the feature branch into master
git merge feature
```

In this example, the `git merge feature` command combines the changes made in the `feature` branch into the `master` branch. After merging, you'll have a new commit on the `master` branch that includes the changes from the `feature` branch.

# **🚧Conclusion:**

understanding when to use `git revert`, `git reset`, `git merge`, and `git rebase` can greatly enhance your Git workflow. `git revert` is handy for undoing specific changes while preserving history, `git reset` allows you to manipulate the current state of the repository, `git merge` is useful for integrating changes from different branches, and `git rebase` helps in maintaining a clean and linear commit history by integrating changes from one branch onto another. Mastering these commands empowers developers to efficiently manage project history and collaboration in Git.

***Happy Learning😊***