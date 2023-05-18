---
title: "7. Getting Started With GIT-Part 2"
seoTitle: "Mastering Git: Getting Started- Part 2"
seoDescription: "Learn advanced Git commands & techniques in Part 2 of our 'Get Started With Git' series. Perfect for developers & DevOps engineers. Start now!"
datePublished: Thu Apr 13 2023 05:11:58 GMT+0000 (Coordinated Universal Time)
cuid: clgeny8nf000509mjapc843a3
slug: 7-getting-started-with-git-part-2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681323250403/ceb57f32-6584-4579-95d4-ac6086e952dc.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1681362542252/0039c7ca-2359-4a0c-b9d3-4f28b87df578.jpeg
tags: github, version-control, git, developer-tools, devops-articles

---

Hope you have gone through my previous article Getting Started With GIT - Part 1; If not then you can go through it ([Mastering Git : Getting Started with Git (Part 1) (](https://itachiuchiha.hashnode.dev/getting-started-with-git-part-1)[hashnode.dev](http://hashnode.dev)[)](https://itachiuchiha.hashnode.dev/getting-started-with-git-part-1) This is the Second Part (Continuation) of part 1.

# **Scenario 2**

If we change/add something in both the files in the **Working Directory**.

Go to the **Workspace** (project2) and modify both files by adding another line.

![](https://lh3.googleusercontent.com/Si3v97k_ZKT7LFlS0bHb12JNBhu5DJ9cC3pJhPZqT8Cca7xcMya3JW3TEwkkVNt-G4zyN7c5BZPN75nDvnzQFMchu47oDMCoW9JIpKDmrO6rwH_AfFJxSZ5oJjv0s_0qMx7SBys68rEXA6vNyHiG align="center")

Now, check the status of GIT in the **Workspace** (project2) using the command `git status`. Now, both files will be modified.

![](https://lh6.googleusercontent.com/sW27mfoQGzFntvWK603_OodfjHhsT598AxsEVD8hV5IvTgIbizU6pW-NXuHkrzyUUprNd-DPjK_edu0HFlgsod-k9ybIINGiP_5-2BJsVWTvZhvVnf0jGsfOpk1SiWWy2ArTx0Y_vSgTo6EEtaHP align="center")

Now, if we have to commit that changes, then we have to again add those changes to the **Staging Area** using the command `git add`. Then we have to commit those changes i.e sending the files from the **Staging Area** to the **Local Repository**.

So, it’s a two-line process. But we can do it by using a single-line command `git commit -am "commit message"`.

**\-a**: Will add changes to the staging area. Then Commit to the message.

![](https://lh5.googleusercontent.com/3KTsVI1BKimd-hQEkfAZUL_yomgjkMbuPx_C3Ac_EuujFI-QphUjHCcuaV6EZR7OEr-Lz91hfmHrOgAUqqbEg7kAscQYQZggD8VQ__UQy2LVkV4agxtFU8g0veOpbGJx_NZ3z_OUrBQ0teJ-AnkR align="center")

**Note:** This command is used when the file is being tracked by the GIT. This command does not apply to the newly created files.

If we will check the log of the GIT, then there will be two commits along with the two **Commit IDs** and other details, for example, **time**.

![](https://lh3.googleusercontent.com/DxFlE99DN2MAEl6_HRDm9VES4ebuSobeCH0jD5Icsw8iDG2TqMHrtU2IetR6nGkIDXmzTVX6pe3czcqML8us_XFhRCIiffEH2Z61c8LYYj-Q6fJS30YKm4UbWR7p2Q9Rirr5QJZ6nKOMk5a9hrFk align="center")

# **Scenario 3**

Go to the directory “gitprojects” and create a **Workspace** named “project3”.

![](https://lh3.googleusercontent.com/bZhwlnL5HP2JcNAYneIyZAX2ruGEni0qKq6qNxwzJHuXntiYH9WyW5Y9Aqm1EPEsLdZvkXGJV2rmDMQONN1rGKLiHELHo0qwJC0YvZvdfmBlWio2qC9pI8ZiDYy3Z4MXpeIJXgX75mPeG9tjZEof align="center")

Now, we’ll check the status of the GIT in the workspace “project1” using the command **git status**. We’ll get the response from the GIT that the **Version Control** is not applicable in the **Workspace**. Therefore we can’t use any GIT command. We have to initialize GIT once we create a **Workspace** and if we want **Version Control** then we require a repository.

![](https://lh6.googleusercontent.com/u6_lCNnGltwdT_6aXBX7v95Qjo4tS71wqIpaGyMAIVhreXVgnEDeMyCYjFlgNoYmoW0uq6HbGu5Q1W01Vjzj4zWBEuQdqSqEI42NptVKD4ybZaKTo88-n22rVDN_6Ytog_V8Z6ZixBfyybUHqtEz align="center")

Now, we’ll use the command `git init` to initialize the GIT in the **Workspace** and create an **empty Local Repository** (named as **.git**) in our **Workspace** (project3).

![](https://lh3.googleusercontent.com/MQC2FQgRD18intuYYqapxmn05akRY8M94bQsfkMlk89e8eVoE9y-Kfhr8ywRfgUDj1xpA7Mwz4DfokeCgh9uQdUXdihRJ8QehtjbHtcjRfA7fe9XbSfcFQ2IzZcOAFw1ySQlSnk_J2CXrBqVoTmm align="center")

Now, if we’ll check the status of the GIT then it’ll tell us no commits have been made yet and there is nothing to commit. So, to check the status of GIT we can use the command `git status`.

![](https://lh3.googleusercontent.com/gUyB-tPa__ms8z3TDm3W-5lWMCe3904sqwCZcc-VD65tO2IAnMTd5LUosIYPDwd8GwpJPYkEt00mss8t6Hzxpeq3DToauM-eIV1ZoEluhhd5cPZ34PfrKigCuBjTDFAmg2b3QwjLBg9RulODyY_c align="center")

Now, create two files “a.txt” and “b.txt”. And write something in those files. For that, we can use the command `cat`.

![](https://lh4.googleusercontent.com/_rwN2ISRGX6LRpPz-Z6_Yz2Am_tf4CRWq_MvHV367hMhTzx-vLbDu-9jAPiWvPapn9JtIoWXdeDyACY8K3ehTigJm_yqLyqVD1OJxFseNG22C30H_ZDfOF7EzlrpKGv8TSB-UmNQvYejWnNFgdvr align="center")

Now, we created two files in our **Workspace**. Those two files aren’t tracked by GIT now. GIT will start tracking the files once it’ll get into or will be added to the **Staging Area**. But, we didn’t put the files into the **Staging Area** till now, so GIT won’t track them.

To check it, we can use the command `git status`. It’ll tell you those files are not being tracked.

![](https://lh4.googleusercontent.com/Gy5M46dg__D544BHLMbyCDUNwag_qWcvO8S2G2DGgVCZmQqIPd_g42ZItp5vjYfKOxLDMDNmfi5pkv9SahQGysu7bALpUq2bWhdqYdG_ETjptIfZq4brvHxLS4mHTekJIc2ZZ08Giw_aytHwo1a_ align="center")

If we want to see the concise version of the status, not the **verbose/detailed output** then, we can use the command `git status -s`. It’ll show the **verbose/detailed output** of the status.

![](https://lh4.googleusercontent.com/DGuq24ypcadkZLxoEvSKblyfGzn_rtZrfBHpBsKL_d2NaZnPqLPfo7VqOLq16-YhgfcWD2wPk_X-bfctzpVISNvR1HhAdvU6cf1YD9EfOB3vIkmCtZAA6Ijfv0RK49RNx1jAzVxkrLP_vXRtBPN3 align="center")

`??`**:** **Question Marks** refer to the untracked files.

Now, add the file “a.txt” to the **Staging Area**. And the other file “b.txt” is still in the current **Workspace**.

![](https://lh4.googleusercontent.com/5mPqwghWK1stBM3ghno64TcPttBPmvkq6xEQjTJLqeYXuFwsSQ0WXv9XsorpqfTMpwUdSqfbxdoTdDR1YggLDalH7rmcJZISTBuRwRr24zOKHMij_lHWfxgzs0rk9_KykPpWOrM9E2PwY0o3W15I align="left")

Once we added the file to the **Staging Area**, then the GIT will start tracking the file and ready for the **Commit**.

**Note:** **Staging Area** is also known as **Index Area** or **Cache Area**.

It is a **Logical / Virtual Area** but not a physical Area.

Now, we’ll check the **Status** of the GIT again. It’ll tell that one file has been added but still, one other file is **untracked**.

![](https://lh3.googleusercontent.com/01oW5nZUsYVyVb-AYTlDoxCb4jT5smZUc_1Axx7mfjAHxYsVH03bxPqkLQRxQ78lopLxVqzzEnUVbBc9Z12juI4pfiyhkTlZ3aBdUvkBMr8lSrtpLsQu2rpwMbcK4z8TuDBi6Ivy-NtsoWQEnit6 align="center")

Now, check the concise output of the status, we’ll use the command `git status -s`

![](https://lh5.googleusercontent.com/h7wkTDTfWd0yfL5a-bnSOif9lAxnd2qW7mqWlj3AcofRKBC-Cy9UutybAxbuE7sSFPFOILDoBOegsV8X05g7icM8Oxg1qhvyRspymOqCdYB7hom4luMgcHYK7jrhv6k46Ny9UIZo62__TSthbnRo align="center")

`A`**:** Letter **A** refers that the file has been added to the staging area.

Add the other file “b.txt” also to the **Staging Area**. For that, we’ll use the command `git add .`

![](https://lh6.googleusercontent.com/oQqkEZPba4jzG__v3P1JTgCzQ-d763sjR5iWswuRyrLA4eQpozcibneCepbVrGF4unf_D5xI-21dsV9FX_rAyMIOkZgDkQpOsDjJ41pxtDb5pBe-WH8UIIGcopK2R4wXugwXLPw-U7wkR535FV8- align="left")

Now, we’ll check which files are there in the **Staging Area** that is which files are being **tracked** by GIT, so for that we can use the command `git ls-files`.

![](https://lh6.googleusercontent.com/XLP2VF8oAnJoiK9_EmAaSDrxdT0pKLtznrSAVP17HZoBDsgar89bT4hLPokmEvNO5HqdxDjMF9ys_kbvcpm8xlh03YLqW1G78nyVOUpv8StI7qSz5gmXOahdYAURJ9dAvhWMGoamtOwlXsiNFcH_ align="center")

Now, if we check the status of the GIT, then we’ll see both the files are being tracked, that is they are in the **Staging Area** and ready to be committed. So, we’ll use the command `git status`

![](https://lh3.googleusercontent.com/NxQ1lYIGSAgkpttieQImPHI25AmrDFO5VRGYfJfQIQ5lUJJS-x61Dlv9F-UoIEmL_f548pWdf2PQPYBuBB7pGoxifhE6g-0N52BBZWWfWQC8ZkyBPklWOju_YrHp8FnCu1gxsuL94fEg_Ao1Zubs align="center")

We can also check the **Concise output** of the status. So, we’ll use the command `git status -s`

![](https://lh4.googleusercontent.com/A4QBal_vqvVYQ_DHJW0In6EcGBWJm47b3hREpbOkZVIHvEh0QN1zXh-vspfmcKl0Z9wqr3IZWAP0cQliBaR3xWinmTeYizhhSdxDshCI1IQkvNfj7I4HMc_VbXCJ74VFNOqK3TDJYDF8spNDIhzK align="center")

We’ll see the **Letter “A”** before both files, so that means both files have been added to the **Staging Area**.

Now, we have to perform the **Commit** operation. So, if we want to **Commit Staged Changes** (Whatever files are added in the **Staging Area**); We’ll use the command **git commit**. And to commit, messages should be compulsory. So, for that, we’ll use `-m` along with the command `git commit` and after that message should be there. So, we’ll use the command `git commit -m "message"`.

![](https://lh6.googleusercontent.com/FwrtZUGdlk4ddDYPhHPUDX7RFv4jE4LCtp4dclmTYuOojlxqGs1br3PRk1LojqT_PcJ5PeSNt1TJrKZ_gCe-lWN4k-f5RMf6mGVMtf3aTbaVFGg7yWCxuEyoXN0lqlEA9q9Ozp0jH0bQJN2TrEFc align="center")

* “**New files added**”: **Commit message**.
    
* **644**: **Permissions**
    
    * **6**: **rw- (Read and Write) (Owner’s Permission)**
        
    * **4**: **r-- (Read) (Group Permissions)**
        
    * **4**: **r-- (Read) (Other Permissions)**
        
* To cross-check the permissions we can use the command `ls -l`.
    

![](https://lh6.googleusercontent.com/fsGcuuZYQYtfRdGabbhSwW96Y7ssr3KmyZfE_5tBS1XGe4QdOIR4T7q52csI5AniUqG14ucW9GHUv53V5QZb2VMg0oaEcbRdiaFONrfPDc7UJYA9MLwFR19Ny_cq7nwo0przh4F5QEAFooAfOgbV align="center")

* **8d0909c**: First 7 characters of the **Git Id**. (Check with the command **git log**).
    

![](https://lh4.googleusercontent.com/TiQ9xQJ-sl-z_PxVP-HC1Du3EqqcxhEnmdiQBrRasaTl5POhMgENVifyeFfZdH0tWYfEBJ39ii157GYDi38aEqL3NkgM6UxZvhj8PMpeb7kDPO-4Wk8_EAQEKCUWLHAnYojDN2hfmnr9gscWP7Uz align="center")

Now, check the log of the GIT. For that, we’ll use the command `git log`.

![](https://lh5.googleusercontent.com/SkRCKte-yqbTGOrY3J5Cc_-4nyRcCTFrLlkxmEqXYdf1F5pIVJkWZPOrnAfeMz6eTohS-Q116m5akgTtlgHXUfuI-fywCqniRV75YsKBY_swMX7KV_CcQzTSnR3Xrl_z25y2YYIq61D7dgGRPNnW align="center")

The advantage of the **Commit Id** that is in the **Hash** **form** are:

1. **Security**: If the **Repository** got hacked, then there will be no problem as the data will in the **Hash Format**. Only GIT can understand that data (**Commit Id**).
    
2. **Less Space**: Even if we are having huge data, then also it’ll store using the **40 Hexadecimal characters** only. So, it’ll take very less space as compared to other **Version Control System Tools**.
    

There will be 40 characters of **Hexadecimal** **Commit Id**, **Author**, **Timestamp** and  **Commit Message**.

Now, modify the files that are present in the **Workspace**. So, again if we want to add/modify anything in the files we’ll use the command **cat**.

![](https://lh3.googleusercontent.com/3SBwQ_NIMK9ptdc76-u0kFE4EEQTAgh4cwNX-Jpy4OH2fY0LB61S75EskhZopJtqC0v317v7Y_n3QWvz0Y0af-em2gzO0keq0M8oP_Qg1qI6XKAcG3fktSG-0j3N5l5z5F61b267bybMt8vEtmJW align="center")

Now, check the status of the GIT. It’ll be objecting the file “a.txt” not the file “b.txt” as we have modified the file “a.txt” not the file “b.txt” and, as the content of the files in both the  **Workspace** and the **Local Repository** should be the same but here it’s not (we have modified the file a.txt).

![](https://lh5.googleusercontent.com/RkjKZWLHQhDSRePI62tdqAr1OKAfhSnrGij-jPs9xODF8QYHgZ1Cx9x_YvY74Ybf8roYW5HSVe2CoGYo4lJfXt9iDNEVp0QYBdewIOI6eR8LVZ9tMsQp9FbBTVN2XCP6f1Y0Cvw33Xc2a6ujJ2Jv align="center")

Now, add the **Modified file** to the staging area, we’ll use the command `git add <filename>`.

But as the file “a.txt” has already been added to the **Staging Area** then we can directly **Commit** the file into the **Local Repository**. We don’t need to do it separately as it’s a two-line process. But we can do it by using a single line command **git commit -a -m “commit message”**.

It’ll tell, one file has been changed and the change is one line insertion.

![](https://lh5.googleusercontent.com/wdOoj69HVVHJ8ctGcj0E4nDw9evaOYyuEX9lCiJvEDaehu5ezxAKh9d-Fey1GkerJvd1Xy2PYCgSoNFvFw5C0FeEI6ygnj6a5F9spadzR6_a7TzRfelyIXUsK8Zu9D251xkWDpm7F2-Je3U2K6eL align="center")

Now, check the log of the GIT. For that, we’ll use the command `git log`.

This time there will be two commits present in the **Local Repository**.

![](https://lh6.googleusercontent.com/6j7ZqR6q-k67RCiw0OOjQufYmJ7X_ME78DAz8GiVbF91bjA7KsNwgXxcNS0izpemafze1OoMyAfrBwnu-w8Gk-Md1jzubqotJbTh7BYuSP1_RwoFq4h1h0fTRx8PnWUFCbACZkRlcOompmHbys0C align="center")

In this log, the **master** represents the **most recent Commit** which is the 2nd one.

**Commit Id**: 6b43326ee85e4d249eaf375b836f28ae2b6ade1e

# **Scenario 4**

Change the user’s details:

Change the **Username** of the User (Without Global). For that, we can use the command `git config` [`user.name`](http://user.name) `"<Changed username>"`

![](https://lh3.googleusercontent.com/hrOASpQLQE1XrGVpAFGJJ5PnJea-KI7i-Hg8nPg4pIvILYZNajxEiVqFgDSBVzHnOAoTvSSwOj36Pk6KkK36UayEEDgv-Aw3DPx3Zko1VXIvum6PPHlsOzEAu8khOy21FOqvSxveAdcgvvaejTg1 align="center")

Change the **email Id** of the User (Without Global). For that we can use the command `git config` [`user.email`](http://user.email) `"<Changed email>"`.

![](https://lh6.googleusercontent.com/vcDycL3O5aaqAvIyEqp7FDxnCwCJt3DCvBGFXNaNs4HHHk7gVPyyG0Ts9X9uZikkPivWqm3tIvkOXoAQZ-GNC3YXU6V8iDq6UnfGhRc4ffqKg_HBlCP7Zio54NSEOVkFc9tjRTohKe05hwcnQ4P- align="center")

Confirm the username and user email Id. For that, we can use the command:

`git config` [`user.name`](http://user.name)

`git config` [`user.email`](http://user.email)

![](https://lh5.googleusercontent.com/QHcxpMAEu-GTm4LBmPgBJrAThLw-DwCECTfJOzhtmpAui0KNCu7hovxeYSLSCUUnnRF-EQmZq3SfSNN0Wqnd-jilWmEMQWiS6Iteb0c_xGFYj1Jmkp8FMvcY8BXIjvN2LQ5ExiWHdRlTQIf-sihZ align="center")

Create a file “c.txt” in the **Workspace** and add something to that file.

![](https://lh6.googleusercontent.com/7YWDpYODKVxoWa0gYMcE3IMXyxUIUhIcYLs6lsoxF6-nx_9DLNTq9IGKvBVqR-EGuUvrv3xUw6VWi_6D9qt7jg8EveoUxBhkeqwqy8IDKVGms9t39SmsAmdwS2vciRU0POkODZG7l1fi7jxcO-DW align="center")

Now, add that file to the **Staging Area**. We can use the command  `git add <filename>`

![](https://lh3.googleusercontent.com/qM6-TXAuC07TueXwD8X5KvpkcZZsbOF26l67fi_Upi1QEAAqVEl9Hg_LTgknKvxkjMUtdaBWWXYHK-jXPJhOq-hY_MHSIXvPIh9rhnCgKMIwt2k4q_jm2nr0GmyZjeYLUfPk1KRGAX8olMniM-fS align="center")

After that commit that file along with a Commit Message. We can use the command `git commit -m "Commit message"`

![](https://lh3.googleusercontent.com/cMKZsw1LAUf2lMMcTaqRZNwmFpt9B2fqKHG2mqkXvU_wxMmNzdqGIBPkYFLLGmyprT9s_pUqYwdBX08xVRVSOjn2lpgsxK_Fvbvb-lagrixWKpgYb063IjhUUPy0rIxPsglUqKYBnqgdoV2BCIoQ align="center")

Now, check the log of the GIT. You’ll see for the 3rd Commit the **username** and the **user’s email** is different (It is the same as what we had changed previously).

![](https://lh4.googleusercontent.com/eonJ4-HshbG4oJOJcKLwoFJXveFhsstDgR8xSqV0kUV6glMjxiPR2dY-l9RgzPk7I0-SrjUWMDFgfM67KYUI0RiV966JT-KmcgTGlRHLrwvVQ-Io37qYj28iGAXxuqhXJ3hPzssNtytbhfpwNkvS align="center")

But it got changed for this particular **Local Repository** (Local Repo of the workspace “project3”) only, as we haven’t configured it **Globally**.

To confirm that we can use the command `git config --list`. We’ll see the **Username** and the **Email Id** that we have configured just now and the **Username** and the **Email Id** that we had configured initially both will be present.

![](https://lh5.googleusercontent.com/DixDzfH6zKn5BZPPqy4dMoaFcZGImO13Hm3wiWjW8LNjwqHVFyp4ANoCHL2IvvTQf840d4BNPB_59VSNaNdR45l4c8FIkcBYxnf5PjwVTwJ1VIb7nWOvpsXV4dJxQU5ANP_GBPZ6FyVNUCrB4Kzk align="center")

This happens because we are still in the **Workspace** where we were working and reconfigured all the details of the user.

Now, just go back to the previous folder (Using the command `cd ..`) or any folder and then in the terminal re-type the same command      `git config --list` again. We’ll see the details (Username & Email Id) that we had configured initially as we had configured that **Globally**.

![](https://lh3.googleusercontent.com/D_DpGl6a-krPsY776iEXpXl49JOX19UTCaDwTVh0BHHNBUQB38PQk40xvX6599ap2j5IPDBh4MILo4qX3EcPoqkNZJCg4zsHycVMIGuMcka2xnRzY6MRBBxnmGLU3FEpbkIbhraNw4xkv7erJJQg align="center")