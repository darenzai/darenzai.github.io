---
title: Linux进程复习
date: 2019-05-21 10:21:00
author: 胡佳艺
img: /images/首页14.jpg
top: false
cover: false
coverImg: /images/1.jpg
password: 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
toc: false
mathjax: false
summary: Linux进程知识复习。
categories: Linux
tags:
  - Linux
---





# Linux进程复习

### 指令：ps

显示当前用户的进程

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/OD0TMX8r3Rnw.png?imageslim)



### 指令：ps aux

显示所有进程详细信息

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/18DfE9cVwcKV.png?imageslim)





### 指令：ps - ef 

显示所有进程详细信息

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/im6QYKzxN9gc.png?imageslim)



![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/zb5NErqe4np0.png?imageslim)



### 指令 ：ps -ef|grep  进程名 

过滤出想要的进程信息

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/B6XWS9DQJ433.png?imageslim)



![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/HQdGbLlGnJs7.png?imageslim)

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/L2ukbxmWLDPP.png?imageslim)

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/XGj63TLUeu2b.png?imageslim)



### 指令：pstree

功能：使用树形结构显示进程间的关系

格式：pstree  【选项】  【进程号或者进程名】

使用说明：

​        如果不指定进程号或用户名称，则会把系统启动时的第一个进程视为根，并显示之后的所有进程。若指定用户名称，便会以隶属该用户的第一个进程当作根，然后显示该用户的所有进程。

​        选项：

​        -a 　显示每个程序的完整指令，包含路径，参数或是常驻服务的标示

　　-c 　不使用精简标示法

　　-h 　列出树状图时，特别标明现在执行的程序

　　-l 　采用长列格式显示树状图

　　-n 　用进程号排序。预设是以程序名称来排序

　　-p 　显示进程号

　　-u 　显示用户名称

　　-V 　显示版本信息

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/q25vG7U8MNbw.png?imageslim)





### 指令：kill

表示杀死进程

ps -ef  查看进程   

为了避免杀死某些进程我就不展示了。









