---
title: "15. Branching In Git (In Depth) - Part 2"
seoTitle: "Mastering Branching in Git: Tips & Techniques (Part 2)"
seoDescription: "Learn the intricacies of Git branching in this comprehensive guide. Dive into advanced concepts and strategies in this in-depth Part 2 installment"
datePublished: Thu May 18 2023 07:09:04 GMT+0000 (Coordinated Universal Time)
cuid: clhssjnb3000609li1zz5f6tx
slug: 15-branching-in-git-in-depth-part-2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684351210609/5fcc6645-dd4c-4eac-82fc-edd06ac778a0.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1684393579298/d0ddca52-96fd-432f-9b6a-e9e3b0de5283.jpeg
tags: github, version-control, git, devops, gitcommands

---

In this article, we'll work on a few examples to understand the concept of branching and many more concepts.

# 🔈Demo Of Branching Concept

Suppose, We have a master branch. And in that master branch, we have created a few files.

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684327625864/4a6bdaf7-c1cb-4f99-805f-f93490ae2a93.png align="center")

And have multiple **commits** as well.

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684327666424/ab13190e-a974-4aa1-94ad-af198a392e58.png align="center")

Now, we want to create a **Child Branch**. And all the files and **commit history** will be available in the **Child Branch** as well.

**Note:** All the files, commit whatever there are in the **Master Branch** by default will be available to the **Child Branch**. All the files, commits etc will be Inherited from the **Parent Branch** to the **Child Branch**.

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684327778018/8b05c8cc-5421-4c05-a857-07fb190722e3.png align="center")

Now if we create a new file & commit it in the Child branch. It won’t be available / present in the **Master Branch**.

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684327936935/7ce318d3-66a3-4015-be64-94d4d703e148.png align="center")

Now, after that, if we make any changes in the **Master branch** then those changes won’t be present in the **Child Branch** as we make the changes after the creation of that **Child Branch**.

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684328030266/dfc15422-b8ac-4543-ac1a-5d8ef6aff008.png align="center")

So, all the branches work in an isolated way.

**Note:** When we merge the Child Branch to the Master Branch, then only the files & commits available in the child branch will be visible in the **Master branch**

After that, we can delete the particular **Child branch**. All the branches will be present in the **same Repository**.

# **🔉Example On Branching Concept**

Create a project named “project1” using the command `mkdir`. And go inside the project using the command `cd`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684328245747/b4fc37bf-2625-4656-9ade-b626a7e53061.png align="center")

Now, initialize the Working Directory “project1” using the command  
`git init`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684329290263/48d37041-871a-4693-9019-36aabf2798ad.png align="center")

So, now the Local repository will be created.

Now, create three empty files in that Working directory “project1” using the command `touch`

`touch <filename>`

We’ll create the files “a.txt”, “b.txt” & “c.txt”. So, the command will be

`touch a.txt b.txt c.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684329412666/48d57bca-4d3b-4f3b-8e2f-01861f22b8d0.png align="center")

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684329486026/980394e4-5698-4e4d-b22c-b550c81856bc.png align="center")

Now, add these files one by one to the **Staging Area** and **Commit** them to the **Local Repository**.

We’ll use the command `git add <filename>; git commit -m "Message"`

Add the file “a.txt” to the staging area & commit it to the Local Repository.

The command will be `git add a.txt; git commit -m "Added a.txt"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684329775184/7c8109ae-60a4-4027-a478-dc29fce2faf3.png align="center")

Add the file “b.txt” to the staging area & commit it to the Local Repository.

The command will be `git add b.txt; git commit -m "Added b.txt"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684330175678/265a4498-99d3-42e2-9773-6cf9f05fcda3.png align="center")

After that add the file “c.txt” to the staging area & commit it to the Local Repository.

The command will be `git add c.txt; git commit -m "Added c.txt"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684330255912/0e5113e6-e301-4eb3-8abe-7bee50fd6ce9.png align="center")

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684330469584/1aa39d25-a412-421a-b626-60e9b65ba03b.png align="center")

So, we added and committed all the files to the **Master Branch**. To confirm this we’ll use the command `git branch`  Or `git status`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684330588482/6c44a08c-bd91-4d5b-8a6b-b1408d2c540c.png align="center")

It’ll show only one **Branch** (**Master**). This means we are having only one branch i.e **Master**

Note: The *symbol* ***Star*** (\*) indicates the current **Active Branch**. This means, currently on which Branch we are working and that’s the **Master Branch**

When we check the status of the git using the command `git status` it'll tell us we are on the **Master Branch**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684330838968/50fec4aa-958c-4fd8-b64c-3365ba9f2674.png align="center")

It’ll tell “On the Master Branch”, which means we have committed all the files to the **Master Branch**.

We’ll check the logs as well to know the total number of **Commits** and the **Commit ID**.

We’ll use the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684331145560/771d6b23-7133-43ac-a74a-d0214eb5e135.png align="center")

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684331222729/dcc8b5a4-804c-47ea-a481-9bf6f30702bd.png align="center")

After that now, we have to work on the new feature in that project.

So, Now instead of mixing the new feature in the master branch, we'll create a separate branch for better organisation of the files.

## 🔈Creating A New Branch

So, we’ll create a new branch named “Child1”. To create a new branch, we’ll use the command `git branch <Branch_Name>`

In our case. It’ll be `git branch Child1`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684331492073/9e997aad-5cae-4420-926b-c983d5f05105.png align="center")

The branch will be created; We’ll confirm that using the command  
`git branch`

It’ll list all the available branches.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684331562917/af84f6e8-7973-42e6-8048-a38d11af4aaf.png align="center")

Now, we’ll switch to that Child branch.

## **🔈Switching To The Branch**

As we had created a new branch “Child1”; So, now we’ll switch to that branch to work on the new feature in the project.

To switch to the branch we’ll use the command `git checkout` along with the **branch name**.

Syntax: `git checkout <Branch_Name>`

In our case, it’ll be `git checkout Child1`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684331747286/01c467ea-3d91-4698-8667-cf2c90dd7140.png align="center")

It’ll display a message “Switched to branch 'Child1'”.

Now, we’ve switched to the child branch “Child1”. To confirm that, we’ll use the command `git branch` Or `git status`

`git branch`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684331880327/2d0375da-7e8c-4927-8151-a3d7a6cd83db.png align="center")

If we’ll use the command **git branch**, then now the **star** symbol will be before Child1, which means the current Active Branch on which we'll be working is the **Child Branch** “Child1”.

If we’ll use the command `git status`, then now it’ll display the message **“On branch Child1”**

`git status`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684332027251/206c9001-36eb-4348-a6be-cfb20eb21e62.png align="center")

That means we have been switched to the branch “Child1” and there is nothing to commit, and the working tree is clean.

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684332171970/12168bd4-01de-4fa1-b926-3c541c4d8a7a.png align="center")

All the files & commits of the **Master Branch** will be available in the **Child Branch** “Child1” as well.

**Reason:** All the files, commits etc will be Inherited from the **Parent Branch** to the **Child Branch**.

# 🏷️ All Files & Commits Will Be Inherited From Parent Branch To Child Branch

We can confirm that all the files, commits etc will be inherited from the parent branch to the child branch by the following steps

* Checking / Matching the tracked files on the Child Branch.
    
* Checking / Matching the Logs in the Child Branch.
    
* Checking The Head in the logs in the Child Branch.
    

## ⚙️ Checking / Matching Tracked Files On Child Branch

As we have been moved to the Child branch “child branch”. So, now to confirm that all the files, commits etc will be inherited from the parent branch to the child branch, we’ll be checking / Matching the tracked files on the Child Branch.

To list the tracked files on the Child Branch we’ll use the  command  
`git ls-files`

It’ll list all the same tracked files present in the Master Branch i.e files “a.txt”, “b.txt” & “c.txt”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684333683556/4f84144e-fd0c-4fa6-98fe-fb113e843a48.png align="center")

This shows that the files have been inherited from the parent branch to the child branch.

## ⚙️ Checking / Matching Logs In Child Branch

As we have been moved to the Child branch “child branch”. So, now to confirm that all the files, commits etc will be inherited from the parent branch to the child branch, we’ll be checking / Matching the  Logs in the Child Branch.

To list the logs in the Child Branch we’ll use the command  
`git log --oneline`

It’ll list all the same logs & commit ID present in the Master Branch after committing the files “a.txt”, “b.txt” & “c.txt” one by one.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684333814271/ab451c5d-c189-480d-8676-274737540957.png align="center")

This shows that the commits have been inherited from the parent branch to the child branch.

## ⚙️ Checking The Position Of Head In Logs In Child Branch

As we have been moved to the Child branch “child branch”. So, now to confirm that all the files, commits etc will be inherited from the parent branch to the child branch, we’ll be checking the position of the **Head** in logs in the Child Branch.

To list the logs in the Child Branch we’ll use the command  
`git log --oneline`

We’ll see that the HEAD has been pointing to the “Child1” Branch as well as the “Master” Branch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684333946865/b558cdf9-b2da-47e4-b934-0e7bae61fa40.png align="center")

This shows that the commits have been inherited from the parent branch to the child branch.

# Operations On Child Branch

Now, as we are on the child branch “Child1”, we’ll perform a few operations in it.

We’ll create three empty files using the command `touch`

Syntax: `touch <filename>`

We’ll create the files “x.txt”, “y.txt” & “z.txt” in the working directory “project1”. So, the command will be `touch x.txt y.txt z.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684334115004/4f20f251-fc61-48ee-bb48-d27fa46fabae.png align="center")

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684334157706/ed7fdb43-8228-443e-815f-891b62bebd26.png align="center")

Now, add these files one by one to the **Staging Area** and **Commit** them to the **Local Repository**.

We’ll use the command `git add <filename>; git commit -m "Message"`

Add the file “x.txt” to the staging area & commit it to the Local Repository.

The command will be `git add x.txt; git commit -m "Added x.txt"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684334306338/026f29a5-db42-4fff-b30c-cd86c102191a.png align="center")

Add the file “y.txt” to the staging area & commit it to the Local Repository.

The command will be `git add y.txt; git commit -m "Added y.txt"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684334364358/811bc487-346c-417c-a826-3024790e6ac3.png align="center")

And lastly, Add the file “z.txt” to the staging area & commit it to the Local Repository.

The command will be `git add z.txt; git commit -m "Added z.txt"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684334454622/ef234743-33e3-456c-9539-b30bf4f481e5.png align="center")

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684334518709/8619c763-2900-430a-97b9-dd2477f9ec22.png align="center")

So, we added and committed all the files to the **Child1 Branch**. To confirm this we’ll use the command `git branch` Or `git status`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684331880327/2d0375da-7e8c-4927-8151-a3d7a6cd83db.png align="center")

It’ll now show two branches **Master** & **Child1**.

The *symbol* ***Star* (\*)** indicates the current **Active Branch**. This means, currently on which Branch we are working and that’s the **Child1 Branch**

When we check the status of the git using the command `git status`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684332027251/206c9001-36eb-4348-a6be-cfb20eb21e62.png align="center")

It’ll tell “On the Child1 Branch”, which means we have committed all the files to the **Child1 Branch**.

We’ll check the logs as well to know the total number of **Commits** and the **Commit ID**. We’ll use the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684334868771/0624e5d7-3e87-467f-9e1e-203e583c6e0d.png align="center")

There are 6 commits in the Child Branch “child1”, but there will be only 3 commits in the Master Branch

To prove that we’ll switch back to the Master branch.

# Switching The Branch

Now, we’ll confirm that the operation done on the Child branch is isolated from the Master Branch.

To do that, we’ll switch to the Master Branch. To switch to the branch we’ll use the command **git checkout** along with the **branch name**.

Syntax: `git checkout <Branch_Name>`

In our case, it’ll be `git checkout master`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684335130927/29da7cbe-2352-456a-bef2-d096c00addda.png align="center")

It’ll display a message “Switched to branch 'master'”.

Now, we’ll switch to the child branch “master”. To confirm that, we’ll use the command `git branch`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684335201083/bd1063a6-8320-4237-935c-f56dbd8bb3c7.png align="center")

# 🏷️Parent Branch Won’t Inherit Files & Commits Of Child Branch

We can confirm that the Parent Branch won’t inherit Files & Commits of the Child Branch by the following steps

* Checking / Matching all the files on the Master Branch.
    
* Checking / Matching the tracked files on the Master Branch.
    
* Checking / Matching the Logs in the Master Branch.
    
* Checking The Head in the logs in the Master Branch.
    

## ⚙️ Checking / Matching All Files In Working Directory Of Master Branch

As we have been moved to the Master branch. So, now to confirm that the Parent Branch won’t inherit Files & Commits of the Child Branch, we’ll Check / Match all files in the Working Directory of the Master Branch.

To list all the files in the Working Directory of the Master Branch we’ll use the  command `ls`

It’ll list all the files present in the Master Branch i.e. files “a.txt”, “b.txt” & “c.txt”. But not any of the files that we had created in the Child branch “Child1” i.e. files “x.txt”, “y.txt” & “z.txt”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684343803319/83e51af5-b5bf-49f6-ac96-6b5f956cb6b6.png align="center")

## ⚙️ Checking / Matching Tracked Files On Master Branch

As we have been moved to the Master branch. So, now in order to confirm that the Parent Branch won’t inherit Files & Commits of the Child Branch, we’ll be checking / Matching all the tracked files in the Working Directory of the Master Branch.

To list all the tracked files in the Working Directory of the Master Branch we’ll use the  command `git ls-files`

It’ll list all the tracked files present in the Master Branch i.e. files “a.txt”, “b.txt” & “c.txt”. But not the tracked files that we had created in the Child branch “Child1” i.e. files “x.txt”, “y.txt” & “z.txt”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684343902222/909b0c08-08c0-4493-a931-2b795337bea2.png align="center")

## ⚙️ Checking / Matching Logs In Master Branch

As we have been moved to the Master branch. So, now to confirm that the Parent Branch won’t inherit Files & Commits of the Child Branch, we’ll be checking / Matching the Logs in the Master Branch.

To list the logs in the Master Branch we’ll use the command  
`git log --oneline`

It’ll list all the previous logs & commit IDs that were present in the Master Branch after committing the files “a.txt”, “b.txt” & “c.txt” one by one.

But it’ll not show any of the commits that we did in the Child Branch “Child1”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684344044227/077abc96-8307-4e18-b6eb-6bb4e5dfc6e6.png align="center")

## ⚙️ Checking The Position Of Head In Logs In Master Branch

As we have been moved to the Master branch. So, now to confirm that the Parent Branch won’t inherit Files & Commits of the Child Branch, we’ll be checking the position of the **Head** in logs in the **Master** Branch.

To list the logs in the Master Branch we’ll use the command  
`git log --oneline`

We’ll see that the HEAD has been pointing to the “Master” Branch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684344164247/9106a05c-8fa6-43f9-a6bc-6b27b27cd678.png align="center")

**Note:** While switching to the branch, Git only does one operation, and that is **Reassigning HEAD** to the current Active Branch.

# 🏷️ Multiple Use Cases Of Branching

There are multiple use cases where branching is required.

Without affecting the main flow of the development, we can hot-fix the error using the concept of Branching.

**Example:**

If we have multiple commits on the Master Branch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684349816432/eac838ee-e7ff-4a7f-ae1d-5450a12cb2e8.png align="center")

Now, if we move the commit “C3’s” code-base to the production.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684349872996/38358f8d-6f95-4ad0-9eba-95e4fcc96918.png align="center")

But still, the developers are working on the next release from the commit of the code-base “C4”, “C5” & “C6”.

Now, if some bugs are being identified in the production’s code-base. And we have to fix it immediately (Hot-fix).

**Note:** Hot-fix means fixing the bug Immediately. And fixing that error is known as Patch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684350002783/bd941528-e6ca-4429-8be0-c70288764afe.png align="center")

So, without affecting the main-flow i.e next release from the commit of the code-base “C4”, “C5” & “C6” we can fix the bug using the concept of Branching by creating a branch at the code-base of the commit “C3”. And then fixing the bug, and after that pushing it to production again.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684350068460/b025da3a-e719-40c7-a4a8-87538acad1c8.png align="center")

**Note:** For every project, there is a separate branch for the production code to fix the error.

If a team wants to work on new features after finishing, they will merge them into the master branch. It's just a good choice to keep the production branch separate so that there will be no confusion. (for example if someone merges anything by mistake it will be merged to the master branch, but if the master branch is itself a production branch it will create issues for the users of the software product)

To support multiple versions of the same code base we’ll require branching.

Ex: An old version of the software is having some bugs, but we don’t want to affect the other new versions after that version.

So, we’ll create a branch at that version by cloning the source code of that version, then fixing the Bugs and after that pushing it to production.

Here are few more real-life use cases where branching is commonly used:

1. **Feature Development**: When working on a new feature, developers can create a separate branch to work on that specific feature without affecting the main codebase. They can experiment, make changes, and collaborate with other team members on the feature branch, keeping the main branch stable and unaffected until the feature is ready to be merged.
    
2. **Bug Fixes**: When a bug is discovered in the main codebase, developers can create a branch to fix the bug. This allows them to isolate the bug fix from ongoing development, test the fix thoroughly, and then merge it back into the main branch once it's verified.
    
3. **Experimentation**: Developers often create branches to try out new ideas, experimental features, or alternative implementations. They can iterate and modify code without affecting the stability of the main branch. If the experiment is successful, they can merge the changes back into the main branch; otherwise, they can discard the branch.
    
4. **Release Management**: Branching plays a crucial role in managing software releases. A stable branch, often called a release branch, is created to prepare the software for deployment. This branch receives only critical bug fixes and necessary updates to maintain stability. Meanwhile, development continues on separate branches, allowing the team to work on new features and bug fixes for future releases.
    
5. **Collaboration and Code Reviews**: Branches facilitate collaboration among team members. Each developer can create a branch to work on a specific task or feature. They can then share their branch with other team members for code review, feedback, and collaboration. Once the code review process is complete, the branch can be merged into the main branch.
    
6. **Hotfixes**: In the event of a critical bug or security vulnerability in the production code, a hotfix branch can be created from the stable release branch. Developers can quickly address the issue in the hotfix branch, test it thoroughly, and deploy it to production. This allows for immediate fixes without disrupting ongoing development on other branches.
    

🤝 Next Topic **Git Merge** on Tuesday !!!!!!!!!!!

👋👋👋👋

%[https://tenor.com/view/talk-soon-talk-to-you-soon-later-leaving-bye-gif-11819904]