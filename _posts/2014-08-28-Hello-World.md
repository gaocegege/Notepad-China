---
layout: post
title: "博文相关设定"
description: 迎接新博客
modified: 2014-08-28
category: 随笔
tags: [jekyll, first article]
imagefeature: 
mathjax: false
chart:false
comments: true
featured: false
---

# 博文结构

首先需要有一段配置描述，本文的配置描述是这样的：

<pre>
	---
	layout: post
	title: "Example"
	description: 迎接新博客
	modified: 2014-08-28
	category: 随笔
	tags: [jekyll, first article]
	imagefeature: 
	mathjax: false
	chart: 
	comments: true
	featured: false
	---
</pre>

Layout是确定使用什么页面模板，Title是标题，Description是描述，Modified是修改日期，Category是分类，Tag是标签，imagefeature是进入博文时候的图片，默认无，mathjax是一个js库，用来写公式，不需要建议定义为false，chart是图表，是amcharts，没需要建议false，comment是评论，featured是确定是否为佳文。

有了这段配置文件，接下来就可以写文章内容了，Markdown支持的语法都可使用，也可使用HTML。

# 博文文件命名方式

YYYY-MM-DD-UniqueID.md

YYYY-MM-DD为博文发布时间，UniqueID是博文的唯一标识符。

在浏览时博文地址为`<Your Host>/<category>/<UniqueID>`，具体到这篇文章就是`http://gaocegege.com/Notepad-China/随笔/Hello-World`

# Helper.py

这个脚本可以用来构建一个空的博文文件，使用方法为：

	./helper.py <UniqueID>