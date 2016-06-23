---
title: Hexo书写博客
date: 2016-06-23 09:12:39
tags: 技术文档
author: 王阳
photos:
- http://bruce.u.qiniudn.com/2013/11/27/reading/photos-0.jpg
---
## Hexo简介
A fast, simple & powerful blog framework, powered by [Node.js](http://nodejs.org).

## 工具推荐
- WebStorm
- Visual Studio Code
- MarkdownPad

## 安装步骤
##### 1. 首先得有[Node.js](http://nodejs.org).

##### 2. 其次全局安装hexo
``` bash
$ npm install -g hexo
```

##### 3. git clone 克隆配置完好的Hexo环境
``` bash
$ git clone git@github.com:TC-Flight-Int-Web/blog.git
$ cd blog
$ git pull origin master 获取最新的代码，防止冲突，搞掉其他人文章
```
> 记住一定要**获取最新的代码**


##### 4. 进入对应目录,安装对应依赖包
``` bash
$ cd blog
$ npm install
```

##### 5. 创建一篇文章
``` bash
$ hexo new "Hello Hexo"
$ INFO  Created: [绝对路径]\blog\source\_posts\hello-hexo.md
```

##### 6. 本地书写文章打开对应目录文件
``` bash
$ 打开对应目录文件【[绝对路径]\blog\source\_posts\hello-hexo.md】
```

##### 7. 打开markdown，默认情况
![markdown默认情况](/img/王阳/img1.png)
> 
  - title 文章标题
  - date 发布时间
  - tags 标签
  - author 作者
  
##### 8. markdown语法书写
![](/img/王阳/img2.png)
- 添加图片统一路径
    ![保存图片路径](/img/王阳/img3.png) 
- 图片添加的语法
    ![图片markdown语法](/img/王阳/img4.png)

##### 9. 启动Hexo Server 本地查看
``` bash
$ hexo s
$ INFO  Start processing
$ INFO  Hexo is running at http://0.0.0.0:4000/. Press Ctrl+C to stop.
```

##### 10. 发布文章
``` bash
$ hexo d
$ INFO  Deploying: git
$ INFO  Clearing .deploy_git folder...
$ INFO  Copying files from public folder...
$ INFO  Deploy done: git
```

##### 11. 提交代码，防止其他人搞掉你的文章
``` bash
$ git pull origin master
$ git add .
$ git commit -m "文章书写"
$ git push origin master
```