---
title: "13. Git Reset: Comprehensive Guide (Part - 2)"
seoTitle: "Unlocking the Power of Git Reset Command - Part 2"
seoDescription: "Master the Git reset command with comprehensive guide. Learn how to undo changes, unstage files, and reset your repo with ease for beginners and pros."
datePublished: Tue May 09 2023 06:57:47 GMT+0000 (Coordinated Universal Time)
cuid: clhfx6h05001709jz1w8ceim9
slug: 13-git-reset-comprehensive-guide-part-2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683097172383/a96186ab-e090-49a8-85c9-f71b34b5cd57.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1683615280602/5432d3e8-7531-4070-a955-24bfd4de1ac2.jpeg
tags: github, version-control, git, devops-tools, gitcommands

---

# Utility 2: Undo Commits At The Repository Level

We can use the option **reset** to undo commits at Repository Level.

Syntax: `git reset`

Let’s consider there are 5 Commits in our Local Repository.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683086840307/c45a648a-c4ec-4783-af33-10ef95d64f68.png align="center")

## Scenario 1: Discard/Ignore the Master

If we want to Discard/Ignore the **Master** i.e. the **Latest Commit**, then we have to make the Second Last Commit as the Master. Then only we can Discard/Ignore the Master. So, to Discard/Ignore the Latest Commit from the Repository we’ll use the command: `git reset <Option mode> <Commit Id>`

**Commit Id**: Whatever Commit Id that we will put in the command, that Commit Id will become **HEAD**. And the previous HEAD or whatever Commits will be there after that Commit Id will be removed from the Repository.

This means if we specify the Commit Id of the 2<sup>nd</sup> Last commit and then the commits after that (Previous HEAD) will be Ignored.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683088066622/6e77fd97-b4ad-4f54-9dd9-142dff886f89.png align="center")

So, in this case, HEAD will be moved to the specific commit, and all the remaining recent commits will be deleted from the **Repository**.

For the commits, some files will be there in the Working Directory and also in the Staging Area. i.e. related to the commits some changes are there in the Working Directory and Staging Area.

So, if we want we can delete those corresponding files from the Working Directory and Staging Area. So, this thing is decided by the mode used in the command to discard the commit.

Mode: Mode will be going to decide whether the corresponding changes in the Working Directory and Staging Area to the discarded commits should be deleted or not.

## Scenario 2: Discard / Ignore Only A Specific / Random Commit

Assume that we have Multiple Commits, and in that all the Commits if want to discard only a specific then it is not possible.

Various types of modes available :

So, the allowed values for the mode are as follows:

\--mixed  
\--soft  
\--hard  
\--keep  
\--merge etc

# \-- mixed reset mode

It is the default mode, i.e. if we are not going to decide any mode then by default --mixed reset mode will be considered. Therefore the syntax for the command can be either of the two:

`git reset --mixed commit Id`

`git reset commit Id`

The mode is used to discard/remove commits from the both **Repository** and the **Staging Area**.

It means if any changes are there, so discard commits from the **Remote/Local Repository** and if any changes are there because of those discarded commits in the **Staging Area**, those changes also will be removed.

We can revert back the discarded commits back because the changes are available in the Working Directory.

## **Working:**

Create a folder “project7” and move inside that folder.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683091805353/bb53c804-a2e0-41b7-bcfb-e7bc1ad2f29d.png align="center")

We have to **Initialize** an **Empty Local Repository** for the **Workspace** then only the **Version Control** will be applicable.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683091871367/1aa059e7-2210-4fe7-b54c-72d77b242f31.png align="center")

We’ll create three files and write something in them. We’ll use the command `echo` for that.

Example:

`echo "First line in a.txt" > a.txt`

`echo "First line in b.txt" > b.txt`

`echo "First line in c.txt" > c.txt`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683091986034/281aebc3-7a6b-4d5a-8072-51d345450a4e.png align="center")

Now, we want to add these files to the **Repository** but in different commits, because to check the functionality of the **reset** command, multiple commits are required.

Therefore we’ll commit the files one by one.

First, we’ll add the file “a.txt” to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683092079596/55e69161-6032-47bf-969f-f31a076ab643.png align="center")

After that commit those changes i.e. the file “a.txt” to the **Local Repository**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683092197071/c0034d6a-f5bb-4ef7-89c6-661850874fa3.png align="center")

we’ll add the file “b.txt” to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683092284304/66ff9b17-c460-48bf-b3a5-6b1b5e4503ad.png align="center")

After that commit those changes i.e. the file “b.txt” to the **Local Repository**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683092337835/cbc924b3-2ae1-4b26-a0f8-3acd65a25b8e.png align="center")

We’ll add the file “c.txt” to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683092389648/5e374809-6204-43f9-b4ce-0b8a8a382d9e.png align="center")

After that commit those changes i.e. the file “c.txt” to the **Local Repository**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683092478258/5ac02728-7bed-4051-9a61-91e58cb8157f.png align="center")

Now, there are 3 Commits present in the **Local Repository**.

To confirm we can use the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683092550536/d0ea9e4e-3222-46b1-9aa0-ee671c67cd6d.png align="center")

### **To delete and Revert the Last / Latest Commit**

If we have to delete the **Last / Latest Commit** from the **Repository** then we’ll use the command `git reset --mixed <2nd last Commit Id>`

Example: In our case, we’ll use the command:

`git reset --mixed fad54a3`

After performing this operation the **Commit** with the **Commit Id “fad54a3”** i.e. the **2nd last Commit** will become the **HEAD**. So, after that, whichever commit will be there, it’ll be removed.

Before that\*\*,\*\* we can check the number of files in the **Working Directory** and the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683093019852/53297810-4c1e-4394-aac4-667f4ee26753.png align="center")

So, there are 3 files in both areas i.e. **Working Directory** and the **Staging Area**.

Now, delete the **Last/Latest Commit** from the **Repository**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683093094729/3696596e-01b8-4f5a-923d-2c4cfe1a38e8.png align="center")

Now, there will be two commits available in the **Repository**. And the **2nd last Commit** will become the **HEAD**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683093160950/dfadfaba-56b0-4640-adaa-df22fd13ca80.png align="center")

The changes will also be deleted from the **Staging Area** as well but not from the **Working Directory**. To confirm we'll check the number of files as well as which files are available in the **Staging Area**. So, for that, we’ll use the command **git ls-files**. And to check the number of files as well as which files are available in the **Working Directory** we’ll use the command **ls**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683093213366/74f4eed7-5dd4-4aea-b068-18e21acad93a.png align="center")

So, the file “c.txt” has been discarded/removed from the **Staging Area**. But all three files are present in the **Working Directory**.

To revert i.e. to add the discarded/removed files from the **Repository** and the **Working Directory**, then again we’ll have to add the discarded file (changes) to the **Staging Area** and then Commit again.

Add file “c.txt” to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683093344395/3fb5e4c4-e4df-47c6-8311-1787bcf56910.png align="center")

After that commit those changes i.e. the file “c.txt” to the **Local Repository**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683093405214/464dfa60-9b0e-480f-9095-0244486a3bb3.png align="center")

Now check the log of Git again using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683093494593/75ce7617-6ff5-4251-b210-10318d8ce5f3.png align="center")

Now, there will be 3 Commits again, along with the different **Commit IDs**.

## \--soft reset mode

It is the same as the **\--mixed mode** except that it won’t touch the **Working directory** and the **Staging Area**.

## **Working:**

Check the number of files in the **Working directory** and the **Staging Area**. We’ll use the command `git ls-files` to check the number of files as well as which files are available in the **Staging Area**. And to check the number of files as well as which files are available in the **Working Directory** we’ll use the command `ls`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683094962247/6240741b-eb4c-412c-be08-68ab64f30aa2.png align="center")

In both areas, we are having 3 files.

Now, Check the log of Git.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683095047598/d144ca02-3905-41ef-ab0f-1a93c6f2c7f8.png align="center")

Delete the Last Two Recent **Commits**. So, for that, we’ll use the command `git reset --soft HEAD~2`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683095134560/fe24b0c2-8a82-4d5a-8a4b-6cdb3c4a361c.png align="center")

Now, check the log of Git.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683095272025/b23d9a1d-ab75-4dce-a9b9-683b47115a97.png align="center")

There will be only one **commit** left in the **Repository**. And nothing will happen to the files in the **Working directory** and the **Staging Area**.

Check the number of files in the **Working directory** and the **Staging Area**. We’ll use the command `git ls-files` to check the number of files as well as which files are available in the **Staging Area**. And to check the number of files as well as which files are available in the **Working Directory** we’ll use the command `ls`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683095628950/da6bc248-edd9-4be8-99f7-1e02de6e7a5d.png align="center")

# \--hard reset mode

It is the same as the **\--mixed mode** except that changes will be removed permanently from everywhere (**Local Repository**, **Staging Area** and **Working Directory**).

This command is **Dangerous** as well as **Destructive**.

It is **impossible** to **revert** the changes and hence while using this command we have to take a bit of special care.

## **Working:**

Create a file “d.txt” and write something in it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683095920234/92444205-0591-4381-ac3a-a169a37e26b7.png align="center")

Add the file “d.txt” to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683095961565/ad9941eb-3c1d-40db-86bb-ca9952194cc8.png align="center")

Now, commit the file to the **Local Repository**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683096013568/0d778038-7d9d-411d-8099-dad527ffb0c4.png align="center")

Now check the log of the Git

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683096064795/449af4b8-8196-4318-854a-9ffada9ed98e.png align="center")

There will be three commits now in the **Local Repository**.

Check the number of files in the **Working directory** and the **Staging Area**. We’ll use the command `git ls-files` to check the number of files as well as which files are available in the **Staging Area**. And to check the number of files as well as which files are available in the **Working Directory** we’ll use the command `ls`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683096155177/f16cb656-b822-4595-9a94-7ca9c9157755.png align="center")

There will be 4 files in both the **Working directory** and the **Staging Area**.

Now, to permanently delete the commit as well as the corresponding files in all the areas we’ll use the command

`git reset --hard <commit Id>`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683096229284/01e522fd-54ae-4b46-98e6-1ecd8fd15d88.png align="center")

The commits after that **Commit Id** which we have provided will be **deleted permanently**. And the **Commit Id** that we have provided in the command will become the **HEAD**.

Now, check the log of the git. The **commit Id** that we have provided in the command has become the **HEAD**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683096335191/d13938ff-8b2a-4d6c-ab23-fd1040007b19.png align="center")

Now, Check the number of files in the **Working directory** and the **Staging Area**. We’ll use the command `git ls-files` to check the number of files as well as which files are available in the **Staging Area**. And to check the number of files as well as which files are available in the **Working Directory** we’ll use the command `ls`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683096434046/8cc73936-1150-46ab-92f7-232d87e1928d.png align="center")

Now, there will be only one file “a.txt” left in both the **Working directory** and the **Staging Area**. The other remaining files will be removed permanently.