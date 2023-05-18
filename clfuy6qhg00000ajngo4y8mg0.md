---
title: "3. Features Of Git & Areas In Git"
seoTitle: "Mastering Git: Features & Areas"
seoDescription: "Explore the essential features of Git and the different areas within Git including working directory, staging area, and repository, in this in-depth article"
datePublished: Thu Mar 30 2023 10:03:07 GMT+0000 (Coordinated Universal Time)
cuid: clfuy6qhg00000ajngo4y8mg0
slug: 3-features-of-git-areas-in-git
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680167977428/afcbb01a-e6aa-4eaf-832d-4c773483d3e2.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680170172189/78540c0a-9d14-465a-9383-b5b0ac387c71.jpeg
tags: github, version-control, git, devops, devops-articles

---

# Introduction

Git is a distributed version control system that is used for managing source code changes. It was created by **Linus Torvalds** in **2005** and has since become one of the most widely used version control systems in the software development industry.

At its core, Git is a tool for tracking changes to files over time. When developers work on a project, they create and modify files that make up the codebase. Git allows developers to save these changes, track the history of the changes, and collaborate with others on the same project.

One of the key benefits of Git is its distributed nature. Unlike centralized version control systems like **SVN**, Git does not rely on a central server to store all the changes. Instead, each developer has their own copy of the repository, which contains the complete history of the project. This means that developers can work on the project even if they are not connected to the internet, and they can merge their changes with the rest of the team when they are back online.

Git uses a branching model, which allows developers to create separate branches of the codebase for different features or bug fixes. This makes it easier to isolate changes and test them before merging them back into the main branch of the codebase. It also enables parallel development, where multiple developers can work on different parts of the codebase at the same time.

Didn't get it??????? 🤔🤔 No problem, let me explain in a simpler way..

Git is a tool that helps people work together on projects. Imagine you and your friends are building a sandcastle together. You each have your own part to work on, but you need to make sure everyone is working together and not undoing each other's work.

Git is like a big notebook that you all share. Whenever someone makes a change to their part of the sandcastle, they write it down in the notebook. This way, everyone can see what changes have been made and what still needs to be done.

If someone accidentally knocks over part of the sandcastle, you can use the notebook to go back and see what it looked like before the accident. This helps you fix the mistake and get back on track.

Git also helps you work on different parts of the project at the same time without getting in each other's way. Just like you and your friends might each work on different parts of the sandcastle, programmers can work on different parts of the code at the same time, and Git makes sure everyone's changes are kept separate and organized.

# Features Of Git

In addition to branching, Git also provides a number of other features that help with collaboration and code management. These include:

1. **Committing changes**: Developers can use the "git commit" command to save changes to the repository. Each commit contains a message that describes the changes made, and a unique identifier that can be used to reference the commit later.
    
2. **Merging changes**: When two branches of the codebase have diverged, developers can use the "git merge" command to combine the changes and create a newly merged branch.
    
3. **Reverting changes**: If a commit causes problems or introduces bugs, developers can use the "git revert" command to undo the changes and restore the codebase to a previous state.
    
4. **Pulling and pushing changes**: Developers can use the "git pull" command to retrieve changes from a remote repository, and the "git push" command to upload their changes to the remote repository.
    
5. **Managing conflicts**: When two developers make changes to the same part of the codebase, Git will detect a conflict and ask the developers to resolve it manually.
    
6. **Checkout & Commit**: All the Checkout & Commit operations are performed locally (Local repository), therefore the performance is more. The operations are performed with high Speed.
    
7. Even Without the network, developers can continue their work. Developer’s workspace need not be connected to the Remote Repository always.
    
8. **Staging Area**: This is the biggest strength of the GIT Version Control System. This type of Arrangement (Staging Area) is not there in the other Version Control System.
    
9. GIT is Freeware and OpenSource i.e based on our requirements we can customize it.
    
10. GIT provides support for multiple platforms.
    
11. **Single Point Of Failure**: This means that every developer has a complete copy of the codebase on their local machine, rather than relying on a central server to store all the changes.
    
    In a traditional **SPoF** (Single Point Of Failure) model, if the central server fails or becomes unavailable, developers are unable to access the codebase or collaborate with others. This can be a major problem for software development teams, as it can result in significant downtime and lost productivity.
    
    With Git, however, each developer has a local copy of the repository, which contains the complete history of the project. This means that even if the central server goes down, developers can continue to work on the project and collaborate with others. They can make changes to their local copy of the codebase, and then sync those changes back to the central server once it becomes available again.
    

# Areas Of Git

In Git, there are several key areas of Git where the user works:

1. **Working directory**: This is the directory on your local computer where you have checked out a copy of the Git repository. It contains all the files and directories that make up the current version of the code.
    
2. **Staging area/index**: This is an intermediate area where you can prepare changes before committing them to the Git repository. You can add files to the staging area using the "git add" command, and then review and modify the changes before committing them.
    
3. **Local repository**: This is a copy of the Git repository that is stored on your local computer. It contains all the changes that you have committed to the repository, as well as the complete history of the project.
    
4. **Remote repository**: This is the copy of the Git repository that is stored on a remote server, such as GitHub or GitLab. It is a centralized location where all the changes made by different developers are collected and stored.
    

# Understanding Staging Area

Assume that there is a working directory created by a developer where he/she is working.

![](https://lh6.googleusercontent.com/J4GvsGTLPxAhaatvti_9yaxEuZAJ4-TKm1L6Sf1wgbFrON4cKnDkPaPljRQuvUWnv5SW53V7I16QXATdJ-x5krC4xCmazi1OMo2tjMN_8i7uc4ASA_xln7SES5MqHiv1PyDp03h6NRSY7wm_PM_QSQ align="center")

And then there is a **Local repository** (We'll discuss later how it'll get created).

![](https://lh3.googleusercontent.com/UO8oPngU2bKVqrY1traMkNsYCddsmClLhq4T6LeFqZzOmbzp6_W-KXEQ3VkHq-B2ijv4ZvhiO2x1ozGXl6jmkbQnGGpcv5oUY9DDkXV8lcAY9me9XFZggYbyI-BxpF6cF1eNTGaxayM-m5QKOR7l8g align="center")

He/She created one file in the working directory and added some code.

![](https://lh5.googleusercontent.com/yd_qU-PGenzTRbMe7YY3qKM3YqWk6dVsTaT97m8kMCjY_APLF49BfOS2MHHkbXnix5axHyR-A83KnjZJjM0Akh1itvTQMb08hS3Wvwsmq4Wo_42FEGwprM4ypl4X1kXcLp2q0paB512PjjI1bFvRhA align="center")

Now, he/she wants to Commit that file to the Local Repository.

**Q.** How is he/she gonna do that? I.e How the Commit operation of the file will be performed to the Local Repository.

**Ans:** Many Developers will think that by performing the commit operations (Commit command) we can commit (send) the file from the working directory to the local repository.

But this is not the way that's gonna happen.

* In GIT, Commit is a **2-step process**.
    
* First, we have to add files to the **Staging Area** and then we have to **Commit** from that Staging Area.
    
* So, in between the **Working Directory** and the **Local repository**, there is one layer/place (Virtual) to store our files before Committing. That Place is known as the **Staging Area**.
    

![](https://lh3.googleusercontent.com/sXQmCkcMtUCivL4JKpvfM_YPyYhTU-I6wcSi5aoxF4P9cjq18LYpNQRuUiUc18D7549F4Zj2xsaBI7qbmYp1TZDxlRWv1RPvfcBLnEkzD0oFarXaRyinIhBUXuwJy2_94eAsFny5UXiO0a8ObB5Z5Q align="center")

* **Staging Area** is also known as **Index Area** or **Cache Area**.
    

**Note:** Usually there will be no copy of the files/codes present in the **Staging Area** after performing the **Commit** Operation.

* **Staging Area** is in between the **Workspace** and the **Local Repository**, so it's present in every developer’s local machine.
    
* We can’t check the size of the file in the **Staging Area** as it'll be in the encrypted form.
    
* In order to Add the files to the **Staging Area** there are various options available:
    
* **git add .** : Command to add all the files to the **Staging Area** from the current **Workspace/Working Directory**.
    
* To Add the particular files.
    

**Syntax:**

`git add <filename 1> <filename 2>`

* To add files of a particular extension
    

To add files of a particular extension i.e we can use the **Regular Expression Patterns** Example: All the .txt only, or All the .py files.

**Syntax:**

`git add *.<filename.ext>`

* To add the multiple extension files
    

In order to add the multiple extension files.

**Syntax:**

`Git add *.<filename.ext1> <filename.ext2>`

## Benefit Of Staging Area

One of the benefits of a **Staging Area** is before committing, the code will be sent/saved to the staging area, that’s why we can double-check/cross-check every change before committing. Even from the staging area, we can get back to the working directory. If everything is fine then we can commit.

![](https://lh5.googleusercontent.com/9GeJ8xJKwtIEpC0d7NJisFWNCzedHlIm7KD9YSXdjxlwo46mxA39o1g38LW_CXLEf_3BLzDnhUosm1800EEMIkpwp7Ye8pbGWS98II8DzlqX199jRnKQKKmr03wgZV1u09sZZp_X9Ov_IyxvZp7vvw align="center")

**Note:** The Versioning system will not be maintained in the **Staging Area**. It’ll be having the files only. Versions will be maintained in the repositories (**Local**, **Remote**) only.

# Branching And Merging

**Note**: I've put just an intro of the concept "Branching and Merging", we'll discuss it in depth later in this series.

Suppose a developer is having a Working Directory and in that having the Local Repository. And he is working on the files in the Working Directory.

![](https://lh6.googleusercontent.com/J2ehEjiUVEVVlGliImX1zhxGYmt8k9gecVGDy8sqmsULjoc-JAqs0VDO_0WO6G4Xu7vSG40C5jjj1rKoisOtiLgwf9fMsy_9_1cZCtaq_ptLKBr_3JDwsaV5VIPhNas9n5x-2P44tLNlNMo2dcdlKw align="center")

Then the client suggested some enhanced features be put in the Application / Project.

So, he can either continue making changes in the files present in the working directory or he can create a separate branch and continue our work related to that (Client’s) enhancement.

![](https://lh3.googleusercontent.com/rmvMgHrVgH2AVpLPiwvrzDVs8rCrHkiE-BZS22DOgnY9ilNcDKfzVaXmzKV50KMAjLEsef3QP76P2ojvoNoh1thE75enwaeEWLOzH6Tn8dhMQwIDfKjyCfr8h44cf3g6uhw_7Tcy07te2MeT-84MEg align="center")

Now, if the client wants the mobile version also then the developer will create another branch from the base and start working on it.

Once we create a branch then we can work on that branch independently. That is, if the developer performs any changes in a **Branch** then those changes won’t be reflected in the working directory.

Which means, all the branches are isolated / independent from each other.

So, the other biggest advantage is **multiple flows of development** which mean: Some developers can be on **Branch A**, some developers can be on **Branch B** and some developers can be on **Branch C** etc.

![](https://lh5.googleusercontent.com/OPNfdiOKCaGvbMnz-FqwGuEpU52sTAI9d-8aeTybjTATNPFgkCbhMorRopWY3hxEL6sgb6jdU-vzFN93xpga9kERr5T7CGPCGVFNr6EhIVAVrz-yCUtEtmtvosthhY4pRSqnu1N37g8cCjB_cKNQQw align="center")

Once the changes are done or the work gets completed then the developer can either Commit / Send that particular branch to the Remote Repository or he can Merge that particular branch with the other branches and then the total changes will be Committed to the local repository and then it’ll be pushed to the Remote Repository.

## Advantage Of Branching

Assume that a developer is working on a project/Application. Suddenly, a new requirement came and he has to work on the new requirement also, so, instead of disturbing the code/files present in the working directory, he’ll create a new branch and in that branch, he or another peer developer can work simultaneously.

So, the biggest advantage of the Branch is whatever files are there in the local repository will get copied into the newly created branch also. Now, he or the new team can work on the new requirements. Here the local repository is considered the **Master Branch**. So, here is the same work but multiple separate units we can do/perform. Such flow is known as **Multiple Flows Of Development** which is more convenient to the developers.