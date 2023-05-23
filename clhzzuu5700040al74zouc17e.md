---
title: "16. Git Merge (Part - 1)"
seoTitle: "Git Merge: Ultimate Guide (Part 1)"
seoDescription: "Discover the essential techniques of Git merge in this comprehensive guide. Dive into Part 1 of our series and learn how to merge branches effectively."
datePublished: Tue May 23 2023 08:08:07 GMT+0000 (Coordinated Universal Time)
cuid: clhzzuu5700040al74zouc17e
slug: 16-git-merge-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684828161816/202451b3-4855-411e-a6d4-5877431b8f42.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1684829215859/5d93f2d1-3bd7-47eb-bf42-385504791f85.jpeg
tags: github, git, devops, devops-articles, gitcommands

---

# Introduction

One of the fundamental operations in Git is merging, which combines changes from different branches into a single branch. This process is commonly used when integrating new features, bug fixes, or updates from one branch into another, such as merging a feature branch into the main branch (often called the "master" or "main" branch).

Merging is the process of taking the changes from one branch and applying them to another branch. It allows you to bring together the work done in different branches and create a unified version of the project.

Assume that we created a branch to implement a new feature. And we complete the implementation of that new feature. Once that implementation is completed for that branch, we have to combine those changes from the **Child Branch** with the **Parent Branch**.

This process of combining the changes from the **Child Branch** with the **Parent Branch** is known as **Merging**.

And then we can push it to the **Remote Repository**.

## Example

Let's consider we are working on the Master Branch for a project and suddenly we need to create a new feature in that, so we have to create a new feature and we don’t wanna create any mess in the project's main code and want that the work on the project should be continuing as well. Therefore, we’ll create a branch (Child branch) for working on the new feature.

After completing the work, that branch (Child Branch) can be either merged with **Parent/Main/Master Branch** and then push to the **Remote Repository** or directly pushed to the Remote Repository.

**Note:** In companies, it’s better to merge/combine the new feature with the **Parent/Main/Master Branch** and then push it to the **Remote Repository**.

**Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684778089167/0d361d04-0348-44a7-be28-01655c1b0eb3.png align="center")

# How To Perform Merging

To do merging of a **Child Branch** to the **Parent / Main / Master Branch** we’ll use the command `git merge` staying at the **Parent / Master Branch** and also specifying the name of the **Child Branch**

**Syntax**

`git merge <Child Branch Name>`

## **Example**

Let’s create two commits on the **Master Branch**. By default, we’ll be on the **Master Branch**.

### **Pictorial Representation**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684778373680/195a545e-cce4-42f9-9af5-93dcd09043bb.png align="center")

Suddenly, a new requirement came to implement a new feature. To implement a new feature without affecting the **Master Branch**, we’ll create a **Child Branch**. And suppose in the **Child Branch / Feature Branch** we did two commit operations.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684778521464/10b45f44-0cfc-4127-b07e-2c052a15846f.png align="center")

In between the work on the Child Branch i.e. on the new feature, the work on the other things i.e. the Master Branch is also going on.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684779002125/282d2cc5-6c2b-4a1e-9bd0-681e8dd97d8a.png align="center")

Now, after the completion of the work on the feature branch. We’ll merge that branch to the **Master Branch**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684779138657/d358c31f-a83d-4855-92ec-7ee38a3e9de3.png align="center")

### Practical

Create a new directory named “merging”. And move inside into that directory using the command `cd`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684779365884/bc27c4f0-4e24-4c53-8768-4d6abaa45ef9.png align="center")

Now, initialize that directory using the command `git init`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684779500245/f358d0d8-f00f-4803-90ec-f444a3a5306e.png align="center")

Create two empty files in that directory named “a.txt” & “b.txt”. To create the empty files, we’ll use the command `touch`

`touch a.txt b.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684779730284/0b4eb614-6a8f-4ef8-b5d8-c760efa5acb7.png align="center")

Now, check the status of the files. To check the status of the files, we’ll use the command `git status` . The files will be **Untracked**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684779957186/f7946e1f-afbd-462b-a65a-e417710b8a3d.png align="center")

Add a file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Commit 1"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684780162910/8d53783a-c160-48f6-9839-b19cd84e6717.png align="center")

And after that add the file “b.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add b.txt; git commit -m "Commit 2"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684780321567/32ee7e61-263c-4294-829f-c4288be4d48a.png align="center")

Now, there are two commits available at the **Master Branch**. To confirm that we’ll check the log using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684780435463/2fe5dfe6-779f-4eb0-84c9-486fd46a754a.png align="center")

Now, we have to work on a feature, so we’ll create a child branch named “feature”. So, we’ll create a child branch and switch to that branch using the command `git checkout -b <branch name>`

In our case, it’ll be `git checkout -b feature`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684780595223/60bc0fc1-36f2-48e8-8b8c-f98c4fbd819b.png align="center")

We’ll now confirm the total no. of branches and whether we switched to the new **Child Branch** “feature” or not. To confirm both, we’ll use the command `git branch`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684817773154/62d201af-e35b-410b-b144-fedf08d5687b.png align="center")

We’ll see there are total two branches

* master
    
* feature &lt;Child Branch&gt;
    

And we’ll also see the position of the star “**\***” is on the “feature” i.e Child Branch; This indicates that we have been switched to the Child Branch.

Create two empty files in that directory named “x.txt” & “y.txt”. To create the empty files, we’ll use the command `touch`  
`touch x.txt y.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684818074073/f8e922fe-570b-40a3-a45e-dcb5e429276b.png align="center")

Now, check the status of the files. To check the status of the files, we’ll use the command `git status`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684818222435/58c90870-c75f-4e96-8d5b-dd4789bdb20f.png align="center")

We are on the **feature branch** and the files are **Untracked**.

  
Now add the file “x.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

`git add x.txt; git commit -m "Child Commit 1"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684818402758/9ecfcbdb-c51b-40bb-a385-0436e3e030e9.png align="center")

And after that add the file “y.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

`git add y.txt; git commit -m "Child Commit 2"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684818552163/244a8594-a887-4b94-af7d-6691731dde82.png align="center")

Now, we’ll check the total no. of files on the Feature Branch using the command `ls`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684819140301/accd21f6-1306-4c96-91fb-8f0c1e359526.png align="center")

There will be a total of four files in the working directory. Two files “a.txt” & “b.txt” from the Master Branch that got inherited from the Parent Branch while creating the Child Branch. And the other two files “c.txt” & “y.txt” have been created in the Child branch.

Now, if we’ll check the logs using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684820496121/de2775d7-d157-48ea-9431-78e8d446c822.png align="center")

Then there will be a total of four commits. Two commits from the Master Branch & the other two commits from this branch i.e. the child branch.

Now we’ll merge the **feature Branch** to the **Master Branch**. So, as Master Branch requires these changes, therefore we have to execute the command i.e. we’ll merge the Child branch to the Master Branch by staying/switching to the Master Branch.

To merge the Child Branch with the Master Branch we’ll use the command `git merge <Branch Name>`

In our case, it’ll be `git merge feature`

But, before that, we have to switch back to the Master Branch, as we are on the Child Branch “feature”. So, to switch the branch, we’ll use the command `git checkout <Branch Name>`

In our case, it’ll be `git checkout master`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684819901733/3eec1592-b8e6-4872-983c-1686f2c6b295.png align="center")

Now we’ll merge the **feature Branch** to the **Master Branch**. Therefore, we’ll use the command `git merge feature`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684820024122/a81e3e82-e227-4551-af49-66cc3c659434.png align="center")

The Child branch “feature” will be merged with the Parent Branch “master”. Two files were added to the Master Branch.

If we want to confirm, then we’ll check the branch we are residing currently using the command `git branch`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684820276383/6b16636b-a8b8-406a-a051-79cff2bad935.png align="center")

We’ll be on the Master Branch.

**Note:** After the Merging of the Branch, the Child Branch will still be present. If we want we can delete it. 

We’ll also confirm by checking all the files available in the Working directory of the Master Branch using the command `ls`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684819140301/accd21f6-1306-4c96-91fb-8f0c1e359526.png align="center")

To confirm we’ll check the log on the Master Branch using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684819655969/8e5ba3a4-cab0-4b65-8e16-2163356c4c4e.png align="center")

Previously, there were only two commits in the logs on the Master Branch. But now there will be four commits. And the HEAD will be pointing to the last commit on the Child Branch.

# Types Of Merge

There are Two-types of Merge:

* Fast-forward Merge
    
* Three-way Merge
    

##  Fast-forward Merge

Imagine we are having two branches (In the project)

* Parent Branch (master)
    
* Child Branch (feature)
    

  

At the second commit the Feature Branch (Child Branch) got created.

And after creating the Feature Branch (Child Branch), we made changes & commit to the Feature Branch only. We didn’t make any changes in the Master/Parent Branch.

So, after creating the Child Branch, if we don’t do any changes or commit in the Parent / Master Branch in that case GIT will perform **Fast-forward Merge**.

If there will be only two branches Parent & Child, and the updation are only available in the Child Branch and not in the Parent/Master Branch in this case the GIT will perform **Fast-forward Merge**.

In the **Fast-forward Merge**, GIT simply moves the pointer from the Parent Branch to the last commit of the Child Branch.

  

To confirm we’ll check the log on the Master Branch using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684819655969/8e5ba3a4-cab0-4b65-8e16-2163356c4c4e.png align="center")

Here both, Master & Child (feature) are pointing to the same commit i.e. the last commit of the **Child Branch**.

In the **Fast-forward Merge**, there is no chance of **Conflicts** because there is an update in the **Child Branch** only, not on the **Master Branch**.

### Example (Pictorial Representation)

Create a file named “a.txt” and add some data to that file.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684822948811/92b45e96-ce41-4961-9298-c10238c7b6af.png align="center")

After that commit that file in the Local Repository.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684823025520/ad18bd4b-5268-4158-8c42-67d7d9e91e22.png align="center")

Now, again add some data in that file “a.txt” and commit that changes in the Local Repository.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684823093670/ee0c403c-d7fc-4795-a238-0ca8ec5b3e57.png align="center")

Now, create a new branch (Child). Then automatically the properties i.e. files in the Working directory & Commits will be inherited to the Child branch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684823218788/d0928d7c-bb79-406a-a93f-3b915670c3d5.png align="center")

Now, add some data in that file “a.txt” present in the Child branch. And then commit those changes to the Local Repository.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684823311162/82aea39e-57fe-4145-9e52-d806043b7aa8.png align="center")

Now, again add some data in that file “a.txt” and commit that changes in the Local Repository of the Child Branch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684823422603/c2ed8fa2-adec-4a4d-bdbb-e0e5a6f3ba96.png align="center")

So, now we’ll merge the Child branch to the parent branch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684823497221/de5fd075-b874-4a12-9060-58152d952ad2.png align="center")

Now, as we see there are only 2 data in the parent branch whereas there are 4 data present in the child branch.

So, if we merge the Child branch to the Master Branch, then the Master will be pointing to the Last commit of the Child branch. And also, the final output after the change in the file a.txt will be having data 4.

  
So, even though the same file will be modified, in the **Fast-Forward merge** there will be no chance of conflicts.

## Practical

Create a new directory named “fastforward”. And move inside that directory using the command `cd`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684824535054/e7b64e46-f8ed-4ea2-8e6a-5d88bf6d7ee6.png align="center")

Now, initialize that directory using the command `git init`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684824658642/70052896-e46d-4123-8d50-8c0b014b5ea2.png align="center")

Create a file “a.txt” and write “data 1” in that file using the command **echo**. Therefore, the command will be `echo “Content” > <filename>`

In our case, it’ll be `echo “data 1” > a.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684824735036/ed64415a-8a56-45a0-8c77-68c5b17a0dee.png align="center")

Add that file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Commit 1"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684824898341/b0933111-d362-45b5-b1ef-be4eb7f3bc64.png align="center")

Now, again add some content by writing “data 2” in that file using the command **echo**. Therefore, the command will be  
`echo "Content" >> <filename>`

In our case, it’ll be `echo "data 2" >> a.txt`  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684825071254/5abda9c5-9f1e-428f-9040-53610746cacb.png align="center")

Add that file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Commit 2"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684825200719/611251a0-bf52-43f6-8549-f702a15e13dd.png align="center")

Now, there are two commits available at the **Master Branch**. To confirm that we’ll check the log using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684825394706/9bcf3927-aa9c-44c5-98b1-6a31686d993f.png align="center")

Now, we have to work on a feature, so we’ll create a child branch named “feature”.

So, we’ll create a child branch and switch to that branch using the command `git checkout -b <branch name>`

In our case, it’ll be `git checkout -b feature`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684825595550/073c8a8d-752b-4f4c-94d9-a2c4fad3360e.png align="center")

We’ll now confirm the total no. of branches and that had we switched to the new **Child Branch** “feature” or not. To confirm both, we’ll use the command `git branch`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684825676769/9f6302eb-c4f6-4360-b11b-23bc5f27375f.png align="center")

We’ll see there are total of two branches

* Master
    
* feature &lt;Child Branch&gt;
    

And we’ll also see the position of the star “**\***” on the “feature” i.e. Child Branch; This indicates that we have been switched to the Child Branch.

Now, again add some content by writing “data 3” in the file “a.txt” using the command **echo**. Therefore, the command will be  
`echo "Content" >> <filename>`

In our case, it’ll be `echo “data 3” >> a.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684825844592/db99627f-f97f-4e38-be17-f88eadf90b6a.png align="center")

Add that file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Commit 3"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684825957281/e7db503a-5644-49bc-b81d-12a56be0c63d.png align="center")

Now, again we’ll add some content by writing “data 4” in that file “a.txt” using the command **echo**. Therefore, the command will be  
`echo "Content" >> <filename>`

In our case, it’ll be `echo "data 4" >> a.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684826076449/e7616464-a08f-4568-8d6e-1b31eb0be394.png align="center")

Add that file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Commit 4"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684826286301/2d08ea8f-3b2e-4408-ae4a-37c4fc332bff.png align="center")

Now, there will be four commits available at the **Child Branch**. To confirm that we’ll check the log using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684826390590/2ac3b7a1-e170-4e3e-adf4-2c29d0b10f26.png align="center")

So, **HEAD** will be pointing to the last commit of the Child Branch.

Now, we’ll switch back to the Master Branch, as we are on the Child Branch “feature” and we have to now merge the Child Brange to the Master Branch. So, to switch the branch, we’ll use the command  
`git checkout <Branch Name>`

In our case, it’ll be `git checkout master`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684826527197/99126851-efda-4be3-b5c9-6c0032dcdb65.png align="center")

Now we’ll merge the **feature Branch** to the **Master Branch**. So, as Master Branch requires these changes, therefore we have to execute the command i.e. we’ll merge the Child branch to the Master Branch by staying/switching to the Master Branch.

To merge the Child Branch with the Master Branch we’ll use the command `git merge <Branch Name>`

In our case, it’ll be `git merge feature`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684826659464/43972e87-5b67-4020-8a22-ca3e70018b8e.png align="center")

Now, there will be four commits available at the **Master Branch**. To confirm that we’ll check the log using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684826849260/f038c7e9-2312-493c-9509-8787bf724e67.png align="center")

Now, both **HEAD** &  **Master** will be pointing to the last commit of the Child Branch.

Now, if we’ll check the content of the file “a.txt” present in the working directory of the Master Branch, then we’ll see there will now 4 lines added.

To check the content of the file “a.txt” we’ll use the command `cat`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684826945799/c0c3ea7a-b551-4b3e-a804-9fa2fd31d8dd.png align="center")

So, we didn’t get any **Conflict**.