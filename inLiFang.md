# 2019.5.8

## web前端开发规范（立方控股）

### 文件名的命名规范

文件名统一采用，英文字母，数字，下划线的组合。
各子页命名的原则首先应该以栏目名的英语翻译取单一单词为名称
    
> 关于我们 \aboutus <br>
> 信息反馈 \feedback <br>
> 产品 \product <br>

如果栏目名称多而复杂并不好以英文单词命名，
则统一使用该栏目的`名称拼音`或`拼音的首字母`表示。
每一个目录中应该包含一个缺省的html文件文件名统一
用`index.htm` `index.html` `index.asp`
    

#### 图片的命名规范

图片的名称分为头尾两部分，用`下划线`隔开，
头部分表示此图片的大类性质

> 例如：广告，标志，菜单，按钮等等<br>
> 
> 放置在页面顶部的广告，装饰图等长方形的图片取名：banner <br>
> 标志性的图片取名为：logo<br>
> 在页面上位置不固定并且带有链接的小图片我们取名为：button<br>
> 在页面上某一位置连续出现，性质相同的链接栏目的图片我们取名为：menu<br>
> 装饰用的照片我们取名为：pic<br>
> 不带链接表示标题的图片我们取名：title<br>
> 
> 范例：banner_sohu.gif pic_people.jpg
>
 
鼠标感应类命名规范为`图片名+_+on/off`

> menu1_off.gif


#### JavaScript命名规范

> 例如广告条的js文件名为 ad.js 弹出窗口的js文件名为 pop.js

#### 动态语言文件命名原则

以`性质_描述`格式命名，描述可以有多个单词，用`_`隔开，性质一般是该页面的概要

> 范例：registe_form.asp   register_post.asp   topic_lock.asp

### 文件存放位置规范

|root|||
|:----|:----|:----|
|-|cn|存放中文html文件|
|-|en|存放英文html文件|
|-|flash|存放flash文件|
|-|images|存放图片文件|
|-|imagestudio|存放psd源文件|
|-|flashstudio|存放flash源文件|
|-|inc|存放include文件|
|-|library|存放dw库文件|
|-|media|存放多媒体文件|
|-|project|存放工程项目资料|
|-|temp|存放客户原始资料|
|-|js|存放javascript脚本|
|-|css|存放css文件|

### css书写规范

css样式可细分为3类：`自定义样式`，`重新定义html样式`，`连接状态样式`

注意细则

- 协作开发及分工时，一定会有全文件通用css样式，每个页面都必须引入，此文件包含
reset及头部底部样式，此文件不可随意修改；
- class与id的使用，id的优先级大于class，id大多为js预留
- 为js预留的钩子，命名机构为`js_xxx.js`
- class和id的命名，大的框架命名统一命名，其他的样式尽量使用`小写英文`，`数字`，`_`，组合
来命名，避免使用中文拼音，尽量使用简单的单词组合。总之命名要语义化，简明化
- 规避class和id命名：
  - 通过从属写法规避
  - 取父级元素id/class命名部分命名
  - 重复率过高的命名，请以自己代号加下划线起始
- css属性书写顺序，建议遵循以下顺序
  - 布局定位属性(margin,padding,float,display,position,visibility,overflow)
  - 自身属性(width,height,background,border)
  - 文本属性(font,color,text-align,text-decoration,text-indent)
  - 其他属性(list-style,vertical-vlign,cursor,z-index,zoom)
- 书写代码前，考虑并提高样式重复使用率
- 充分利用html自身属性以及样式继承原理，减少代码量
- 样式表中中文字体名，请务必转码成unicode码，以避免编码错误时乱码
- 背景图尽可能使用雪碧图，减少http请求，考虑到多人协作开发，雪碧图按模块制作
- 使用table标签时（尽可能避免使用table标签），请不要用width/height/cellspacing/cellpadding
等table属性直接定义，尽可能利用table自身私有属性分离结构与表现。
- 杜绝使用<meta http-equiv="X-UA-Compatible" content="IE=7" />兼容ie8
- 避免兼容性属性的使用，比如text-shadow||css3的相关属性
- 减少使用影响性能的属性，比如position||float；
- 必须为大区块样式添加注释，小区块适量注释
- 代码缩进与格式：建议单行书写

#### 命名规则

|cn|en|
|:---:|:----:|
|头|header|
|内容|content/container|
|尾|footer|
|导航|nav|
|侧栏|sidebar|
|栏目|column|
|页面外围控制整体布局宽度|wrapper|
|左中右|left center right|
|登录条|loginbar|
|标志|logo|
|广告|banner|
|页面主体|main|
|热点|hot|
|新闻|news|
|下载|download|
|子导航|subnav|
|菜单|menu|
|子菜单|submenu|
|搜索|search|
|友情链接|friendlink|
|页脚|footer|
|版权|copyright|
|滚动|scroll|
|内容|content|
|标签页|tab|
|文章列表|list|
|提示信息|msg|
|小技巧|tips|
|栏目标题|title|
|加入|joinus|
|指南|guild|
|服务|service|
|注册|regsiter|
|状态|status|
|投票|vote|
|合作伙伴|parter|

#### 注释的写法

```html
/* footer */
content
/* end footer*/
```

#### id的命名

##### 页面结构

|cn|en|
|:---:|:----:|
|容器|container|
|页头|header|
|内容|content/container|
|页面主体|main|
|页尾|footer|
|导航|nav|
|侧栏|sidebar|
|栏目|column|
|页面外围控制整体布局宽度|wrapper|
|左右中|left right center|

##### 导航

|cn|en|
|:---:|:----:|
|导航|nav|
|主导航|mainbav|
|子导航|subnav|
|顶导航|topnav|
|边导航|sidebar|
|左导航|leftsidebar|
|右导航|rightsidebar|
|菜单|menu|
|菜单|menu|
|子菜单|submenu|
|标题|title|
|摘要|summary|


##### 功能

|cn|en|
|:---:|:----:|
|标志|logo|
|广告|banner|
|登录|login|
|登录条|loginbar|
|注册|regsiter|
|搜索|search|
|功能区|shop|
|标题|title|
|加入|joinus|
|状态|status|
|按钮|btn|
|滚动|scroll|
|标签页|tab|
|文章列表|list|
|提示信息|msg|
|当前的|current|
|小技巧|tips|
|图标|icon|
|注释|note|
|指南|guild|
|服务|service|
|热点|hot|
|新闻|news|
|下载|download|
|投票|vote|
|合作伙伴|partner|
|友情链接|link|
|版权|copyright|

##### 基本样式

```css
body{margin: 0;padding: 0;font: 12px "\5B5B\4F53",sans-serif;background: #fff}
div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,form,fieldset,input,textarea,blockquote,p{padding: 0;margin: 0;}
table,td,tr,th{font-size: 12px}
li{list-style-type: none}
img{vertical-align: top;border: 0;}
ol,ul{list-style: none}
h1,h2,h3,h4,h5,h6{font-size: 12px;font-weight: normal}
.fB{font-weight: bold}
.f12px{font-size: 12px}
.f14px{font-size: 14px}
.left{float: left}
.right{float: right}

a{color: #2b2b2b;text-decoration: none}
a:visited{text-decoration: none}
a:hover{color: #ba2636;text-decoration: underline}
a:active{color: #ba2636;}
```
重定义最先，伪类其次，自定义最后

不同浏览器上字号保持一致，字号建议使用`pt`，`px`

`pt`一般使用中文宋体的9pt和11pt，
`px`一般使用中文宋体的12px和14.7px，
黑体字或者宋体字加粗时，一般选用11pt和14.7pt的字号比较合适。
中英文混排时，我们尽可能的将英文和数字定义为verdana和arial两种字体

### html书写规范

#### head区

```html
<!--必选-->

<!--简体中文-->
<meta http-equiv="content-type" content="text/html;charset=gb2312">
<!--翻译中文-->
<meta http-equiv="content-type" content="text/html;charset=utf-8">
<!--英语-->
<meta http-equiv="content-type" content="text/html;charset=utf-8">
<!--网页制作者信息-->
<meta name="author" content="webmaster@markdown.com">
<!--网站简介-->
<meta name="DESCRIPTION" content="xxxxxxxxxx">
<!--搜索关键字-->
<meta name="keywords" content="xxxxxxxxxx,xxxxx">
<!--网页的css规范-->
<link href="" rel="stylesheet" type="text/css">
<!--网页标题-->
<title>xxxxxx</title>

<!--end-必选-->

<!--可选-->

<!--设定网页的到期时间。一单页面过期，必须到服务器上重新调阅-->
<meta http-equiv="expires" content="Wed,26 Feb 1997 08:21:57 gmt">
<!--禁止浏览器从本地机的换从中调阅页面内容-->
<meta http-equiv="Pragma" content="no-cache">
<!--用来防止别人在框架里调用你的页面-->
<meta http-equiv="Window-target" content="_top">
<!--自动跳转,5指代停留5秒-->
<meta http-equiv="Refresh" content="5;url=http://www.baidu.com">
<!--网页搜索机器人向导，用来告诉搜索机器人哪些页面需要索引，那些页面不要索引-->
<meta http-equiv="robots" content="none">
<!--收藏夹图标-->
<link rel="Shortcut Icon" href="favicon.icon">
<!--所有的JavaScript的调用尽量采取外部调用-->
<script language="JavaScript" src="xxxxxx.js"></script>
<!--为保证浏览器兼容性，必须设置背景颜色-->
<body bgcolor="#ffffff"></body>

<!--end-可选-->

```

#### 字体

- 设定字体样式时，对于`文字字号样式`和`行间距`应必须使用css样式表
- 首选宋体，黑体字或者宋体字加粗时，一般选用11pt和14.7pt的字号比较合适。
       中英文混排时，我们尽可能的将英文和数字定义为verdana和arial两种字体
- 为了最大程度发挥浏览器自动排版功能，在一段完整的文字中请尽量不要使用`<br>`来干预
分段
- 不同语种的文字之间应该有一个半角空格，但避头的符号之前和避尾的符号之后除外，汉字标点要用
全角标点，英文字母和数字周围的括号应该使用半角括号
- 请不要在网页中连续出现多余一个的  也尽量少用全角空格（英文字符集下，全角空格会变成乱码）
，空白应该尽量使用text-indent，padding，margin，hspace，vspace以及透明的gif图片来实现
- 行距建议用百分比来定义，常用的两个行距的值`120%`和`150%`
- 排版中我们经常会遇到需要进行首航缩进的处理，不要使用    或者全家空格来达到效果，
规范的做法是在样式中定义p{text-indent:2em;}然后再给每一段加上<P>标记

#### 链接

- 网站中的链接路径全部采用相对路径，一般链接到某一目录下的缺省文件不必写全名
- 在浏览器里，当我们点击空链接时，他会自动将当前页面重置到首端，从而影响用户正常阅读内容，我们用代码`javascript:void(null)`代替原来
的#标记

#### 下载速度

- 首页flash网页的大小应该在200k以下，尽量使用矢量图形和action来减小动画大小，
非静态页面含图片大小应该在70k左右，尽可能的使用背景颜色替换大块同色图片

#### include

- asp标准写法 <!--#include file="xxxxx.asp"-->
- jsp标准写法 <%@include file="xxxx.jsp" %>

#### alt和title

- 都是提示性语言标签，请注意他们之间的区别，alt给图片提示，title给链接文字或者普通文字提示

#### banner

- 全尺寸banner 468x60px（大小不超过14k）
- 半尺寸banner 234x60px
- 小尺寸banner 88x31px
- 小图标尺寸 120x90 120x60
- 普遍的banner尺寸 760x100 750x120 468x60 468x95 728x90 585x140
- 次级页的pip尺寸 360x300 336x280
- 游标 100x100 120x120

#### logo国际标准规范

- 大logo 120x90
- 一般logo 120x60
- 最普遍logo 88x31

#### 页面修饰图片处理

- 页面经过优化以加快下载的速度，有较佳的视觉空间效果，用图要与页面风格，页面内容相符，制作精美，细节处理得当

### JavaScript书写规范

- 封号结尾，原则上功能需要原生开发
- 引入新库需要与团队其他人员讨论
- 使用驼峰式命名，jq变量要求首字符为_
- 类命名，首字母需要大写，驼峰式命名
- 函数命名：首字母小写，驼峰式命名
- 命名语义化
- 尽量避免使用存在兼容性以及消耗资源的方法或属性，例如eval和innertext
- 后期优化，js中非注释类中文字符需要转换成unicode编码使用，以避免编码
错误时乱码显示
- 代码结构明了，加适量注释，提高函数重用率
- 注重与html分离，减小reflow，注重性能

### 图片规范

- 页面元素类图片，均放入img文件夹，测试类图片放于img/demoing文件夹
- 格式只能为 gif png jpg
- 命名只能用小写英文字母，数字，下划线的组合
- 保证视觉效果的情况下选择最小的图片格式和图片质量，以减少加载时间
- 尽量避免使用半透明的png图片
- 合理运用雪碧图

