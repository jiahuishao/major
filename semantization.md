# h5新增语义化标签

## header

> 通常被放置在页面或者页面中某个区块元素的顶部，包含整个页面或者区块的标题、简介等信息，起到引导与导航的作用。
```html
<header>
    <img src="logo.img">
    <h1>xxxxxx公司</h1>
</header>
```
页面中通常可以标记一对及以上的 `<header>` 标签。

## nav
> 表示页面的导航，可以通过导航连接到网站的其他页面，或者当前页面的其它部分。
```html
<header>
    <img src="banner.img" alt="xxxx">
    <h1>xxxxxxx</h1>
    <nav>
        <li><a href="xxxx">aaaa</a></li>
        <li><a href="xxxx">bbbbb</a></li>
        <li><a href="xxxx">cccccc</a></li>
        <li><a href="xxxx">ddddddd</a></li>
    </nav>
</header>
```
`<nav>` 也可以在页面中多次使用，也可以放入 `<header>` 中使用，搜索引擎通常会使用 `<nav>` 标签中的内容来确定网页的具体内容

## aside

> 所包含的内容不是页面的主要内容、具有独立性，是对页面的补充。
```html
 <article>
    <h1>HTML5学习之语义化标签</h1>
    <p>....正文.....</p>
    <aside>
        <h2>什么是语义化标签</h2>
        <p>语义化标签就是......</p>
    </aside>
</article>
```
`<aside>` 一般用来装在广告，链接，文章补充之类的

## footer

> 一般被放置在页面或者页面中某个区块的底部，包含版权信息、联系方式等信息。
```html
<footer>
    <small>
        版权所有 © 2016-2017 **信息科技有限公司
    </small>
</footer>
```
`<footer>` 与 `<header>` 相同，没有使用限制，可以设置在任意区块的底部

## article

> 表示包含于一个文档、页面、应用程序或网站中的一段独立的内容，可以被独立的发布或者重新使用文章标记标签。
  
```html
<article>
    <h1>HTML5学习之语义化标签</h1>
    <p>....正文.....</p>
    <footer>版权所有*伪版必究</footer>
</article>
```

`<article>` 可以嵌套使用，但是他们必须是从属关系

## section

> 是一个主题性的内容分组，通常用于对页面进行分块或者对文章等进行分段
```html
<article>
    <h1>JavaScript框架</h1>
    <p>Javascript框架是指以Javascript语言为基础搭建的编程框架。</p>
    <section>
        <h2>angular.Js<h2>
        <p>angular.Js是一款优秀的前端JS框架</p>
    </section>
    <section>
        <h2>Vue.js<h2>
        <p>Vue.js是用于构建交互式的Web界面的库</p>
    </section>
    <section>
        <h2>jQuery<h2>
        <p>jQuery是一个快速、简洁的JavaScript框架。</p>
    </section>
</article>
```
`<section>` 标签通常包含一个 `<header>` 标签以及一个 `<footer>` 标签，同时 `<section>` 标签中可以嵌套 `<section>` 标签

## ruby rt rp
> ruby是一种排版注释系统，是位于横排基础文本上方的简短文字
```html
<ruby>
    北<rt>bei</rt>
    京<rt>jing</rt>
</ruby>
```
如果在不支持 `<ruby>` 的浏览器中，需要向下面这样进行隔离
```html
<ruby>
    北
    <rp>
        <rt>bei</rt>
    </rp>
    京
    <rp>
        <rt>jing</rt>
    </rp>
</ruby>
```

## time
> 为了将现在的常用的日期和时间语句用规范的、利于机器识别的格式进行表述，time元素提供了一个可选的时间和时区组件
```html
<!--确保机器能够正确识别,添加datatime属性-->
<time datetime="2017-07-03"> 
```

## mark
> 为了强调一个词或者一段句子，从而进行高亮标记
```html
<mark>highlight</mark>
```
## wbr
> 如果单词太长，或者您担心浏览器会在错误的位置换行，那么您可以使用 <wbr> 元素来添加 Word Break Opportunity（单词换行时机）
```html
<p>如果想学习 AJAX，那么您必须熟悉 XML<wbr>Http<wbr>Request 对象。</p>\
```

## 备注(进行略微变动的语义化标签)
在HTML4版本中的标签元素在HTML5中有了新的定义。

使用`<b>`表示文档渲染为粗体，而`<i>`表示文档渲染为斜体。使用`<strong>`和`<em>`来强调一段重要的文本。`<cite>`用来为对参考文献的引用进行定义，比如书籍或杂志的标题。`<small>`不仅仅指的是小字体，它还同样为法律声明增添不具有重要性的旁注或小字。`<hr>`现在表达的是主体性的间断，不再仅仅是分割版面的一条水平线。



