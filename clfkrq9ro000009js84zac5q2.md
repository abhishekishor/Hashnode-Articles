---
title: "1. Version Control system"
seoTitle: "Version Control System: In An Easy Way"
seoDescription: "If you're new to version control systems, this article will give you a basic idea of version control systems and its importance."
datePublished: Thu Mar 23 2023 07:04:39 GMT+0000 (Coordinated Universal Time)
cuid: clfkrq9ro000009js84zac5q2
slug: 1-version-control-system
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679554363161/e3758fc0-58e7-45e9-bb77-ccd9565fd82c.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679554573487/453d2d21-8e29-4d8b-b66b-72159b310be8.jpeg
tags: github, version-control, git, devops, devops-articles

---

# Version Control System Tool

Version Control System is also known as **Software Configuration Management (SCM)** or **Source Code Management (SCM)**. But the **Version Control System** and **Software Configuration Management** (SCM) are the more meaningful words.

## Need For Version Control System

Assume there is a developer, and his/her job is to write codes. And the codes will always be maintained in the form of files. It can be “.java” files or “.py” files.

### **Scenario 1:**

Now, assume that a client came along with the requirement and asked to develop the project. So, I agreed to that and started developing the code for the project.

Process:

I’ll create one folder for the client and name it “Client Project”.

![](https://lh5.googleusercontent.com/v6Vyutf9oe8XBqeqkvShZsz0-6SxHsuHdIyqfWW3HFj8NTW_lEGyYVux_2bzFEsrWTLqFHpGT6v2Z1oI7vp8RCLtZ8W54f1udHV2O11Q9PR1bSnIrx1HE52SB1vh1g9sNfgUa6tGuZEP5XTIpGfa align="center")

I wrote 100 files that contain code to fulfil his/her requirements.

![](https://lh4.googleusercontent.com/JJfPyVr6xfIJ9Zh5Ss8XTvVOgBR2aNnRI8gs93rECtsYGwF2-xpylrp_06rdMAC8Uy72SlTF1TZM7Rm5T-taXscD6JUrD7lZK0r-YQzWJ2YAnZVguWDi-Owkp48ojP69T7uCTJgM-srTNVseC1D7 align="center")

After the development, I went to the client for the Demo. And the client suggested some changes be made to the project.

I changed some file source codes to meet the client's requirements. “Ch” referred to the changed files.

![](https://lh6.googleusercontent.com/cTrQmr9J1JvLy74OksZGZyKQqKc5ZzyYapHEV7OHW8Nvf1yOX5mqmcsgTsd430oX95o8q5nEqdJXuH1kb-VsZOHJQquc50-Uy8w4RU6-ykqDPGhtZAu4r91xdGe8MkexJuMW0z4Qf1_Q8gENynAd align="center")

After the development again I went to the client for the Demo. And the client again suggested some changes be made to the project.

Again I changed some more file source code to meet the client's requirements. “Ch” (brown) refers to the changed files.

![](https://lh5.googleusercontent.com/zFF_rFWd7jgfARN5qD5YO8WqqBHg0HlGp24cdoRCrcCPOCiBYPl9oKkN9bMx9Qax4UrqfMV0WNqV1Y_LCmaBLoO-NRrIMKwyjhoe6fs5OjvWKRniRkusjItpf0CJBUBRDHc3vAjsdXtl1SkXceYD align="center")

After the development again I went to the client for the Demo for the 3rd time. Now, this time he asked us to show the demo that I showed for the first time.

Now, the problem is I have performed the changes in that same file in the same folder. So, I don't have that 1st demo code with me. I have to recollect all the things that I had done for that demo. And that’s very complicated.

So, we have to maintain every version of the code.

Now, what if 100 developers are there working on the same project?

So, now each person is required to maintain multiple versions of the code and that’s too complicated (manually maintaining each version (multiple versions) of the code).

Also, every change should be tracked i.e who did the changes, when he/she did the changes and most important which lines he/she has changed.

### **Scenario 2:**

Assume two developers “Dev A” & “Dev B” are working on the same project.

![](https://lh4.googleusercontent.com/Vq9AyD4ZykvqUxPbEP8wthjvR0cG09ceyIijAPNLmNv3a7WFGuykJWhJO79icxKNU4avJ_UVN3KDSJ9z2to8gNnUm_KfjJB-rOkAYwoCl0Xgo40xGVsPvP8Iwv4LAy1zNDtNw7aDtc_MqMjd2FkC align="center")

Now, as part of the development both the developers developed a file “[util.java](http://util.java)” (common generic technologies).

![](https://lh6.googleusercontent.com/fjLPF7lnYtszymQQ7LT3pQrDqAjUufE-1NOpajB85mzcSK3TuGu7yDAqG68XK-OXkq1g4MHp51sPMz4D3xQCW5Uj0zGmTUJ7f8l8OknhlTD7GD18TYPbpt3x842cRlJ387vwYrGZVA7G2VIYZ6O- align="center")

Now, if they plan to integrate that code and want to deliver it to the client. Then definitely one file will override the other at the time of integration; which may show abnormal behavior in the project.

So, we want both the files to be there which are having the changes in the project. So, some mechanism should be required to do it.

And that mechanism is the **Version Control System (VCS)** to maintain the different versions.

### **Scenario 3:**

1. Assume there is a bigger project and multiple developers are working on it.
    

![](https://lh6.googleusercontent.com/uRjVd_Q6VVZgyz0lceu-WXuQixUcISgdYJ0QPwrbtn2du9AkadXDM4_fSTPvqOg78SJv-AI0Ii1TnPfXvJ1etya5zhzBM_-obXptSy5JWgHTmZGjAM02rg-5SPH3IFztU2kKrqv7cmUigy1J3f4K align="center")

Now, the code developed by “Dev A” has to be shared with the remaining developers. In the same way, the code developed by “Dev B” has to be shared with the remaining developers. All developers working on the same project require to share the code with each other.

So, to share the code with the peer developer, there must be some mechanism.

And that mechanism is nothing but the **Version Control System (VCS).**

* Each and every change should be tracked i.e who did the changes, when he/she did the changes and most important which lines he/she has changed.
    
* Overwriting of the code should not happen.
    
* So, developers have to share the code with the peer developer, so that multiple developers work collaboratively.
    
* Parallel development must be required.
    

So, to follow the above things there must be some mechanism required. So, such a type of source code management system is known as the **Version Control System (VCS).**

# Where Version Control System Needed

Version Control System always talks about files as the source code is kept in the form of the files.

**Note:** Wherever multiple versions of the same file are required to maintain then we require to go for the **Version Control System**. So, for any document it is applicable.

Example:

* If a tester is writing some test script, and multiple versions of the same script are required to maintain so the Version Control System is required.
    

* If an Architect is there and he develops some documents, therefore multiple versions of the documents must be required.
    

* If a project manager is there and he is working on the Excel sheet, therefore multiple versions of the same excel must be required.
    

## How Version Control System Works:

Let’s assume that one directory (working directory/workspace) has been created where I'm going to develop all my files.

![](https://lh3.googleusercontent.com/C3ZPuXGvMJ3q1rYPewHfcdhz18FfBgsGIus9pjpnCCeCjz9hcx1F9XKDWuUfr8EU-3wQDPKhlnRpCj2E9Pkw-oe2ieUxPE3oy7PCFfNz4ev9VO6m8pvR1F9zjc3UEEPrH0PHxAcnvRFUv4lZIHvk align="center")

Assume that I developed three files “[A.java](http://A.java)”, “[B.java](http://B.java)” and “[C.java](http://C.java)”.

![](https://lh4.googleusercontent.com/WgFxetNOn_2FPHEzv2qf1C_4FCpAyl1jXG1pN9vf-QEJaURfBr91Ya7udWTgjKnkuDEUn43371xbJONbie2TFaNurKVFB2s4TvON7qwOAwrIwHlxFzHc8fh_GpBjxC6hDKaXber9cBUXcWh-e5Rk align="center")

So, for this thing the version control system is not applicable.

If you want the version control system, something must be required, that thing is considered a “**Repository**”.

## Difference between “Working directory/workspace” and “Repository”

* In a repository, a version control system is applicable. In the Working directory/workspace version control system is not applicable.
    

* But both store files (a group of files) only.
    

* The repository is under the Version Control System, but the Working directory/workspace is not under the Version Control System.
    

* So, the Working directory/workspace is what the developer is working on currently.
    

* **Working directory**: Where developers are required to create/modify files.
    

**Repository**: Where we have to store files and metadata.

The repository is a directory into which all the commits will be stored.

If we have a repository then only we have the Version Control system.

Now, if I have to show the demo to the client, and before going for the demo I save/send all the files in a repository. But for that, I'll require some client version control system like Git, SVN, CVS etc to send the files to the repository.

* So, now if I have to show the demo to the client, I'll save the 3 files that I had changed before in the **Repository**. And to send the files to the Repository, we’ll need a client program for Version Control System
    

![](https://lh5.googleusercontent.com/TTLHQfhP_VewOKkomB35W5bUTFwM4LWHTVqE54R2IoGH8pQBqEqmegj2WNhZnqgcRSvAZzSvexAxDtguUI5XFo9aOZFkm5BGHfW6Cixzx75HUhQsSwbx2M3aE4Kb4n4XLz3_osPpDOJYCC1lDklA align="center")

Here in the repository, those files will be stored in the form of **Commit**. And for every **commit**, a separate unique **commit id** will be generated which will represent the particular version.

**Commit:** The process of sending files from the working directory to the repository is considered as **Commit**. Every commit is associated with a unique id (Hash) which is a **commit id**.

Commit is just one ID or commit object which contains the state of the particular time interval. **It’s not a directory**. Commit objects internally contain the files.

Commit is a verb at the same time it’s a noun. This means it is a process at the same time it is the thing that is going to hold.

![](https://lh3.googleusercontent.com/MoEsSjjA-m7q7hzSpby2-dItiuU3b8TkDhlTWVJNYKHoenpi8qIZd2R6UPnAkmLusb-C6sB05r1lbMbps-HNrD0AEmlKj9QZ7pXjzsoDsVpO2EzZ35OpBaFZhw4SoH8ob5xh9lH7DAoFnXvRvdCW align="center")

The client suggested some changes be made. So, in order to meet the client’s requirement, I made some changes in the files “[A.java](http://A.java)” and “[C.java](http://C.java)”.

Now, again before going for the demo I saved/sent all the files in the repository. As I made the changes in the two files only, therefore I’ll commit only those changes (Modified files) in the repository. The remaining other files will be considered from the previous version.

![](https://lh3.googleusercontent.com/vPsO6A6_qrVsRK5XoIAwJtzPrgmWR84DXwi-AFtt-DZMY5D6aLpt4zXHCDhnaqbbSpMCFH9pZFjNtrc_SNMVdCSys-Ri4Lbd6Mput3jhIa-JG0oBRzqSMnBs3YmxppJXS_egt88N5SNZrKF2ETbG align="center")

* In every commit ID, complete information is there example:
    

* When does that particular **commit** happen?
    

* Who did that change?
    

* What changes did he/she make?
    

* What is the mail ID?
    

* Which files are there? etc
    

The client suggested some changes be made. So, in order to meet the client’s requirement, I made some changes in the file “[B.java](http://B.java)”.

Now, again before going for the demo I saved/sent all the files in the repository. As I made the changes in one file only ([B.java](http://B.java)), therefore I’ll commit only those changes (Modified file) in the repository. The remaining other files will be considered from the previous version.

![](https://lh3.googleusercontent.com/jc7g8j8VfkqVBD12QYq3KCklDoiLvCq28vMgE9vB3GQmaVwuUlVt0P5oJgJ3SpAtMIDSZWoc2zs-bzOzbr1iWM35b50cLqu2KeDYqvHEjOpm07GBTrFcYUPjPIlUPRKIfnN9uxP8wDGlKpNmo30S align="center")

After the development again I went to the client for the Demo for the 4th time. Now, this time he asked me to show the demo that I showed for the first time.

So, now we can take the files that we had committed/saved for the first time. Now, this time I have to bring the files from the repository to my current working directory. Then, that will override the files with the specified version files.

The process of sending files from the repository to the working directory is considered **Checkout**.

After that, I'll show him the demo that I had shown him for the first time.

# Benefits of Version Control System

1. We can maintain different versions and we can choose any version based on the client’s requirements.
    

1. With every version / commit we can maintain metadata like Commit and commit message. Who made the changes? When did he/she make the changes? What changes does he/she make? So, complete extra information will be maintained with every version/commit.
    

* It provides an environment to share the code with the other / peer developer in a very easy way.
    

* Multiple developers can work collaboratively.
    

* Parallel development is enabled.
    

* We can provide Access Control like Who can read the code? Who can modify the code?