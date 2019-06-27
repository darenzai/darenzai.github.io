---
title: Servlet获取JSP表单内容
date: 2018-09-07 09:25:00
author: 胡佳艺
img: /images/首页20.jpg
top: false
cover: true
coverImg: images/首页21.jpg
password: 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
toc: false
mathjax: false
summary: 用Servlet获取Jsp表单里面的内容，然后打印出来。
categories: JavaWeb
tags:
  - JSP
  - Servlet
---



### JSP提交表单简单方式不含复选框部分

```javascript
  <form action="./servlet/Check" method="post">
  name:<input type="text" name="username" /><br/>
  pawd:<input type="password" name="pwd" /><br/>
  <input type="hidden" name="hidden" value="隐藏" />
  <input type="submit" value="submit"/>
  </form>
```



### 接着在就是获取以上的值 

```java
PrintWriter out = response.getWriter(); 

String u = request.getParameter("username"); 

String p = request.getParameter("pwd");

String hd=request.getParameter("hidden"); 

out.print(u);//输出用户名
```

