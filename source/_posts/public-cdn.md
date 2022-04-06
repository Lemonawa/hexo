---
title: 常用静态公共CDN评测
date: 2022-01-30 20:00:00
tags:

- CDN
- 评测

categories:
- 评测

---

静态公共CDN，几乎每一位站长都会使用，因为它不仅可以节省服务器的流量，同时还有助于提升访问速度。  
本文将以内容、速度、宕机率来测评。

<!-- more -->

# 1.Jsdelivr

推荐指数：⭐⭐⭐  
官网：[CDN加速站](https://cdn.jsdelivr.net) [主站](https://www.jsdelivr.com)  
内容：NPM（无registry），Github，Wordpress  
速度：国内慢，国外快到离谱（2021年12月20日，他们丢失了ICP许可证，如今走Cloudflare）

```
Unfortunately today jsDelivr unexpectedly lost its ICP license in China. 
As effect the Quantil CDN disabled our account.
From now on all Chinese traffic will be served by "near China" locations 
provided by global CDN providers.
```

IT狗测速如下：
![](https://i0.hdslb.com/bfs/album/5331fb9acc1f451a5c7a98f5b3b54eb3c2b9242f.png)

# 2.Cdnjs

推荐指数：⭐⭐⭐  
官网：[CDN加速站](https://cdnjs.cloudflare.com) [主站](https://cdnjs.com)  
内容：Cdnjs
速度：国内慢，国外快到离谱  
测速：  
![](https://i0.hdslb.com/bfs/album/5331fb9acc1f451a5c7a98f5b3b54eb3c2b9242f.png)  
~~同一张图，因为都走cloudflare~~

# 3.Staticfile

推荐指数：⭐⭐⭐⭐⭐
官网：[CDN加速站](https://cdn.staticfile.org/) [主站](https://staticfile.org/)  
内容：Cdnjs+国内开发者贡献库
速度：快到离谱  
测速：  
![](https://i0.hdslb.com/bfs/album/a5fd5fa61af3e4246ba99b90cea9dfd952c274af.png)

# 4.Bootcdn

推荐指数：⭐⭐  
官网：[CDN加速站](https://cdn.bootcdn.net/) [主站](https://bootcdn.cn/)  
内容：Cdnjs+国内开发者贡献库
速度：国内快到离谱，海外慢（国内多节点）  
测速：  
![](https://i0.hdslb.com/bfs/album/97fd70385bea1c50455e6dac1908819826642a37.png)

# 5.75CDN

推荐指数：⭐⭐⭐⭐  
官网：[CDN加速站](https://lib.baomitu.com/) [主站](https://cdn.baomitu.com/)  
内容：Cdnjs  
速度：快到离谱  
测速：  
![](https://i0.hdslb.com/bfs/album/a5fd5fa61af3e4246ba99b90cea9dfd952c274af.png)

# 等等，宕机率呢？

除了Bootcdn，其他好像都不错  
可以在[此处](https://uptime.lemonawa.xyz)自行查看