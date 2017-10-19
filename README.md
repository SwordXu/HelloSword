# HelloSword
This is my first GitHub Test

link和@import的区别
页面中使用CSS的方式主要有3种：行内添加定义style属性值，页面头部内嵌调用和外面链接调用，其中外面引用有两种：link和@import。外部引用CSS两种方式link和@import的方式分别是：

XML/HTML代码
<link rel="stylesheet" rev="stylesheet" href="CSS文件" type="text/css" media="all" />   
XML/HTML代码
<style type="text/css" media="screen">   
@import url("CSS文件");   
</style>  

两者都是外部引用CSS的方式，但是存在一定的区别：

　　区别1：link是XHTML标签，除了加载CSS外，还可以定义RSS等其他事务；@import属于CSS范畴，只能加载CSS。

　　区别2：link引用CSS时，在页面载入时同时加载；@import需要页面网页完全载入以后加载。

　　区别3：link是XHTML标签，无兼容问题；@import是在CSS2.1提出的，低版本的浏览器不支持。

　　区别4：link支持使用Javascript控制DOM去改变样式；而@import不支持。

补充：@import最优写法
@import的写法一般有下列几种：

@import 'style.css' //Windows IE4/ NS4, Mac OS X IE5, Macintosh IE4/IE5/NS4不识别
@import "style.css" //Windows IE4/ NS4, Macintosh IE4/NS4不识别
@import url(style.css) //Windows NS4, Macintosh NS4不识别
@import url('style.css') //Windows NS4, Mac OS X IE5, Macintosh IE4/IE5/NS4不识别
@import url("style.css") //Windows NS4, Macintosh NS4不识别
由上分析知道，@import url(style.css) 和@import url("style.css")是最优的选择，兼容的浏览器最多。从字节优化的角度来看@import url(style.css)最值得推荐。
