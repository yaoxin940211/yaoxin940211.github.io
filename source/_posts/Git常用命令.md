---
title: Git常用命令
date: 2019-03-14 21:45:51
tags: Git
categories: Git使用
---
<!-- toc -->

#Git常用命令
<!--More-->
## 分支操作
```
查看远程分支: git branch -r
查看本地分支: git branch
查看所有分支: git branch -a
删除本地分支: git branch -d <BranchName>
删除远程分支: 1. git branch -r -d origin/<BranchName>
             2. git push origin (空格):<BranchName>
             或 git push origin --delete <BranchName>
```
