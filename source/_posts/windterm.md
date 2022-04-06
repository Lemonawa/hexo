---

title: Windterm：用于DevOps的一个更快更好的SSH/Telnet/Serial/Shell/Sftp客户端.
date: 2022-03-21 00:33:42
tags: 

- 终端
- SSH
- Sftp

---

### 简介

用于DevOps的一个更快更好的SSH/Telnet/Serial/Shell/Sftp客户端  
项目地址：https://github.com/kingToolbox/WindTerm (部分开源)  
屏幕截图：(部分来源于原作者存储库处)
![](https://i0.hdslb.com/bfs/album/c59d5f8f270a2fe3fbdd539cad5236817e1dc3b7.png)  
![](https://i0.hdslb.com/bfs/album/d552838bd18ecb633f6a90914f214f9e7f5458c4.png)  
![](https://i0.hdslb.com/bfs/album/baff806dc52276f98985385be5e5746e8236f1af.png)  

### 特性(翻译自原作者存储库处)

#### SSH, Telnet, Tcp, Shell, Serial

- 实现了SSH v2、Telnet、Raw Tcp、Serial、Shell协议。[介绍视频](https://kingtoolbox.github.io/2020/01/22/new-session/)
- 支持SSH在会话认证时自动执行。
- 支持SSH ControlMaster。
- 支持SSH ProxyCommand或ProxyJump。[介绍视频](https://kingtoolbox.github.io/2021/03/11/proxycommand/)
- 支持SSH代理转发。[介绍视频](https://kingtoolbox.github.io/2020/08/22/ssh_agent_forwarding/)
- 支持SSH自动登录，包括密码、公钥、键盘交互式、gssapi-with-mic。[介绍视频](https://kingtoolbox.github.io/2020/01/23/auto-login/)
- 支持X11转发。[介绍视频](https://kingtoolbox.github.io/2020/07/21/x11_forwarding/)
- 支持直接/本地端口转发，反向/远程端口转发和动态端口转发。[介绍视频](https://kingtoolbox.github.io/2020/07/21/port_forwarding/)
- 支持XModem、YModem和ZModem。[介绍视频](https://kingtoolbox.github.io/tags/modem/)
- 集成sftp、scp客户端，支持下载、上传、删除、重命名、新建文件/目录等。[介绍视频](https://kingtoolbox.github.io/tags/transfer/)
- 集成了本地文件管理器，支持移动到、复制到、复制自、删除、重命名、创建新文件/目录等功能。
- 支持Windows Cmd、PowerShell和Cmd、PowerShell作为管理员。
- 支持Linux bash, zsh, powershell core等。
- 支持MacOS bash, zsh, powershell core等。
  
  #### GUI
- **支持Windows、MacOS和Linux.**。
- **支持多语言用户界面。
- 支持Unicode 13。
- 会话对话框和会话树。
- **聚焦模式。** [介绍视频](https://kingtoolbox.github.io/2021/06/28/ui_focus_mode/)
- **同步输入。** [介绍视频](https://kingtoolbox.github.io/2021/05/27/sync-input/)
- **加强了对会话用户名和密码的保护。** [介绍视频](https://kingtoolbox.github.io/2021/03/11/protection-username-password/)
- **命令调色板.** [介绍视频](https://kingtoolbox.github.io/tags/command-palette/)
- **命令发送器.** [介绍视频](https://kingtoolbox.github.io/tags/sender/)
- **探索者窗格.** [介绍视频](https://kingtoolbox.github.io/2021/05/27/explorer/)
- **Shell Pane.**
- **快速栏.** [介绍视频](https://kingtoolbox.github.io/2020/08/22/quickbar/)
- **粘贴对话框.** [介绍视频](https://kingtoolbox.github.io/2020/08/22/paste_dialog/)
- **本地和远程模式与vim键的绑定。(使用Shift+Enter键在远程和本地模式之间切换**) [介绍视频](https://kingtoolbox.github.io/2020/06/21/keyboard-modes/)
- 支持时间戳、折叠、勾勒、分割视图。
- **支持Linux和PowerShell中的powerline，例如Oh-My-Zsh，Oh-My-Posh。** [介绍图片](https://github.com/kingToolbox/WindTerm#screenshots)
- 支持像vscode那样的颜色方案。[介绍视频](https://kingtoolbox.github.io/2020/01/23/highlight/)
- 支持搜索和预览。[介绍视频](https://kingtoolbox.github.io/2020/01/22/search-and-mark/)
- 支持突出显示开头和结尾的分隔符，如（）、[]、{}和自定义的分隔符。[介绍视频](https://kingtoolbox.github.io/2020/06/28/pair/)
- 支持改变用户界面主题。[介绍视频](https://kingtoolbox.github.io/2020/09/18/theme/)
- 支持设置标签的颜色。[介绍视频](https://kingtoolbox.github.io/2020/09/18/tabbar-change-tabcolor/)
- 支持搜索打开的标签。[介绍视频](https://kingtoolbox.github.io/2021/03/11/tabbar-search-tab/)
- 支持向右关闭标签。
- 支持设置窗口的透明度。[介绍视频](https://kingtoolbox.github.io/2020/11/13/windows-opacity/)
- 支持从选择到复制，从右键到粘贴或从中间键到粘贴。
- 支持用Google、Bing、Github、Stackoverflow、Wikipedia和DuckDuckGo在线搜索文本。[介绍视频](https://kingtoolbox.github.io/2020/11/13/search-online/)
- 支持打字时隐藏鼠标光标。
- **支持锁定屏幕。** [介绍视频](https://kingtoolbox.github.io/2021/04/23/lock-screen/)
  
  #### Term
- 支持 vt100, vt220, vt340, vt420, vt520, xterm, xterm-256-colors.
- 支持unicode, emojis, true-color, mouse protocol等。
- 支持自动换行模式。[介绍视频](https://kingtoolbox.github.io/2020/01/22/auto-wrap/)
- 协议和术语可以自定义。
- 除Tektronix 4014外，所有vttest测试都已通过。
  
  #### Session
- **支持HTTP和SOCKS5代理。** [介绍视频](https://kingtoolbox.github.io/2021/03/11/proxy-http-socks5/)
- **支持跳跃服务器代理。** [介绍视频](https://kingtoolbox.github.io/2021/03/11/proxy-jump-server/)
- 支持手动和自动会话记录。[介绍视频](https://kingtoolbox.github.io/tags/logging/)
- 重命名和复制会话。[介绍性视频](https://kingtoolbox.github.io/tags/tabbar/)
- 重新启动时恢复最后的会话和布局。[介绍视频](https://kingtoolbox.github.io/2020/01/22/restore-sessions/)
- 支持在启动时打开一个特定的会话或一组会话。
  
  #### Pefomance
- 高性能、低内存、低延时。[介绍视频](https://kingtoolbox.github.io/2020/01/23/windterm-putty-performance/)
  
  ### 下载地址
  
  https://github.com/kingToolbox/WindTerm/releases  
  请自备翻译器