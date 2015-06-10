---
layout: post
title: "CSS 菜单图片翻转效果"
excerpt: 下面的例子展示如何利用CSS实现菜单背景图片的替换效果，是时候做一个真实的例子了！
---

下面的例子展示如何利用CSS实现菜单背景图片的替换效果，是时候做一个真实的例子了！

**CSS 图片翻滚实例**

可翻滚菜单有三种可能的状态：

- 正常（Normal）
- 滚下（Rollover）
- 选择（Selected）

{% highlight html %}

<div id="menu">
  <ul>
    <li><a id="selected" href="#">主页</a></li>
    <li><a href="#">菜单选项 #1</a></li>
    <li><a href="#">菜单选项 #2</a></li>
    <li><a href="#">菜单选项 #3</a></li>
  </ul>
</div>

<style type="text/css">
  body {
    margin: 30px;
  }
  #menu {
    position: relative;
    display: block;
    width: 350px;
  }
  #menu ul {
    list-style-type: none;
    width: 800px;
  }
  #menu ul li {
    display: block;
    float: left;
    width: 200px;
    height: 60px;
  }
  #menu a,
  #menu a:visited {
    display: block;
    width: 200px;
    height: 60px;
    text-align: center;
    color: #000;
    line-height: 60px;
    text-decoration: none;
    font-family: arial, sans-serif;
    font-weight: bold;
    margin-top: 5px;
    background-color: transparent;
    background-position: left top;
    background: url("http://7xjjkz.com1.z0.glb.clouddn.com/nav_block.jpg");
  }
  #menu a:hover {
    background-position: left center;
    overflow: hidden;
    color: #fff;
  }
  #menu a#selected {
    background-position: left bottom;
  }
</style>

{% endhighlight %}

上面的代码干净，简单，你应该可以很容易理解它们的意思。请自己把玩代码，做出属于自己的心中的炫酷效果。

<p data-height="268" data-theme-id="15197" data-slug-hash="aOWprG" data-default-tab="result" data-user="li-xinyang" class='codepen'>See the Pen <a href='http://codepen.io/li-xinyang/pen/aOWprG/'>ST-0003-CSSMenuWithRolloverImage</a> by Li Xinyang (<a href='http://codepen.io/li-xinyang'>@li-xinyang</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>