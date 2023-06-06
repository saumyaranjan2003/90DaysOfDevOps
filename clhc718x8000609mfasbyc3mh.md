---
title: "Day 9 Task: Deep Dive in Git & GitHub for DevOps Engineers."
datePublished: Sat May 06 2023 16:22:35 GMT+0000 (Coordinated Universal Time)
cuid: clhc718x8000609mfasbyc3mh
slug: day-9-task-deep-dive-in-git-github-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/KPAQpJYzH0Y/upload/126dcc40a9dd98a301f077390957cd8b.jpeg
tags: linux, aws, github, git, devops

---

**What is Git and why is it important?**

Git is a tool that allows you to *VCS(Version Control System)*. So What is the VCS(Version Control System) Version Control allows you to version your code/file.(it is a version control system that gives you whenever your file/code is created/deleted/modified). Git is a powerful tool that helps developers work more efficiently and collaborate more effectively. By tracking changes to code over time, Git makes it easier to develop high-quality software that meets the needs of users.

Git is important for several reasons:

1. Collaboration: Git allows multiple developers to work on the same codebase simultaneously, making it easier for teams to collaborate and merge their changes into a single codebase.
    
2. Version Control: Git tracks changes to a codebase over time, allowing developers to easily revert to earlier versions of the code if necessary. This is particularly important when bugs are introduced or changes need to be made to an earlier version of the code.
    
3. Branching and Merging: Git makes it easy to create new branches for experimental features or bug fixes and merge them back into the main codebase when they are complete.
    
4. Distributed Development: Git allows developers to work on their local copy of the codebase, making it easier to work offline and reducing the risk of conflicts with other developers.
    

**What is the difference Between Main Branch and Master Branch?**

In Git, both "main" and "master" branches are commonly used to refer to the primary branch of a repository that contains the latest stable version of the codebase. The difference between them is mainly in the naming convention.

the main difference between "main" and "master" is their naming convention. They both serve the same purpose, which is to represent the primary branch of a repository that contains the latest stable version of the codebase. It's important to note that Git itself does not have a preference for either term, and both "main" and "master" can be used interchangeably in Git commands.

**Can you explain the difference between Git and GitHub?**

Git is a distributed version control system that allows developers to manage changes to their codebase over time. It was developed by Linus Torvalds in 2005 to help manage the development of the Linux kernel. With Git, developers can track changes to their code, collaborate with others, and revert to previous versions if necessary.

GitHub, on the other hand, is a web-based platform that provides hosting for Git repositories. It was founded in 2008 and was later acquired by Microsoft. With GitHub, developers can create repositories, collaborate with others, and contribute to open-source projects. It also provides features such as bug tracking, wikis, and project management tools.

In short, Git is a version control system that allows developers to manage their codebase, while GitHub is a web-based platform that provides hosting for Git repositories and additional collaboration features.

**How do you create a new repository on GitHub?**

To create a new repository on GitHub, follow these steps:

1. Go to the GitHub homepage ([https://github.com/](https://github.com/)) and log in to your account.
    
2. Click the "+" icon on the top right corner of the page and select "New repository".
    
3. On the "Create a new repository" page, enter a name for your repository in the "Repository name" field.
    
4. Optionally, you can add a description for your repository in the "Description" field.
    
5. Choose whether you want your repository to be public or private. Public repositories are visible to everyone, while private repositories are only visible to you and the people you give access to.
    
6. Optionally, you can initialize your repository with a README file, a .gitignore file, and/or a license. These files can help you get started with your repository.
    
7. Click the "Create repository" button to create your new repository.
    

After creating your repository, you can start adding files to it, making changes to your code, and collaborating with others. You can also customize your repository settings, such as adding collaborators, enabling issues and pull requests, and configuring branch protection rules.

**What is the difference between local & remote repositories? How to connect local to remote?**

Local repositories and remote repositories are two different instances of the same Git repository, with the main difference being their location and accessibility. A local repository is stored on your local machine, while a remote repository is stored on a remote server or hosting service.

Here are some key differences between local and remote repositories:

|  | Local Repository | Remote Repository |
| --- | --- | --- |
| Location | Stored on your local machine | Stored on a remote server or hosting service |
| Access | Only accessible on your local machine | Accessible to anyone with the appropriate permissions |
| Collaboration | Only one person can work on it at a time | Multiple people can collaborate on it simultaneously |
| Backup | Not automatically backed up | Typically backed up automatically by the hosting service |

To connect your local repository to a remote repository, you will need to perform a process known as "remote tracking". Here are the general steps to follow:

1. Create a new remote repository on a hosting service like GitHub, GitLab, or Bitbucket.
    
2. Copy the remote repository URL provided by the hosting service.
    
3. In your local repository, use the `git remote add` command to add the remote repository to your local Git configuration. For example, if the URL is [`https://github.com/your-username/your-repo.git`](https://github.com/your-username/your-repo.git), you would run `git remote add origin` [`https://github.com/your-username/your-repo.git`](https://github.com/your-username/your-repo.git).
    
4. Use the `git push` command to upload your local changes to the remote repository. For example, if you want to push your local changes to the main branch of the remote repository, you would run `git push origin main`.
    
5. Use the `git fetch` command to retrieve any changes that have been made to the remote repository since you last synced with it.
    
6. Use the `git merge` or `git rebase` command to merge the changes from the remote repository into your local repository.
    

Overall, connecting your local repository to a remote repository allows you to collaborate with others and keep your code backed up and easily accessible from anywhere.

Or Watch This Video For Reff

%[https://youtu.be/uFaYgSVzy3w] 

## **TASKS**

**1) Set your user name and email address, which will be associated with your commits.**

git config --global [user.name](http://user.name) "Your Name"

git config --global [user.email](http://user.email) [you@example.com](mailto:you@example.com)

**2) Create a repository named "Devops" on GitHub**

**Connect your local repository to the repository on GitHub.**

**Create a new file in Devops/Git/Day-02.txt & add some content to it**

**Push your local commits to the repository on GitHub**

1. Log in to your GitHub account and click the "New" button on the left side of the screen.
    
2. Enter "Devops" as the repository name, select any other options you want (e.g. public/private, initializing with a README), and click the "Create repository" button at the bottom of the page.
    
3. Copy the URL of the repository, which should look something like [`https://github.com/your-username/Devops.git`](https://github.com/your-username/Devops.git).
    
4. On your local machine, navigate to the directory where you want to create your local repository for the "Devops" project.
    
5. Open a terminal or command prompt in that directory and run the following command to create a new local repository:
    
    ```plaintext
    git init
    ```
    
6. Use the following command to add a remote repository to your local Git configuration:
    
    ```plaintext
    git remote add origin https://github.com/your-username/Devops.git
    ```
    
    Replace "your-username" with your GitHub username.
    
7. Use the following command to pull the remote repository down to your local machine:
    
    ```plaintext
    git pull origin main
    ```
    
    This will synchronize the remote repository with your local repository.
    
8. Use the following command to create a new file named "Day-02.txt" inside the "Git" directory:
    
    ```plaintext
    touch Devops/Git/Day-02.txt
    ```
    
    This will create an empty file with the specified name.
    
9. Open the "Day-02.txt" file in a text editor and add some content to it.
    
10. Use the following commands to stage your changes and commit them to the local Git history:
    
    ```plaintext
    git add Devops/Git/Day-02.txt
    git commit -m "Add content to Day-02.txt"
    ```
    
    This will create a new commit with the changes you made to the file.
    
11. Use the following command to push your local commits to the remote repository on GitHub:
    
    ```plaintext
    git push origin main
    ```
    
    This will push your changes to the "main" branch of the remote repository on GitHub.