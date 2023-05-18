---
title: "8. Understanding Git Logs: The Complete Postmortem Of git log command"
seoTitle: "Mastering git log command: The Complete Postmortem Analysis"
seoDescription: "Discover how to effectively use Git logs to analyze changes in your codebase. Learn the ins and outs of Git log postmortem analysis with a detailed guide."
datePublished: Tue Apr 18 2023 07:10:11 GMT+0000 (Coordinated Universal Time)
cuid: clglxdivo000409kye88h4sya
slug: 8-understanding-git-logs-the-complete-postmortem-of-git-log-command
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681800637261/9609e1df-e7f3-4c82-b407-34872ba5d175.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1681801698224/d5d14927-b7bf-4b3b-9511-38dd9225c6a1.jpeg
tags: github, version-control, git, devops, devops-tools

---

# Introduction

"git log" is a command used in the Git version control system to display a detailed list of all the commits that have been made to a repository. It is a very useful tool for anyone who wants to keep track of the changes made to a codebase over time.

This command is used to display the **History** of all the **Commits** in the **Local Repository**.

It is the most **commonly** used command.

It’ll provide complete/detailed information on the log of all the **Commits**.

* **40** Character alphanumeric **Commit ID**.
    
* **Author** and his / her mail id.
    
* **Timestamp**
    
* **Commit message**
    

### **Example**

Create a directory named "project3"; And create 3 files "a.txt", "b.txt" & "c.txt" in that directory.

Now, Go to the **Workspace** “project3” and check the number of files. Use the command `ls` for that. It’ll display the 3 files: “a.txt”, “b.txt” and “c.txt”.

![](https://lh5.googleusercontent.com/oaeQC_xtXN68GxN1NWZkDPwLNSwfrGqZXAD-JoU-EjCOPK8c6KZI78t8p6zveu_yyY6CueADmDu2j7c7i1ss0NbocpgsAJvZMMlh1_DYxJf7tXXFhvny3-xrECeCPQVtCqldoL9K8uqNazLtTD7tKA align="center")

Now, initialize the workspace using the command `git init`

![](https://lh6.googleusercontent.com/JfRRJU5BaXLMwSAicuMoj6rNlmXE-zlHQ1jgLwoQV0KK3IFYBQA_c9321csj9NrjoJHyyB-Yav6tertxohHDwOEiLXQWqVGVNDoPrfZ9Al_nkU0UY1g2GS2vSLIU6TbXWCTHvsDDZ_sD1Iwm8wCr align="center")

After that, we'll add all three files in the Staging Area using the command `git add .`

Then, check which files are being **tracked** by GIT. For that, we can use the command `git ls-files`. All three files are being tracked by the GIT.

![](https://lh3.googleusercontent.com/aUh8L4RHsQcnBrGIOnVOSyY9he4POFY58dgbeHHUBY8C6jUWKAxiJ5OmJyJjeHoAg-E8xuqUtuXdhrSU97pjAWgQU0FYGf9zDW2Yffpx22e2N_ZI_d_uHdaLznltsY2xai9xKkLzc10Y845xMDJStA align="center")

Now, create a new file "d.txt" in that **Workspace** "project3" and write something in that file.

![](https://lh5.googleusercontent.com/XkY_IE2A-krI-kPymVeeIG0pzoQInzBbRlHr4QcuKf3QngCyWRM6TNsLiLhPjfPljFWUhUEXKo2v33MYjemX_nr9nbD2YwSck9HQ--vWoICYjbWg25jBbUW6leZgpGSL3V8K0Rd4n8_550Afoddf7g align="center")

Now the new file "d.txt" will be present in the **Workspace** “project3”. Use the command `ls` to verify that.

![](https://lh6.googleusercontent.com/FY0e2d2uwOU5qh-BbuiVixry0CfVR68fEcy4-qRzmss6o45A13zZ27_lUR9ouzVJRvv2GsUpQt5Bujgo8M6hYh0uPaDf3mbSlsJ40Q6djmBJoqmhovKxdtZIA5700PVMXFSrgmUR3NpamuVLWdUk5w align="center")

But it’ll not be **tracked** by GIT. To verify that we can use the command

`git ls-files`

![](https://lh6.googleusercontent.com/XOw07UdF6FhDE99jlT5XHhp_w7wGlo8Kaq4QLqchoCf9ydJXtIIRshdVBohnrb-N02Ye9hBRuzArZSvIVpWhBiCrbTKu7g4cQIGpT-Cvi819Jh-oxssdkN4yVrR3h9lJb_u9MEWOMaiZNMI3jz7NsA align="center")

The file "d.txt" is not present there in the tracking list (Staging Area).

To confirm that the file "d.txt" is still untracked, we’ll check the status of the GIT. For that, we can use the command `git status`

![](https://lh5.googleusercontent.com/dbgapIBrbaW911CpKW_cvbbUo1NdIISElJYbT7F2FKLtz5GAV407rOtTsjVAG-yHzWyol9306knQdLaPvuSGadf0haIhXMXzcFjgrIHj72HerLG0w2kw8OcNPVCWh8M3d39WGg-mQGK_n0vbMmbjJA align="center")

It’ll display that the file "d.txt" is not being tracked by GIT.

Now, we’ll add the newly created file “d.txt” to the **Staging Area**. For that, we can use the command `git add <filename>`.

In our case, it'll be `git add d.txt`

![](https://lh6.googleusercontent.com/4L3z4GcUNhm2lyqyWEWnpQQ4uRiHHsAfqJe8ssKzMevadV_EHWliWBd92_EC5gc7AGC-KHYt57p51ko4iMVnbwR-SAvt_4eZxiWvqMKt2HCepi6SDKGI5elS0hgV2L5F2TBA_GxyOToEhJTm9cxBSw align="center")

Now, the file “d.txt” will be added to the **Staging Area**.

Now, check again which files are being **tracked** by GIT. For that, we can use the command `git ls-files`. Now, this time all four files (“a.txt”, “b.txt”, “c.txt” and “d.txt”.) are being tracked by the GIT as we have added the file “d.txt” to the **Staging Area**.

![](https://lh4.googleusercontent.com/EVBPx921oduxTTTEcUOE25o9NtcAvA6C0bKLJE2vF5zMhxI8gBdVo2AgRxtyZ4WFTlTUSRuSemyJGnFCfktL0xeLUkWl7bsHSzLtRdaSLgs4WcJ3muCB1lgrY_diPyfl2VvH_iJASbMQVqJ2D3R3Hg align="center")

Now, we’ll **Commit** the changes to the **Local Repository**. For that, we can use the command `git commit -m "Commit message"`. So, now all the changes will be committed.

![](https://lh6.googleusercontent.com/FDk-SuxJcGbJdfWjXGDArapoRoCKMTvKpyPLPLi4qevJ3F9WtmRG_Sz-CPF3Om9Dvc4FbXhNPEIaWkZZP1w8yFVeNGddGqsuXLcbvOeE6Rz-7iGwlxSGXVfjfu_TDC8Fy2-YKu_TPuBTQ-KfzK_Cog align="center")

Now, we’ll check the status of GIT again. For that, we can use the command `git status`. It’ll tell: Nothing is there to **Commit**, everything on the **Working Tree** is clean. Everything is being **tracked** by GIT.

![](https://lh6.googleusercontent.com/7vvJupOnOmldYMwkCtEoUlVNRW7S0dzKiiAGiNEVmFHrHOVysaXUoVqa-mTaICyAT-PmwaCa_eKllZV4izc00iZtgaz4Cw7VnnDxbSqs0Gld91p8SOrsMTF6Uzy98iREcx_x0ppjFhmg-iJo1MBs_Q align="center")

Now, we’ll check all the **Commits** or want to check the history of all the **Commits**. For that, we can use the command `git log`

So, there are 4 commits present in the **log**.

![](https://lh4.googleusercontent.com/YGFPqneYCsayIeaG9_4XHlG10J-dU1GpUCvrFm_vd-VHAq2rGz4ogStmVwCxbTioj1PLdzeKnfr5pAvteQmzSGe6jZK3978aQ85XbUOKsewiCcT1I18X5HOXiHvk4hHuK_pGIhKL5hcFQ1A6JR4CFw align="center")

**Note**: I've committed the file a.txt and c.txt before (In the previous Article [Mastering Git: Getting Started- Part 2 (](https://itachiuchiha.hashnode.dev/getting-started-with-git-part-2)[hashnode.dev](http://hashnode.dev)[)](https://itachiuchiha.hashnode.dev/getting-started-with-git-part-2))

If we want the **Specific Information,** not the **Complete / Detailed Information** so, for that there are various **options** available. To check that we’ll use the command `git log --help`. It’ll display various options available for the `git log`.

![](https://lh3.googleusercontent.com/j0yGyfrCmEq0iVGqkKj9ggZ6QlQxuOp3Acbq4Vg0g9T0g6qO3dFfubNUBDSbST4rtc5qu0TSmxnAfsOoVLDDSyk57DrhTRzOQGipVNNyi5ItjF_g4w7Ampz_Gfvzrbffv74R50sa6VDHx0Qi6_3ASQ align="center")

![](https://lh4.googleusercontent.com/dbuT9hPwehG1v1c-7-H2ui4Kdo23zaoByWkGxIiQ-jUaAW7cOIRa4532zGxTadzHNS-nljMqsZlUDs1aLHYE1DuURJDmzJTheDorov9oUnvGe83hRBmXeB9pQLySgIiweoiesgB_tfmDqNG3CjQ2xA align="center")

# Display Log Information Of A Particular File

* The Commands, `git log` and `git log .` both are the same i.e to display the **Complete/Detailed Information** of the **Commits**.
    
* So, if we want the log of a particular file then we’ll put the file name in the place of the **dot** (**.**).
    

Syntax

`git log <filename>`

In the **Workspace**, if we want to see the **Log Information** related to the file “a.txt” then we’ll put the filename (a.txt) in the place of the **dot** (**.**), in the command `git log .`

The command will be `git log a.txt`

![](https://lh5.googleusercontent.com/WSqGfCtyKSrT4nmL_t_wlSxTFQzb35DPRQOMlZs8erSikN3b031cqccw5cmibpUyxoZX0qXKZYJaVFLKkhUznPFYQwQ8TMnFy2xdr26NTiAByLA9Nkpt149oHR8Td-9Ls1csFR9z0d8ZWAhMj0j4Mw align="center")

Now, we’ll see only two commits in place of 4 commits. First, commit (Lower) is associated with both “a.txt” and “b.txt”. And the second commit (Upper) is associated with only "a.txt"

Now, if we want to see the **Log Information** related to the file “d.txt” then we’ll put the filename (d.txt) in the place of the **dot** (**.**), in the command `git log .`

The command will be `git log d.txt`

![](https://lh5.googleusercontent.com/oD093BTiiIzywIAdiKGVRd0V43r_aWsCx4aHXFcmXkLrdvzI5n216Zx0zadb4AxvHCGuaYXsumyb7zItMmcMuLk9YpuAEHa0dPybZbX7YB7hHLqu_QL9ITiQX4SfWuMpgxilQOFfe82f4V6iWKlObg align="center")

Now, we’ll see only one commit in place of 4 commits. It’ll be associated with only “d.txt”.

# Display The Brief / Concise Log Information

To get concise **Information** of all the commits, we’ll use the option `--oneline` along with the command `git log`

So, the command will be `git log --oneline`

This command will show all the commit Information in **one line per Commit**, as for commit there are multiple lines displayed when we use the command `git log`.

And in the one-line information, we’ll see the information:

* **Commit ID** and
    
* **Commit message**
    

![](https://lh3.googleusercontent.com/QciU6etSbDNh6LvyPZVuPbQqarD2zb1oeIjl1v1U08Bi9C7roqDen5XtjeNAkZU8DoMSH5-OfcbzpoOLbcRPQxZhGGw-OG5st7Sod_fRsUeqTGou98CbsAuEEKoPd5XVj-l4tclU82DRivXpYD46QQ align="center")

**Note:** When we use the command `git log --oneline` and want to check the **Commit ID** then, it’ll show only the **first 7 Characters**.

The GIT is following the order:  **Latest** (Upper) **to Oldest** (Lowest).

The **Commit Id** will be the same if we Move the file from **Local Repository** to the **Remote Repository**.

# Display The Particular Number Of The Latest Commits

If we want to see the Particular Number Of The Latest Commits i.e     2 out of 5 commits, then we can use the option `-n` along with the command `git log`

Syntax

`git log -n <number of the latest commit to be displayed>`

This command will limit the number of **Commits** to display.

### Example 1

If we want to see the **2 latest Commits** to be displayed then we can use the command `git log -n 2`

It’ll display 2 out of 4 commits that are present in the **Local Repository**.

![](https://lh5.googleusercontent.com/pivAssgK120wxykeAe0PpNL80C6MgoKchW9x8qu-zYRbRDR9ZibeaIqhdvXNsW45FMM_Wm-XeubkhcSo9fnAUpz8GrYobLkf-ytoOY9wYoEruJ478oo-LXx_YKvaB4PRKUmj_2f28GePVWg3rbx0HA align="center")

### **Example 2**

If we want to see the **latest Commits** not in **Detailed Information**, but in concise **Information**, then we can use both options **\-n** (Used First) and the `--oneline` (Used Second) along with the command `git log`

Syntax

`git log -n <number of the latest commit to be displayed> --online`

It’ll display the **n latest Commits** out of **m** number of commits that are present in the **Local Repository** and share concise **Information**.

In our case, if we want to see the two latest commits, then the command will be `git log -n 2 --oneline`

![](https://lh6.googleusercontent.com/5cWvPVb2GooDiQf7ppj8x2Dco-b3Mwla2rf7OHNalTkZWitzGo5UgA5LP3WYi9kSYYAx05OIJcFbaNBIELJGNFnAPR5T1nldMvkB6oSBYiRPhiCp7oqjmPpolpuKQZ3CAYexpRuXmilCbdYc_bKUzw align="center")

If we want we can remove the option **\-n** from the command `git log -n <number of the latest commit to being displayed>` Instead we can use

`git log -<number of the latest commit to being displayed>`

If we want to see the **2 latest Commits** to be displayed then we can use the command `git log -2`

It’ll display 2 out of 4 commits that are present in the **Local Repository**.

![](https://lh4.googleusercontent.com/gzDeS1yoOBcfU6Se_0d7KE20QkO7Ptr7vueqIeHZBD-5t3AEnCLwnYRJ-qB_pfm2r1TJgwCcP9_ha68-orhk7-qMW5iaQuEn9sGl-DSHnYDrtfnfE_1SzphzpsCbKPbA5x4QtVhm3bv1TlNIWGMRLA align="center")

Just like before we can remove the option **\-n** while displaying the **Concise Information**. We can use the command

`git log -<number of the latest commit to being displayed> --online`

I

t’ll also display the **n latest Commits** out of **m** number of commits that are present in the **Local Repository** and share concise **Information**.

In our case, if we want to see the two latest commits, then the command will be `git log -2 --oneline`

![](https://lh3.googleusercontent.com/9GtCe2icKwKHhqPdf8Du97Gby3ZpfQV11eldjJSZia9jNovQup2HE__VKVJzEnxNYcqrZb9CdAP2yLN8x7FZILZry0cBw7q_wQp5d7nOirbGh42YlvowrUKkaQoY7sOTOGjSdXWmy2U0Y1Snz0lEHQ align="center")

### Example 3

We can use the option `--max-count` along with the command `git log`

`git log --max-count=<number of the latest commit to be displayed>`

This command will also limit the number of **Commits** to display.

If we want to see the **2 latest Commits** to be displayed then we can use the command `git log --max-count=2`

It’ll display 2 out of 4 commits that are present in the **Local Repository**.

In our case, if we want to see the two latest commits, then the command will be `git log --max-count=2`

![](https://lh4.googleusercontent.com/pmTgp842fDk0812syF4ew-sv3lKqeVrLiSifCah9Tzh_fo0WHMBQFv_Q2EPtm8V42d9FSec47X4UW3l0xIFHW0pCbKOJ2czKNE3WsJEVozQCvvFBjsAnfSpw8EzhTOW0AWUfRubMaP7PNDBZ4_F8-Q align="center")

### Example 4

If we want to see the **latest Commits** not in **Detailed Information**, but in concise **Information**, then we can use both the option `--max-count`(Used First) and the `--oneline` (Used Second) along with the command `git log`

`git log --max-count=<number of latest commit to display> --online`

In our case, if we want to see the two latest commits, then the command will be `git log --max-count=2 --oneline`

![](https://lh3.googleusercontent.com/8F93UzOQWW8rLLQw-lrnub2Pwoq1EI58rji7iHlkACscyizdYRL9uo0aoc9YhQZbcZhErDZADWji1VON9QpaOzcjKbdSWQZwxxMQEF3E849jOyBihvwR8ISa3PA-bmckSqo86Ol2fG-QQAFTCdnqTg align="center")

It’ll display the **n latest Commits** out of **m** number of commits that are present in the **Local Repository** and share concise **Information**.

So, the commands:

* `git log -n <number of the latest commit to be displayed>`
    
* `git log -<number of the latest commit to be displayed>`
    
* `git log --max-count=<number of the latest commit to display>`
    

All three commands are the same

# Display Commits Based On The Commit Message

If there is a project in which too many **changes/Commits** are made, few of them are to solve a particular issue. Example: "Issue in Service Request 123".

And we have also put the **Commit Message** related to that particular issue. So, if new developers start working on the Issue in Service Request 123, then they don’t have to go through the whole **Commits**.

Instead, they can search/filter the **Commits** based on the Issue in Service Request 123 using the **String** in the **Commit Message**.

**Example**

If we have **Changed/Modified/Added** something in the Service Request Add a line in the Service Request 123, then we’ll put a **meaningful/Structured Message** for that while Committing and essentially use the term "**Service Request 123**", so the developer will use that string to display/filter the whole commits based on the Service Request 123.

For this, the developer / we can use the option `--grep` along with the command `git log`.

We can use the command `git log --grep=Pattern/String`

The **Pattern** need not be a single word, it can be a regular expression also.

## Case 1: Display The Commits Based On The String

### Example 1:

If we have to display the commits based on the string “a.txt” then we’ll use the command `git log --grep=String`

In our case, it’ll be `git log --grep=a.txt`

It’ll display all the Commits based on the string “a.txt”.

![](https://lh4.googleusercontent.com/tRHq9WgHS20T_9qAWy0UmUYRBO-ttEHpesKjQfr7c2lzSQyqNaMLIWk2iDtHibQjlRd4115Q3pxXFiFUrefR39dCmun68PgQvqfDLZPjYI5Btwf7n3bISa9YPqZPBNzTM3p0YVIyBM52Ysuh4gO7Jg align="center")

### Example 2:

If we have to display the commits based on the string “added” then we’ll use the command `git log --grep=String`

In our case, it’ll be `git log --grep=added`

It’ll display all the Commits based on the string “added”.

![](https://lh3.googleusercontent.com/4V00lYHHFp6vjM-DPRouBjxwmIsW7A7_8DghIa3aDaATmW2j8iV0MZ35OKtJTsX3bHrc8z3lXe6o7D7ao0xk-6sII2mowogKRecKvVGzzRd1ZBc75b12LmR2nVeyLN-7ayM4EebnJGfnfMg9HvNMfQ align="center")

### Example 3:

We can use both the option `--grep` and `--oneline` together with the command `git log` to filter/display the **Commits** based on the particular **string / Patterns** and give Concise **Information**/**In Oneline** about the **Commit**.

Syntax

`git log --grep=String --oneline`

In our case, it’ll be `git log --grep=added --oneline`

![](https://lh3.googleusercontent.com/jPU42nRQomTRVIWcL-KSPHMmnvMM8A_lstAKYWxvfTMHLN_3c59DUk-JrjZ-ctkWP6MM4nKiaFwTZMMRTipzhu4Nk3HTZYZCHReEzSpvzj2dwuWWhWZ2jMZt6Mx7X0F4ArbQQxxM6cnk93EKOEmYGQ align="center")

# Display Commits Based On The Specific Date / Time

If we want to filter the Commit based on the specific Date / Time, then we have to use the option `--since` or `--after` along with the command **git log**. It will exclude the commit that happened on that date.

Syntax

`git log --since=Date<>`

Example

If we want to display/filter the commits, since/after 5<sup>th</sup> May 2021 then we can use the command `git log --since=2021-5-07`

![](https://lh3.googleusercontent.com/m0-2S88vory45jx3JlkUlqz1PPy11M3Iez3g5i_uzYGqWfayw-tJhf-O-VsiU-Oz0bch-KIh0criv2g39aZe0n33ehGt9QMaNzvQUb4Aw6dJ7saM0Tg6bvA41Cn7Pf7qPXbQkWnUMDH8EkcBHk2etg align="center")

We can even display the commits via **days**. For this, we can use the option `--after` along with the command `git log`. We can use the command `git log --after="n days ago"`

Single or double quotes are not mandatory.

Example:

If we want to display the 1 day ago then we can type the command `git log --after="1 days ago"`

# Display Commits Based On The Author

If we want to display/display the Commits based on the **Author Name**, then we can use the option `--author=Name/Pattern` along with the command `git log`. It’ll filter the **Commits** based on the **Author Name** who has committed in the **Local Repository / Remote Repository** then we can use the command `git log --author=Name/Pattern`

**Example**

If we want to display all the commits made by the author "abhishekkishor" then we can use the command

`git log --author=abhishekkishor`

![](https://lh4.googleusercontent.com/t7nMBiYL1axVw-uIwLSmEmaVxrmsB-WGJ32d7uua81dmZxoX9IRNL5O8XEe4k-9BCOb9EsKHTXPo1g4LXhr8H--NCnsrJ2yy_NKDui5R-L18hCKo33vgMJcVp-I_DFGR2eoiPzGGyRejXdCJh6HKAA align="center")

We can also use Concise **Information** which is the Information in One line as well. We can use both the options `--author` and `--oneline` together along with the command `git log`.

We can use the command `git log --author=Name/Pattern --oneline`

**Example:**

If we want to display all the commits as Concise Information made by the author “abhishekkishor” then we can use the command

`git log --author=abhishekkishor`

![](https://lh3.googleusercontent.com/v_-A7ZSBzCM2rHrdLXb3rq4kmaiBEhk9k_eV9k0XkOqrBDdWCg2tUIw04iqU0Y51yQ0B-berUIEcBfBbGFhrzom2uygc_6CWHoKoMTDg_8Qa4vWVYpo3gdsbpBk9WGzsxNUmpFN9-_OaGj3N-RZUsA align="center")

To display the commit messages along with the commit information in the `git log` output, we can use the `--pretty=oneline` option. This will display each commit on a single line, along with its full commit hash and commit message.

`git log --pretty=oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681798801656/1f73c11e-99bb-4c79-90ec-35b4ddfd6896.png align="center")

To display the commit history in a graphical format, you can use the `--graph` option. This will display the commit history in a graph-like structure, with each commit represented by a node and its branches represented by lines.

`git log --graph`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681798955866/546a6c09-6e75-4868-a411-21700ad07de5.png align="center")