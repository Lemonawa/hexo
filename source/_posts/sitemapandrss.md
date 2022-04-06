---

title: 为Hexo添加RSS订阅页面和站点地图
date: 2022-03-21 01:17:52
tags:

- RSS
- Sitemap
- 站点地图
- 教程
  
categories: 
- 教程
  
  

---

### RSS订阅插件安装

打开hexo所在目录的命令行，输入以下命令安装

```
$ npm install hexo-generator-feed --save
```

如果你有安装`yarn`的话，建议使用`yarn`：

```
$ yarn add hexo-generator-feed
```

然后在`_config.yml`中添加此项：

```
rss： /atom.xml
```

最终RSS文件`atom.xml`会在`https://example.com/atom.xml`处生成

### 站点地图插件安装

打开hexo所在目录的命令行，输入以下命令安装

```
$ npm install hexo-generator-sitemap --save
```

如果你有安装`yarn`的话，建议使用`yarn`：

```
$ yarn add hexo-generator-sitemap
```

最终站点地图文件`sitemap.xml`会在`https://example.com/sitemap.xml`处生成