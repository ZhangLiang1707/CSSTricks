---
layout: post
title:  "如何在保证 SEO 的同时使用图片标题"
permalink: header-text-image-replacement
---


正如你所知的那样，像谷歌，雅虎还有 MSN 的搜索引擎主要是根据你的网页文本内容来进行索引并确定它们与搜索关键字的相关程度。想必你也了解，使用标题标签，如 `<h1>` 在 HTML 中的重要性，因为搜索引擎能更好的为结构性强的文本内容进行索引。但如果你并不要使用大而丑的文本标题该怎么办？使用自己制作的漂亮图形标题？你当然可以这样做，然而你同时也不想因为使用了图片 `<img>` 而放弃 `<h1>` 对于搜索引擎优化的支持。这里我们可以鱼和熊掌兼得（译者注：既使用漂亮的图片标题，也不放弃结构化和语义化的文本支持）！

其中一个妙招是使用一个类来替换文本标题成为图片。像往常一样使用你的标题标签，只是给它一个特别的类名称，像是 `<h1 class =“headerReplacement”>网页标题</h1>` 之后在你的 CSS 中定义将类定义成下面的样子：

{% highlight html %}
<style>
.headerReplacement {
    text-indent: -9999px;
    width: 600px;
    height: 100px;
    background: url(pathtoyourimage) #cccccc no-repeat;
}
</style>
{% endhighlight %}

这样你漂亮的图片标题就能在合适的位置替换掉难看的文本标题，当然这样做也并不会丢失页面对于搜索引擎优化的支持。同时使用这种方法还可以让使用屏幕阅读器的人或者关闭浏览网页图像或CSS的读者得到一个优雅降级版的网页。

<p data-height="268" data-theme-id="15197" data-slug-hash="OVmXaL" data-default-tab="result" data-user="li-xinyang" class='codepen'>See the Pen <a href='http://codepen.io/li-xinyang/pen/OVmXaL/'>ST-0000-HeaderTextImpageReplacement</a> by Li Xinyang (<a href='http://codepen.io/li-xinyang'>@li-xinyang</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>