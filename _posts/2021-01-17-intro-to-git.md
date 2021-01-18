---
layout: post
title:  "Beginner's Guide to Git"
date:   2021-01-17 12:07:19
tags: ['git', 'beginner']
categories: [beginner-friendly, git]
comments: true
---

Git is a very powerful tool, and should be included in every system admin's toolbox, whether you are new to scripting, or new to the IT industry, it is a powerful tool to get started with. By the end of this post, you should have your very own repo setup and ready to use!

<!--more-->

## Table of contents
* [Basics](#basics)
    * [File Management](#file-management)
        * [Adding Files](#adding-files)
        * [Removing Files](#removing-files)
    * [Remote Repository](#remote-repository)
        * [Push to Repo](#push-to-repo)

<a name="basics" />
# Basics

<a name="file-management" />
## File Management

<a name="adding-files" />
### Adding Files

There are several ways to add changed files, this is considered staging them.

Adding a single file
```bash
git add filename.sh
```

Adding a directory
```bash
git add directory/
```

Add everything from current directory (including nested directories)
```bash
git add .
```

Add everything
```bash
git add --all
# or
git add -A
```

Check whether files would be added or ignored, but don't actually add anything
```bash
git add . --dry-run

# or
git add . -n
```

<a name="removing-files" />
### Removing Files

When working from within a git repository, it is best to use git to manage deleting files.

```bash
git rm filename.txt

# instead of
rm filename.txt
```

However, if you did delete a file using rm, but the file was already pushed to git repo, you can remove the file manually

```bash
git add -A
```
<a name="remote-repository" />
## Remote Repository


<a name="push-to-repo" />
### Push to a Remote Repo

In order to push to a remote repository, you must first create one.

Github and Gitlab offer free private/public remote repositories.

Let's assume your new repo is https://github.com/awesome_user/amazing_repo.git

You can now stage your changes, commit them, and finally push them to this repo.
