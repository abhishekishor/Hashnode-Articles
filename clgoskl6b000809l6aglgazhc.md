---
title: "9. Removing Files By using "git rm" command"
seoTitle: "Git rm command: Removing files from Git"
seoDescription: "Learn how to remove files from a Git repository using the "git rm" command in this comprehensive article. Master Git file management today."
datePublished: Thu Apr 20 2023 07:19:01 GMT+0000 (Coordinated Universal Time)
cuid: clgoskl6b000809l6aglgazhc
slug: 9-removing-files-by-using-git-rm-command
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681973027303/37fcebd9-0116-4c47-b59a-7950b75e6bb5.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1681975020011/f1614562-6253-43a4-94a4-2396030f1987.jpeg
tags: github, version-control, git, devops-tools, devops-articles

---

# Introduction

The `git rm` command is used in Git to remove files from the Git repository. It is short for "Git remove." When you use this command, Git removes the specified files from the working directory and the index.

Create a **Working Directory** “project5”, and enter that folder. We'll use the command `mkdir` command to create a directory. And `cd` to enter into that directory.

![](https://lh3.googleusercontent.com/U-Y3yAHK4e5zYEIxTYmoUCiqcwYVKs8x2LTfVVL9FH-2cYiB6q5wzD0pDvOgSiwaqDYGDoQrYI-v6wk0VSj3FeKHuksvb_DPUf4TgBtBkihxHmxZOd8FwwmMhvMluL4fSElpcsjzL5V4bxe4X6AhMg align="center")

Now, **Initialize** the **Workspace**, and it’ll create an **Empty Repository** in the **Workspace**. So, for this, we’ll use the command `git init`

![](https://lh4.googleusercontent.com/VmWhokmOwB53-BmSM5krw2TieHceKCRtfWQPA_390Gxm4ozEh0J5ua04hUXjjIWtYPosMw25cvC38R7VelGAZc8iNtj5UnF9lXGm2YfTiFsqQlFxYJuazfKrty_TaA8h1qb-oTecGDbfeyk3CJawjQ align="center")

Create three files “a.txt”, “b.txt” and “c.txt” into the **Workspace**, and write something in it. We’ll use the command `cat` to create the file.

![](https://lh6.googleusercontent.com/CLzyHqo85_fJCk0ca_TsswJpf2DbPPmaMsO_o0_KcwLWTUMnXV8JnHRX7RNGacXzYWEImH8T-G7rss2szWCmWui8bh7rLYZZMekT1NSLmUgjpF-KNk80hqLG2lnLzytBBcYTalzZVTkyfMq24El4cQ align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681969282484/7c8bbec0-a19a-4b80-8db0-67158eb686d9.png align="center")

So, we have created 3 files in the **Workspace**, and these all files are available in the **Working Directory**.

If we’ll check the **Status**, using the command **git status** then it tells us all three files are **untracked**. And no commits have been made.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681969406873/c1a0cf65-ecbe-4336-a250-1615e650adc4.png align="center")

![](https://lh3.googleusercontent.com/_-KlCmggvKv_37hyie3Xi6ks3mkXiUE_td0gXHaFfFZWHSVoWOThC22NXHQjxhKvUvJ9AM92d_9vlBYH-RclgLsUCVFTexOkBfVhFqCxQTFs0UPruFzuX6gLzW6lZDro0zaRzhvRT23Mkw-m8G9h5w align="center")

So, now we’ll add all the files to the **Staging Area**. So, for this, we’ll use the command `git add .`

![](https://lh4.googleusercontent.com/p7DRD_0JX18oF9brVlUwUa6fUOHgNjjzvLSrusMmyICUPD9S9dSaCv8X65-77YoUeaRKgJ8kxT7yKm_et2Q2Ao-0949WnRqbiTVegc-eOx4DdOuq_7WLohWj86qmTWRRBDFT2kawOayyiXfhkSQF9Q align="center")

If we’ll again check the status then it’ll tell all the files are being **Tracked** and added to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681969511139/721fb4e7-7418-45b7-a0dd-678626ae1d10.png align="center")

![](https://lh5.googleusercontent.com/VNwtH17lfEefe3FIkVvT-1Gbb0etss-B1Zckt9mv1ZiezvuDaAcZgL9MIpSTGSo-I9UvM1OJPXkNgenIYEkdfatXYOrjQyU8bRhyo6WiDMB09qZbHgKSoQh3n3DxtA4hjkOLaTXthX9IEMm_jaD79g align="center")

Now we’ll commit the files present in the **Staging Area** to the **Local Repository**. So, for that, we’ll use the command

`git commit -m <Commit Message>`

In our case, the command will be `git commit -m "3 Files added"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681969636613/82ab43c0-433f-40f2-860e-cbe6f7736f3e.png align="center")

![](https://lh6.googleusercontent.com/DshLcg-BgsE5p87Ha2A-jbiDPi5pdUz1GVY6fnLEQQw8UO3Hxn-_IGhg_Uzl316HLrjphu7vYxsZWbHJjD0IVB4c5SJsMgSd9JpsEF15WqDS9Ht2ddWwtx_JnWZWUpd0cG9EkxRLWeW_ewmtjhSo4A align="center")

And now, we'll check the log of Git. So, to check the log of Git we’ll use the command `git log`

It’ll show, three files have been committed to the **Local Repository**.

![](https://lh5.googleusercontent.com/5yXstwXJGUVJoYmm1T9qZjIPzXx0knoW4R2QYi9E2tO0nzmJQOGmRJYqawJVca8GU8bKJFDB2jhKwPHbej3enK_QijQw9EJL5EtM1uydC1fwNTC5hklPuNk_eBqiUM30P-Nh6JMLcJOtoXiXSbv8Uw align="center")

# Remove Files From Both Staging Area And The Workspace

If we want to remove a file from both **Staging Area** and the **Workspace**, we’ll use the command `git rm <filename>`

Example:

In our case, First, we’ll check the files present in both Areas i.e the **Staging Area** and the **Workspace**.

So, if we want to check the files present in the **Workspace** we’ll use the command **ls**, it’ll lists out all the files present in the **Workspace**.

And,  if we want to check the files present in the **Staging Area** then, we’’ have to list all the files that have been tracked by Git. So, for that, we’ll use the command `git ls-files`

it’ll list all the files present in the **Staging Area**.

![](https://lh4.googleusercontent.com/TqX9ZhYFVq0ZkIwdbdla4LIe7xKKrXaJifABIaq8pW0Bw-hTGMbY-lWPytikPWRnT4lA8w7rFC0kiu5DSkTWMgrpgkheE3DrrQMFtkfmoOZ4--Opzov9H0JbyjM4gptS7uhL3TAILlyv8Aw8oBM9hQ align="center")

After that check the **Status** of Git again using the command `git status`, It’ll tell you everything is clean, and there is nothing to **Commit**.

![](https://lh4.googleusercontent.com/uGBQA9Cg6ndjZw_Ugzwj7V_BrSt0Loiey7_AEsflaJyUrBlspZsfuWZV6B-cPuZr4MX8SkjmruhQfdbqSVJf8CobSKANWK0BLN1F2uMaBpZfl-3KyqmqPsPkSr2iqdqSIuoh01JnB3POniVATS2QOg align="center")

In our case, three files are there in both Areas. So, now If we want to delete a file “c.txt” from both **Staging Area** and the **Workspace**, we’ll use the command `git rm <filename>`

In our case, it’ll be `git rm c.txt`

Then it’ll get removed from both the **Staging Area** and the **Workspace**.

![](https://lh4.googleusercontent.com/Ycc99ag-dSx-qudIRKO3yv9aSJR7uAradiPwfn2sqXixwvLFqTZ0zhImnWN4gFqECBQ6wLip8rvDA6o9qanvKrvJ5sk7iz6KklDbvuXAskHsLdCbm6-pfsHKUiAqw5USeFMpqUJOrGOd_8OgknGWOw align="center")

Now, if we check the files present in both the **Areas** i.e the **Staging Area** and the **Workspace**. Now, the file “c.txt” will be removed from both Areas.

`ls`

![](https://lh5.googleusercontent.com/F_teYJaGt8KvP1v7fc5dK2lDPntNSl-dB0ZdlESABktj2VoZj5aCJPDWxH9I9UoKQlbyTYwWO3CJXApdYImay-z31eyuzyjD7Q5XgkwLOJEZ6Q6LNUQSnZbMSwL9F_KCqPfH7KY4MM7BEMCIfaV1hQ align="left")

If we’ll check the status of Git now, using the command `git status` then it’ll tell one file “c.txt” has been deleted from the **Staging Area**.

![](https://lh6.googleusercontent.com/O58XmGPxETDoOJhWE0tky7kYiQiXZw1krmNqedb7KbO_1KFqkAX1aYwbOZfPJGhS6zTjxN7DYXZDm66iOUeWQmmTlhXZqHkZb75aWtUjnziItjs3ofTsqU-6I2CG-ol5nUBMJacux9pplk50SMxJxA align="center")

So, the changes made in the **Workspace** and the **Staging Area** should be **Committed** to the **Local Repository**. So, we’ll commit again; this time 2 files “a.txt” and “b.txt”.

We’ll use the command

`git commit -m "File "c.txt" has been deleted from both Workspace & the Staging Area"`

![](https://lh5.googleusercontent.com/xLh_pQ3EdHe9CeTlDcGzFMx0rTIKGY4JJ8rG66m2GTWBCqxmFeoAqiceV7XVOzRU7yOYSSP5ywoT9NacBDEDhugGYiFxjPp-D6mfyvu0Xmpa1zxPmyku_azI_THLm7GL5bxrh5CW5uhh3E9U9SNZ1Q align="center")

Now, we'll check the status of Git again. It’ll tell you everything is clean, there is nothing to **Commit**.

`git status`

![](https://lh4.googleusercontent.com/uGBQA9Cg6ndjZw_Ugzwj7V_BrSt0Loiey7_AEsflaJyUrBlspZsfuWZV6B-cPuZr4MX8SkjmruhQfdbqSVJf8CobSKANWK0BLN1F2uMaBpZfl-3KyqmqPsPkSr2iqdqSIuoh01JnB3POniVATS2QOg align="center")

# Remove All Files From Both Staging Area And The Workspace

If we want to remove all the files from both **Staging Area** and the **Workspace**, we’ll use the command `git rm -r .`

**Example:**

In our case, First, we’ll check the files present in both Areas i.e the **Staging Area** and the **Workspace**. So, if we want to check the files present in the **Workspace** we’ll use the command **ls**, it’ll lists out all the files present in the **Workspace**.

And,  if we want to check the files present in the **Staging Area** then, we’’ have to list all the files that have been tracked by Git. So, for that, we’ll use the command `git ls-files`

it’ll list all the files present in the **Staging Area**.

![](https://lh4.googleusercontent.com/pLVF-jXEfcwEykjnshH9OGQS5UCrkOnMGnygSotK7zyfWHeftfzgEUVEINz1HBWwXM54PM0e7ia4B0-m49AIqL2a9tf0BIb4RAE-hsgWBmVaA8siYcv0oyl0BciBNDiKIEY7GTfw4FBMIHKdkXaVnw align="center")

After that check the Status of Git again using the command `git status`

It’ll tell you everything is clean, there is nothing to Commit.

![](https://lh4.googleusercontent.com/uGBQA9Cg6ndjZw_Ugzwj7V_BrSt0Loiey7_AEsflaJyUrBlspZsfuWZV6B-cPuZr4MX8SkjmruhQfdbqSVJf8CobSKANWK0BLN1F2uMaBpZfl-3KyqmqPsPkSr2iqdqSIuoh01JnB3POniVATS2QOg align="center")

In our case, two files are there in both Areas. So, now If we want to delete both the files “a.txt” &“b.txt” from both **Staging Area** and the **Workspace**, we’ll use the command `git rm -r .`

Then all the files will get removed from both the **Staging Area** and the **Workspace**.

![](https://lh5.googleusercontent.com/zP1fRMVcVsqWsjgMaJWzy7jBTBJ8UfFb1fmiVt_s70NpA55dpDl7sRi5cbEZLwuwCZBy788Hb88YMA7Xh5LUzcFGTqw5Z8OkFBwYXnSFnns5sJRge4kHWolcA0my1vLqdJcuClHxSliWA1yavShakg align="center")

Now, we’ll check the files present in both Areas i.e the **Staging Area** and the **Workspace**.

We'll use the commands:

`ls`

`git ls-files`

![](https://lh3.googleusercontent.com/VVaXZ1Tf2gtJ1iMeZjrL1b-xhoK7GNOtLbouQ1k09IRJqRnLSKtXrtv6L4xZfk2DGtqtH2pYcDGtZbW2el-yFzQVACDTYITupinovEiYL46rXERpl7NrbGLtvldSh0RGAPC5lJxWPfuOHLTuuFRtRQ align="center")

Now, all the files will be removed from both Areas.

If we’ll check the status of Git now, using the command `git status`

Then it’ll tell us two files “a.txt” and “b.txt” have been deleted from the **Staging Area**.

![](https://lh6.googleusercontent.com/YtD0m1tlgdf4ydwAcqig-ztPvT23F90fS6DXwmyT97nToPlSYjlBoJvjs4UssUMOEAEAM0oz5KEm9c5r-wMvCrDiWd2iXqylFIBdlHLJUpILo9yUiNmLcKQVf5rBwetuXyYUh0ikBBNe2Sx1KIKZ6Q align="center")

So, the changes made in the **Workspace** and the **Staging Area** should be **Committed** to the **Local Repository**. So, we’ll commit again.

We’ll use the command `git commit -m "Messege"`

In our case, it’ll be

`git commit -m "Removed all files from Workspace and Staging Area"`

![](https://lh3.googleusercontent.com/5p50eyoSGzz6kdnsEkiiVFqzjYk7qnjqxe1eTCmdylG9yRNDZx03xxXtp95zGfyl1LjvQRmlY0zhui50iOg4H-mUK6HcCBaZG6-aqodq5dytlYJe54YKxOZRvd38dddYaVF1PwgZ4XfSw5uu1_-peQ align="center")

The changes will be committed.

**Note:** If we have to delete all the files from a **Workspace** or the **Staging Area** then we should use the option “**\-r**”. Otherwise, it’ll throw an error:

`"fatal: not removing '.' recursively without -r"`

![](https://lh3.googleusercontent.com/o3O2fJOQS6YgH2HcfTAab-dCedL0GA25_Y1oUiCQKarekJ9LFMhG7HIivEwKQmXRIWNfYs6cv_DUmAKjdpMjK2qLSN3YNeCrLU0RzQMLqQ52UE9pMnOc4oZb5wADN3k8MjMm9X1ye3-UuS1Hj2wrVw align="center")

# Remove Files From Only Staging Area Not From The Workspace

Now, Again we’ll create two files “d.txt” and “e.txt” into the **Workspace**, and write something in it. We’ll use the command `cat` to create and add something to the file.

![](https://lh6.googleusercontent.com/GkozNq1N1uCyz1BsCNpZTH5iMZ1UtA4VkWhqodeQsCMj5ByTXXTQhXrfIjDXUhX6CuEYu1yLM0vRtFSVurN6brNzCNVwq-YMjs8sgHGLmI2XH9JUYkh__BexE4ei_iSAYQyc_bRnnEXxsz_YIrT7AA align="center")

So, we have created 2 files in the **Workspace**, and all the files are available in the **Working Directory**.

If we’ll check the **Status**, using the command `git status` Then it tells us all three files are **untracked**. And no commits have been made.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681971525803/c7e67100-ec87-4522-a042-4cd24e68040f.png align="center")

![](https://lh6.googleusercontent.com/NlrS7PCE_geaoJmDH-1QcKBx8aijc_oplTdrs26LfRkEbT4TOGk5qOPCZIYTtshw1mksf-wep612FRAtrK2cH5yqC5xWy6lm6B-5Zoh5j-mpvJ_4dVLojD0yR-0dMntw1TY7C950Ygk83UlsT9BbCA align="center")

So, now we’ll add all the files to the **Staging Area**. So, for this, we’ll use the command `git add .`

![](https://lh4.googleusercontent.com/p7DRD_0JX18oF9brVlUwUa6fUOHgNjjzvLSrusMmyICUPD9S9dSaCv8X65-77YoUeaRKgJ8kxT7yKm_et2Q2Ao-0949WnRqbiTVegc-eOx4DdOuq_7WLohWj86qmTWRRBDFT2kawOayyiXfhkSQF9Q align="center")

If we’ll again check the status using the command `git status`

Then it’ll tell all the files are being **Tracked** and added to the **Staging Area**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681971639033/61123286-d97d-40c1-82ce-4081c1e494ae.png align="center")

![](https://lh5.googleusercontent.com/TOSN0r5DhLNiUGYBDwKGqXvVc2481tiiK7O3rvGvtqKzoJOz8Al1ElKHf1yD7BXuvVbjJ1k0-4aSScxPwPEBef9luGyc-nlv0owUCdxorwL3kYCiXKDzqPrKtxD-sriH7G6tkBY6_9aYXrzZPQNa8g align="center")

Now we’ll commit the files present in the **Staging Area** to the **Local Repository**. So, for that, we’ll use the command:

`git commit -m <Commit Message>`

In our case, the command will be

`git commit -m "Files "d.txt" and "e.txt" added"`

![](https://lh4.googleusercontent.com/zUPR8xPJYlq0nq4lEbicSwNBfOFtK-zjHP-EB40BQx_JstP8TVX8L6pm-PNNnfqvURuhx6E59a6j1C30_TBAWVj5iHsbKfSEDeL5ZfBD-Tir2PgwxZtZujQW6Hei71nqvJ5gvzZ7gIo2JPFcSRiy5g align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681971797354/6cf543b9-14a1-4454-9e50-2ea34d8b1e13.png align="center")

If we want to delete a file from the **Staging Area** only, not from the **Workspace**, we’ll use the command `git rm --cached <filename>`

Then the file will get removed from the **Staging Area** only.

In our case, two files are there in both Areas. So, now If we want to delete a file “d.txt” from the **Staging Area** only not from the **Workspace**, we’ll use the command `git rm --cached d.txt`

Then it’ll get removed from the **Staging Area** only.

![](https://lh3.googleusercontent.com/y2Cpgov_AGHgLwl7wn716yuB9PS7ztk7WkBljwPqe4tDbYPvoVCXRgBSa1pufxs9xzk3e9CjinzTJDs3lJnV1QPhijVFG3PJdZtVT2-QO4gZy8NcQ8QHlVosmChJncdiCh81r_OMvLSJBI4ffZkXiQ align="center")

Now, if we verify the total number of files in the **Workspace** using the command `ls`

It’ll display two files “d.txt” and “e.txt”.

But if we verify the total number of files in the **Staging Area** using the command `git ls-files`

it’ll display only one file “d.txt”.

![](https://lh5.googleusercontent.com/v1oVbltGXUwSWQqdIWeV8KYyRBDzKh8m7qRhkQz6X1oA7i0YR9K9o5pxuxz6RZELdhh-eKB5lS_vLTMsktEJm2NyoX6X2FrbU2HtyBvRMzvF0q46Z7C8JZf2Fjj3W_xBtYol0i-VL3waKBglIKXheQ align="center")

Now, if we’ll check the status of git, it’ll tell file “d.txt” has been deleted and now the file “d.txt” is untracked as it’s still present in the Workspace.

# Remove Files From Only Workspace Not From The Staging Area

So, in this case, there is no Git command for this as a working Directory means a simple folder in the local machine. So, if we have to delete a file from the local machine then we’ll use the normal Linux command `rm` for it.

Before this operation first add the files to the **Staging Area** (Ex: After any changes) using the command `git add .`

![](https://lh4.googleusercontent.com/r25rONyKZowHiZ-BZAQQuEGbOZvF9cA3S35i1fNROt1qDwsXLTgZoqC5CB6nqdZrzNF8uhl0T6WB4Kx1ncBVnbaPR_ZqZ8C4vjh5mbwtpNne-WZ8VgP-dTHcdv7-Rj6hgiZWILSwNgvjylkMtZlo7g align="center")

Now, 2 Files will be displayed as we added again the files from the **Workspace** without committing the previous changes.

Now, commit all the changes to the **Local Repository** using the command `git commit -m <Commit Message>`

In our case, the command will be

`git commit -m "Files “d.txt” got deleted"`

![](https://lh4.googleusercontent.com/vV_FQk5_YPX2pAc6Mh_45XmbnjPh8mQyqWlYsOrJldRGHhfVMIFxMXEY2IYSlH0pi7clwnwdK8W08mTZiStthxMQFLHMaqRFwVSmSKlgf-UAuZkqOumy7Lg2gG9K2HhaZqloDaM7a15M47g8acXWyw align="center")

Now, to delete the file from the **Workspace** we’ll use the command

`rm <filename>`

In our case, if we want to delete the file “d.txt” then the command will be `rm d.txt`

![](https://lh4.googleusercontent.com/r7n7hzF3-mPSRJeiRLotPABjwGti-eXH5C56v5EN2inctARfkxpND7L3nEZUalPr0yRhun5DJVcz3iGrlvtLuV7F2V936d5hWscLvvMHLaY-Y0e4j0fGtebTrXh4iBcg6HPVqyngGzOKmd1PYzEdXw align="center")

Now, if we verify the total number of files in the **Workspace** using the command `ls`, it’ll display only one file “e.txt”.

But if we verify the total number of files in the **Staging Area** using the command `git ls-files`, it’ll display only one file “d.txt”.

![](https://lh5.googleusercontent.com/Z28p5-usA5YIb07H86mQh-QObYhsGUin9fI8y3KlwHSe77m7mqeruXMJ8M4tCP3luIBSfSDMRqKeke3i145CEv9zfZ-2SWBJRCKX23RUZKn09zrRgTj8ontw_uzuj0cFH3gglGsIXcIbi7WDRTrMkA align="center")

So, again if we’ll check the status of the git using the command

`git status`

It’ll tell that the file “d.txt” has been deleted.

Now we’ll add the changes to the staging area. We’ll use the command `git add .`

Now, if we’ll list all the tracked files using the command `git ls-files`

Then the changes will be overridden to the staging area, i.e previously there were, two files “d.txt” & “e.txt”, but now there will be only one file i.e “e.txt”.