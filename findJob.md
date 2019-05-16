# 2019.04.-- 悦玩

1.vue生命周期

    vue的生命周期共有八个节点，分别为
    beforecreate    创建前
    created     创建
    beforemount     挂载前
    mounted     挂载
    beforeupdate    更新前
    updated     更新
    beforedestory   销毁前
    destoryed   销毁

2.css选择器有

    兄弟选择器 + ~
    后代选择器  >
    类选择器 .
    标签选择器 body
    伪类选择器 ::after
    继承选择器 
    id选择器 #
    通配选择器 *
    属性选择器 

# 2019.04.08 大名

1.
```js
for(var i=0;i<5;++i){
setTimeout(function(){console.log(i)},0);
}
```
上述能正确输出012345么，不能那么如何解决？(知识点：闭包)

```js
for(var i = 0;i < 5;i++){
    (function(k) {
        setTimeout(()=>{
            console.log(k);
        },0)
    })(i)
}
```

2.数组相关方法

```js
array.splice(a,b,c...) //删除指定数组元素，同时可以添加元素 a-起始位置 b-删除个数 c...-添加元素
array.slice(a,b) //截取数组指定部分 a-起始位置 b-结束为止
array.push(a) //在数组末尾添加元素
array.pop()//删除数组末尾元素
array.unshift()//在数组头部添加元素
array.sort()//数组元素排序
array.shift()//删除数组头部元素
array.concat()//合并数组
array.reverse()//数组倒序
array.toString()//数组转字符串
array.join()//以括号内的值为分隔号，转化成字符串
```

3.字符串转number

```js
parseInt();
parseFloat();
```

4.页面加载顺序

    页面是自上而下加载的，当遇到外部链接，就会暂停解析，下载文件，当文件下载结束时，继续向下解析。
    因此我们将css文件放在头部，否则用户容易看到乱糟糟的布局。
    而js文件我们则放在底部，防止整张页面空白时间过长。    

# 2019.04.10 天正

1.节点的复制,粘贴,创建,添加,转移,删除

    复制节点 - cloneNode 
    创建节点 - createElement
    粘贴(配合复制节点),添加节点 - appendChild
    删除节点 - removeChild
    
2.css3新特性

    animation 动画
    ,transition 过渡
    ,transform 元素的移动
    ,font-face  字体
    ,word-warp  文字断行
    ,gradient 渐变
    ,shadow 阴影
    ,background-origin 背景位置
    ,background-size 背景尺寸
    ,background-break 背景可以放在不同区域
    
3.localstorage,sessionStorage,cookie的区别

    localStorage和sessionStorage都属于webStorage，存储在客户端
    localStorage的生命周期为永久，大小为5mb
    sessionStorage的生命周期截止到关闭浏览器或者页面为止，大小为5mb
    cookie拥有高可用性和高扩展性。但是可存储数据量小，安全性也存在一定的问题

4.页面间传值

    url传值，表单传值，cookie传值，session传值，webStorage传值
    
5.左中右布局，在两端宽度自适应的前提下如何实现中间部分的自适应

```html
<div id="divleft" style="float:left; width:200px;height:100px;background:red;">left</div>
<div id="divright" style="float:right;width:100px;height:100px;background:blue;">right</div>
<div id="center" style="height:100px;background:yellow" >center</div>
```

# 2019.04.11 硕电
1.new操作符
    
    1.声明一个中间对象
    2.将该中间对象的proto指向构造函数的原型
    3.将构造函数的this通过apply指向中间对象
    4.返回该中间对象,也就是返回了实例对象
    
# 2019.04.28 全人健康
1.在jQuery中，$符如何定义

    $符为jq为select
    
# 2019.05.05 文谷（前）

1.webpack配置文件webpack.congfig.js的各项属性

    devtools：打包模式
    entry：入口文件
    ouput：出口文件
    module：编译所需依赖
    module-rules-test：匹配文件名称
    module-rules-use-loader：所用依赖
    resolve-alias：路径指代
    devServer：本地服务器设置
    
2.vue常用

    v-for
    v-on = @
    v-bind = :
    v-model (双向绑定)
    组件 components
    自定义命令 
    
    
# 2019.05.16 立方 (已入职)

### rem

- rem是css3新增长度单位，是指对根元素html和font-size计算值的大小
- 简单理解为屏幕宽度百分比
- rem和em相似，但是em相对于父元素的大小设置，rem相对于根元素html的字体大小设置

#### rem对常用单位的优点

- 相对于px来说，px的大小直接设定死，兼容性很差，rem可以通过js直接控制
根元素font-size来设置，兼容性更好。
- 相对于em来说，em是针对父元素设置，层级越多，越麻烦，rem的参照物为根元素，更加简明
- 相对于vh vw 来说，浏览器兼容性更好，更加适用于字体（vh vw可能更加适合容器宽高）

#### rem兼容程度

- 支持`ie`9+，`firefox`3.6+，`chrome`4.0+，`opera`15.0+，`safari`4.1+，`Android Borwser`2.1+，`Android Chrome`18.0+


#### rem布局常用脚本

```js
//具体数值根据设计稿定制
$(function() {
  var thisScreenWidth = $(window).width();
  if(thisScreenWidth < 1200){
      thisScreenWidth = 1200;
  }
  var thisFontSize = 16 * (thisScreenWidth/1366)+'px';
  $("html").css("font-size",thisFontSize);
  $(window).resize(function() {
      var thisWidth = $(window).width();
      if(thisWidth < 1200){
          thisWidth = 1200;
      }
      var thisSize = 16 * (thisWidth/1366)+'px';
      $("html").css('font-size',thisSize);
  })
})
```

### 接口基本格式（jq ajax）

#### 路径包
```js
let url = {
    pageName:{//页面名称
        functionName:"",//功能路径
        // ...
    },
    // ... 
}
```

#### 数据包格式
```js
let Interface = {
    url:url.pageName.functionName,
    data:{
        //数据格式参照各个接口文档
    }
}
```

#### 接口格式
```js
$.ajax({
    url:Interface.url,
    // ...
    data:Interface.data,
    success:function(res) {
      // ...
    },
    error:function(e) {
      console.log(e);
    }
})
```

    
