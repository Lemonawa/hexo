---
title: 使用GPG密钥验证Github的提交
date: 2022-03-20 23:00:29
tags: 
 - 教程
 - Github
 - 密钥
 - GPG
categories:
 - 教程
---
在Github浏览Commits时，我们应该经常可以看见一个绿色标记：Verified(已验证)  
![](https://i0.hdslb.com/bfs/album/1cf0577a84afcf4bc8ec5e98cb4c6cd65214663b.png)  
那么，如何拥有这样的标记呢？
### GPG简介
（摘自维基百科）

>GNU Privacy Guard（GnuPG或GPG）是一个密码学软件，用于加密、签名通信内容及管理非对称密码学的密钥。GnuPG是自由软件，遵循IETF订定的OpenPGP技术标准设计，并与PGP保持兼容。

简单的说，就是用于加密的密钥。  
众所周知，Git的提交只需要自己的邮箱和密码，这就出现了一个漏洞：  
只要他人有你的用户名和邮箱，就可以进行提交，就可以更改你的仓库内容。  
一个典型的案例：https://spencerwoo.com/blog/wait-this-is-not-my-commit
### 具体操作
1. 电脑上安装好Git
没有安装的可以在此处下载：https://repo.huaweicloud.com/git-for-windows/
2. 打开Git Bash，输入
```
$ gpg --full-generate-key
```
在第一处，选择RSA  
在第二处，选择4096bits
在第三处，选择过期时间，回车为永不过期  
在用户ID处，填写自己的Github用户名  
在签名邮箱处，填写Github上绑定的邮箱  
最后，为密钥设置一个密码，也可以不设置，如果设置了则一定要记住这个密码  
这样，就成功生成了一对GPG密钥  
3. 运行
```
$ gpg --list-secret-keys --keyid-format LONG
```
来查看我们当前拥有的所有GPG密钥：
```
Lemonawa@Inspiron-3670 MINGW64 ~/hexo
$ gpg --list-secret-keys --keyid-format LONG
/c/Users/Lemonawa/.gnupg/pubring.kbx
------------------------------------
sec   rsa3072/FB8FA623E7013D41 2022-03-17 [SC]
      0722D31772F81E20A945BDD0FB8FA623E7013D41
uid                 [ultimate] Lemonawa <lemonawa1209@gmail.com>
ssb   rsa3072/34F49A369E312009 2022-03-17 [E]
```
其中，sec一行的`FB8FA623E7013D41`即为GPG私钥ID
4. 运行
```
$ git config --global user.signingkey FB8FA623E7013D41(此处替换为你自己的私钥ID)
$ git config --global commit.gpgsign true
```
此后的每一次提交，Git都会用其进行签名
5. 运行
```
$ gpg --armor --export FB8FA623E7013D41
```
来导出自己的GPG公钥，类似这样：
```
-----BEGIN PGP PUBLIC KEY BLOCK-----
dasSJDsiiiaF......
-----END PGP PUBLIC KEY BLOCK-----
```
将这一段粘贴到https://github.com/settings/keys 的GPG keys处，随后进行一次提交，即可看见自己的commit上有了Verified的绿色标签
### End.