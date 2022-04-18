---
title: Hexo+github搭建自己的技术博客
date: 2017-09-13 01:27:51
updated: 2019-01-27 21:14:10
tags: [blog, hexo]
categories: Hexo使用教程
---
<!-- toc -->

# Hexo+github搭建自己的技术博客
<!--More-->

# 大致分以下几个步骤
1. 环境搭建（node.js、git环境、gitHub账户)
2. 安装和配置Hexo
3. 将Hexo与github page联系起来
4. 发表博文

## 环境搭建
- node.js安装

[node-downloads](https://nodejs.org/en/ "node官网")

>node -v

>npm -v

- git安装

[git-downloads](https://git-scm.com/downloads "GIT官网下载")

>git --version

- gitHub账户

注册完成以后，新建代码库， 命名为 yourname.github.io

## 安装Hexo

- 新建一个空文件夹，依次输入以下命令

	> npm install -g hexo-cli
	> hexo init(首次才需要)
	> npm install
	> npm install hexo-deployer-git --save

## 配置git个人信息
1. 设置git的username和email
	>git config --global user.name "yaoxin940211"
	>git config --global user.email "765076035@qq.com"

2. 生成密钥
	>ssh-keygen -t rsa -C "765076035@qq.com"

## 配置_config.yml
```
deploy:
  type: git
  repo: git@github.com:yaoxin940211/yaoxin940211.github.io.git
  branch: master
```

## 发布博文
>hexo new post "title" 或者 hexo n "title"

>hexo g //生成
> hexo d //部署

> hexo g -d //生成+部署

## 下载next主题
>git clone https://github.com/iissnan/hexo-theme-next themes/next