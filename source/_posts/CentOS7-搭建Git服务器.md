---
title: CentOS7 搭建Git服务器
date: 2017-09-17 17:03:00
tags:
---
# 安装Git
`yum -y install git`

# 查看Git版本
`git --version`
<!--More-->
# 创建Git目录和一个空的Git仓库
>cd /
>mkdir git
>cd git
>git init --bare test.git
>chown -R git:git test.git

>一个简单的Git服务器就搭建完成了

# Windows下运行git bash
>git clone git@ip:/git/test.git
>cd test
>git remote -v

