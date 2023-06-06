---
title: "Day 10 Task: Advance Git & GitHub for DevOps Engineers."
datePublished: Sat Jun 03 2023 17:18:09 GMT+0000 (Coordinated Universal Time)
cuid: clig9ck17000p09l9f1ps6wj9
slug: day-10-task-advance-git-github-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/MAYEkmn7G6E/upload/6eee4c1ee1cf2d704ac8f5a47d416676.jpeg
tags: aws, github, git, devops, gitlab

---

### Git Branching

Git branching is a powerful feature that allows developers to create separate paths of development within a Git repository. By creating branches, developers can work on new features or bug fixes without affecting the main codebase. Branches provide isolation and enable collaboration, making it easier to manage and merge changes later. This flexibility and version control capability makes Git branching an essential tool for efficient and organized software development workflows.

### Git Revert and Reset

Git Revert and Reset are two commands used in the Git version control system. "Git Revert" is used to create a new commit that undoes the changes made in a previous commit, while "Git Reset" allows you to move the HEAD and branch pointers to a specific commit, effectively erasing commits or changing the branch history. Both commands are powerful tools for managing and manipulating Git commits, but they have different purposes and implications.

### Git Rebase and Merge

Git Rebase and Git Merge are two different ways to integrate changes from one branch into another in Git. While both accomplish the same end goal of combining changes, they have different approaches and implications. Let's take a closer look at each of them:

1. Git Rebase: Git rebase is used to combine the changes from one branch onto another branch. It works by moving or applying the commits of one branch onto another branch. When you perform a rebase, Git takes the changes of the branch you're rebasing and replays them on top of another branch.
    
    Here's how the rebase process typically works:
    
    * Choose the branch that you want to rebase onto (the target branch).
        
    * Use the command `git rebase target-branch` while you're on the branch you want to rebase.
        
    * Git will rewind your branch to the common ancestor of the two branches and replay each of your commits on top of the target branch.
        
    
    The result of a rebase is a linear history where the commits from the rebased branch are "replayed" on top of the target branch. This can make the branch history cleaner and more straightforward. However, it's important to note that the original commits are discarded and replaced by new commits with different SHAs.
    
2. Git Merge: Git merge is another way to integrate changes from one branch into another. When you merge branches, Git combines the commits from both branches and creates a new commit that represents the merge result. The new commit has two parent commits, one from each branch being merged.
    
    The process of merging is straightforward:
    
    * Choose the branch that you want to merge into (the destination branch).
        
    * Use the command `git merge source-branch` while you're on the destination branch.
        
    * Git will create a new merge commit that incorporates the changes from the source branch into the destination branch.
        
    
    The result of a merge is a commit that has multiple parents, preserving the original commit history of both branches. This can result in a more complex branch history, especially when dealing with frequent merges.
    

## Task 1:

Add a text file called version01.txt inside the Devops/Git/ with “This is first feature of our application” written inside. This should be in a branch coming from `master`, \[hint try `git checkout -b dev`\], swithch to `dev` branch ( Make sure your commit message will reflect as "Added new feature"). \[Hint use your knowledge of creating branches and Git commit command\]

* version01.txt should reflect at local repo first followed by Remote repo for review. \[Hint use your knowledge of Git push and git pull commands here\]
    

Add new commit in `dev` branch after adding below mentioned content in Devops/Git/version01.txt: While writing the file make sure you write these lines

* 1st line&gt;&gt; This is the bug fix in development branch
    
* Commit this with message “ Added feature2 in development branch”
    
* 2nd line&gt;&gt; This is gadbad code
    
* Commit this with message “ Added feature3 in development branch
    
* 3rd line&gt;&gt; This feature will gadbad everything from now.
    
* Commit with message “ Added feature4 in development branch
    

Restore the file to a previous version where the content should be “This is the bug fix in development branch” \[Hint use git revert or reset according to your knowledge\]

Ans

1. Open a terminal or command prompt.
    
2. Navigate to the directory where your Git repository is located.
    
3. Create the `version01.txt` file inside the "Devops/Git" directory with the specified content:
    
    ```plaintext
    echo "This is the first feature of our application" > Devops/Git/version01.txt
    ```
    
4. Add the file to the staging area:
    
    ```plaintext
    git add Devops/Git/version01.txt
    ```
    
5. Commit the changes with the desired commit message:
    
    ```plaintext
    git commit -m "Added new feature"
    ```
    
6. Push the changes to the remote repository:
    
    ```plaintext
    git push origin dev
    ```
    
7. Open the `version01.txt` file and append the additional lines as mentioned:
    
    ```plaintext
    echo "This is the bug fix in development branch" >> Devops/Git/version01.txt
    echo "This is gadbad code" >> Devops/Git/version01.txt
    echo "This feature will gadbad everything from now." >> Devops/Git/version01.txt
    ```
    
8. Add the modified file to the staging area:
    
    ```plaintext
    git add Devops/Git/version01.txt
    ```
    
9. Commit the changes with the specified commit message:
    
    ```plaintext
    git commit -m "Added feature2 in development branch"
    ```
    
10. Push the changes to the remote repository:
    
    ```plaintext
    git push origin dev
    ```
    
11. To restore the file to a previous version, you have two options:
    
    Option 1: Using `git revert` (creates a new commit to reverse the changes)
    
    ```plaintext
    git revert HEAD
    ```
    
    Option 2: Using `git reset` (discards the last commit entirely)
    
    ```plaintext
    git reset HEAD^ --hard
    ```
    
    Choose the appropriate option based on your requirements.
    

Note: Make sure to replace `origin` with the name of your remote repository if it's different.

## Task 2:

* Demonstrate the concept of branches with 2 or more branches with screenshot.
    
* add some changes to `dev` branch and merge that branch in `master`
    
* as a practice try git rebase too, see what difference you get.
    
    Ans
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685812398496/84ab8056-37b7-44ac-aca8-452817663786.png align="center")
    
    Let's demonstrate the concept of branches with two branches named "dev" and "feature":
    
    1. Initialize a new Git repository or navigate to an existing repository in your terminal or command prompt.
        
    2. Create a new branch named "dev" and switch to it:
        
        ```plaintext
        git checkout -b dev
        ```
        
    3. Make some changes to the code or create new files in the repository.
        
    4. Add and commit the changes in the "dev" branch:
        
        ```plaintext
        git add .
        git commit -m "Made changes in the dev branch"
        ```
        
    5. Create another branch named "feature" from the "dev" branch:
        
        ```plaintext
        git checkout -b feature
        ```
        
    6. Make additional changes in the "feature" branch.
        
    7. Add and commit the changes in the "feature" branch:
        
        ```plaintext
        git add .
        git commit -m "Made changes in the feature branch"
        ```
        
    8. Switch back to the "dev" branch:
        
        ```plaintext
        git checkout dev
        ```
        
    9. Merge the "feature" branch into the "dev" branch:
        
        ```plaintext
        git merge feature
        ```
        
    10. Resolve any conflicts if they occur. If there are no conflicts, Git will automatically merge the branches.
        
    11. Now, switch to the "master" branch:
        
    
    ```plaintext
    git checkout master
    ```
    
    1. Merge the "dev" branch into the "master" branch:
        
    
    ```plaintext
    git merge dev
    ```
    
    1. Resolve any conflicts if they occur.
        
    2. Alternatively, you can use Git rebase instead of Git merge to integrate the changes from the "feature" branch into the "dev" branch. Run the following commands:
        
    
    ```plaintext
    git checkout feature
    git rebase dev
    ```
    
    This will apply the changes from the "feature" branch on top of the "dev" branch. 15. After resolving any conflicts, switch back to the "dev" branch:
    
    ```plaintext
    git checkout dev
    ```
    
    1. Merge the updated "feature" branch into the "dev" branch:
        
    
    ```plaintext
    git merge feature
    ```
    
    1. Finally, switch to the "master" branch and merge the updated "dev" branch into the "master" branch:
        
    
    ```plaintext
    git checkout master
    git merge dev
    ```
    
    Remember, it's important to review the changes and resolve any conflicts that may arise during the merge or rebase process.
    
    I hope this explanation helps you understand the concept of branches and their usage with Git.
    

## Note:

Simple Reference on branching:

%[https://www.youtube.com/watch?v=NzjK9beT_CY] 

Advance Reference on branching:

%[https://www.youtube.com/watch?v=7xhkEQS3dXw]