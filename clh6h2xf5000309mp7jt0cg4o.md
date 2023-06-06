---
title: "Day 8 Task: Basic Git & GitHub for DevOps Engineers."
datePublished: Tue May 02 2023 16:17:12 GMT+0000 (Coordinated Universal Time)
cuid: clh6h2xf5000309mp7jt0cg4o
slug: day-8-task-basic-git-github-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/wX2L8L-fGeA/upload/e53b283a18f11961293fe47b39f79818.jpeg
tags: aws, github, git, devops, gitlab

---

### What is Git?

Ans:- Git is a version control system that allows you to track changes to files and coordinate work on those files among multiple people. It is commonly used for software development, but it can be used to track changes to any set of files.

With Git, you can keep a record of who made changes to what part of a file, and you can revert to earlier versions of the file if needed. Git also makes it easy to collaborate with others, as you can share changes and merge the changes made by different people into a single version of a file.

### What is GitHub?

Ans:-GitHub is a web-based platform that provides hosting for version control using Git. It is a subsidiary of Microsoft, and it offers all of the distributed version control and source code management (SCM) functionality of Git as well as adding its own features. GitHub is a very popular platform for developers to share and collaborate on projects, and it is also used for hosting open-source projects.

### What is Version Control? How many types of version controls do we have?

Ans:- Version control is a system that tracks changes to a file or set of files over time so that you can recall specific versions later. It allows you to revert files to a previous state, revert the entire project to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more.

There are two main types of version control systems: centralized version control systems and distributed version control systems.

1. A centralized version control system (CVCS) uses a central server to store all the versions of a project's files. Developers "check out" files from the central server, make changes, and then "check-in" the updated files. Examples of CVCS include Subversion and Perforce.
    
2. A distributed version control system (DVCS) allows developers to "clone" an entire repository, including the entire version history of the project. This means that they have a complete local copy of the repository, including all branches and past versions. Developers can work independently and then later merge their changes back into the main repository. Examples of DVCS include Git, Mercurial, and Darcs.
    

### Why do we use distributed version control over centralized version control?

Ans:- Better collaboration: In a DVCS, every developer has a full copy of the repository, including the entire history of all changes. This makes it easier for developers to work together, as they don't have to constantly communicate with a central server to commit their changes or to see the changes made by others.

1. Improved speed: Because developers have a local copy of the repository, they can commit their changes and perform other version control actions faster, as they don't have to communicate with a central server.
    
2. Greater flexibility: With a DVCS, developers can work offline and commit their changes later when they do have an internet connection. They can also choose to share their changes with only a subset of the team, rather than pushing all of their changes to a central server.
    
3. Enhanced security: In a DVCS, the repository history is stored on multiple servers and computers, which makes it more resistant to data loss. If the central server in a CVCS goes down or the repository becomes corrupted, it can be difficult to recover the lost data.
    

Overall, the decentralized nature of a DVCS allows for greater collaboration, flexibility, and security, making it a popular choice for many teams.

### **Basics of Git**

## Exercises:

1. **Create a new repository on GitHub and clone it to your local machine**
    
    Ans:-
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682703099742/9c94010c-95dc-48e8-ac20-d872c734244e.png align="center")
    
    git clone [https://github.com/saumyaranjan2003/testgithub.git](https://github.com/saumyaranjan2003/testgithub.git)
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682703137202/8b0eebba-76cd-4df6-ade3-c254aae88d52.png align="center")
    
2. **Make some changes to a file in the repository and commit them to the repository using Git, Push the changes back to the repository on GitHub**
    
    Ans:- Before
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682704215805/d69bd425-faff-4d22-8c86-4aa2c09d3fdb.png align="center")
    
    ```bash
    vim test
    git add test
    git commit -m "changes done"
    git push
    ```
    
    After
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682704366574/188fbf15-270f-4db3-a979-8fc8fe4e5224.png align="center")