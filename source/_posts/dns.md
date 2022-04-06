---

title: 各大厂商公共DNS大全【持续更新】
date: 2022-03-21 23:26:11
tags:

- DNS
- Cloudflare
- Dnspod
- Tencent
- Aliyun

---

### 简介

(摘抄自维基百科)

> 域名系统（英语：Domain Name System，缩写：DNS）是互联网的一项服务。它作为将域名和IP地址相互映射的一个分布式数据库，能够使人更方便地访问互联网。

### 名词解释

此处仅展示**广义上**的概念，部分(如Cloudflare)有特殊解释的将会在后面说明  
DoH: DNS over HTTPS (基于HTTPS的DNS)  
DoT: DNS over TLS (基于TLS的DNS)
DNS64: 一种在不存在 AAAA 记录时从 A 记录合成 AAAA 记录的机制，用于支持纯IPv6网络

### DNS

#### 大陆

##### Dnspod

Dnspod目前为腾讯所有，海内外的连通性都不错  
IPv4: `119.29.29.29`  
IPv6: `2402:4e00::`  
DoH: `https://doh.pub/dns-query`
DoH(IP): `https://1.12.12.12/dns-query`, `https://120.53.53.53/dns-query`  
DoH(国密SM2): `https://sm2.doh.pub/dns-query`  
DoT: `dot.pub`  
DoT(IP): `1.12.12.12`, `120.53.53.53`  

##### Alidns

阿里巴巴提供的DNS服务，国内连通性好，国外连通性差  
IPv4: `223.5.5.5`, `223.6.6.6`  
IPv6: `2400:3200::1`, `2400:3200:baba::1`  
DoH: `https://dns.alidns.com/dns-query`  
DoT: `dns.alidns.com`

##### 114DNS

老牌，国外一般
IPv4: `114.114.114.114`, `114.114.115.115`

##### CNNIC DNS

中国互联网信息中心提供，国外连通性差
IPv4: `1.2.4.8`, `210.2.4.8`  
IPv6: `2001:dc7:1000::1`

##### Baidu DNS

百度提供，海外一般  
IPv4: `180.76.76.76`  
IPv6: `2400:da00::6666`

##### 360 DNS

国内单节点  
IPv4(电信+铁通+移动): `101.226.4.6`, `218.30.118.6`  
IPv4(联通): `123.125.81.6`, `140.207.198.6`  
DoH: `https://doh.360.cn`  
DoT: `dot.360.cn`

#### 海外

**此处列出的DoT服务大部分无法使用**

##### Google Public DNS

老牌，国内连通性还可以，国外连通性极好  
IPv4: `8.8.8.8`, `8.8.4.4`  
IPv6: `2001:4860:4860::8888`, `2001:4860:4860::8844`  
DoH: `https://dns.google/dns-query`  
DoT: `dns.google`  
DNS64: `2001:4860:4860::6464`, `2001:4860:4860::64`  
DoH(DNS64): `https://dns64.dns.google/dns-query`  
DoT(DNS64): `dns64.dns.google`

##### Cloudflare 1.1.1.1

国外连通性天花板，大陆连通性一般，移动友好  
IPv4: `1.1.1.1`, `1.0.0.1`  
IPv6: `2606:4700:4700::1111`, `2606:4700:4700::1001`  
DoH: `https://cloudflare-dns.com/dns-query`  
DoT: `1dot1dot1dot1.cloudflare-dns.com`, `one.one.one.one`  
DNS64: `2606:4700:4700::64`, `2606:4700:4700::6400`  

##### Quad9 DNS

IBM，国外不错  
IPv4: `9.9.9.9`, `149.112.112.112`  
IPv6: `2620:fe::fe`, `2620:fe::9`  
DoH: `https://dns.quad9.net/dns-query`  
DoT: `dns.quad9.net`  

##### OpenDNS

Cisco提供，老牌，国外不错  
IPv4: `208.67.222.222`, `208.67.220.220`, `208.67.222.220`, `208.67.220.222`  
IPv6: `2620:119:35::35`, `2620:119:53::53`  
DoH: `https://doh.opendns.com/dns-query`  

##### Neustar UltraDNS

Neustar提供，有国内节点，移动会被丢到国外  
IPv4: `64.6.64.6`, `64.6.65.6`  
IPv6: `2620:74:1b::1:1`, `2620:74:1c::2:2`  

### More...

有更多的DNS服务器推荐吗？  
欢迎到 https://lemonawa.xyz/about 页面中的`Contact me`联系我添加~