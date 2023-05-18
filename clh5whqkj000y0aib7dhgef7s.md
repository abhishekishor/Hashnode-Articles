---
title: "12. Git Reset: Comprehensive Guide (Part - 1)"
seoDescription: "Master Git reset command with comprehensive guide. Learn how to undo changes, unstage files, and reset your repo with ease. Perfect for beginners and pros."
datePublished: Tue May 02 2023 06:40:51 GMT+0000 (Coordinated Universal Time)
cuid: clh5whqkj000y0aib7dhgef7s
slug: 12-git-reset-comprehensive-guide-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682923657348/9cd1086c-e691-40d0-bdab-fe86d812b37e.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1683009431091/4aefa718-7c98-45a7-8139-7b15f8424520.jpeg
tags: github, version-control, git, devops, devops-tools

---

Sometimes, we might make a change to our code that we later decide we don't want to keep. The `reset` command is a tool in Git that can help us to undo changes and move our code back to the previous state.

Imagine we're working on a drawing, and then decide we don't like the colour we just added. We can use an eraser to remove the colour and go back to the previous state. In Git, the `reset` command works similarly.

When we run the `reset` command, we're telling Git to move our code back to a previous point in time. There are different ways we can use the `reset` command, depending on how we want to undo changes. For example, we can use `reset` to undo changes we've made but haven't yet saved (in Git, we call these "staging" changes), or to undo changes we've already saved.

Just like with an eraser, it's important to use the `reset` command carefully. If we're not sure what we're doing, we might accidentally erase something that we didn't mean to. But with practice and careful use, `reset` can be a powerful tool for managing our code changes in Git.

There are two utilities of the command `git reset`

1. **Discard / Remove** the changes from the **Staging Area**.
    
2. **Undo Commits** At **the Repository level**
    

# Discard Changes From The Staging Area

Suppose there are all three Areas present for a directory.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682916218351/ca12ab9a-0e2a-4a55-9f66-fe5bdc704f48.png align="center")

Let’s consider there are multiple **Commits /Versions** present in the **Local Repository**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682916290022/0377ea6d-9212-44ff-b88b-8361021340b0.png align="center")

We did some changes in the **Working Directory**, and now we have to **Commit** those changes then we have to add those changes to the **Staging Area** using the command `git add`. And after that, the changes will be added to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682916489426/2d0550ff-faf1-4286-8d80-43d1545223e5.png align="center")

After that, we’ll Commit those changes.

Now, the first utility of the command `git reset` is whatever changes we have added to the **Staging Area** we can discard those changes (By mistake we added the changes, but still few more changes have to be made before committing the changes).

So, whatever changes we added to the **Staging Area** by default will be reset back. So, if such a case is required, then we’ll have to go for the command `git reset`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682916808092/4c7a31e6-c2fa-4bdd-afc0-5d3c469638de.png align="center")

# Undo Commits At Repository Level

In the **Local Repository**, till now 4 commits have been made.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682916967765/980f3786-7b5d-4c82-a8f7-8486542c64fe.png align="center")

Now, let's consider we have to discard whatever commits that have been made after Version2\*\*/Commit 2\*\*.

As the **Second** **utility** of the command **git reset** is whatever **Changes /Commit** we have added to the **Local Repository** we can discard those changes.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682917452970/a98676d1-fd17-4a44-8279-c91689faf174.png align="center")

## Utility 1: Discard/Remove Changes From Staging Area

In this case whatever changes are added to the Staging Area, if we don't want to use the commit operation, but want to add more changes then we require to use the command `git reset`. It’ll bring changes from the Staging Area back to the Working Directory.

Example:

Create a Working Directory “project7” and enter that Workspace. Automatically, Version Control is not Applicable for the Workspace.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682918217148/d771859e-95f5-49fe-b361-2aa6d7e75154.png align="center")

Now, We have to **Initialize** an **Empty Local Repository** for the **Workspace** then only the **Version Control** will be applicable.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682918326561/8f195a53-62ba-46a0-956e-eae7b8f36247.png align="center")

So, to **Initialize** an **Empty Local Repository** for the **Workspace** we’ll use the command `git init`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682918425596/6a6aeecb-565c-4538-a801-f51950cc3964.png align="center")

Now, an **Empty Local Repository** is available for the **Workspace** and the **Master Branch** is also available.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682918482956/b9a4b695-bc70-4977-91e1-976b9fccc6e8.png align="center")

Create a file “a.txt” in the **Workspace** and add a line “First line in a.txt”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682918569529/e40657ec-9fb4-4e0d-bcae-47d6366028ac.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682918612816/96d183cf-29fd-412c-89bd-4e1e6a969db2.png align="center")

Now, add both files to the **Staging Area**. For this operation, we’ll use the command `git add .`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682918744649/127b1237-370d-445c-abeb-ad39a6566a0c.png align="center")

Both files will be now added to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682918853550/b1d5494b-9ce1-4ff4-93ce-7dd01c62e41d.png align="center")

Now, we’ll commit the files to the **Local Repository**. For this operation, we’ll use the command `git commit -m <Commit Message>`

In our case, the command will be `git commit -m "Files a.txt added"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682918978426/fa84c702-3e82-480c-849f-537a8f2395fb.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682919034265/43774adc-8af3-4286-996a-09cc53765212.png align="center")

If we’ll check the **Status** of the git then it will tell us the Working tree is clean and there is nothing to commit.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682919274585/cb5aa013-8a34-4bb4-9938-1c736dd232e1.png align="center")

Now, we'll add / Modify the file “a.txt”. Add one more line “Second line in a.txt”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682919339145/798ca741-eac7-44dd-8c8f-d9fdbbf9c32c.png align="center")

Now, if we’ll check the status of the Git, then it’ll display that the file “a.txt” has been modified. Modified Changes not staged for commit. That is we didn’t add the changes to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682919425508/7eae42cb-48e8-440e-9146-1b0fdcc1e556.png align="center")

Now, add the changes in the Workspace to the Staging Area. For this operation, we’ll use the command `git add <Filename>` .

In our case, the file that we have to add to the Staging Area is “a.txt”. So, we’ll use the command `git add a.txt`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682919553238/858e9b3c-18e7-477e-9f64-acf2ec9909dd.png align="center")

Now, the file “a.txt” has been added to the Staging Area.

Now, if we’ll check the status of the Git, then it’ll display "On branch master, changes need to be committed".

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682919685047/4a6d680e-053b-468f-a0bf-f6c10fa77fc7.png align="center")

Now, if there is a condition in which we thought that the file “a.txt” which has been modified now, won’t be a part of the commit. By mistake, we added it to the Staging Area. So, we can revert that particular change.

For this, we’ll use the command `git reset <filename>`

filename: The file that needs to be discarded/reverted/ignored.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682920579971/8e6fa14d-4752-4fac-b396-0eabb11cc529.png align="center")

Now, the changes will be removed only from the **Staging Area**, and not from the **Working Directory**.

To confirm that, we'll check the status of the git repository using the command `git status`. It’ll be displaying that the file “a.txt” has been modified. Modified Changes are not staged for commit. That is, we haven’t added the changes to the Staging Area.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682920976128/16ae5fb5-d540-44ad-8b99-d6ed63ea64c7.png align="center")

So, the changes reverted now. So, whatever changes we added to the **Staging Area** will be discarded.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682921079625/a0cba852-d087-4c29-86a6-1ed2e9facf8c.png align="center")