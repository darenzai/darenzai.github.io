---
title: Linux文本编辑器使用
date: 2019-11-10 08:17:00
author: 胡佳艺
img: http://ptagesjik.bkt.clouddn.com/blog/20190619/O5hBoFRg6Eos.jpeg?imageslim
top: false
cover: false
coverImg: /images/1.jpg
password: 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
toc: false
mathjax: false
summary:  Linux文本编辑器使用
categories: Linux
tags: 
  - Linux
---



# Linux文本编辑器使用

###  简述

Vi命令是Unix操作系统和类Unix操作系统中最通用的全屏幕纯文本编辑器。Linux中的Vi编辑器叫Vim，它是Vi的增强版（Vi Improved），与Vi编辑器完全兼容，而且实现了很多增强功能。

 Vi编辑器支持命令模式、编辑模式和末行模式。


命令模式：在该模式下是不能对文件直接编辑，可以输入快捷键进行一些操作（删除行，复制行，移动光标，粘贴等等）【打开文件之后默认进入的模式】；

 编辑模式：在该模式下可以完成文本的编辑功能；


末行模式：可以在末行输入命令来对文件进行操作（搜索、替换、保存、退出、撤销、高亮等等）；

要正确使用Vi编辑器就必须熟练掌握着两种模式的切换。默认情况下，打开Vi编辑器后自动进入一般模式。从编辑模式切换到命令模式使用“Esc”键，从命令模式切换到编辑模式使用“A”、“a”、“O”、“o”、“I”、“i”键。


![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/pKLktdzTDnGF.png?imageslim)



### Vim的打开文件的方式（要求掌握的就前三种）：

**（1）#vim 文件路径**  

​	作用：打开指定的文件


**（2）#vim  +数字  文件的路径**  

​	作用：打开指定的文件，并且将光标移动到指定行


**（3）#vim  +/关键词  文件的路径**  

​	作用：打开指定的文件，并且高亮显示关键词


**（4）#vim 文件路径1 文件路径2 文件路径3**   

​	作用：同时打开多个文件，进入末行模式： “:open file1 ”



**（5）vim -on file1 file2 ...其中:**

​	o(是小写字母o,不是数字零)n(表示你要分屏的文件个数)

作用：vim水平分屏的使用 ；文件之间的切换（ctrl+w）



（6）**vim -On file1 file2 .....**


​	其中:O(是大写字母O,不是数字零)n(表示你要分屏的文件个数)

作用：vim垂直分屏；文件之间的切换（ctrl+w）





### **（一）**命令模式

注意：该模式是打开文件的第一个看到的模式（打开文件即可进入）

#### **1**、光标移动

*①光标移动到行首*

​	按键：shift + 6 或 ^（T字母上面的6，不要按小键盘的6）

 *②光标移动到行尾*

​	按键：shift + 4 或 $（R字母的左上角的4，不是小键盘的4）

 *③光标移动到首行*

​	按键：gg


 *④光标移动到末行*

​	按键：G


 *⑤翻屏*	

​	向上翻屏：按键ctrl + b   （before）或   PgUp


​	向下翻屏：按键ctrl + f     （after）或       PgDn





#### 2**、复制操作**

*①复制光标所在行*

​	按键：yy

​	粘贴：在想要粘贴的地方按下p键

 


*②以光标所在行为准（包含当前行），向下复制指定的行数*

​	按键：数字yy


 


*③可视化复制*

​	按键：ctrl + v（可视块）或V（可视行）或v（可视），然后按下↑↓←→方向键来选中需要复制的区块，按下y	键进行复制，最后按下p键粘贴



###### 


##### **4**、撤销****/****恢复**

​	撤销：输入:u （不属于命令模式）  或者   u  （undo）

​	恢复：ctrl + r  恢复（取消）之前的撤销操作

 


##### **5**、扩展****1****：光标的快速移动**

​	*①快速将光标移动到指定的行*


按键：数字G    


 


​	****②以当前光标为准向上/向下移动n行****


按键：数字↑，数字↓

 


*③以当前光标为准向左/向右移动n字符*

按键：数字←，数字→

 

*④末行模式下的快速移动方式：移动到指定的行*

按键：输入英文“:”，其后输入行数数字，按下回车

 




### **（二）**、末行模式

进入方式：由命令模式进入，按下“:”或者“/（表示查找）”即可进入

退出方式：

 	 a. 按下esc

  	b. 连按2次esc键

​	  c. 删除末行全部输入字符

 *①保存操作（write）*

​	输入：“:w”  保存文件

​	输入：“:w  路径”  另存为 


*②退出（quit）*

​	输入：“:q”  退出文件

*③保存并退出*

​	输入：“:wq”  保存并且退出


*④强制 （!）*

​	输入：“:q!”  表示强制退出，刚才做的修改操作不做保存


*⑤搜索/查找*

​	输入：“/关键词”然后回车“Enter”


​	例如：我想在passwd文件中搜索“sbin”关键词

**在搜索结果中切换上**/下一个结果：N/n **（**next）

如果需要取消高亮，则需要输入：“:nohl”【no highlight】



*⑥替换*

​	:s/搜索的关键词/新的内容  替换光标所在行的第一处符合条件的内容

​	:s/搜索的关键词/新的内容/g  替换光标所在行的全部符合条件的内容

​	:%s/搜索的关键词/新的内容  替换整个文档中每行第一个符合条件的内容

​	:%s/搜索的关键词/新的内容/g  替换整个文档的符合条件的内容

 

%表示整个文件

g表示全局（global）

 

*⑦显示行号（临时）*

输入：“***:set nu***”[number]

如果想取消显示，则输入：“:set nonu”



###  按键操作



​        按『sp』                分页显示

​        按『close』           关闭当前页面

​        按『new』             新建页面

​        按『wqall』           退出并保存所有页面

​        按『qall!』             不保存退出所有页面

​        按『ctrl+w』          页面之间切换

​        按『e』filename    打开文本文件

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/9HwlAaxzakO6.png?imageslim)

​	重点看前2个进入方式：i（insert）、a（after）。

​	退出方式：按下esc键


​        .vimrc是Vim的配置文件，通过此文件可以对用户的Vim的使用环境进行定制。.vimrc是隐藏文件，保存在用	户的主目录里。

​     

```properties
         set nu                    显示行号 

​        syntax on                 语法高亮度显示

​        set ruler                 底部显示行列号

​        set autoindent            使用自动对齐

​        set smartindent           智能的选择对齐方式

​        set background=dark       背景使用黑色

​        set cursorline            突出显示当前行

​        set tabstop=4             设定 tab 长度为 4


```





[引用自老师的PPT]: 

