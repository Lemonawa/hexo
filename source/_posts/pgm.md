---
title: Telegram 人形自走机器人 PagerMaid-Modify安装教程
date: 2022-03-15 00:11:18
tags: 
 - Telegram
 - 教程
categories:
 - 教程
---
### 前言
在Telegram中，我们有时能看见聊天的人们做出一些神奇的操作：  
![](https://i0.hdslb.com/bfs/album/54c4917b1de5723fc05d1b57f39a5f40459cef51.png)  
这种操作可以通过使用`PagerMaid-Modify`来实现  
### 简介
（摘自官方repo）  
```
Pagermaid 是一个用在 Telegram 的实用工具。  
它通过响应账号通过其他客户端发出的命令来自动执行一系列任务。
```
你需要一台位于海外的服务器来完成部署操作
### 操作步骤
一、用SSH连接工具连接上你的服务器  
二、运行以下命令：（本次以`Ubuntu 20.04 LTS`作为示范，其他系统可相应替换）
```Shell
apt-get update
apt-get install git imagemagick libzbar-dev neofetch tesseract-ocr tesseract-ocr-eng tesseract-ocr-chi-sim redis-server python3-pip -y
git clone https://gitlab.com/Xtao-Labs/pagermaid-modify.git pagermaid && cd pagermaid
pip3 install -r requirements.txt
cp config.gen.yml config.yml
```
三、访问[https://my.telegram.org/apps](https://my.telegram.org/apps)，使用注册Telegram的手机号码登录  
填写你的应用名称、URL等（可以随便填写），随后单击Create application创建应用  
有时可能会出现错误提示，请换用美国节点重试  
完成后复制`App api_id`和`App api_hash`  
四、使用`vi config.yml`命令编辑配置文件，将上面复制的`App api_id`和`App api_hash`粘贴进对应位置，注意引号  
五、运行`python3 -m pagermaid`，根据提示依次输入手机号、验证码和二次验证密码  
当看到`PagerMaid-Modify 已启动`字样时，在任何聊天输入`-help`测试运行状态  
不出意外的话，你应该可以看见自己的`-help`已经被替换成命令列表了  
此时按下`Ctrl+C`终止运行  
六、运行
```Shell
cat <<'TEXT' > /etc/systemd/system/pagermaid.service
[Unit]
Description=PagerMaid-Modify telegram utility daemon
After=network.target
[Install]
WantedBy=multi-user.target
[Service]
Type=simple
WorkingDirectory=/root/pagermaid
ExecStart=/usr/bin/python3 -m pagermaid
Restart=always
TEXT
```
来设置守护进程  
> `WorkingDirectory`请按自己实际环境配置，一般应为`/root/pagermaid`   

此时运行
```Shell
systemctl start pagermaid
```
来启动程序，运行
```Shell
systemctl status pagermaid
```
来检查运行状态，检查完成按`q`退出界面  
再运行
```Shell
systemctl enable pagermaid
```
来设置为开机自启  
现在，你可以在聊天中使用`-help`获取使用帮助了  
安装过程结束