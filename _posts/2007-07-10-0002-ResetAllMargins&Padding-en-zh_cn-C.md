---
layout: post
title:  "重置全部边距及填充"
excerpt: 最近这样的做法非常流行。这些代码将毫不留情在所有浏览器中的移除所有元素的默认边距和填充。
permalink: reset-all-margins-and-padding
---

{% highlight html %}
<style>
* {
    margin: 0;
    padding: 0;
}
</style>
{% endhighlight %}

最近这样的做法非常流行。这些代码将毫不留情在所有浏览器中的移除所有元素的默认边距和填充。这样做为不同浏览器中的页面设计提供了一个干净的开始，并确保所有存在的间距都是有意而为之。而且这样做也并没用什么坏处。

有些人喜欢给元素也添加上边框属性 `border: 0` ，但它已经被发现并不是在所有情况都会起到去除多余空间的作用，那又何必加它呢？

如果你想要完全[无脑的重置一切](http://ask.metafilter.com/34797/Holy-Shit-Batman)，那不妨看看这个[这个](http://meyerweb.com/eric/thoughts/2007/05/01/reset-reloaded/)。