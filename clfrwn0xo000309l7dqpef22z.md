---
title: "2. Types Of Version Control System"
seoTitle: "Mastering Git: Types of Version Control"
seoDescription: "Learn about the different types of Version control systems and discover about - centralized, decentralized, and distributed - in depth the Git article."
datePublished: Tue Mar 28 2023 06:56:29 GMT+0000 (Coordinated Universal Time)
cuid: clfrwn0xo000309l7dqpef22z
slug: 2-types-of-version-control-system
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679984764218/cf99c538-b2af-4219-a5c9-f92590061ac3.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679985370324/35a39eb4-bc5d-4b52-be78-c38e88a77ebf.jpeg
tags: github, version-control, git, devops, decentralized-version-control

---

All Version Control Systems are divided into two types.

* Centralized Version Control System
    
* Decentralized / Distributed Version Control System
    

# Centralized Version Control System

This type of Version Control System contains only **one repository**. Working directories may have multiple files, but there will be only one central repository and every developer is required to connect with that to continue his / her work.

Let's assume we have a central repository server.

![](https://lh4.googleusercontent.com/0txHYDMYRyL0WcphdNdSQNDyzJvl8kpP8Pvsy5-dXCSrh9eETM8N0a-oEFqxY2YbioJUozsKjCfTpez0uURTwuECENytd1n9GibELLA0iXgaxpkvxMt5DEJ0llayBLjHnUc4fZrBo7VDmp-FR-iBoA align="center")

In the Central Repository, the data will be stored in the form of versions. So, assume multiple versions are there in the central repository.

![](https://lh5.googleusercontent.com/5nl5GpmbQThqwdiYkXiU3ZusbduUkg9gqd9OqYDGflV5hUVfnJ50WZyU_ObUYvqhKvD39m85N0-i8AzSA10HSUewR7TWG6Mc8oG4hB1TpZjiXdP2hlwG9KhR4RLc9n06BPvZQIgJS-4erXB76rwZ3w align="center")

Now, assume that there are multiple developers. And every developer is required to connect with the Central Repository to continue the work.

![](https://lh3.googleusercontent.com/fw4sTNqhdRKCwMrgkr3ZY8zqBqJpQpsAMgk0W_GB1XQnnzsgDU-NoUrbU6A43w9el_P8bWJXVQsqIzYa1NVgx3gn9k_D49Zhfa96ep8L87C2WH9h9f3UMH29wHgGavy4B3tl7lMfvWwjbeXZRmEu-w align="center")

Now, in the Developer’s workspace whatever files the developer requires, he’ll get that version from the central repository and then he will work on the project.

Assume that there are several files available in the Developer’s workspace. That is whatever he /she is going to provide to the central repository or whatever he /she is going to get from the central repository.

![](https://lh3.googleusercontent.com/qMkcriIAGuoQoEgaOqdCp2L68Kmc2U2ZRdqZQC6NGA8IQxXR0ftFM6dUnjA3zBSG3MVqIyb2xJJdFr4RBXzjdVvNTr5lmKvtXX58n0yhM61AfrpUMAi-8EHpg_8kKfu5gTjtUd2hDBbichZ4s9AF9w align="center")

If a developer is required to work, he’ll connect to the central repository and will get the required files and then he’ll start working on those files.

![](https://lh4.googleusercontent.com/EOuIpFOAk8sa5czoUmFw2JcbVkcvLU7fhiDjlsG980EongHcOpuHL-TbF3PJafPc8CfKf63iko00WsEDI77iwowaOvuFV_Mihu251lNp4J4Yf5VYU_3YyDTM-09YpHOvsTx9ios6mIPNmHyMRScd6g align="center")

The developer will get the files in two ways:

1. He may create new files/files.
    
2. He’ll get / checkout from the repository.
    

After completing the total work i.e changes in the code, he/she has to commit that work to the central repository.

![](https://lh4.googleusercontent.com/eis2Vap1mcsfCoyvZij_cfkr8O89nehkY26VKOwOiqTM8QHb2YAKnp2E4ev-RXdXq-LMmG7muceqmhmw2TwoUUivW9hrkrxrcl4OcXh_r8pmNlzHwTj-GVnZqoTuwzAJV-cYTbpFuh8bJfqPKBJcCQ align="center")

Developers submit / checkout those files only in which he/she is making changes. But all the files will be present in the central repository.

The same goes for multiple developers working on the same project, so every time they are required to communicate with the central repository, then they will get / checkout some files and after completing the work they’ll commit the changes to the central repository. As version control is happening in only one place that’s why this model is considered the **Centralized Version System**.

![](https://lh5.googleusercontent.com/3gIlCZWEAy0dDgzlK-tXC0rky6vJq6UVNNiRd_Dzhp3MwTi-juVk15rVjkKopnBoX3OY9SXlddY_uZPnHh4w1TpWqEogfZjl7mR8sj_G250-dNqRw-a4pdc4DwVDTb1KQ9ZDp9GmA8azwctwCE7sGQ align="left")

* The total project code will be stored in the central repository.
    
* All operations will be performed on the central repository but not in the developer’s workspace (It contains only dummy working files).
    
* It is very easy to set up and easy to use.
    

Centralized version control system tools:

* CVS
    
* SVN
    
* Perforce
    
* ClearCase
    
* TFS etc.
    

## Limitations Of The Centralized Version Control System

1. The total code/files are stored at a single place (Central Repository), So if something happens to the Central repository server, then the recovery is very difficult which causes a **Single Point Of Failure**.
    
2. If developer “A” wants to perform the checkout operation, then he/she has to connect with the Central Repository Server (Remote Repository Server) and then get the files.
    
    So, the checkout operation happens over the network by connecting with the remote server, and then he wants to commit the changes. So, the commit operation will be performed on Central Repository Server. So, all the developers should be always connected to the central repository. So, if the network outage (Cutdown) will happen then the Version Control won’t be available for the developers as they’ll not be able to communicate with the Central Repository until the network availability.
    
3. As for every operation we have to connect to the remote Central repository. It’s not a local operation, so it’s going to take time, which will affect the performance (It’ll be low).
    
4. If the number of developers increases or the number of files increases for Version Control, then the organization of the central repository is a bit difficult.
    

# Distributed Version Control System

In this type of Version Control System, the repository is distributed. If four developers are there then 4 repositories will be there.

## Distributed Version Control System Model

Assume that there is a developer’s working directory/workspace.

![](https://lh5.googleusercontent.com/N4JiohHiwGgAE9g5q29u3-WmNp06MNz86AzAzEUDI_nyx73-Xuq-rpWx6RjioYykeJpKx2wcLsK1f2e9QZJ6grFpADfSL_FTS1qqy_5y6v3oPpzaRIflLuGmg59huJSUyMOov-MdckP2L5dsstdAMw align="center")

In the previous model, the working directory/workspace contains only files, not versions. But in the Distributed Version Control System, every workspace has a **local repository**.

![](https://lh4.googleusercontent.com/rGfQj7apNbmSL2I0usrdEAIwXLEQ3-9hUoTiOdcawPt5WrnTUYzgyCBThEC-lsYdV3vn5DtD79KglZ5IYwz6DXxk55WqAbi9pjRN7mApoU1vWgBpQrs7abPQd1EQW2VDN9hen3dw79yKEa6nIUUhUA align="center")

So, if 10 developers are there then every developer will have their own local repository, and then there is no question of the centralized repository.

All the versions will be maintained in the local repository.

![](https://lh3.googleusercontent.com/KZpAl5snDHc3SNne7ivk-_1eJ5Wb0bbZ5H1pu_PO6i-ptqRBZoK07oeBIouy5vCetzUdE0QgR9Gq5L7i9FmQdIUnYzH8tpcufYu6-_eI_UFNb0SZbQxpOJLkez2FTwjC3p58beOgCd8YH_zdoi7Guw align="center")

In the working directory, he /she (the developer) is going to work with files.

![](https://lh5.googleusercontent.com/DMmi5HBxD40is94oxjgpjY_KHiBsTFB1uBhgheigaTokIWT7h5btrKXPW8Iwyr9YwCEp9fCNdegtP8XLjq5FaVg9Zn0_7d8bUF-UToEO62o2Rp5_HBkAEWe8EMrcjQVUrB278UdzrrEZJAvlYNj5Qg align="center")

Now the developer wants to perform the checkout operation. So, the checkout operation will be performed from the local repository. He /she is not required to connect with any remote central repository.

![](https://lh4.googleusercontent.com/iFywtO5RDO9S3CdT7xQ5wkkFo9KHIieGKKP5e3yJSKLwFf4j6kWzpAHAiTU-hrdDS3oLCCl6pSD_h7TTPWGjLI5aQ0kGIei1vKBLhrcqHqea2Az_zEBYg7T9dG6eiiedR8A3TrsXjHvCXffpyGT4qw align="center")

Now, he works on some files and wants to perform the Checkout operation. So, the commit operation will be performed from the local repository. He /she is not required to connect with any remote central repository.

![](https://lh4.googleusercontent.com/3FGSzM5bYgqspZJhTMBTdspe2VnvupvBkVV9eZbJtAADQxNQ5KTtlri-OB5NBFcSnVYuRCZ1VWn2qEx5Spo2O1mq-Ll_fURHd4ZinnmnjxndBDpTHL_gG37DZTUFBynr5laeLdHa5yQvs13IFwDnIA align="center")

## Advantages Of Distributed Version Control System

1. So, the biggest advantage is all the commits and the checkout operations will be performed locally and hence the performance will be more.  
    
2. Even with a network outage, the version control will be available, so the client machine/developer’s machine need not be connected always.
    
    Suppose if the remote repository is there, just for the sake of sharing, network issues must not be there.
    
3. Every developer has his / her own local repository (in the developer's machine), that’s why there will be no **Single Point Of Failure**.
    

**Q.** All the operations (Commit & Checkout) are happening within the same system only, so how do the developers work in a collaborative way means how will the developers share their work with the other developers?

**Ans:** So, here also all the developers can work collaboratively.

**How is that gonna happen?**

Let’s consider four developers working on the same project. 

Every developer has their own local copy of the files (project).

![](https://lh6.googleusercontent.com/DooeNw0VZCF6vZ-vTDf1rrJsujeEstSgM10RMZMOpgdQqYs3eIJfqs3fVbIKSr16kI3jjAiglwHT_Cy-OV5n3l28J2MXe_Mq-yUSD63BUazkcUJp65oe1Ni5EUhWvnEMDNa-lhjk-FTnZe4cd71SDQ align="center")

  
Now, if developer A wants to share his / her files with developer B. So, now he/she will push his / her repository to another developer’s (Developer B) repository.

This operation is considered the **Push** operation.

**Push**: The process of sending files from one repository to another repository is considered the **Push** operation.

So, if we want to send the changes of our repository to the other developer’s repository then we have to perform the **push** operation.

![](https://lh4.googleusercontent.com/Jprhd7i9LQLHTHU4uikThA7ZPbe2QiccJC2PDg1KrWis61PVAM5zqnfbA0HxQp53oRBvJ0-kjJ9JsXr5SeobI7AuyfXOyKUdn0adrGrdgNPEFQNwOvUTFOXp50Z3-RlcHTVjuCgTaahpUlb8MVaqng align="center")

  
So, whatever changes we’ll do in our repository will be **Merged** into the other developer’s repository.

  
And now, if Developer “D” wants the changes of developer “C”, so he/she now he’ll get them from developer C’s repository.

This operation is considered a Pull operation.

**Pull**: The process of getting files from another's repository to our repository is considered the **Pull** operation.

![](https://lh4.googleusercontent.com/K5ksRZ_hf1z94GRrExYiISBSaFf8MmP_qRiBgJJHyTErUHkLs9xEvnUJVLsQ2FHGiAiylTIHxwDW8-9w7y-p771n5v8M0iV-VFUqbkkrMpcXyV_ogP4aX8MF2VIg_R5f1b1yJ9dUIp98-RrJQoBRuA align="left")

Decentralized version control system tools:

* Git
    
* Mercurial
    
* Fossil
    

# Distributed Version Control System With Remote Repository

It’s not the mixed approach of the Centralized Version Control System and the Distributed Version Control System, It’s Distributed only.

Let’s assume there is a working space for Developer A. It’s having **Working** **Files**, **Versions** under the **Local repository**.

![](https://lh4.googleusercontent.com/ePKTHzu9waYNKL3dl97sjWSwEbdfE-hZ5eBpZQo9KF-bQbu-NG3ZfgO0bxUB6-MklALOXuKVxahBNY7QFbTUb1PtD-VCGVc4C1BF9eGdGftmo_bKBAXSD03lJTOHYSqPR25cC3mSHnawaz7YKXGDSQ align="center")

  
Let’s assume multiple (four) developers are there.

![](https://lh5.googleusercontent.com/eAp2tPSx3_60sxHqieJP1P1nxp44H2ta7z0LJO8mXjoPK1Nc232h5C9JLhXtZgYBJOxjuJ6k038SkGlXszV2USe51-nUjY-sy78lUmfBfjXKoRLJ83bmTIrBvYHyLoRuUQdJyo28phzMK5gu_Z7Yog align="center")

Now, here we’ll maintain one remote repository server.  

![](https://lh4.googleusercontent.com/gBJd9oHLbpQpF_KiB20VYQjperWvwwzaH7wxzNxUhjXUjFxV61fdq3PDzjjZWSYn5WHE4pif5DsVVx9iDEb82NKWfts8aalyRBcS-2W1VZbI_On-KD_3mNfIsdMG5Y5E8dc8C7BCoV-qJVN5e7ZBcA align="center")

And in the Remote repository, we’ll have multiple versions.

![](https://lh6.googleusercontent.com/5qZSQ9HbjN6c_ngkoi3yT5d4JgB9UP1p-LEVYJdKnfsVPeqMblCBwya1QqUlc8NOYQ0QRzzElDF8JElw5geEKJ-MUV24CKcaEP2Yze5r_97A8Udc991F5Icn2Z6NplrfwzK1Y8YnCwTDGJnp2gJsiQ align="center")

Now, suppose there is a new Developer i.e Developer A got assigned to work on the project. He does not have anything in his local machine.

![](https://lh5.googleusercontent.com/t3kBPfH7OHPHTOuh4Vit23q4q0lu5kb2q0lx27WS7Z71tEjvAxT_A_TRrdERp4tvBhN2sFGyhEIdmehAbujHKrhYhhCyulGAPHIo8HMevblboDv6_yxdo-QywX9-7aQFdR_0C2JrprtKeKk7QiP5NA align="center")

So, he’ll perform the **Pull operation** in order to bring the files from the remote repository to his workspace. We can use the word **Clone** if we are pulling the files from the remote repository for the first time.

![](https://lh5.googleusercontent.com/juXc6jqbYmJ3Y0XVgDBLF08ilTWtrEzA9bPjP5YQkKiMQhg3de81lMZNpzw3b68SKF2L-w2tYD1Hw4iXa4kUuxrzYivbJMtLVcGNQN0XSJiESbZAKcdClQZ-xkr9uUkIaeS9RVvEEsgl7Gg8_FuvIA align="center")

Now, the total repository will get to developer A’s workspace.

![](https://lh6.googleusercontent.com/Lmp7c2Si45YroM7seOGpaD855Ut8w7JkK2N8QUhV_PaFgJcqxiJxXH3smgydMAS67YzB7p4xEZfP-NZvQNV_UPxLu4LSrT8SD6vck2-iWN_9jA-3QDehq8_T_5DEdUdBgWqVsZydByHNRUp4edhJOA align="center")

Now, he can perform all the operations on his local machine (Commit & Checkout), and after performing all the changes in the files/codes he will perform a Push operation in order to share his code/changes with the other developers.

The same goes for other developers as well. If they want to get the latest version of the files/codes, then they will **Pull** the code from the remote repository and after performing all the changes in the files/codes they will perform a **Push** operation in order to share their code/changes with the other developers.

![](https://lh4.googleusercontent.com/tChc1AR-n-q3r19Brprmo5tNpfgKrN3dizJrMI2rAaaM2RZZjVgc5yoVaeKjJoSazZr6uPmV_VAYH3ehRO6eMs5NE83adtnKTpMqkj2q7zB-RQf0jyK0OLs9iUxgt9-TqZT3GHBbky3N8VN8nuMm2Q align="center")

Instead, there is a remote repository, then also we can’t use the word centralized version control system.

# Remote Repository Vs Centralized Repository

1. In the centralized repository, we are performing the **Commit** & **Checkout** operation on the centralized repository. But in the case of a remote repository in the Distributed Version Control system, we are performing the **Commit** & **Checkout** operation locally.
    
2. In the Centralized Version Control System, there is only one repository. But in the Distributed Version Control System, every developer has their own local repository.
    

* That’s why even adding the remote repository server it’s not the combination of a Centralized Version Control System & Distributed Version Control System.
    

**Q.** Now, if we are not performing any Commit & Checkout operation in the remote repository then what is the use of it?  

**Ans:** The main use of the remote repository is just to share the changes with the other peer developers.

**Q.** From where the final project is going to be delivered?

**Ans:** The final delivery of the project is going to be delivered from the remote repository. But we are never going to develop any code in the remote repository. All the code development and then **Commit** & **Checkout** operations are performed locally on the developer’s machine.

Just to merge (Get & Share the code/files) the local repository with the remote repository we are gonna use **Pull** & **Push** operations.

Remote Repository Server tools:

* Github
    
* Gitlab
    
* Bitbucket
    
* Cloud Platforms