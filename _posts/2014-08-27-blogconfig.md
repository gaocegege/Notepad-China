---
layout: post
title: "博客配置设定"
description: 博客配置设定
modified: 2014-08-27
category: 随笔
tags: [随笔]
imagefeature:
mathjax: false
chart:
comments: true
featured: true
---

# 配置

配置文件为_config.yml，其中都有比较清楚的注释。

# 文件结构

<pre>
Notepad-China
*	_includes/      Directory    分模块模板
		xxx.html    模板文件
*	_layouts/       Directory    页面模板，依赖_includes文件夹下的内容
		xxx.html    模板文件
*	_posts/         Directory    博文目录
		YYYY-MM-DD-UniqueID.md    博文文件
*	assets/         Directory    脚本以及CSS
		css/    css文件
		js/     js文件
*	images/         Directory    图片
	404.md          File         404页面
	about.md        File         个人介绍页面
*	_config.yml     File         配置文件
	analytics.html  File         统计页面
	categories.html File         分类浏览页面
	featured.html   File         佳文浏览
*	index.html      File         index页面
*   link.md         File         友情链接
*   relaxed.html    File         水文浏览
</pre>

其中\*表示必有文件或目录

# 博文相关

博文都在_post文件夹下

## 博文结构

首先需要有一段配置描述，本文的配置描述是这样的：

<pre>
	---
	layout: post
	title: "博客配置设定"
	description: 博客配置设定
	modified: 2014-08-27
	category: 随笔
	tags: [随笔]
	imagefeature:
	mathjax:  false
	chart:    true
	comments: true
	featured: true
	---
</pre>

Layout是确定使用什么页面模板，Title是标题，Description是描述，Modified是修改日期，Category是分类，Tag是标签，imagefeature是进入博文时候的图片，默认无，mathjax是一个js库，用来写公式，不需要建议定义为false，chart是图表，是amcharts，comment是评论，featured是确定是否为佳文。

有了这段配置文件，接下来就可以写文章内容了，Markdown支持的语法都可使用，也可使用HTML。

## 博文文件命名方式

YYYY-MM-DD-UniqueID.md

YYYY-MM-DD为博文发布时间，UniqueID是博文的唯一标识符。

在浏览时博文地址为`<Your Host>/<category>/<UniqueID>`，具体到这篇文章就是`http://gaocegege.com/Notepad-China/随笔/Hello-World`

## Helper.py

这个脚本可以用来构建一个空的博文文件，使用方法为：

	./helper.py <UniqueID>