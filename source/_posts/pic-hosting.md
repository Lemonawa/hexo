---
title: 各类主流图床评测
date: 2022-04-05 01:39:28
tags:
- 评测
- 图床
categories: 
- 评测
---

### 开端

在写博客的时候，我们通常都要给自己的文章插入图片

而图片通常会托管于某个图床(或公共api)上

本文将对主流的几个图床进行测试

### 评测

#### 1. sm.ms图床

官网： https://sm.ms

这是一个老牌图床了，使用CloudFlare进行CDN加速

Itdog测试：

![](https://i0.hdslb.com/bfs/album/7657b5efd90f682508c5a55c660529c59a29bbd3.png)

测试地址：

https://s2.loli.net/2022/04/05/Ae6swOFVzgMr8ij.png

#### 2. GitHub 图床

使用GitHub作为存储位置，使用Fastly进行加速

**注意：移动已墙**

Itdog测试：

![](https://i0.hdslb.com/bfs/album/8915d5f686de8195991139d90ff235b819acd22c.png)

测试地址：

https://raw.githubusercontent.com/Lemonawa/pic-hosting/main/97b97ee1173042d5ba667df7ecbe43f6.png

#### 3. GitHub + JsDelivr

官网：https://jsdelivr.com

GitHub存储，JsDelivrCDN加速(Cloudflare+Fastly)

**注意：违反ToS**

Itdog测试：

![](https://i0.hdslb.com/bfs/album/61b1ea1a5a031fd213b8269ca5615187c08ef497.png)

测试地址：

https://cdn.jsdelivr.net/gh/Lemonawa/pic-hosting@main/97b97ee1173042d5ba667df7ecbe43f6.png

#### 4. Bilibili图床

B站御用，国内外大量节点

我自己目前也在使用

![](https://i0.hdslb.com/bfs/album/78d4b13f13c8229df2f42a024affce944bf7dc6b.png)

测试地址：

https://i0.hdslb.com/bfs/album/f7def05bfa96d26b40ace918cff4ea4ef9aad9b5.png
