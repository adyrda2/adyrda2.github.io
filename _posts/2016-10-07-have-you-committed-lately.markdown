---
layout: post
title: Have you committed lately?
date:   2016-10-07
categories: Git
location:
tags: git
---

As developers we’ve been taught to commit our work a lot and often, but sometimes that isn't the case. Here are a couple awesome git features that could help get your commits organized again.

#### Scenario 1: You haven't committed in a while. 

`git add --patch`

You can use this command to get diffs of your work in smaller patches, and by  pressing ‘y’ or ’n’ you can decide which of those snippets to stage. Once you get through all of the patches of code you want to add for your next commit, you can just commit as you normally would. Use the command over again as needed. 

#### Scenario 2: You have some unstaged changes that really should have gone into your last commit. 

Simply stage those changes and use the following command:

`git commit --amend`




Everything is easier when we commit as we go, but I find myself using these commands a lot and I hope you are able to find them useful.

#### Additional references: 

[`git add --patch`]("https://git-scm.com/docs/git-add")

[`git commit --amend`]("https://help.github.com/articles/changing-a-commit-message/")
