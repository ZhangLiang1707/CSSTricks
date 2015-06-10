---
layout: post
title: 跨浏览器 CSS 粘性页脚
---

网页页脚是放置版权信息，联系信息和快速导航的好地方。访客习惯在页面的底部去找这类东西，那我们为什么不能帮助他们，把我们的页脚固定再底栏（相对固定）？一个问题是，当页面的内容不够长时，页脚可能会显示在浏览器中中央而不是底部。

有什么办法可以让一个页脚 `div` 老老实实的显示在浏览器窗口的底部不论窗口的大小呢？貌似没有明显的解决方案，这也一直是一个困扰大家太久的问题。

但这不再是个问题啦！*瑞安*编写了一个简单而又优美的方式就做到这一点（代码见下方）他慷慨分享了他的方法[这里](http://ryanfait.com/sticky-footer/)（翻译在下面）。它可以兼容所有主流浏览器（IE，火狐，Safari 和 Opera），并且是完全免费。*瑞安*谢谢你！

**使页脚保持在页面底部（翻译）**

CSS固定页脚兼容跨浏览器的方法。

这个CSS粘性页脚代码将把网页的页脚退至浏览器窗口的底部。这种方法使用了有效的 CSS 和 HTML（并没有使用任何奇技淫巧），所以它适用于所有的主流浏览器（甚至是现已无人问津的IE5和IE6）。


如何在你的网页中使用 CSS 黏黏页脚

把下面的 CSS 添加到你的样式表中。`.wrapper` 外边距（margin）的负值应同 `.footer` 和 `.push` 的高度一致。外边距的负值应始终等于页脚的（包括任何你添加填充或边框）的最大高度。

{% highlight html %}
<style type="text/css">
* {
  margin: 0;
}
html, body {
  height: 100%;
}
.wrapper {
  min-height: 100%;
  height: auto !important;
  height: 100%;
  margin: 0 auto -4em;
}
.footer, .push {
  height: 4em;
}
</style>
{% endhighlight %}


如果按照这个 HTML 的结构。没有任何内容可以在 `.wrapper` 和 `.footer` 的 `<div>` 标签之外，除非它使用了绝对定位（`position: absolute`）。此外，在 `.push` 的 `<div>` 中不因该存在任何内容，因为它是一个隐藏元素仅仅用于将页脚“推”倒底部，因此不会与任何元素重叠在一起。

{% highlight html %}
<html>
  <head>
  <link rel="stylesheet" href="layout.css" ... />
  </head>
  <body>
    <div class="wrapper">
      <p>Your website content here.</p>
      <div class="push">
      </div>
    </div>
    <div class="footer">
      <p>Copyright (c) 2008</p>
    </div>
  </body>
</html>
{% endhighlight %}

如需使用多列布局，需要给 `.push` 加上 `clear`。

{% highlight html %}
<style>
.footer, .push {
  clear: both;
}
</style>
{% endhighlight %}

给元素添加外边距（margin）会让页脚不能么听话或者行为诡异。
只需使用填充（padding）就可以解决那些问题。
如果你用了我的代码，并没有达到预期的效果。那一定是你代码什么地方写错了！
看看 CSS 粘滞页脚的主页（上面提供的因为原文地址）是否在你的浏览器中正常显示。如果正常显示了，那么就一定是你的代码有问题！

在 ASP.NET 中不遇到问题了？

如果你正在使用 ASP.NET，添加下面的 CSS 代码。

{% highlight html %}
<style>
form {
  height: 100%;
}
</style>
{% endhighlight %}

关于 `height: auto !important; and height: 100%; ` 属性值。
我收了电子邮件告诉我，粘性页脚在没有前面的属性时也可以正常工作。它们的存在是为了解决 IE6 及其以下版本的兼容，所以如果你想在 Internet Explorer 6 中使用粘性页脚，就不要删除它们！

有很多种几种方法可以用 CSS 将页脚粘在页面底部， 但这些方法往往都使用了太多奇技淫巧或者添加了很多额外的 HTML 标记。然而这种方法只使用15行的 CSS 且几乎没有任何额外的 HTML 标记（赞）。更绝的是，它是完全有效的CSS，并可以在所有主流浏览器中正常工作。Internet Explorer 5 及以上版本，火狐，Safari，Opera 和还有更多。

<p data-height="268" data-theme-id="15197" data-slug-hash="xGdXgb" data-default-tab="result" data-user="li-xinyang" class='codepen'>See the Pen <a href='http://codepen.io/li-xinyang/pen/xGdXgb/'>ST-0005-sticky-footer</a> by Li Xinyang (<a href='http://codepen.io/li-xinyang'>@li-xinyang</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
