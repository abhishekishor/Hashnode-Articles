---
title: "18. Merge Conflicts and It's Resolution"
seoTitle: "Git Merge Conflict & Resolution: Complete Guide"
seoDescription: "Learn how to handle Git merge conflicts and effectively resolve them. This comprehensive guide provides step-by-step solutions for seamless collaboration."
datePublished: Wed Jun 07 2023 04:25:04 GMT+0000 (Coordinated Universal Time)
cuid: clil7hrws00070ampgao0elnt
slug: 18-merge-conflicts-and-its-resolution
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1685901819056/5e6f4188-4c54-4e80-8110-87c998b493bc.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1686111820141/9385c3fb-a57c-41b9-ac12-5a07d24b8452.jpeg
tags: github, version-control, git, devops, gitcommands

---

# 🔊 Introduction

A "merge conflict" occurs when there are conflicting changes to the same file or files that Git cannot automatically resolve during a merge operation. A merge conflict typically happens when two or more branches have made conflicting modifications to the same lines of code or when one branch has deleted a file that another branch has modified.

When Git encounters a merge conflict, it marks the conflicting sections in the affected files and presents you with a "merge conflict" status. It indicates that you need to manually resolve the conflicts before completing the merge.

GIT will markup the content of both the branches (Parent & Child), to resolve the conflict very easily.

If we have multiple files & large codes, then solving the conflicts manually will take more time.  
But to resolve this issue we have **Merge tools**.

Ex: **p4Merge**

Merge conflicts can arise in various scenarios, such as:

1. Modifying the same file in different branches: If multiple branches have made changes to the same part of a file, Git may not know which changes to keep and presents a conflict.
    
2. Deleting or renaming files: If one branch has deleted or renamed a file that another branch has modified, a conflict can occur.
    
3. Diverging commit history: When attempting to merge branches with diverging commit histories, conflicts can arise if changes made in one branch affect the changes made in another branch.
    

# 🔊 Practical

Create a new directory named “conflict” using `mkdir`. And move inside into that directory using the command `cd`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685885717925/778e4007-bcf1-4548-8139-197bab2538ce.png align="center")

Now, initialize that directory using the command `git init`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685885898843/099d31dc-4a79-49fc-adfa-f3f89da49f32.png align="center")

Create a file “a.txt” and write “Added first line” in that file using the command **echo**. Therefore, the command will be  
`echo <“Content” > <filename>`

In our case, it’ll be `echo "Added first line" > a.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685886060265/3ccb67b5-21f5-42ba-a426-dd17abc8869a.png align="center")

Add that file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Master Commit 1"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685886318343/a4999e78-a465-4312-93dc-fd14f4f3108c.png align="center")

Now, again add some content by writing “Added second line” in that file using the command **echo**. Therefore, the command will be  
`echo “Content” >> <filename>`

In our case, it’ll be `echo “Added second line” >> a.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685886427876/78d3f1a2-5e84-499e-9097-e9d3d5991104.png align="center")

Add that file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Master Commit 2"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685886692392/14ef4621-b76e-45a9-bbe5-ad98c7da7f3a.png align="center")

Now, check the content of the file “a.txt” using the command `cat` . There will be 2 lines.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685886909395/c1911c2c-2afb-4023-8cc4-5fc5571e2a8e.png align="center")

Now, there are two commits available at the **Master Branch**. To confirm that we’ll check the log using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685887420606/d80b752d-c2c9-4141-a50e-ffcb3d440fc5.png align="center")

Now, we have to work on a feature, so we’ll create a child branch named “feature”.

So, we’ll create a child branch and switch to that branch using the command `git checkout -b <branch name>`

In our case, it’ll be `git checkout -b feature`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685887730075/3151d665-032d-4787-b2ea-ddcced2e55c2.png align="center")

We’ll now confirm the total no. of branches and whether we switched to the new **Child Branch** “feature” or not. To confirm both, we’ll use the command `git branch`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685887817310/95e0187e-f21f-4d7e-993a-98fcdc760ff2.png align="center")

We’ll see there are total of two branches:

* master
    
* feature &lt;Child Branch&gt;
    

And we’ll also see the position of the star “**\***” on the “feature” i.e. Child Branch; This indicates that we have been switched to the Child Branch.

Now, from the feature branch again add some content by writing "Added first line in the feature branch" in the file “a.txt” using the command **echo**. Therefore, the command will be  
`echo “Content” >> <filename>`

In our case, it’ll be `echo “Added first line in the feature branch” >> a.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685888035492/d125f7e1-a5fe-4453-a610-5f5a97bfb97c.png align="center")

Add that file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Child Commit 1"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685888113461/9e26f61d-f4ee-406e-a230-45e12e465e88.png align="center")

Now, there will be three commits available at the **Child Branch**. To confirm that we’ll check the log using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685888207734/3e6ab4bb-39bf-40f6-90c2-19dcae1a9147.png align="center")

Now, **HEAD** will be pointing to the last commit of the Child Branch.

Now, we’ll switch back to the Master Branch, as we have to perform the demo of the **Three-way Merge**. And we are on the Child Branch “feature”. So, to switch the branch, we’ll use the command  
`git checkout <Branch Name>`

In our case, it’ll be `git checkout master`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685888334528/a87868be-cc6a-4786-9500-93d1bd8d0db3.png align="center")

Now, we switched back to the **Master Branch**.

Here, we’ll confirm the total no. of lines/content that we had added & commit in the file “a.txt” on the Master Branch using the command **cat**

There will be a total of 2 lines that we had added & commit in the file “a.txt” on the Master Branch as we didn’t perform the Merge operation till now.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685886909395/c1911c2c-2afb-4023-8cc4-5fc5571e2a8e.png align="center")

Now, we’ll again add some content by writing “Added third line” in the file “a.txt” using the command **echo**. Therefore, the command will be  
`echo “Content” >> <filename>`

In our case, it’ll be `echo "Added third line" >> a.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685888617579/1b782453-f639-45e6-a099-a7b6696e1eba.png align="center")

Add that file “a.txt” to the **Staging Area** and then **Commit** that file to the **Local Repository**.

We’ll use the command `git add a.txt; git commit -m "Master Commit 3"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685888687396/36f58c28-8d0c-427a-a674-377fc76680b5.png align="center")

Now here we added and committed some content in the Master Branch as well.

Now we’ll merge the **feature Branch** to the **Master Branch**. We’ll merge the Child branch to the Master Branch by staying/switching to the Master Branch.

As we have made the changes in the same file “a.txt” by adding some data in both branches. So, if we’ll merge the Child Branch with the Parent Branch, then GIT will not be able to decide which changes are to be considered as the final change in the file “a.txt” on both branches.

This will result in Conflict. To merge the Child Branch with the Master Branch we’ll use the command `git merge <Branch Name>`

In our case, it’ll be `git merge feature`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685888820156/54bcc187-bade-4898-84cb-df561731a621.png align="center")

It will be displaying that the automatic merge has failed; We have to fix the conflicts and commit the result manually.

This shows internally GIT will compare the content of the files.

Now, we’ll check the status of GIT using the command `git status`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685889797744/3787e0da-6456-48be-974a-b41a2e79dde1.png align="center")

Now, as we know that in the case of conflict, GIT will markup (mention) the content of both the branches (Parent & Child), to resolve the conflict very easily. Therefore, we’ll check the content of the file “a.txt” using the command `cat`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685889990703/36ffb995-cda3-4067-998a-ae9d2787d66e.png align="center")

The first & Second lines had been added before creating the Child Branch (feature).

The third & fourth line is telling that the data mentioned in the fourth line has been added to the **Master Branch**.

The sixth & seventh line is telling that the data mentioned in the Seventh line has been added to the **feature branch**.

So, now it depends on us to decide which content we want to be there in the file “a.txt”.

If we want any of the content, then the other content should be deleted.

If we want to keep both the content, then we have to keep the file as it is.

# 🔊 Resolving Conflicts

We can resolve the conflict in two ways:

1. Using Mergetool (ex: p4merge)
    
2. Manually
    

## 🏷️ Using Mergetool

We can resolve the conflict using the merge tool. Example: **p4merge**.

### ⚙️ Setting Up P4merge

We’ll download the p4merge tool from its official website

[https://www.perforce.com/products/helix-core-apps/merge-diff-tool-p4merge](https://www.perforce.com/products/helix-core-apps/merge-diff-tool-p4merge)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685890287311/5041dbd5-74b3-420c-8def-8ae9a2768547.png align="center")

Now, we’ll then choose the OS (family).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685890340583/48c55684-30d3-4c9d-8c3e-505766840467.png align="center")

And then download the application.

**Note:** If we’ll download the p4merge tool in Linux then it’ll get downloaded as a **.tgz** file. So, we’ll convert it as a .**tar** file using the command `gunzip<filename>`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685890409941/351c6578-ab69-4e27-9369-661e9724b9e4.png align="center")

After that, we have to **untar** that file. Therefore we’ll use the command `tar xvf <filename>`

**xvf** :

**x : Extraction**

**v: Verbose mode**

**f: file**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685890495595/e1f8aa58-00c1-45e9-9f74-dbb89ea07088.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685890548131/dce1b94c-6151-4f3e-9752-084559997380.png align="center")

Once downloaded extract it and copy the contents of the folder to a new folder **/opt/p4merge**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685890613717/3f74b1aa-53e2-4170-89d6-db1be6c35f0d.png align="center")

Move that extracted folder **p4-2022.2.2304646** to the newly created folder in the p4merge in the opt directory under root (**/opt/p4merge**)

Therefore, we’ll use the command  
`sudo mv p4v-2022.2.2304646/* /opt/p4merge`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685890685348/b38a10fb-764c-442c-97ce-76ea16d8667a.png align="center")

To create a **symlink** for p4merge we’ll use the following command:

`sudo ln -s /opt/p4merge/bin/p4merge /usr/local/bin/p4merge`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685890817121/1337fa3b-455e-4705-920c-64c035d13b63.png align="center")

We need to configure it for all the projects and repositories (i.e. Globally) in GIT.

So, we’ll use the command: `git config --global diff.tool p4merge`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685890916113/dc9b8e0f-7e43-4277-a1fc-defa91d136e9.png align="center")

Now, once we configure the tool then we have to set the path for it.

So, we’ll use the command:  
`git config --global difftool.p4merge.path <path of the p4merge>`

For me, the path is `/usr/local/bin/p4merge`**.**  
Therefore, the command in our case will be

`git config --global difftool.p4merge.path /usr/local/bin/p4merge`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685891860231/4b94329a-c209-4b5e-a88f-0e62df727205.png align="center")

After that we have to configure the prompt message (Do you want to open… type of message) on the screen. So, to remove that we have to configure it.

So, we’ll use the command: `git config --global difftool.prompt false`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685891119545/a6c105ad-ce6d-4765-979c-719b5ff9323d.png align="center")

So, we’ll not be prompted for confirmation each time. We need to configure the p4merge tool for all the projects and repositories (i.e Globally) in GIT.

So, we’ll use the command: `git config --global merge.tool p4merge`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685891281242/4d0edd8b-739c-4de3-8dfa-aedb355d9ebf.png align="center")

Now, once we configure the tool then we have to set the path for it.

So, we’ll use the command:  
`git config --global mergetool.p4merge.path <path of the p4merge>`

For me, the path is **/usr/local/bin/p4merge**

Therefore, the command in our case will be  
`git config --global mergetool.p4merge.path /usr/local/bin/p4merge`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685891016497/cc7b157f-1e49-4f3a-8cce-4bcc029b3a5e.png align="center")

After that, we have to configure the prompt message (Do you want to open… type of message) on the screen. So, to remove that we have to configure it.

So, we’ll use the command: `git config --global mergetool.prompt false`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685891969556/b7484cde-8196-47ab-a353-49bc78b984bc.png align="center")

So, we’ll not be prompted for confirmation each time.

Now, if we want to check all the configurations that we have configured (globally) so far. So, for that, we’ll use the command  
`git config --global --list`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685892081004/03d67f0f-2587-4bef-8778-f97399a03174.png align="center")

### ⚙️ **Using GUI (Mergetool)**

Now, to compare & merge the content of both branches, we’ll use the merge tool (GUI based).

To open the merge tool, we’ll use the command `git mergetool`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685892205361/d36aa2d7-61eb-48fe-a4aa-247577859fa9.png align="center")

The GUI of Mergetool will get opened.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685892286558/c966e62c-c0d5-4b21-99f7-e009280c2103.png align="center")

That tool will be having all the contents in each branch

**Child Branch**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685892469929/788332d5-73f0-4ecc-a685-00d536421b34.png align="center")

**Base Content**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685892559711/05fca3c3-0d5d-4f8e-96bf-4afe70dda15a.png align="center")

**Master Branch**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685892607574/46b2637d-2e9e-4921-9cf8-4b18b8188c69.png align="center")

Which content we are required to keep? We can have both the contents or any of the two.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685892933745/81e75ece-5671-4e98-9688-9e4f3f6c07a4.png align="center")

Total no. of conflicts

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685892975295/422a6bc6-8d63-4740-92d2-a1da033ab5cd.png align="center")

Switching between the conflicts.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685893012781/34ca568f-02c9-4036-bed2-3dbb7bf864ad.png align="center")

There are background colours in both the branches

* Blue
    
* Green
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685893068234/4ebb8a6f-ff66-4888-9742-d58bc61a8b96.png align="center")

So, now if we want to keep the content in Blue then we’ll click on the blue symbol on the right (down)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685893129535/32439f26-9ea6-4e22-9b93-a80d8654266d.png align="center")

If we want to keep the content in Green then we’ll click on the green symbol on the right (down)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685893159347/f35fd973-284e-45f4-ae72-1846b26797f0.png align="center")

If we want to keep both the contents then we don’t have to do anything.

After changing things according to us we’ll click on the save button on the upper left side. Then the content by default will be saved.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685893213057/1dfccb9d-e2b8-4e73-aaf1-ead1d54ab3fa.png align="center")

Then close the merge tool.

While closing the merge tool it’ll ask if the merge was successful or not. So, we can type Y/N according to us.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685893309653/21509f49-d769-4a34-a020-d3fcdf69cd8e.png align="center")

In our case, we’ll type “n” because we’ll have to resolve the conflict manually i.e. without using GUI/tool.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685893355596/a91c6c8a-1882-4851-b274-93d3d6c0a57f.png align="center")

# 🏷️ Resolving Conflicts Manually

Open the file “a.txt” using any editor.

In our case, we’ll use **vi** editor. To open the file in the **vi** editor, we’ll use the command `vi <filename>`

In our case, it’ll be `vi a.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685899775723/3a529bf9-06c5-425e-adc4-13eada4a2a04.png align="center")

So, we want to keep both the contents. To keep both the contents we’ll have to delete the following:

* &lt;&lt;&lt;&lt;&lt;&lt;&lt; HEAD
    
* \=======
    
* \&gt;&gt;&gt;&gt;&gt;&gt;&gt; feature
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685899875986/7a83e7d0-80b3-4414-afe5-c2051e9deb5e.png align="center")

In order to delete we’ll go to that particular line and delete it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685899953564/68128ed1-15c8-4093-8dc8-7092f41cca8b.png align="center")

Now press **ESC** and then type `:wq` to save the file.

Now, we’ll check the content of the file “a.txt” using the command `cat`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685900049644/569778d6-80ba-4b91-9405-34a6ce34403a.png align="center")

So, now the conflicts will be resolved. Now, we’ll merge the **Child branch** with the **Parent Branch**.

# 🔊 Merging Continues

So, now we have resolved the conflicts. Now we can merge the Child branch with the Parent Branch.

Before that, we’ll check the log on the Master Branch. There will be 3 commits on the Master Branch. To confirm that we’ll check the log using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685900219830/b7adfea4-92da-4d87-a1ca-e68e8569251f.png align="center")

Both the HEAD & master are pointing to the last commit on the Parent Branch i.e **Commit 3**

But before that, we’ll add the changes in the file to the **Staging area**.

So, check the status of git, using the command `git status`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685900326655/7ea5a066-f61d-4bcb-b3c6-848853c5a17f.png align="center")

Now, we’ll add the file **a.txt** using the command `git add a.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685900388568/e0209a3c-7ec3-4f0f-b152-79ac24eaa9b6.png align="center")

The file will be added to the staging area. To confirm that, we’ll use the command `git status`

We’ll see if it’ll be telling changes to be committed.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685900492260/bb525456-a417-4adb-86f4-af71a647ed0e.png align="center")

Now, we’ll commit the file using the command  
`git commit -m "Message"`

In our case, it’ll be `git commit -m "Resolved Merge Conflicts"`

This is known as the **Merge Commit**. That is, a new commit we’ll be creating which is known as the **Merge Commit**.

So, after resolving the Merge Conflicts we created a new commit manually known as the **Merge Commit**.

Now, we’ll check the log on the Master Branch. To check the log we’ll use the command `git log --oneline` Or `git log --oneline --graph`

`git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685900656612/5a228bb1-d22d-48b3-9246-c6789b93b266.png align="center")

As the Child Branch (feature) has been merged with the Parent Branch, therefore the Commit of the feature branch is also present.

Now, Both the HEAD & master are pointing to the **Merge Commit** (Previously it was pointing to the last commit on the Master Branch i.e. **Commit 3**).

**Merge Commit**: If we’ll try to merge the Child Branch (feature) to the Master Branch, then a new commit will be created. That commit is considered as the **merge Commit**.

And, both the pointer i.e. HEAD & master will move to that new commit i.e. **merge commit**.

`git log --oneline --graph`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685900783296/3559c2e4-9bb0-4d67-af49-81f31aa4d7d4.png align="center")