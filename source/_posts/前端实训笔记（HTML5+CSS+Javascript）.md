---
title: 前端实训笔记（HTML5+CSS+Javascript）
date: 2019-03-27 08:17:00
author: 胡佳艺
img: /images/首页22.jpg
top: false
cover: false
coverImg: /images/1.jpg
password: 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
toc: false
mathjax: false
summary: 前端实训笔记（HTML5+CSS+Javascript）。
categories: 前端
tags: 
  - HTML5
  - CSS
  - JavaScript
---



## 前端实训笔记（HTML5+CSS+Javascript）

#### 1 Java的平台

  1）JavaSE  Java平台的标准版 Java基础+Java高级  --> Client（客户端）架构    Client(客户端)/Server（服务器端）架构
  2）JavaEE  Java平台的企业版 （互联网程序应用 ->  Browser（浏览器）/Server（服务器）架构 ）  数据库  Web开发基础（HTML5 CSS JavaScript...） JSP Servlet SSH框架等
                                                                                                        Browser浏览器端的开发                Server服务器端的开发
 Web开发基础
 HTML5    一个HTML就是一个页面，主要是显示一个网页（页面）的内容  
 CSS      美化页面，样式
 JavaScript 完成页面的动态效果

#### 2 互联网开发的工作流程/原理

​    浏览器端      服务器端      数据库端

#### 3 HTML

  HTML是一种标记语言，HTML的全称:Hypertext Markup Language,超文本标记语言。学习HTML，主要是在学习标记。
  HTML负责一个页面的内容，实现页面中的图片、超链接、按钮、列表、输入框等等。

######   1）创建第一个HTML页面

  

```properties
  Java程序：xx.java    HelloWorld.java
    world文档：xx.doc
    记事本文档:xx.txt
    html页面：xx.html
```



######   2）HTML文档的结构

​    

```properties
头  <head></head>
    体  <body></body>
    HTML文档的开始和结束： <html></html>
    版本信息：<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"> 可以省略的
```



######   3）标记：是尖括号<>包围的单词，很多标记都是成对出现的，一个是开始标记<??>，一个是结束标记</??>

######   4）HTML中的专业术语

​    

```properties
1）元素：每一对尖括号包围的部分，元素由三部分组成：开始标记、内容、结束标记
    2）属性：用来修饰元素内容的，通常属性写在开始标记中
```



######   5）HTML中的注释：<!-- xxxxxx -->

######   6）HTML中常用的标记

######     一、写在头<head>中的标记

​       

```html
 （1）<title>标记：设置页面的标题
        （2）<meta>标记：a 设置页面自刷新
                         b 设置页面中文编码
        （3）<script>标记：在该标记中主要写JavaScript代码的
        （4）<style>标记：写CSS代码的
        （5）<link>标记：引入CSS代码的
```



###### 二、写在体<body>中的标记

```css
    分类：
​       行内标记：不会另起一行的标记 <font> <strong> <em>...
​       块标记：会另起一行的标记 <h1>~<h6> <center> <p>...

######     （
```



```html
###### 1）<h1>~<h6>标记：标题标记，在HTML中设定了6个标题标记，分别为<h1>~<h6>标记，数字越小，级别越高 显示的文字越大，字体都是加粗的效果。

######     （2）<font>标记：用于设置字体、字号（1-7）和颜色

######     （3）<strong>、<b>标记：加粗标记

######     （4）<br/>标记：换行标记

######     （5）<em>、<i>标记：斜体标记

######     （6）<u>标记：下划线标记

######     （7）<center>标记：居中标记

######     （8）空格标记：转移标记的特点是&开始，不用<> &nbsp;表示一个空格
    （9）大于、小于标记：&lt; 小于    &gt;大于
    （10）<p>标记：段落标记，段落标记的特点在段前和段后各添加一个空行
    （11）<hr/>标记：在页面中画出一条水平线
    （12）<div>、<span>标记：div是典型的块标记，span是典型的行内标记
                             典型在div只会另起一行，span不会另起一行，没有其他功能
                             div和span常用于一个页面的布局

######     （13）文字列表标记

​        ①无序列表   <ul>  <li>
​        ②有序列表   <ol>  <li>

######     （14）超链接、图片标记

​          ① 超链接：<a>标记  
​                       属性：href=""超链接的跳转地址
​                             target=""超链接的跳转方式  _self本页面内部发生跳转的方式(默认)
​                                                       _blank 新页面发生页面跳转的方式
​          ② 图片：<img>标记
​                     属性：src=""所显示的图片名称
​                           width="" 设置图片的宽度
​                           height="" 设置图片的高度
​                           title=""设置鼠标指向图片时显示的标题
​                                   （alt=""不建议用，有的浏览器不支持）
​                           border=""设置图片的边框

​           ③图片热点分割技术（将一张图片进行分割）：<map>标记
​                   <area>分割的区域
​                        shape="" 分割区域的形状 （rect矩形  circle圆）
​                        coords="" 分割区域的坐标（左上,右下的坐标值   圆心,半径）

​           ④返回页面顶部 href="#top"

######     （15）表格标记

          <table>标记：表示表格的开始和结束
          <tr>标记： 行
          <td>标记：列
          <caption>标记：表格的标题，存在于表格的正上方
                         （写在table标记里，第一个tr的上面）
          属性：
            border=""：设置表格的边框
            cellspacing=""：表格中行列之间的空隙（0~）
            width="" :设置表格的宽度
            height="" 设置表格的高度
            align="" 水平对齐方式    left左对齐  center居中对齐  right右对齐 
              （在table标记中使用，让表格整体的左，中，右对齐
                在tr标记中使用，让这一整行的内容左，中，右对齐
                在td标记中使用，单独让一个单元格的内容左，中，右对齐
               ）
            valign=""垂直对齐方式 top顶部对齐 middle居中对齐 bottom底部对齐
              （valign只能用在tr或者td中,不能在table标记中使用）

​           表格的跨行和跨列
​               跨行：从上往下垂直方向合并单元格  属性:rowspan="数字" 数字表示跨几行
​               跨列：从左往右水平方向合并单元格  属性:colspan="数字" 数字表格跨几列

​           <marquee>标记：能够将标记中的内容做成漂移的效果
```



######     （16）表单标记

​     

```properties
  表单：一个表中列出的很多单项，这些列出的单项可用于收集用户的信息。
       比如输入框，单选按钮，多选按钮等都是表单中的单项。
       
       表单的标记：<form>
     
       表单中的单项分类：
         一、input标记系列
           ①单行文本框   type="text"
           ②单行密码框   type="password"
           ③单选按钮     type="radio"
           ④多线按钮     type="checkbox"
           ⑤文件域       type="file"
           ⑥提交按钮     type="submit"
           ⑦重置按钮     type="reset"
           ⑧普通按钮     type="button"
           ⑨图片域(按钮) type="image" 在表单中借助于input标记显示图片，
                                       该图片具有和提交按钮相同的功能
           ⑩隐藏域       type="hidden" 隐藏域用于将数传递给服务器端，
                                        但是不想在页面中看到

​         input标记中的常用属性：
​           type=""属性：
​           name=""属性：
​           value=""属性:
​           checked=""属性：只对type="radio"和"checkbox"起作用，设置单选或者多选
​                           按钮是否处于被选中状态
​           disabled=""属性：设置表单中的单项为不可用，灰色状态。
​                            赋值的内容disabled="disabled"
​           maxlength=""属性：只对type="text"和"password"起作用，设置输入
​                             文字的个数

​         二、非input标记系列
​          ①下拉列表框

            <select>标记：表示下拉列表框的开始和结束
            <option>标记：下拉列表框中每一个列表项             

​            属性：
​               name="" :写在<select>标记中
​               value="":写在<option>标记中
​               selected="":设置下拉列表框默认选择的列表项
​                           selected="selected"
​               size=""设置列表框中显示的选项数量

​          ②多行文本域

            <textarea>标记

​              属性：
​                name=""：
​                cols="":设置列数（宽度）
​                rows="":设置行数（高度）
​                disabled=""设置不可应
​              CSS样式：设置多行文本域的大小不可调节
​                sytle=""    resize:none大小不可调节
​                            color:red  字体颜色为红色
```



#### 4 HTML5

  在HTML4版本上提供了更多，功能更加强大的标签，H5可以充分满足Web应用多元化的需求，通过使用H5，开发人员
  可以很轻松地在网页中实现音频、视频的嵌入，动画效果，表单自动验证等。
  如果不用H5新增的这些强大标签，要实现上述那些功能，需要第三方插件或者JavaScript，或者大量代码才能实现。
  H5对音频，视频，地理定位等功能的良好支持，直接决定了在移动设备的Web应用，和游戏方面。

######   4.1 检查浏览器对HTML5支持

​      浏览器是否支持<canvas>标记，那就支持HTML5

######   4.2 HTML5页面的结构

​      相对于HTML4比，语法结构更加简便了。
​      （如：版本信息，meta标记等）

#### 5、HTML5的表单

```properties
   <fieldset>标记：可以将表单中的内容分组
   <legend>标记：分组后的表单定义标题
```

   5.1 新的input标记中的类型

#####        1）type="email"类型   输入框，该输入框用于输入电子邮件地址。

​                             如果在输入框输入的内容不符合电子邮件的格式，
​                             提交表单时会给出错误提示
​           multiple=""属性：如果值为true，该输入框允许用户输入多个电子邮箱，用
​                            逗号隔开
​      

#####    2）日期时间类型

​    

```css
  H4中通常通过第三方JavaScript插件来提供日期输入界面
      H5中定义如下类型就可在页面中生成一个日期时间类型的输入框
      type="time"        时间
      type="datetime"
      type="datetime-local"
      type="date"      日期/天
      type="week"      星期
      type="month"     月份
```



#####     3）range类型

​    

```css
   在页面中生成一个滑块，通过移动该滑块，选择值
       type="range"
       属性：min=""  设置滑块的最小值
             max=""  设置滑块的最大值
```



#####    4）search类型

​     在H5中，当一个input标记的类型设置为search时，该输入框用于输出查询的关键字
​     
​     说明：search类型的input标记和text类型的input标记相似，可以正常接收输入
​           的字符串信息。
​           但是也有区别，区别是search类型input标记，在输入内容后显示叉号，点击
​           叉号会清空输入的内容。

#####    5）number类型

​      是一个数字类型的文本输入控件。number类型的输入框只允许输入数字类型的内容

#####    6）url类型

​      生成一个只允许输入网址格式的输入框

####    5.2 H5中新增的input标记的属性

#####        1）autofocus=""属性

​        

```properties
  该属性主要用于设置在页面加载完毕后，页面中控件是否自动获取焦点。
          所有的input标记都支持autofocus属性，属性的值为true，自动获得焦点，
          如果值为false，不自动获取焦点（浏览器兼容问题，不写）
```



#####    2）pattern=""属性

   

```properties
  该属性主要用于设置正则表达式，以便对输入的内容进行自定义验证。
     正则表达式语法：以^开始  以$结束

- 表示匹配零次到多次

- 表示匹配一次到多次（至少有一次）

  ​                    []中括号表示匹配括号中一个字符 范围描述
  例子：[0-9a-zA-Z]
  ​                    {}大括号用于限定匹配次数
  例如{n}表示匹配n个字符
  ​    {n,}表示至少匹配n个字符，n到多个
  ​    {n,m}表示至少n个，做多m个。 n到m个,范围
```



#####   3）placeholder属性

 

```properties
    该属性用于设置输入框中默认显示的内容。
     当在输入框中输入内容后，该提示内容消失；当清空输入框输入的内容时，
     该提示内容又显示了。
```



#####    4）required属性

   

```properties
  该属性主要用于设置输入框是否必须输入信息（检测是否为空）
     如果required的值为true，提交表单时输入框不允许为空
     如果required的值为false，提交表单时输入框允许为空
```


​        

#####    5）min属性和max属性

​      

```properties
这两个属性主要用于数值类型或者日期类型的input标记
      用于限制输入框所能输入的数值范围
```



#####    6）step属性

  

```properties
   该属性主要用于数值型或日期类型的input标记，用于设置每次输入框内数值
     的增加或减小的变化量。
```



#####     7）novalidate属性

   

```properties
   该属性用于表单设置不验证
      novalidate="true"
```



#### 6 JavaScript技术

  互联网开发     Browser(浏览器)      /    Server(服务器)
             (html css JavaScript)        Servlet技术 SSH M框架等技术

#####   1）概念：

​     JavaScript是一种在浏览器端运行的脚本语言，有自己的语法，JavaScript是写在html页面中。

#####   2）功能：

​     （1）数据验证
​     （2）动画效果
​     （3）浏览器的版本，类型等
   （说明：JavaScript实现的任何功能都是在函数里完成的）

#####   3）体验神奇的JavaScript

​    （1）直接嵌入式写法
​         将JavaScript代码写在html里的

​     （2）文件调用式写法
​     将JavaScript代码写在.js文件里，在html页面中引入.js文件

#####   4）获取标签对象

​     document是JS中提供的内置对象
​     document.getElementById();  根据id的值获取body体中的标记

```javascript
 声明变量，js是一种弱类型的语言，声明变量统一用var类型
 java:   int age=20;
         double d=3.14;
         char c='男';
         String name="张三";
         System.out.println(age);
 javascript： var age=20; 
              var d=3.14;
              var c='男';
              var name="张三";
           alert(age);
```



Web开发-->互联网开发-->Browser/Server
Web开发基础
  HTML5         -- 页面的内容（<a><img><table><form><b>...  ）
  CSS           -- 美化页面  style=""添加样式
  JavaScript    -- 页面端动态效果（数据验证，动态效果）

JavaScript

#####  1)写法

  （1）直接嵌入式写法
  （2）文件调用式写法

#####  2）获取标签对象

​    document.getElementById() 

```css
xx.style        获取css样式
xx.value        获取具有value属性标记的值
xx.innerHTML    获取没有value鼠标标记的值（<div> <span> <h1> <p>..） 
```



#### 7 HTML5关于多媒体的应用

  HTML在诞生的时候，完全是静态的世界。
  HTML4只能通过第三方插件（JavaScript jquery等），能够在页面中支持音频、视频等
  HTML5，只需要浏览器是支持HTML5技术的，就可以不借助于任何的第三方插件，直接用标记实现音频，视频。

#####   7.1）视频

```css
       <video>标记是用于显示视频的

​         

   属性： src="" 将要播放视频的路径/名称
          autoplay="" 在页面加载完毕后是否自动播放
          width=""  height="" 设置大小，只适用于视频<video>标记
          controls="" 该属性用于在页面播放器面板上，显示控制按钮工具栏
          poster="" 在点击视频播放之前，显示的内容
          （注意：去掉autoplay=""属性。如果不去掉，页面加载完直接自动
           播放视频，看不到播放前的内容了）
```



#####   7.2）音频

       <audio>标记是用于显示音频的

```css
   属性：src="" 
         autoplay="" 
         controls=""
```

#####   7.3）error属性

 

```css
多媒体在加载读取的时候如果出现了错误，用error提示错误

 （onclick="" ondblclick="" onmouseover="" onmouseout=""）

  事件监听  onerror="" 监听多媒体播放中出现的错误

  error.code获得错误代码号   如果代码号为4，是视频播放的格式不正确
```



#####   7.4）networkState属性

 

```css
   该属性用于返回加载媒体文件的网络状态

事件监听   onprogress="" 浏览器在加载视频/音频时触发的事件监听

video.networkState属性的返回值
```



###### 1）等于1  表示媒体加载成功，等待播放请求

###### 2）等于2  表示正在加载媒体信息

######   7.5）H5中多媒体播放的方法

​      

```html
load()方法：该方法用于重新加载待播放的媒体文件。
      play()方法：该方法用于播放媒体文件
      pause()方法：该方法用于暂停播放的媒体文件
```



######   7.6）H5中多媒体的事件

​      

```css
onerror=""       该事件监听多媒体播放中出现的错误
      onprogress=""    该事件监听浏览器在加载多媒体时的触发
      ontimeupdate=""  当前播放时间改变，正常播放、快进、拖动播放进度条都会
                       触发该事件
       currentTime获取已经播放的时长
       duration   获取总时长
       Math.floor(number)  取小于或者等于参数的最大整数
```

​       

#### 8 HTML5中的图像和动画

#####   一、图像

```css
  H5中实现了绘画操作，主要是依赖<canvas>标记以及canvas相关的属性和方法

  <canvas>从字面上理解是画布的意思，在页面中就相当于在网页中添加了一块画布
    属性：sytle="" 添加css样式，给画布添加边框，画布的背景色
          width=""
          height="" 设置画布区域的大小
```



#####    8.1 一个简单的canvas画图实例

​       （在画布中画一个矩形）

  

```css
  getContext("2d")   ---> 获得2d类型的画笔，该画笔画平面图形
    strokeRect(x,y,width,height) -->画一个矩形
```



#####    8.2 使用路径画图

​       H5中路径是绘图的基础，使用路径画图主要是绘制一些基本的线条、曲线等。

######    （1）使用moveTo、lineTo画线

   

```css
    moveTo(x,y)   绘制直线的起始坐标

​       lineTo(x,y)   结合moveTo一起使用，绘制直线的终点坐标

​       stroke()      结合moveTo和lineTo一起使用，该方法是将定义好的轨迹在画布上绘制并展示
```



######    （2）使用arc方法画弧形

 

```css
     arc(参数1，参数2，参数3，参数4，参数5，参数6)

​      参数1：表示绘制弧形曲线圆心的横坐标
​      参数2：表示绘制弧形曲线圆心的纵坐标
​      参数3：表示绘制弧形曲线的半径
​      参数4：表示绘制弧形曲线的开始弧度
​      参数5：表示绘制弧形曲线的结束弧度
​               弧度=（Math.PI/180）*度
​               Math.PI=3.141592653589793
​      参数6：表示绘制弧形曲线的方向，该参数为布尔类型的值；
​                如果为true时，按照逆时针方向绘制弧形
​                如果为false，按照顺时针方向绘制弧形

​      stroke()  该方法按照设定好的轨迹在画布上绘制并展示出来
​                所以arc方法使用后，记得使用stroke方法。
```



#####    8.3 图形操作

###### **1）图形样式的设置**

   

```css
fillStyle=""属性： 设置画笔的样式（css样式，一个图案，一个渐变）
   fillRect(x,y,width,height)方法：填充一个矩形（矩形实心）

​                                                                                                                                               

   strokeStyle=""属性:和fillStyle用法相同
   strokeRect(x,y,width,height)方法：画一个矩形（矩形空心）

   clearRect(x,y,width,height)方法：清除指定矩形区域
```



##### 2）渐变图形

   渐变在网页设计中是经常用到的一种技术手段，指的是图形填充颜色从一种颜色逐渐的转变为另一种颜色
   HTML5中实现渐变的两种方式：线性渐变和径向渐变。

######    （1）线性渐变

​      

```css
  指的是点到点之间的渐变。
        在HTML5中通过createLinearGradient方法实现的。
        createLinearGradient(参数1，参数2，参数3，参数4)
            参数1：渐变起始点的横坐标
            参数2：渐变起始点的纵坐标
            参数3：渐变终止点的横坐标
            参数4：渐变终止点的纵坐标
         addColorStop(参数1，参数2)设置渐变颜色及渐变度的方法
            参数1：该参数是一个浮点类型的值，范围0.0到1.0之间，表示渐变的开始点和结束点
                   的一部分。参数1的值为0对应开始点，如果为1.0，对应的是结束点
                   （0.0对应上述方法的参数1和参数2
                     1.0对应上述方法的参数3和参数4
                    ）
             参数2：渐变使用的颜色
```



######    （2）径向渐变

​    

```css
    指的是以圆心为起点，沿圆形半径方向向外扩散方式逐渐改变颜色               
        createRadialGradient(参数1，参数2，参数3，参数4，参数5，参数6);
        参数1：渐变开始圆的圆心横坐标
        参数2：渐变开始圆的圆心纵坐标
        参数3：渐变开始圆的半径
        参数4：渐变结束圆的圆心横坐标
        参数5：渐变结束圆的圆心纵坐标
        参数6：渐变结束圆的半径
```



###### 3）图形坐标的变换

   **（1）坐标平移** 
     

```css
   指的是将默认坐标系的原点，沿x轴方向或y轴方向移动指定单位的长度。
        translate(x,y)
        参数x：为沿x轴方向位移的长度
        参数y：为沿y轴方向位移的长度
```

   **（2）坐标放大**
       

```css
 指的是将图像沿x轴方向或者y轴方向放大的倍数
        scale(x,y);
        参数x：沿x轴方向放大的倍数
        参数y：沿y轴方向放大的倍数

​        注意：使用scale方法，如果参数值是大于1的图形将被放大，如果参数值
​              是小于1的图形将被缩小
```

   **（3）坐标旋转**
     

```css
   指的是以原点为中心，将图形旋转指定的角度。
        rotate(angle)
        参数angle表示旋转的弧度，angle如果为正值，图形按照顺时针旋转
        如果angle的值为负值，图形按照逆时针旋转

​       弧度=(Math.PI/180)*度
```

   **4）绘制图片**
    

```css
  drawImage(参数1,2,3) 直接绘制图片
          参数1：哪张图片
          参数2和3：将图片画在画布上的坐标位置

  drawImage(参数1,2,3,4,5)  绘制缩放图片
     参数1：哪张图片
     参数2和3：将图片画在画布上的坐标位置
     参数4和5：将图片画在画布上的宽度和高度

  drawImage(参数1,2,3,4,5,6,7,8,9)
     参数1：哪张图片
     参数2和3：图片被绘制部分的坐标
     参数4和5：图片被绘制部分的宽度和高度

​     参数6和7：将图片画在画布上的坐标位置
​     参数8和9：将图片画在画布上的宽度和高度
```

   **5）绘制文字**
     

```scss
 fillText("",x,y)
      strokeText("",x,y)
```

   **6）制作动画**
      

```scss
setInterval(参数1，参数2)
      参数1：设置要执行的绘图函数
      参数2：设置时间间隔，单位毫秒
```

  功能：按照设置的时间间隔，反复执行参数1中的函数