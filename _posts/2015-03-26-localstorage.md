---
layout: post
title:  "html5客户端存储数据"
date:   2015-03-26 14:10:55
categories: bookmark collect
---
# 客户端存储数据 #

两种方式：localstorage 和 sessionStorage
这两种方式相比cookie的优点：空间大，效率高，速度快。

1. localStorage：长时间存储，只有清空缓存时（或者人为代码删除），数据被删除。
	
	应用：*统计访问次数*

2. sessionStorage 方法针对一个 session 进行数据存储。当用户关闭浏览器窗口后，数据会被删除。

# meta 页面刷新与跳转 #

<meta class="myrefresh" http-equiv="refresh" content="5;url='http://www.linkshop.com.cn/index.htm'">

感谢浏览，页面5s后将为您跳转到联商网首页