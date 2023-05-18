---
title: "10. Git References (Master and Head)"
seoTitle: "Git References: Master & Head Explained ||  A Bit More"
seoDescription: "Learn how and where to use Git references like Master and Head efficiently."
datePublished: Tue Apr 25 2023 03:41:51 GMT+0000 (Coordinated Universal Time)
cuid: clgvq0k7o000509k183bdfpj0
slug: 10-git-references-master-and-head
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682362168036/8a664005-64e8-44ae-aeae-bde46d5a959c.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1682394007128/61347f88-aeba-4b59-b1e1-817266d62ee4.jpeg
tags: github, version-control, git, devops, devops-tools

---

In Git, a "**reference**" is a pointer to a commit or branch in the version control system. It allows you to easily navigate and keep track of different versions of your codebase. Git references come in various types, including branch references, tag references, and remote references.

**Branch references** are the most common type of reference in Git. They are used to keep track of different branches of development in your repository. When you create a new branch, Git automatically creates a new branch reference that points to the latest commit in the current branch. As you make changes and commit them, the branch reference is updated to point to the latest commit in the branch.

**Tag references** are used to mark specific commits as important milestones or releases. When you create a tag, Git creates a new tag reference that points to a specific commit in the repository. Unlike branch references, tag references are static and do not change as new commits are added to the repository.

**Remote references** are used to keep track of branches in remote repositories. When you clone a repository, Git creates a remote reference for the default branch in the remote repository. You can create additional remote references to track other branches in the remote repository.

Reference: It is a pointer that is pointing to something else.

For most of the commands in Git, we have to use **Commit Ids** as arguments. So, we have to remember it; But remembering the **Commit Ids** is very difficult. Therefore for those **Commit Ids** if we have some easy names, then it’ll be easy for us as well. As remembering **alphanumeric** **characters** is quite difficult, so instead of remembering, if we have some meaningful word/name to refer to the **Commit Ids** then it’ll be easy for us.

Such a type of simple name is nothing but the **Git References**. Git provides some sample names for the **Commit Ids**.

Most of the time we require the **Commit Id** of the most **recent/latest Commit**. So, for the **recent/latest Commit,** we can **name/use** it as **master** or **HEAD**.

# Scenario

Create a **Working Directory** “project7” and enter that **Workspace**. Automatically, **Version Control** is not Applicable for the **Workspace**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682357884542/c9fec0fc-59c1-425b-b434-188477a7870c.png align="center")

We have to **Initialize** an **Empty Local Repository** for the **Workspace** then only the **Version Control** will be applicable.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682357948233/1983be80-50a6-4fb8-93e3-86d4e4c8651e.png align="center")

So, to **Initialize** an **Empty Local Repository** for the **Workspace** we’ll use the command `git init`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682358110786/11bf4eec-d692-46c5-af72-9b5399ffafb8.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682358142845/9f18163b-d167-415c-9fe2-078850b9f865.png align="center")

Now, an **Empty Local Repository** is available for the **Workspace** and the **Master Branch** is also available.

Create a file “a.txt” in the **Workspace** and add a line “First line in a.txt”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682358295498/73108be6-e7ae-4a20-a08c-29b3d28542b4.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682358344974/558aa3f6-38cd-4d1a-a4e1-fe43bf5ed4bc.png align="center")

Now, add the file to the **Staging Area**. For this operation, we’ll use the command `git add .`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682358605777/26221b03-4e4d-464b-b2e3-69dcf836ab95.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682358651437/0d2d31bf-d56b-48b7-84e0-0bc69b349ed9.png align="center")

The files will be now added to the **Staging Area**.

Now, we’ll commit the files to the **Local Repository**. For this operation, we’ll use the command `git commit -m <Commit Message>`

In our case, the command will be `git commit -m "Files a.txt added"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682358800569/69ce641b-147b-4665-b405-a3070da65c48.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682358829499/3e011c36-b68b-4aa7-a87a-a6d0887702d6.png align="center")

And now, we'll check the log of Git. It’ll show, one file has been committed to the **Local Repository**.

So, to check the log of Git we’ll use the command  `git log`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682358996615/8a04171f-0351-420b-88d9-3ac115d26649.png align="center")

So, the **last/latest** **Commit Id** of Version **1/Commit 1** is **24900f8165f546d72a9e070349d4edd66d600851**

Remembering the alphanumeric character is not easy, so to remember or to use that **Commit Id** wherever it is required, we can use either **master** or **HEAD**.

# Master

Whenever we are using the command `git status` then we are getting one common result as "**On branch master**".

So, according to the result, we can understand **master** is the name of the **Branch**.

It is a **Reference** to the  **Last/Latest Commit**. So, wherever the **Last/ Latest Commit Id** is required, then simply we can use **master**.

To prove it go to the directory **.git/refs** that is present in the current **Workspace**.

Then there will be two folders named:

* **heads**
    
* **tags**
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682359929574/cc2f6375-7770-4e08-bae7-620d5f7598bd.png align="center")

We didn’t use the **Remote Repository** therefore the directory "**remotes**" is not present.

And we didn’t use the **tags** as well so that directory will be empty. To confirm that, go inside the folder **tags** and put the command `ls` to list all the files in that directory.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682360086677/29f8f274-876c-40bb-91a7-a46c884c42a0.png align="center")

But there will be nothing in that folder.

Now, go to the directory **heads** and put the command `ls` to list all the files in that directory. We’ll get a file named **master**. To check if it is a file or a folder we'll use the command `ls -l`. It’ll display the information about that file.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682360210896/498e77ab-9ebe-4c70-9021-dcc83cac341f.png align="center")

It displays the information "**\-rw-r--r--**". And if there is a hyphen sign at the beginning then it means that thing is a **file**.

Now, if we check the content of the file using the command `cat` then we’ll get the **Commit Id** of the **last/latest commit**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682360344065/691b8222-2e00-444a-971c-944bfef68daa.png align="center")

To verify that use the command `git log`. Then we can see both of the alphanumeric characters are the same.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682360431960/7fa79922-58d1-4529-9b38-5ad7272dc54e.png align="center")

So, the **master** is pointing to the **Commit Id**.

Now, add/Modify the file "a.txt". Add one more line "Second line in a.txt".

We'll use the command `cat`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682360564046/040e4802-2285-45fa-b906-d1463ead09e1.png align="center")

Now, we’ll commit the changes to the **Local Repository**. For this operation, we’ll use the command `git commit -m <Commit Message>`

In our case, the command will be

`git commit -m "Second line added in File a.txt"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682360778973/10468811-41bb-4a89-b48b-c8ed43041f05.png align="center")

Now there will be 2 commits in the **Local Repository**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682360866979/be50d322-85e9-4278-ae6b-f60202ddfa11.png align="center")

Now, the **master** is pointing to the Commit 2 Id i.e the **latest Commit**.

**97d4d2c7fd30865e1a819d56f44bbaa95cc5e464**

Now, if we cross-check the **latest commit Id** inside the file **master** which is inside the folder **heads** under the folder **refs** inside the **.git directory** then both of them will be the same.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682360928434/9b180783-4a6f-4445-a144-c1738f7b8255.png align="center")

So, whenever there is a new commit then the content of the file **master** will be updated to the **new commit Id** automatically.

# Head

HEAD is a **Reference** to **Master**. It is a **Reference** pointing to another **Reference**.

By default, **HEAD** is always **pointing** towards the **Master**. But sometimes HEAD may not **point** towards the **Master**.

The information related to the **HEAD** is stored at the following path:

**.git/HEAD**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682361253650/68a99cdb-3698-4272-a337-45acd81b3ba5.png align="center")

## Inside The HEAD

We can check the content of the file **HEAD** using the command `cat`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682361480256/3026eb9f-6f2d-40d4-8ffc-66f3236484ab.png align="center")

It is a **Reference**, internally this **Reference** points to the **master** (Path: **heads/master**). And the **master** is **pointed** to the **Last Commit**.

**Note:** Instead of the **latest Commit Id** we can use **master** at that place. And at the place of **master,** we can use **HEAD**, as HEAD points towards the **master**, and **master** points towards the **Last/Latest Commit**.