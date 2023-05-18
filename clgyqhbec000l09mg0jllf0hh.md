---
title: "11. Git Aliases - Simplifying Commands"
seoTitle: "Streamline Git Commands with Aliases"
seoDescription: "Make your Git workflow more efficient with custom Git aliases. Learn how to simplify Git commands and save time with this easy-to-follow guide."
datePublished: Thu Apr 27 2023 06:18:11 GMT+0000 (Coordinated Universal Time)
cuid: clgyqhbec000l09mg0jllf0hh
slug: 11-git-aliases-simplifying-commands
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682503642766/cb9818c7-def5-44bc-bdef-683fc52e7907.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1682576181846/78356533-2b76-4a65-b2cc-464f649bc3b8.jpeg
tags: github, version-control, git, devops, devops-tools

---

# Introduction

In Git, an alias is a custom command or a shortcut that you can create to make your Git workflow more efficient. You can create an alias for any Git command or a sequence of commands, as well as for other shell commands.

**Alias** - Nickname or Alternative Name

If we are using any lengthy git command multiple times and get bored, so we can use an Alternative Name for that command and use it in the place of that lengthy command.

Example:

Instead of using the full command `git log --oneline` we can use `git one` at our convenience. If we use `git one` then the command `git log --oneline` will be executed.

Git Alias compresses big commands (ideally) or any command if that matters.

So, to create Alias for the Git command certain steps are there:

First, check whether the Alias Name has been already taken/used/ available or not.

# Confirm Alias Name

We can test the Alias Name by just typing the command  
`git <Alias Name>` In the terminal, and if it is telling "Alias Name is not a git command" then we can use the Alias Name for the particular Git command.

So, in our case, we’ll check for the Alias Name "one". We’’ just type `git <Alias Name>` in the terminal.

In our case, the command will be `git one`

It’ll display " 'one' is not a git command. See 'git --help' ". So, we can use the Alias Name "one" for the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682494439217/5409ed5e-9fb7-4bd6-bc83-0786eae06379.png align="center")

Create a Workspace "project7", and create 3 files in it using the command `touch`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682494648419/023c0813-99d0-493b-a0bf-dc2bd31ded3f.png align="center")

Now, add the files one by one in the **Staging Area** and commit the changes/files in the **Local Repository**.

For this, we'll use the command:

`git add <file name>; git commit -m "message"`

Example:

`git add a.txt; git commit -m "a.txt added"`

`git add b.txt; git commit -m "b.txt added"`

`git add c.txt; git commit -m "c.txt added"`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682494891209/826729d2-aa5d-420b-a291-11bf03720fbc.png align="center")

Now, check the log using `--online` option with Git. We'll see Multiple commits (three) are available in the Local Repository.

Using the command `git log --oneline`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682495089811/0868b33c-80d9-4656-ba74-7012bfc160dd.png align="center")

# Create Alias Name

* Original command: `git log --oneline`
    
* Alias name: `one`
    

So, we can define the Alias Name by using the command `git config` We’ll use the Syntax:

`git config --global alias.<alias_name> "original command"`

`--global`: For all the repositories, i.e. set the Alias Name Globally.

**Note**: Whenever specifying the original command we should not use git along with that.

In our case, the command will be:

`git config --global`[`alias.one`](http://alias.one)`"log --oneline"`

* original command: `log --oneline`
    
* aliasname: `one`
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682495630210/66e17efb-f5f0-4369-8889-31e99be925c1.png align="center")

To confirm it, we’ll use the Alias name along with the utility git i.e.  
`git one`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682495742920/6489e7b6-aa2f-444c-ac2c-0378683ead72.png align="center")

We’ll get the same result as when we were using the command `git log --oneline`

# Common Errors

## Using Linux Command As Alias Name

We have to confirm that the Alias Name that we are going to use is not an OS-based command.

Every Git command should be executed by using git only.

Example:

If we want to set the alias name `ss` for the command git status.

And use the command `git config --global alias.ss "git status"`

Original command: `git status`

aliasname: `ss`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682497106637/64a36396-4960-4a07-8be8-90ab941d18bb.png align="center")

It’ll not throw any errors. But when we try to execute the command using the Alias name then it’ll not show the correct output (Based on our choice).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682497222057/08814be8-e287-40b9-aa74-bc6f17b15f75.png align="center")

`ss`: ss is the socket statistics command in Linux.

Sometimes it may throw an error "Command not found".

## Placing "Git" In Place Of Orginal Command

Whenever specifying the original command we should not use **git** along with that.

Example:

If we choose `git status` as the original name, then we'll get an error.

* aliasname: `kk`
    
* original command: `git status`
    

Firstly, we’ll check for the Alias Name "kk" is a command or not. For that, we’ll just type the aliasname in the terminal.

In our case, the aliasname is `kk`

It’ll display "Command not found"

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682498648319/10fc6d36-9de0-48f3-97b1-2c54bbe56df7.png align="center")

So, we can use it as aliasname.

Now, We’ll use the command: `git config --global alias.kk "git status"`

# Remove Git Alias Commands

If we want, we can remove the commands created using Git Alias.

To remove the commands created using Git Alias, we'll follow certain steps:

## List All Aliases Created In Git

Firstly, we'll list all the aliases we created in Git. To list all the alias in Git we'll use the command `git config --get-regexp alias`

This will show us a list of all the aliases we have defined in Git, along with their corresponding commands.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682571397462/95a78468-1e10-486c-a5a1-02831fabb367.png align="center")

## Delete Created Alias

Now, we'll Identify the alias we want to delete from the list.

Once we have identified the alias, we'll use the `git config --unset` command followed by the name of the alias we want to delete.

For example, if we want to delete an alias named "lo", we'll enter the command `git config --global --unset alias.lo`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682572453745/0a270b86-3275-4f4c-a5a4-b95a6383bc7d.png align="center")

This will remove the "lo" alias from our Git configuration.

Now, we'll verify that the alias has been deleted by running the command `git config --get-regexp alias` again. The deleted alias should no longer appear in the list.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682572827899/9327b4c2-c9c8-407f-9e57-574f3e689eec.png align="center")