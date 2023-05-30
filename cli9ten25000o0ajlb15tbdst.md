---
title: "17. Git Merge (Part - 2)"
seoTitle: "Git Merge: Ultimate Guide (Part 2) - Three Way Merge"
seoDescription: "Discover the power of three-way merge in Git Merge - Part 2. Learn advanced techniques for merging branches seamlessly. Level up your Git skills now!"
datePublished: Tue May 30 2023 05:05:15 GMT+0000 (Coordinated Universal Time)
cuid: cli9ten25000o0ajlb15tbdst
slug: 17-git-merge-part-2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1685385170225/c09cd02f-2864-49e1-b4a8-57a0f1517d0e.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1685422990303/1665bcab-f3ad-4af9-86e3-48d91f241a15.jpeg
tags: github, version-control, git, devops, gitcommands

---

# **🔈** Three-way Merge

Three-way merge is a common merging strategy used in Git to combine changes from two different branches or commits into a single unified result. It is designed to handle situations where multiple branches have made conflicting changes to the same file or lines of code.

When performing a three-way merge, Git identifies three versions of the code:

1. The common ancestor: This is the version of the file that both branches originally diverged from. It serves as the reference point for comparing the changes made in each branch.
    
2. The "ours" version: This represents the changes made in the branch where the merge is being performed. It includes any modifications or additions made to the file.
    
3. The "theirs" version: This refers to the changes made in the branch being merged into the current branch. It includes any modifications or additions made to the file in that branch.
    

Git uses these three versions of the code to intelligently merge the changes. It compares the differences between the common ancestor and the "ours" version and also between the common ancestor and the "theirs" version. Then, it combines these changes, considering both sets of modifications, to create a merged version of the file.

During the merge process, if there are conflicting changes (i.e., changes that overlap and cannot be automatically merged), Git will mark those conflicts and pause the merge. It prompts the user to manually resolve the conflicts by editing the affected file(s) to choose which changes to keep. Once the conflicts are resolved, the user can complete the merge by committing the changes.

The three-way merge strategy in Git helps to ensure that conflicting changes are handled properly and allows for an automated merging process in many cases. However, it may require manual intervention when conflicts occur, enabling developers to make informed decisions on how to merge conflicting changes.

So, basically after creating the Child Branch if the Parent Branch also contains some new commits then GIT will perform **Three-way Merge**.

## **🏷️** Practical

Create a new directory named “threewayMerge”. And move inside that directory using the command `cd`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685380986386/dd1f89b9-8755-4ffe-9d57-7bf831796b10.png align="center")

Now, initialize that directory using the command `git init`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381062785/3a84f9ec-61c2-45bf-990d-7257309f6732.png align="center")

Create two empty files “a.txt” & “b.txt” using the command `touch`.

We’ll use the command `touch <file1> <file2>`

In our case, it’ll be `touch a.txt b.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381187965/d12c8a62-2b58-443f-8c1f-275d5bd402af.png align="center")

Add the file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Commit 1"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381290547/c4dd6a07-d2dd-429e-95f4-2bad6358f0eb.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381333101/a48f9cd9-e261-460b-a3c4-9f018a29cff2.png align="center")

And after that add the file “b.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add b.txt; git commit -m "Commit 2"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381449315/2a5e6183-bf48-44a7-acf1-305baf166366.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381501280/39f7a9fe-a36d-40a3-a00e-4bd3fabab931.png align="center")

Now, there are two commits available at the **Master Branch**. To confirm that we’ll check the log using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381582688/50b3478c-dea7-4bca-b4aa-3dbcc298bdb9.png align="center")

And also confirm the total no. of files available in the Working Directory of the Master branch using the command `ls`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381645107/b0fe2500-b7f3-4812-aa05-a460501d54b1.png align="center")

So, there will be 2 files available.

Now, let's consider we have to work on a feature of the application, so we’ll create a child branch named “feature”.

Now, we’ll create a child branch and switch to that branch using the command `git checkout -b <branch name>`

In our case, it’ll be `git checkout -b feature`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381800100/b5974814-fb4c-41d6-8036-109dd9468dce.png align="center")

We’ll now confirm the total no. of branches and whether we switched to the new **Child Branch** “feature” or not. To confirm both, we’ll use the command `git branch`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685381887407/ba1b6ecc-b3c2-4c29-876d-b277e5f535cc.png align="center")

We’ll see there are total two branches

* master
    
* feature &lt;Child Branch&gt;
    

And we’ll also see the position of the star “**\***” on the “feature” i.e. Child Branch; This indicates that we have been switched to the Child Branch.

Now, Create two empty files in that directory named “x.txt” & “y.txt”. To create the empty files, we’ll use the command `touch`

**Syntax:** `touch x.txt y.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382007580/131e6bd0-c1ce-40fc-b45a-1a646b1ab5ac.png align="center")

Now, check the status of the files. To check the status of the files, we’ll use the command `git status`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382094246/1abef7ad-3ae8-41a7-89cc-b2eebc8af0b4.png align="center")

Add a file “x.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

Command:

`git add x.txt; git commit -m "Child Commit 1"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382171716/e0345588-eed4-4acd-ac6f-687ecffb60e5.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382339340/79c2f012-50f6-44bd-88b7-cbff74c231ff.png align="center")

And after that add the file “y.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

Command:

`git add y.txt; git commit -m "Child Commit 2"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382444135/0cd3a5ea-6d24-4576-a289-46a7c8e00532.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382488115/9340457e-1ff5-4b62-9a26-170a6b1552dd.png align="center")

Now, we’ll check the total no. of files on the Feature Branch using the command `ls`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382563728/ab86f53f-2cfd-4be4-b743-56838a8cad78.png align="center")

There will be a total of four files in the working directory. Two files “a.txt” & “b.txt” from the Master Branch that got inherited from the Parent Branch while creating the Child Branch.

And the other two files “c.txt” & “y.txt” have been created in the Child branch.

Now, if we’ll check the logs using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382694035/cc57b81c-76e4-4b1f-aae6-da1055568ebc.png align="center")

Then there will be a total of four commits.

Both HEAD will point to the last commit in the Child Branch (feature).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382783272/eba3b96f-0780-489a-ac35-ad9b1db62023.png align="center")

Two commits from the Master Branch & the other two commits from this branch i.e. the child branch.

So, now we’ll switch back to the Master Branch, as we are on the Child Branch “feature”. So, to switch the branch, we’ll use the command `git checkout <Branch Name>`

In our case, it’ll be `git checkout master`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382882891/23fd5285-ed2a-4724-8cc0-4597c1494b77.png align="center")

Now, we’ll create an empty file “c.txt” again on the Master Branch using the command `touch`

We’ll use the command `touch c.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685382966420/d5901bfc-c9a8-49e1-937e-dbbbb9655b40.png align="center")

Add the file “c.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add c.txt; git commit -m "Commit 3"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383089284/b566aebe-0d08-4767-b331-c50bfc6f0c35.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383120539/15f74874-1cd8-46fc-8ce1-a397f840bd02.png align="center")

Now, we’ll check the total no. of commits in the **Master Branch**. So, There will be three commits available at the **Master Branch**. To confirm that we’ll check the log using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383185037/696cb060-56a1-4e1e-b3b2-36831f397bf8.png align="center")

Both HEAD & master are pointing to the last commit in the Master Branch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383246401/743bfe22-44ef-47b8-8a7b-27cd552de3fa.png align="center")

Now, we’ll check the total no. of files on the Master Branch using the command `ls`

There will be a total of three files.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383305226/746a46a3-5991-49e1-a544-2289b2447487.png align="center")

Now, here we can see, both the Child & Parent Branch are Updated.

So, GIT will perform **Three-Way Merge**.

If we try to merge the Child Branch (feature) to the Master Branch, then a new commit will be created. That commit is considered as the **merge Commit**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383423336/61592f4b-16a0-439c-a35d-135f17d345fe.png align="center")

And, both the pointer i.e. HEAD & master will move to that new commit i.e. **merge commit**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383486644/5ffa1090-c452-47d4-9c21-10f33bfdb741.png align="center")

And then both the branch master & Child Branch will merge to the **merge commit**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383561656/f7c1aaba-f2c4-4b80-aae6-1cc76239f1be.png align="center")

### **🏷️ Proof:**

Now we’ll merge the **feature Branch** to the **Master Branch**. So, as Master Branch requires these changes, therefore we have to execute the command i.e. we’ll merge the Child branch to the Master Branch by staying/switching to the Master Branch.

To merge the Child Branch with the Master Branch we’ll use the command `git merge <Branch Name>`

In our case, it’ll be `git merge feature`

An editor will open showing a default message  
“Merge branch ‘feature’ ”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383714305/b8d18b51-ad63-4cda-abe7-c157f307e808.png align="center")

If we want, we can change the message according to us. Here we’ll keep it the same.

We’ll now exit from the editor (nano) by pressing `^x`

Once we exit from there, we’ll see that the feature branch has been merged.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383769130/9e19ae73-c54c-4e26-982b-09904ca99fcd.png align="center")

Now, after the merging operation if we’ll check the log on the Master Branch using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383905400/91253676-a954-4e9b-bcc4-4cfe917c7f4e.png align="center")

We’ll see now we are having a total of **6 commits**.

The commit message “**Merge branch ‘feature’**” is the same as we saw/saved while we were merging the Child Branch (feature) to the Master Branch (parent).

**HEAD & master** are pointing to the Last commit i.e. **Merge Commit**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685383561656/f7c1aaba-f2c4-4b80-aae6-1cc76239f1be.png align="center")

Now, we’ll check the total no. of files on the Master Branch using the command `ls`

There will be a total of five files.

* 3 from Master Branch.
    
* 2 from the Child branch.
    

Here, the files on both branches were different, that’s why we didn’t get any **Conflict**. But if the Master Branch & Child Branch modify the same file, then there will be a chance of getting **Conflict**.

If we want to display the log graphically, then we’ll use the command  
`git log --oneline --graph`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685384224016/d7a03d29-bc81-4680-93be-b5c5e6b39ea7.png align="center")

**Next Article**: Merge Conflicts And Its Resolution