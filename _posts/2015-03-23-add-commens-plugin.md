---
layout: post
title:  "Add Commens Plugin"
date:   2015-03-23 16:19:50
categories: comments plugin
---
###博客增加评论插件###


1. 插件来源[多说](http://dev.duoshuo.com/)

	*这插件的名是后妈取的吧，不过很容易上手，也没有广告，感谢。*
	
	目前使用[disqus](https://disqus.com/ "disqus")

1. 使用。
	
	- 注册多说的用户，我用豆瓣授权登录。因为我看到注册方式都是要通过社交产品授权登录。
	- 在_includes文件夹中建立一个comments.html页面。
	- 在用户工具页面会看到以下代码，将以下代码放到comments.html。

		html部分：

		![](http://i.imgur.com/VCG6Gvy.png)

		js部分：
		<pre><code>
		var duoshuoQuery = {short_name:"你的多说short_name"};
		(function() {
		var ds = document.createElement('script');
		ds.type = 'text/javascript';ds.async = true;
		ds.src = (document.location.protocol == 'https:' ? 'https:' : 'http:') + '//static.duoshuo.com/embed.js';
		ds.charset = 'UTF-8';
		(document.getElementsByTagName('head')[0] 
		 || document.getElementsByTagName('body')[0]).appendChild(ds);
		})();
		</code></pre>

	- 将这个评论模板用到页面上。我把它放到了_layouts/default.html中。

		![](http://i.imgur.com/N9CaL95.png)

1. 总结
	
	-思路：就是把别人的html+js 代码放在博客页面中。

	-报错解决。
	
	用git hub提交了代码后页面没有出现评论框。comments.html中评论的代码没被default.html包含。
	
	然后我删掉了script中的中文注释（乱码），重新上传到库中，刷新页面就出现了评论框。
	
	-使用disqus感受下，用法基本跟多说一样。 
	

	
	    	


