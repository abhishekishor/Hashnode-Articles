---
title: "4. Architecture Of Git"
seoTitle: "Mastering Git: Architecture Explained"
seoDescription: "Get a detailed understanding of Git's architecture and how it manages versions and changes in your codebase in this comprehensive article on Git."
datePublished: Tue Apr 04 2023 06:54:45 GMT+0000 (Coordinated Universal Time)
cuid: clg1wnrck000508jx2nophrpk
slug: 4-architecture-of-git
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680590922946/f6997194-34bd-4ac3-abf6-e2f3d0974ba3.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680591132397/49c714b8-0680-4710-b300-c8f304ebcd4a.jpeg
tags: github, version-control, git, devops, devops-articles

---

In the Git Architecture there are four areas:

![](https://lh4.googleusercontent.com/sj9HH9UfEc4Uf3A1FeAKPD-ypeyefSw2FVsrcCSEQI94WKhrRqHofRQyqhM3GgrHktk2gZPZy5G5sL-jo4kd8dp5SVXrsOXl5zKo_-TELYtOPtfDnGNg5d1v1NRlDVKWP6GySEtEoRvM1r4XFKBZ align="center")

First Area we can use the word/term **Working Directory**. Assume that the third area is the **Local repository**. So, between the Working Directory and the Local repository, there is one virtual layer/storage named the **Staging Area**. So, the second area will be the **Staging Area**. And the fourth area will be the **Remote Repository**.

So, in GIT there are four areas. We have to move our files/codes around the four areas only.

1. **Working Directory**
    
2. **Staging Area**
    
3. **Local repository**
    
4. **Remote Repository**
    

![](https://lh6.googleusercontent.com/dMRaWZ5oAK9at0NGZmJjo4DQ0W6Ey22udxGBxsZBIUBOs8q-08Zp3CEHh3j45BFMr0HEgAaGwQJj4DrCYwmI7C2O7k4dsulUq-wq5wEnxELImrnxj6KvsOEPkKnn7rqZHzC62W0EjAK-Vt306DWg align="center")

GIT has two types of repositories:

1. **Local repository**
    
2. **Remote Repository**
    

Usually, all the project's code will be available in the **Remote Repository** (**Global Repository**).

Whatever the work that the developer is currently doing it is mostly available in the **Local Repository**.

Assume that a developer created multiple files in the **Working Directory**. And now he has to commit those changes to his local repository. So, to do that he has to first add those files to the **Staging Area / Index Area**.

That is if new files are being created in the working directory.

And once the work gets completed then those changes/files have to be added to the **Staging Area**. So, for this, we have to use the command “**git add**”.

`git add`

So, we have to use this command to send the code/files from the **Working Directory** to the **Staging Area**.

![](https://lh3.googleusercontent.com/1Q7vJ_kL82MR0YC696N3hvSSOgggctGcSWh6-fWgAoxZz51innPK3C8om1fJtF9Nbm0avhAP2A2igCdFoLpVBN_qf1AjzLWguGF_xyTmSyK1P5a3v7UzgfyNMiqkxxQZlzsdDm1LZMgNzeSN6XjH align="center")

Now, the files are available in the **Staging Area**.

So, we have to send the files from the **Staging Area** to the **Local Repository**.

So, to do this work we’ll use the command “**git commit**”.

`git commit`

That is, to send/move the Staged changes from the **Staging Area** to the **Local Repository** we will use the command “**git commit**”

![](https://lh6.googleusercontent.com/Rca7FNmBUsafnWpzfz2AciE-DN_V197ogqBo8s6KsFf9dA2puLYYz1TnS-wVlw1-bJW4dN7D_9xdzUUA1doyAQXRSd-89LXXo-RcvWaDWRXCQ8HSk9GN_WBcFdLGdTPoM6Hsg6lbk1L_5fXaEAne align="center")

Now, if all the work gets over, we want to share/publish the changes/files to the **Remote Repository**, so that other peer developers can get the changed files. So, we have to send the files from the **Local Repository** to the **Remote Repository**. Therefore, we will use the command “**git push**”. Then, whatever files are available in the **Local Repository** will be updated in the **Remote Repository**.  

`git push`

And from the **Remote Repository,** all the work is going to be shared with the other developers so that multiple developers can work collaboratively.

To send the files from the **Local Repository** to the **Remote Repository** we can use the command “**git push**”.

`git push`

![](https://lh4.googleusercontent.com/HbbiauCE0wUTqj_oplYiTc5kKQZfQGDdlGLmH2Z_VABVONtxMHW17CKDsbGg30gE2axd5rDAOyCyl23-B_ihEjv0--UovsxfvWPO6woOV0vnvvw0Rmhb01STI7vAHHy9W_Ufs1QkILwb37bxGTvY align="center")

Now, another developer wants the files from the **Remote Repository** to his **Local Repository**. So, he can use the command either “**git clone**” or “**git pull**”.

`git clone`

`git pull`

To bring the files from the **Remote Repository** to the **Local Repository** we can use the command either “**git clone**” or “**git pull**”.

![](https://lh4.googleusercontent.com/ENN1O4Bs70Wlq0OOVoP6f_eE9Q5fAiTITFHaYsYt3PbFXMXfSLXfQyiZgJHDjs5aHcCfePrNzaUbhXX7g6-0RLXknMxtZa_5D4-Usc2p5Cii8DAQVwRzvxP4haOEPCxJeJAW_mq_fic1m_4aI89O align="center")

**Q.** What is the difference between “**git clone**” & “**git pull**”?

**Git Clone**

**Ans:** **Cloning** means creating the exact duplicate copy.

Suppose a new developer joins the team and starts working on the project. So, he wants to copy the entire **Remote Repository** to his **Local Repository**. So, he wants to create a new **Local Repository** which is the exact copy of the **Remote Repository**. So, he’ll use the command “**git clone**”.

If we want the complete exact copy of the **Remote Repository** in our **Local Repository** then we require to use **clone** and the command will be “**git clone**”.

For the first time, we are required to clone the project, so we use the command “**git clone**”.

When we run the `git clone`, Git creates a new directory on our computer that contains a complete copy of the remote repository, including all branches and commit history.

**Git Pull**

Now, suppose there is a developer who is already working on the same project as the other developers. He is already working on some files. Now, the other developer **pushes** some changes/updates to the **Remote Repository** and that developer wants those changes only in his **Local Repository** then if any updates are available which are not there in his **Local Repository** then for that he will pull the code from the **Remote Repository** to his **Local Repository**.

  
If we want the updated files/codes from the **Remote Repository** to our **Local Repository** for this we will **Pull** the updates / updated files / newly added changes and for that, we will use the command  “**git pull**”

`git pull` is a command that you use to update your local copy of a Git repository with any changes that have been made to the remote copy since you last fetched or pulled. If you have made changes to your local copy, `git pull` will try to merge those changes with the changes from the remote repository.