---
layout: post
title: 整理你的 CSS
---

层叠样式表论其根本就是为了将样式从页面结构中分离。这样做不仅为了使代码维护更具容易，同时也让代码变的易读美观。花点时间看看 [CSS Zen Garden](http://www.csszengarden.com/) （英文） 或者其他来自 *Smashing Magazine* 关于 CSS 的好文章，你就能发现 CSS 尽然可以做到这些叹为观止的事儿了。

如果 CSS 做出的效果可以如此的美丽，那么 CSS 代码本身不因该也很易读美观吗？让你的代码漂亮其实就是保持你代码的一致的风格，说白了就是保留一致空格，间距和语法的问题而已。你当然可以手动这样做，但它只会让你的效率变慢。（译者注：不论是代码编写还是修改的过程）幸运的是，有很多好工具可以帮助你整理的你 CSS 代码。

[Tabifier](http://tools.arantius.com/tabifier)

适用于HTML和CSS。 Tabifier 特别简单，只需粘贴 CSS，点击 Tabify 按钮，再复制整理好的代码就可以了。

[Pretty Printer](http://www.prettyprinter.de/)

Pretty Printer 是一个更全功能的代码整理美化工具，它支持 PHP，JAVA，C ++，C，Perl，JavaScript 还有 CSS。它还有额外的选择，可以选择合适添加额外的换行符。但它有个问题，它输出代码是不在文本框中，所以你不能一下子选中所有整理好的文字。

[Format CSS Online](http://www.lonniebest.com/FormatCSS/)

提供更多更全的 CSS 美化功能。可以整理好的提供代码下载，你也就不必再担心拷贝与粘贴的困扰了。

<del>[CSS Formatter and Optimiser](http://floele.flyspray.org/csstidy/css_optimiser.php?lang=en)</del>

<del>支持有四种语言：英语，德语，法语和中文。</del>

**<time datetime="2015-06-09">2015年6月9日</time> 译者话**

上面提到这那些老工具都是七年前的老方法了，甚至一些工具的链接都已经失效。现在通常的做法是直接在编辑器（ IDE 或编辑器原生自带的功能或者通过第三方插件）中对代码进行美化与整理，无需使用这些网页服务的整理服务。

再给常用的两款常用编辑器（Adobe 公司的开源编辑器 Brackets 和 Sublime Text 3）推荐两款代码（同时支持 HTML, CSS, JavaScript）整理的插件。

**Brackets**

 [Brackets-Beautify](https://github.com/drewhamlett/brackets-beautify) 可直接在 Brackets 的插件安装中找到，安装后可即刻使用。

**Sublime Text 2/3**

[Sublime-HTMLPrettify](https://github.com/victorporof/Sublime-HTMLPrettify) 可也可通过 [Package Control]() 进行安装，但是要让它正常工作，机器必须装有 [Node.js](https://nodejs.org/)。安装 Node.js 的方法可以在[这里](http://www.w3cschool.cc/nodejs/nodejs-install-setup.html)（W3CSchool 提供的 Node.js 安装教程）找到。