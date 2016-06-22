---
title: webpack从入门到精通（一）
date: 2016-06-17 18:23:44
tags: 分享日志
author: 徐伟
photos:
- http://bruce.u.qiniudn.com/2013/11/27/reading/photos-0.jpg
- http://bruce.u.qiniudn.com/2013/11/27/reading/photos-1.jpg
---
## 什么是webpack
事实上它是一个打包工具，而不是像RequireJS或SeaJS这样的模块加载器，通过使用Webpack，能够像Node.js一样处理依赖关系，然后解析出模块之间的依赖，将代码打包

## webpack安装步骤
1. 首先得有Node.js
2. 其次全局安装webpack

		npm install -g webpack

3. 在项目目录中安装webpack和插件

		nam install —save-dev webpack

4. 配置webpack

## webpack配置

默认使用webpack.config.js

	var path = require('path');
	module.exports = {
	    entry:'./jsx/app.jsx',
	    output:{
	        path: path.join(__dirname , "/build"),
	        filename:'app.js'
	    },
	    module:{
	        loaders:[
	            {
	                test:/\.(js|jsx)$/,
	                loaders:['babel'],
	                exclude:[path.join(__dirname , "/build")]
	            }
	        ]
	    }
	};


其中*entry*是入口文件，*output*是编译后输出文件，*module*中*loaders*是解析操作

##未完待续h