---
title: 在Vercel部署umami网站统计
date: 2022-04-02 23:13:42
tags:
 - 教程
 - Vercel
categories: 
 - 教程
 - Vercel
---

![](https://i0.hdslb.com/bfs/album/b417c98fd5236e1ad605ad1ac14e6ba8bc5ce62b.png)

### 简介

> Umami 是一种简单、快速的网站分析替代品，可替代 Google Analytics。

### 准备

* 一个[GitHub](https://github.com)账号

* 一个[Vercel](https://vercel.com)账号（可直接由GitHub登录）

* 一个[supabase](https://app.supabase.io/)账号（可直接由GitHub登录）

### 部署

访问[umami的代码仓库](https://github.com/mikecao/umami)，将其Fork至自己的账户中

登录[supabase](https://app.supabase.io/)，单击`New Project`来新建一个数据库，根据提示设置数据库名称和密码

![](https://i0.hdslb.com/bfs/album/61afd24107353687f780c389338ef46013037d1b.png)

进入刚刚新建的Project，点击左边的SQL Editor（命令图标）- New query来新建查询，并将[此处](https://github.com/mikecao/umami/blob/master/sql/schema.postgresql.sql)的命令全部复制到框中，随后点击RUN，看见Success即可

![](https://i0.hdslb.com/bfs/album/92c485b86ef9fd70989be6526d5553055f37778b.png)

然后打开[Vercel](https://vercel.com/)，登录，点击`New Project`，在左侧选中Fork的项目，点击Environment Variables来设置环境变量：

![](https://i0.hdslb.com/bfs/album/014d6163604a1448ac1c845deb50d144abc49154.png)

`DATABASE_URL`: `postgresql://postgres:[YOUR-PASSWORD]@[Your-URI]:5432/postgres`（在supabase project-左侧设置-Database-Connection string-URI获得）

`HASH_SALT`: 随机英文字符串（滚键盘）

然后点击部署，部署完成后会给一个域名，点击即可进入

用户名：admin

默认密码：umami
