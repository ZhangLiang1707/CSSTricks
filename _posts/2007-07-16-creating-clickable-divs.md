---
layout: post
title: "创建可以点击的 div"
excerpt: <div> 对于CSS的网页设计是必不可少的（译者注：2007年的时候）。它们能提供各种定位功能外的同时还可以提高你的 HTML 页面的结构性。
---

`<div>` 对于CSS的网页设计是必不可少的（译者注：2007年的时候）。它们能提供各种定位功能外的同时还可以提高你的 HTML 页面的结构性。你当然可以把链接放在任意一个 `<div>` 中，但有时你也想让整个 `<div>` 成为可以点击的链接。使用下面的方法可以做到：

{% highlight html %}
<h1>2007 方法</h1>
<div id="div2007" onclick="location.href='http://li-xinyang.com'" style="cursor:pointer;">
  <p> li-xinyang.com</p>
</div>
{% endhighlight %}

光标样式参数可以当用户将鼠标移至 `<div>` 时改变默认光标指针样式成为*小手*，这样可以很好提供一个视觉指示并告诉用户这是可以点击的。

**于2011年5月12日 更新**

内嵌JavaScript的方式已经不想 2007 年的时候那么酷了（如果它曾经酷过）。使用事件处理器（Event Handler）可在提供语义化的同时也可以更方便的在分离的 JavaScript 中通过处理器附加对应事件的函数。如果使用jQuery，我们可以这样做：

{% highlight html %}
<h1>2011 方法</h1>
<div id="div2011">
  <p>li-xinyang.com</p><a href="http://li-xinyang.com"></a>
</div>
<script src="http://code.jquery.com/jquery-2.1.4.min.js"></script>
<script type="text/javascript">
$(document).delegate('#div2011', 'click', function(){
  window.location = $(this).find('a').attr('href');
});
</script>
{% endhighlight %}

**于2015年6月7日 译者增**

译者直接将 `<div>` 整个放入 `<a>` 之中来实现同样的效果。

{% highlight html %}
<h1>2015 译者方法</h1>
<a href="http://li-xinyang.com">
  <div id="div2015">
    <p>li-xinyang.com</p>
  </div>
</a>

<style type="text/css">
#div2015 {
  color: #000;
}
a {
  text-decoration: none;
}
</style>
{% endhighlight %}

<p data-height="268" data-theme-id="15197" data-slug-hash="eNWvJy" data-default-tab="result" data-user="li-xinyang" class='codepen'>See the Pen <a href='http://codepen.io/li-xinyang/pen/eNWvJy/'>ST-0004-creating-clickable-divs</a> by Li Xinyang (<a href='http://codepen.io/li-xinyang'>@li-xinyang</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>