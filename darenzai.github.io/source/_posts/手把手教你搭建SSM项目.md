---
title: 手把手教你搭建SSM项目
date: 2018-10-11 08:17:00
author: 胡佳艺
img: https://ws3.sinaimg.cn/large/005BYqpggy1g4325cpa13j31900u0e8c.jpg
top: false
cover: false
coverImg: /images/1.jpg
password: 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
toc: false
mathjax: false
summary: Eclipse搭建SSM项目的基本步骤。
categories: Spring
tags: 
  - SSM
---



## 手把手教你搭建SSM项目

打开File->NEW ->Maven Project

![1555723865658](https://ws3.sinaimg.cn/large/005BYqpggy1g4327iyj18j30vx0kqdj7.jpg)



选择默认存储空间，点击下一步

![1555723977409](https://ws3.sinaimg.cn/large/005BYqpggy1g4328fk6c1j30lu0i7abe.jpg)

选择创建的Maven类型，点击下一步

![1555724147996](https://ws3.sinaimg.cn/large/005BYqpggy1g4328fk6c1j30lu0i7abe.jpg)





填写类路径

![1555724256164](https://ws3.sinaimg.cn/large/005BYqpggy1g4328fk6c1j30lu0i7abe.jpg)

项目创建完了，在Package Explorer列显示

![1555724378847](https://ws3.sinaimg.cn/large/005BYqpggy1g4328fk6c1j30lu0i7abe.jpg)

出现这个错误很正常，那是因为我们还没有给项目添加Tomcat服务器

![1555724500923](https://ws3.sinaimg.cn/large/005BYqpggy1g4328fk6c1j30lu0i7abe.jpg)









![1555724702022](https://ws3.sinaimg.cn/large/005BYqpggy1g4328fk6c1j30lu0i7abe.jpg)





![1555724728672](https://ws3.sinaimg.cn/large/005BYqpggy1g4328fk6c1j30lu0i7abe.jpg)





![1555724806342](https://ws3.sinaimg.cn/large/005BYqpggy1g4328fk6c1j30lu0i7abe.jpg)









![1555724824798](https://ws3.sinaimg.cn/large/005BYqpggy1g4328fk6c1j30lu0i7abe.jpg)







![1555724911740](https://ws3.sinaimg.cn/large/005BYqpggy1g432g6ngr1j30ye0l9dky.jpg)







项目启动成功



![1555725176028](https://ws3.sinaimg.cn/large/005BYqpggy1g432hrcg5sj30sg0lc782.jpg)



打开路径下的POM文件

![1555725263870](https://ws3.sinaimg.cn/large/005BYqpggy1g432jpcwnjj30sg0lc43h.jpg)





我们用Maven形式导入jar包，百度搜索Maven 我们进入maven仓库进去查找我们需要的jar包



![1555725475068](https://ws3.sinaimg.cn/large/005BYqpggy1g432k2pbaij30ph0jggoc.jpg)



我们以搜索MySQL为例



![1555725637596](https://ws3.sinaimg.cn/large/005BYqpggy1g432kpu32bj30oc0jpjuv.jpg)



这里面就有我们想要的 jdbc 连接jar包，选择好自己想要的版本



![1555725737046](https://ws3.sinaimg.cn/large/005BYqpggy1g432l4o9hcj30o50kw41a.jpg)







![1555725992641](https://ws3.sinaimg.cn/large/005BYqpggy1g432lhkljij30z10ss12u.jpg)







![1555726102410](https://ws3.sinaimg.cn/large/005BYqpggy1g432luyst8j30tx0icgnj.jpg)



我们已经看到负责数据库连接的Jar已经自动下载完成了，由于我们要完成的是SSM项目所有我们还要去复制几段依赖我这里就不一一赘述了。

![1555726153260](https://ws3.sinaimg.cn/large/005BYqpggy1g432m5wvfhj30j30eeta4.jpg)



连续去终于那个仓库复制了 几个依赖以后可能会出现排版混乱的情况 我们用快捷键 Ctrl+Shift+F   

来重新排一下版

![1555726569345](https://ws3.sinaimg.cn/large/005BYqpggy1g432mo4c9oj30gb0bqq4j.jpg)



我们创建一个数据库表

![1555727892833](https://ws3.sinaimg.cn/large/005BYqpggy1g432mxt2o8j30c20623yi.jpg)

然后我们修改数据库时区

![1555832242131](https://ws3.sinaimg.cn/large/005BYqpggy1g432n8p0akj30g808o0ss.jpg)



下一步我们创建实体类，并设置get和set方法



![1555832416456](https://ws3.sinaimg.cn/large/005BYqpggy1g432nijz8xj30sg0lc78q.jpg)





创建Mapper接口（注意一点在导入List 的时候 注意看清之后再导入，否则很容易导入 awt.List,正确导入的应该是util.ist）

![1555833238452](https://ws3.sinaimg.cn/large/005BYqpggy1g432ntpg5vj30sg0lcn27.jpg)



下面我们在Mapper.xml

![1555834665605](https://ws3.sinaimg.cn/large/005BYqpggy1g432o2sx3pj30tt0itwga.jpg)



我们编写Userserevice接口文件

![1555835118449](https://ws3.sinaimg.cn/large/005BYqpggy1g432oef76aj30t70iedgj.jpg)





![1555835305040](https://ws3.sinaimg.cn/large/005BYqpggy1g432pwr6rbj30sv0i7myi.jpg)







![1555835610210](https://ws3.sinaimg.cn/large/005BYqpggy1g432qgor82j30tz0iyabg.jpg)

