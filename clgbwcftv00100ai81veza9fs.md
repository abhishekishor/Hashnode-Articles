---
title: "6. Getting Started With GIT- Part 1"
seoTitle: "Mastering Git : Getting Started with Git (Part 1)"
seoDescription: "Learn how to getting started with Git, create a repository, add and commit changes in this comprehensive guide to working with Git - Part 1."
datePublished: Tue Apr 11 2023 06:43:39 GMT+0000 (Coordinated Universal Time)
cuid: clgbwcftv00100ai81veza9fs
slug: 6-getting-started-with-git-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681193746806/e19c1a82-c60a-46e6-b872-b8582902d3f6.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1681195272524/8a9052a4-a005-4eb2-ae5e-900db5bebf8d.jpeg
tags: github, version-control, git, devops, devops-articles

---

Create a Folder named “gitprojects”. Use the command **mkdir**.

![](https://lh3.googleusercontent.com/oyTvcNvZuKHmKnfV34XICbOPupW1RMM1omJUygVyRtwPC9cojFfI-YWDj5CpZQhCg0Q677J7n1WX4VihD6PPm4rlBbbEYc7g7p5PHbZyIAeGQqI_wYy0oq0GWUXjdlkgq0RWSmTS6ntd7ATztDQw align="center")

Enter into that newly created folder “gitprojects”. Use the command **cd &lt;folder name&gt;**.

![](https://lh3.googleusercontent.com/n8_13osvMG_miD45l6Xga_G826LOris2_aHS930fjj3V9V3rXiiTWPpXH3o7s4bM4lQASMLVvSNcFJ8tYIcNG4-AeKU6umW6XyHURk7nZ1UQ1IJVrQYC7THmEpm8BVQY4bC9cYzLkdg49Rq2s59z align="center")

Check if is there anything (File / Folder) in that newly created folder “gitprojects” or not. Use the command **ls**. There won’t be anything.

![](https://lh6.googleusercontent.com/cEnNLsuGbLwtrpMFw1SZuTbn7IqZr8WlSdOQljNu_NVEAleHNBl-dTi--NXIOfnyaTqDMk__A9fXMi5YbftqGprxe8aU9o7vSxoYbk7t8GKTm1Qm2fw_mlj7Ob8CsmAN7AncS-LcgZUuLT1Hnozj align="center")

In the project “gitprojects” we want to work on the first project. So, create a folder named “project1”.

![](https://lh3.googleusercontent.com/DsaDW4TNDzeIDqs6hIRPLXE2zTBWkwHGgm8H4YbKjkf5V1cyMRY69dQEgkHT_Sv68iAdOsgY3N6ZC8BtuTjmZuBpGfyCtC1bfad97jgu8MtiVZ45LIqRNc3mjQLq9ZcyB_B1Hy1FQSJsMMFOkHY_ align="center")

Enter into that newly created folder in the “gitprojects” i.e “project1”.

![](https://lh3.googleusercontent.com/Yfy1XC9v1HK6SP9P9vjIKbYqQQwotM_tEDwzDP6otx9NdS367hYLZ_Vkf2Z2WdiI2XFv1F-iAzFIvHbGs99dWCNuuh-Akne1RlvIbPOSxxIkrhRbjK1ZPc9t80kaRJ0LebzIQGqIqzWyYp6GzmE4 align="center")

  

Check / Confirm the location of the folder. Use the command **pwd**. So, on the Desktop we created one folder named “gitprojects” and in that folder, we created one more folder named “project1”. And currently, we are in the folder “project1”.

![](https://lh3.googleusercontent.com/TEX_8bXMuKaATE45k6eWJFDZMRm6DbBQ9Azp2lrPitS-u94_P08MG2K-Jo-94iEbww935jd4xPWXMFni06TTnAK49bnMq8fNdVUNoTuvWk8MdKhSJ_m9n4AalNLdAMQnSyCXixhtxKKZOfBOC-63 align="center")

Now, the folder “project1” will be our workspace. So, we prepared our workspace.

Version Control will not be available for our workspace “project1” now.

**Note:** By default, Version Control is not available for the Workspace / Working Directory.

We can check it by using the command **ls**, nothing will be there, then we can use **ls -a** and there also we will not get anything.

There will be one dot (**.**) and two dots (**..**) in that folder representing every directory containing two hidden directories, one is the current working directory (**.**) and the other is the parent directory (**..**).

![](https://lh6.googleusercontent.com/17uNQmWlyjBeLhyCNg1RVm40Qi0dSgM8YKt55VXnK9HCkLebm8QnH4sE9a6NGvXMK0YNMdbOQWmKtpqYxqRDSseoyGZ34ZQAorn3zNvHyd49HTe06u8-tnLQHK3LKTCLqZPm7NdfNzvbmJ6k_vZO align="center")

Now, GIT is not aware of our Workspace. So, we have to tell it that the folder “project1” is our **Workspace**. And let the GIT know that we want Version Control for the “project1”.

**Q.** For the **Workspace** “project1” is the **Version Control** applicable?

**Ans:** No, also if the **Version Control** is not applicable then we can’t use any GIT command. To get the **Version Control** for the **Workspace** there should be a **Local Repository** in the **Workspace**, and the **GIT** is responsible to provide the **Local Repository**. For that, we can use the command **git init**.

![](https://lh3.googleusercontent.com/BlRfJF1RBKq1CEUnqKphUQyYxXx_WWwlhixPMd2N8sHrRmaoc1tpvZLgXgjBdGDX57AskDlEgSIYAPYLRwll7hrolfyjz8FB4EVH3BjZIj75o2t1PMDbeTrC4dViWFnZWPDvVqXSj7k39VR22ObG align="center")

So, for that, we have to **initialize** the **Repository**. This means we want the **Repository** to maintain different **Versions**. Then Git will provide an empty **Repository**.

  

![](https://lh4.googleusercontent.com/bEYlWhof5X36AIDVKe4OmqzZdDroZsVRzI5Nk83LQ_kqUyK0D1H2Zc8f-Ria_gzIS5U6CwOes6fDEK5WdETBrEav3ObSYvPO-Us4iI3QvI1c1NEc_J4b-Yw--6moM3vC-27vanSX0iDRN1kOom8f align="center")

To initialize the Workspace (Create an empty Repository) so that the Version Control is available to our **Working Directory**, or re-initializing an existing one (**Local Repository**) we’ll use the command **git init**.

We have to execute the command **git init** in the **Working Directory**.

**Note:** The name of the **local Repository** will be **.git**. As the name starts with a dot (**.**) therefore it’s a hidden directory, internally this directory is used for the **Version Control** purpose.

Now, we’ll check the status of the GIT in the workspace “project1” using the command **git status**.

**git status** shows the current status of all the files in each area, Ex:

* **Untracked files**
    
* **modified files**
    
* **staged files** etc.
    

So, it's “fatal” (Dangerous) i.e it’s a severe error. It’s not a git repository then why are we using this command?

![](https://lh3.googleusercontent.com/cSgPMgN07Em46oQGIhhpeppHQUKIr2icY5CQJcLTaafrGv8KMUlG5Exg5pxGpwwbFDxnPHZ3t1SivswMqGtt7VGKX4fkyREsvQutnICOs_JAq3ESqekMJbKGfdoQTY9XgHW8XhiwendgX00rwclA align="center")

If we don’t know about any command in GIT then we can use the command **git** only, and a list of all the commands in GIT will be printed on the screen.

![](https://lh6.googleusercontent.com/AwdDBwbkZQTMP6uAi441aHEsMwFLXwqtYtihtfpx-N-wdFpEizPyvZP-h2XgJj28jz-5WumQyV7N8wUQ2mutxIXCuV__sCQnqwIjMiXpNNbgCXTOe6Y6qBTWJa7riGO_cOwXS2K5bRSX34MrieCA align="center")

Now, we want the **Version Control** for the workspace “project1”. So, we’ll use the command **git init**.

Now, it says it **initialized an empty** GIT repository inside the workspace **.git** directory.

![](https://lh3.googleusercontent.com/UbyM047YWgzXbNIh3vZPYAzAyfpBFZ6K86MctcIRQljGnFZYm_FDD1pdfWTcDUMpZ_7DybMhdmF5fftypR9HWcFLyU0R6f4_SGHqoGnBvrhIvmlLxlest7ZpYzf-4nM3Cvr7KiFOTHCbFMR9zTWu align="center")

Now, to confirm it we’ll use the command **ls -a** as **.git** is a hidden folder.

![](https://lh3.googleusercontent.com/sezTWtZkE6T9y-TRJk2iPNvxQu3kfFe9PmOFtUWLPKkyE9goiiGxVtWWUnTEY3nAbtyYbXn-8SCld5LnLQLf5o4KlznxlL-6i0WOE38iEwe8Z_LRsgFrbLR7Y9s-OJAdbcrrx4wZ6NFSoTwEvXfQ align="center")

Now, use the command **git status** to check the status of the GIT in the workspace.

![](https://lh6.googleusercontent.com/mzUHIEIWlPRos-U6Ku1AOHM9yARccPgN7W8MihR-v1_i3fNcPyuEnqP0VkpGnny1Dhm-OhrGc0ZN4kC-Q6uGl0srrHVZ0E-xk_MmM8ATHYBJrYsSD2Y-C1kEhB_n4USXifrrQ7p0NthEPiea01Vc align="center")

Till now, nothing is available in the GIT.

Create one more workspace in the directory “gitprojects” named “project2”.

![](https://lh6.googleusercontent.com/QZZ4jhbeGNbja0l0-3xTZK7R1i7Fijehq6_tbmuYA6odY80TLzWaIUKwPxiDxTWOFY5J_rTaZgnv0BUWBtQGYfF1d9cI0GW7-mWmNs1O_k0Xyccu6pDRVie8wboIMsFkxotAbSVKExdxR3q_T0_K align="center")

Create two files inside the folder “project2”. We can use the command **touch** or **cat**. And write something in that file.

![](https://lh5.googleusercontent.com/accwVvCSX6C1l_ZeTV00cajK2mgeJConLcme5YCrtFy3BNHaJGNHNURfQgw37owPlRzsCgpJrcGLOWjf0DeaMq71n9ufnjTS5lJOPZ8TyE0Ey65_uzH4sHb7DixCwktucKVjZsi3OMEmXlnduE7i align="center")

Now, the workspace “project2” is not empty, it has two files in it.  

![](https://lh5.googleusercontent.com/uGPSs72P71tsBIlvyuum4z6jQcfbaVdr7fe9FGl_ALBC_BhldWU05ZCHIOkNiP3fy8N-SQs-zo0yHn9HVLk9AiaLB2ldDXuqXObpnL4I2FOceGs867Dk3pviQyztq8BuIwoxG_CGqSFdQsXLepch align="center")

Now, we’ll use the command **git init** to initialize the GIT in the **Workspace** and create an empty Local Repository in our **Workspace** (project2).

![](https://lh5.googleusercontent.com/lVnzWgI5ZR7x-6Rofz7yxlDkBZA0ifmj-5-XzjKRst10Jm4f_dlwYgMVMOT_dfg1z7rrnTxd3--CxcYevQtsl2yiJ8qMfxzCSQKt_5bNpObKPOtNJDFP16mAzqnH0kbjVMAvTWAE1b4-MswKnsRS align="center")

![](https://lh3.googleusercontent.com/pusT1ehpKbk1Hdxd1oj_mQtsfSP7sb_wwjOSGxtMgg0l5UoDwxbT4hew-rZN2-gW2_jAiF3lpz3LHIwXlxrQEOubYyDb102Z-0sER_KddfySURDTtJmNjNBDxTI-WVPgCvLJCD6I_2gWaD-148jh align="center")

Now, we have to manually/explicitly add the files in the **Local Repository**. As there is nothing in the **Local Repository** (It is empty) So, nothing is being **tracked** by the GIT. We can check it by using the command **git ls-files**.

![](https://lh5.googleusercontent.com/CZ-8eBMcfmyN9myKXiwJfadbNONoefggZhqidi8YpubviNCYN3wpUxVnDnX83jskJTJUuSj8MLKOPVboKyBgasQBPgC1M7Y98CG4PK1TeNb8X8Dj2NdJumlth0L0wY_HIxJoqg3nMNL38VyjpiK5 align="center")

### **Scenario 1:**

As we have already created a **Workspace** (project2), and the **Local Repository** is already there.

Now, the **Local Repository** already contains 2 files i.e. one **Commit** is there and that commit itself contains 2 files “a.txt” & “b.txt”.

![](https://lh5.googleusercontent.com/3hejoEPRHhFGA4lOY9cr9ClD204ERlo6bzmmFTVUQqYXgLLsvjZBiA0tIXySKgz9CVh7FLk4zOeH4LVRACs2F9gga6kec8prmqGuNnEwezvdv5V35Bc7h7jZAyXMR5MfvzwDwuciKE7ucFaQHhpM align="center")

Now, if we’ll use the command **git init** then it’ll reinitialize the empty **Local Repository** (directory) means, it’ll become **Empty** again.

So, we’ll Check / Confirm that.

If we’ll check the status of the GIT in the working space “project2”  using the command **git status** then two untracked files will be present in the **Workspace** (project2).  

![](https://lh5.googleusercontent.com/NSrkiMfnWczVom5HQy4UJ-Y35H1cqAepO3dizjSIRA9pSZLXdYe18l1kZyfrVviu0ZCP0Har9i2wvrbBz8bkdEEec_itEzW2PKyxEfPMOWkzlPlEDmBEbSMAtSaNMUFx9HCt-12Q7apIRPaotyWw align="center")

Now, we’ll add the files to the **Staging Area**. So, for that, we can use the command **git add .** (We use dot (.) so that the whole files in the workspace will be added). Or we can use **git add \*txt** then all the txt files will be added to the **Staging area**. Or we can just write the file names also.

![](https://lh5.googleusercontent.com/m551JvAODsceqZr3XbsnqFXfoECl8TX9lu7muYnobpYQflNAAJJpCvyYxl9wpyd7Hq2vfANIoD0QrfzpqMUqAs7z_bYeqzqT1XPgjn4QjkbTgsxpF_su0JBmw1qJ9xhTU2cw-S4mfEKYAKPCSQLc align="center")

Now, again change the status of the GIT in that **Workspace** (project2). It says we are on the **Master Branch**, but no **Commit** is made yet, we have to Commit the 2 Files.

Also, it starts tracking the files. So, GIT starts **tracking** the files when we add them to the **Staging Area**. 

![](https://lh5.googleusercontent.com/dq8gmXCsTF9Cv53F9DQXe0irTdkpldeAl7MrmBDk-HmF6UYO3WJz1qfxtq4ZgeKiY0xnRLisucbcXxIC_LyJA8bjV8yJwBtVcOSPHMjBwf3CQ9AGZu3bsVt6Op1MSzyQk-GFj9B46Unkn8Yt79XO align="center")

So, now, we’ll **Commit** both files to our **Local Repository**. For that, we’ll use the command **git commit -m “&lt;message&gt;”**.

Now, if we are doing these operations for the first time then we have to configure GIT. Otherwise while **Committing**, it’ll ask for the details of the user as it’ll not be able to detect the email id of the user.

![](https://lh5.googleusercontent.com/BGp4pFLknavVWDDuRsvW4TtV6_vgAKzrbWIIao30stO7JtMPaZypnUaLRnB_wmSgwLfGiyafml2zAbQEbQ3gOdmofXvqrcqbcUvrCpTF5Rc60jkuQd5osuDduI7oaykrVLzuLQn4gK9hvMButcON align="center")

So, to configure we’ll use the following commands:

`git config --global` [`user.email`](http://user.email) `"`[`you@example.com`](mailto:you@example.com)`"`

`git config --global` [`user.name`](http://user.name) `"Your Name"`

In our case it’ll be

`git config --global` [`user.email`](http://user.email) `"`[`aviaadiikishorr@gmail.com`](mailto:aviaadiikishorr@gmail.com)`"`

`git config --global` [`user.name`](http://user.name) `"abhishekkishor"`

![](https://lh5.googleusercontent.com/sXn6iABbj344xwjwHgBOOvmk3mo0Zf5L2xZXMPfYHvDn-YKPKAaElAtMa29VKmeb2y21LmKCubyjuT4wtjOJrcwA4Wa7PxCq5bWj9gPIJBcoWOXlR9-C4gewwBooaFlN3nEmBHk5UNY align="center")

Now, once we **Configure** it, we are good to go.

`git config`**: It is the command used for the GIT Configurations.**

`git config --list`**: To check which are all the configurations configured in GIT.**

![](https://lh3.googleusercontent.com/Bms3qcynnbv5Bm4vVDpJ8gBCtafl2mwRam54Z23Z5bEfIUbJswsO8sO-uUrZU9nINpiTSMxWDHd4lennrGFoqcB9KjCrW3zh5TSB1hgzEwTa137QBpuQBAfmGwD8qFpRSZSE19qhwEOMZ6lFOOUB align="center")

`git config` [`user.name`](http://user.name)**: Display the username.**

![](https://lh4.googleusercontent.com/V_K1xOyCAavSas0EZnwDTJ9VUeq2iZ1M4w1WDmQpBUOUHtt7mKaCZktNvKLqTEbGd7r1kC2tIorD55BIBuCj_csyXWPP-PW8a5qrYvibif4OcyOxaSIZesKB8AU4xlKAh4piGec_TgsJZpg1qJ_g align="center")

`git config` [`user.email`](http://user.email)**: Display the user’s email id.**

![](https://lh4.googleusercontent.com/72_lha3xdSDTswb3Yn6nWx1u-kYiFOL4xfG66wRugiWjRZfNV3d4coY7r7etjg_2d6XsU5BhMwGPx30VDB_iFgaHvlxIF9b6gKOdEoX60gC-GES0utuWWFiJxReP2P7WuKMckWfYy_khm2F3aAAR align="center")

# Without Global vs With Global

For all the **Repositories** which are managed by the GIT currently; if we want to use the same username and mail id then we require to use **Global**. It means, for all the repositories (Git & Github) these configurations are applicable.

**Without Global** means, the **Configurations** apply only to the **Current Repository**. So, if we are using the GIT configurations **Without Global** for a project, then if we start working on another project, then the GIT will ask for the user’s details again for that project.

So, if we are working on **multiple Remote Repositories** then it’s recommended to configure GIT **Without Global**.

Considering we are working on three projects, 2 Projects are personal repositories and another one is in the office's repository.    

Now, if we **Commit** again then the files will be Committed to the **Local Repository**.

![](https://lh6.googleusercontent.com/1lSMRHh2whnWMgrKe34fQcCSM1XELYotdwMdLlT2kr3j8sBfdNx_HrfHcDIgsKWZrEa5JUQY7E5tqzALOHNnLTpsf7XUtC3OpXqKjXrF4H18IyCq1fepb_unI-8eQuq9wyDpdrl8UHnAa5AmHKMW align="center")

Now if we check the status of the GIT again using the command `git status` then, it’ll tell us nothing is there to **Commit**.

![](https://lh5.googleusercontent.com/JDVhXz2yRC8iZdlSONn5AnEnjWOFSy_97CQgBIDqToxomqhGzDYyaN0bhpJOYgjuGms-YdiViF1R4RNRLegDmQdMPAZhjFv7glysfVdhKrVi-K9VqJShmkt1i0sqfbKKSJ--LubprJpluKfQg_Hv align="center")

After that if we check the log of the GIT in the workspace using the command `git log` then we’ll get the following things: 

* **Commit** **Id** - It is a 40-digit alphanumeric Hash value representing the Committed file content.
    
* **Author name** along with the **email id**,
    
* **Timestamp i.e At what Date and time the files had been Committed?**
    
* **Commit the Message that we had written/given while committing.**
    

![](https://lh3.googleusercontent.com/pnKwlww86e_Y8gCc_6TuvWrQqaeJUPsl_iABzN4JOCB6vW2fHLEAgmsI-68R3YABaZbA1jL3bdkMwZcTjeOxY1Fh9oTA8GgOC1Lp1icQu9PPKaHtmv8LGLZib2qj2nnPW1kxgC8YaDO4yhnM2Rqz align="center")

`git log`: It shows the history of all the **Commits**.  

* `HEAD -> master`**: HEAD is a reference which is pointing to the master.** 
    

* `HEAD`**: It is the most recent Commit. We can change HEAD to the other Commit also.**
    

* `master`: It is the name of the **Branch**. As well as at the same time it is a reference to the **Recent Commit / Version**.
    

![](https://lh4.googleusercontent.com/fNJ7PG-pJgzvfnC5uQ8ABoIWXzRFzCheMmsYnOQis4KuVQjmKn8YtjtylpkSwqDzp-O8ib4yqlWxzcyvfj1mdug4ZG2SxnduLcNCPE2QNm1whMFCVcFX0r7kWGnkeJ3kHTX1nfguiQMtKshZbNmF align="center")

And then the **Master** is pointed by another **Reference** called **HEAD**. So, HEAD is a reference to the other reference. And this reference is known as the **Symbolic Reference**(Reference to another reference).

![](https://lh6.googleusercontent.com/zECDWr1R-iy1CWcduDjC3CMEHHnd0Q6ADajWCgXwk1adv-lWVtZAXJpiYMGD7C2-5BZjM1L1JbZBoUVEUCpit3fiKVAt3ACV5ioCNWW9FX3psMm8tusEdJTedWUUn74fl-S1LZNM1gcpNWf9Ijj_ align="left")

We’ll check the files in our Workspace also. For that, we can use the command `ls`. We’ll see there are two files present in our **Workspace** “a.txt” and “b.txt”.

![](https://lh3.googleusercontent.com/pFLtMRBC5P4sAMXu8XFDQHGu2-plS9IT-LQK0Nq6q676waYznvjjMSmuAO8qXxTEqhVrbYx0sBiLW42kuiELP29MwFNF95d_d0TYYn5NPLcFErxZx40PmxOHkqhujZhKNHP5FabVZi6LfX888dUk align="center")

Now, if we’ll check the list of the tracked files then we can use the command **git ls-files**. So, we’ll see GIT will be tracking both the files “a.txt” and “b.txt”.

![](https://lh4.googleusercontent.com/V48n8Vk8Lb1UYLVtBVmG4qODRImlubE0dpjl2PGhepk_2EXzuC-J9fmTKeWyj_omYE9ADl8MvOQTNPhJPvvknC6Btr7fxzciT2TyjmI4OTlQSBJN-6SB24Sm7lnh9hIvuSZuD5ekITQkcL11zrrQ align="center")

And there is already one commit in our **Local Repository**. We can use the command `git log`

![](https://lh3.googleusercontent.com/pnKwlww86e_Y8gCc_6TuvWrQqaeJUPsl_iABzN4JOCB6vW2fHLEAgmsI-68R3YABaZbA1jL3bdkMwZcTjeOxY1Fh9oTA8GgOC1Lp1icQu9PPKaHtmv8LGLZib2qj2nnPW1kxgC8YaDO4yhnM2Rqz align="center")

Now, if we use the command `git init` to **re-initialize** the workspace again. It’ll tell that it reinitialized the Git **Local Repository** again.

![](https://lh6.googleusercontent.com/S-pSSHSFCHV-IGI_89ooH9mDhKGYlroMPCTHwqdeptUhvTCOj1vd2aHvZX94zvmHx8JOBNg1edo2pHWDc82ARZhsf21qKw6ri9yCTsqfhL6RfAawLIEdo8EKlue7gKrBwfxDF7rLDU8-x6p4Qs0L align="center")

Now, again if we’ll check our **Workspace** then again two files will be present in it.

![](https://lh3.googleusercontent.com/pFLtMRBC5P4sAMXu8XFDQHGu2-plS9IT-LQK0Nq6q676waYznvjjMSmuAO8qXxTEqhVrbYx0sBiLW42kuiELP29MwFNF95d_d0TYYn5NPLcFErxZx40PmxOHkqhujZhKNHP5FabVZi6LfX888dUk align="center")

GIT will be Tracking the same two files as before.

![](https://lh4.googleusercontent.com/V48n8Vk8Lb1UYLVtBVmG4qODRImlubE0dpjl2PGhepk_2EXzuC-J9fmTKeWyj_omYE9ADl8MvOQTNPhJPvvknC6Btr7fxzciT2TyjmI4OTlQSBJN-6SB24Sm7lnh9hIvuSZuD5ekITQkcL11zrrQ align="center")

Only one **Commit Id** will be there, the same as before.

![](https://lh3.googleusercontent.com/pnKwlww86e_Y8gCc_6TuvWrQqaeJUPsl_iABzN4JOCB6vW2fHLEAgmsI-68R3YABaZbA1jL3bdkMwZcTjeOxY1Fh9oTA8GgOC1Lp1icQu9PPKaHtmv8LGLZib2qj2nnPW1kxgC8YaDO4yhnM2Rqz align="center")

**Q.** Then what is the meaning of **Reinitialized**?

  
**Ans:** It means everything is available, maybe internally the space gets refreshed. Means **Reinitializing** GIT again makes no difference. So, by mistake, if we use the command **git init** after **Initialization** and **Commit** by mistake then also nothing will happen.