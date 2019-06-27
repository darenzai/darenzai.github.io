---
title: Linux文件系统复习
date: 2019-04-12 08:27:00
author: 胡佳艺
img: http://ptagesjik.bkt.clouddn.com/blog/20190619/nJkA6mLwlhFS.jpeg?imageslim
top: false
cover: false
coverImg: /images/1.jpg
password: 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
toc: false
mathjax: false
summary: 这学期学了Linxu操作系统，其实之前有自学过但是这些东西老师容易忘，所以写博客记录一下。
categories: Linux
tags:
  - Linux
---





# **Linux文件系统复习**



#### **Linux系统目录**

| **常见的Linux系统目录如下：**                                |
| ------------------------------------------------------------ |
| **/：Linux系统的根目录，包含Linux系统所有目录和文件。**      |
| **/etc：有关系统设备与管理的配置文件。**                     |
| **/sbin：存放系统启动时所需的运行程序。**                    |
| **/bin：该目录中含有常用的命令文件，不能包含子目录。**       |
| **/boot：操作系统启动时的核心文件。**                        |
| **/usr/local：存放用户后期安装的应用程序文件。**             |
| **/root：超级用户主目录。**                                  |
| **/dev：接口设备文件目录，保存外围设备代号。**               |
| **/mnt：设备文件的挂接点，默认有/mnt/cdrom和/mnt/floppy两个目录，分别用于挂载光驱和软驱。** |
| **/**                                                        |
| **home**                                                     |
| **：用户的宿主目录，通常将其设置在独立的分区**               |



### **输出重定向指令**

**一般命令的输出都会显示在终端中，有些时候需要将一些命令的执行结果想要**

**保存到文件中进行后续的分析/统计，则这时候需要使用到的输出重定向技术。**

**\> ：覆盖输出，会覆盖掉原先的文件内容**

**\>>：追加输出，不会覆盖原始文件内容，会在原始内容末尾继续添加**

**ls >>+文件名** 

**输出追加重定向，不存在会创建出来，把显示的目录文件都放到txt中保存**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/Y7oE12mIpSTd.png?imageslim)



### **pwd指令**

**用法：#pwd**

**含义：（print working directory，打印当前工作目录）**

![1560843243722](http://ptagesjik.bkt.clouddn.com/blog/20190618/D6emYU5R1p0J.png?imageslim)



### **指令：mkdir**    

**含义：（make directory，创建目录）**

**注意：ls列出的结果颜色说明，其中蓝色的名称表示文件夹，白色的表示文件，绿色的其权限为拥有所有权限。**

**![1560843349685](assets/1560843349685.png)**

**语法2：#mkdir** -p 路径****


**含义：当一次性创建多层不存在的目录的时候，添加-p参数，否则会报错**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/QUaoJcawdwY1.png?imageslim)**



**语法3：#mkdir** 路径1 路径2 路径3 ….  【表示一次性创建多个目录】****

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/94v8tBYw0Vqw.png?imageslim)**



### **指令：touch**   


**作用：创建文件**

**语法：#touch 文件路径  【路径可以是直接的文件名也可以是路径】**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/S5eETL7K4zCk.png?imageslim)**



### **指令：cp  （copy，复制）**


**作用：复制文件/文件夹到指定的位置**

**语法：#cp**    被复制的文档路径    文档被复制到的路径****

**注意：Linux在复制过程中是可以重新对新位置的文件进行重命名的，**
**但是如果不是必须的需要，则建议保持前后名称一致。****

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/rE1dk5GKE1iT.png?imageslim)**



**当使用cp命令进行文件夹复制操作的时候需要添加选项“-r”****

**【-r表示递归复制】，否则目录将被忽略**


![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/XKs3iORstct7.png?imageslim)**



### **指令：mv   （move，移动，剪切）**



**作用：移动文档到新的位置**

**语法：#mv 需要移动的文档路径  需要保存的位置路径****

**确认：移动之后原始的文件还在不在原来的位置？原始文件是不在原始位置的**


![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/P9rerb3X2c7R.png?imageslim)**



### **指令：rm （remove，移除、删除）**

**作用：移除/删除文档**

**语法：#rm 选项 需要移除的文档路径**

**选项：**

  **-f：force，强制删除，不提示是否删除**

****

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/PaTlBr36zeI0.png?imageslim)**

**-r： r递归删除，删除一个完整目录及其子目录**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/uPL4H70Axmpo.png?imageslim)**



### 指令 cat**

**-A：相当于 -vET 的整合选项，可列出一些特殊字符而不是空白而已；**

**-b：列出行号，仅针对非空白行做行号显示，空白行不标行号！**

**-E：将结尾的断行字符 $ 显示出来；**

**-n：打印出行号，连同空白行也会有行号，与 -b 的选项不同；**

**-T：将 [tab] 按键以 ^I 显示出来；**

**-v：列出一些看不出来的特殊字符**



**cat -n 打印行号****

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/8HT3u8OWARlV.png?imageslim)**



**cat -b 列出行号，仅针对非空白行做行号显示，空白行不标行号！**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/M3TNngjQJtAa.png?imageslim)**



**-T：将 [tab]**
**按键以 ^I 显示出来；**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/hzx7nWOwgAQ0.png?imageslim)**



**-v 列出一些特殊字符**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/VpOQBd9gYiE7.png?imageslim)**



### **nl指令**

​        **功能：以输出行号的方式显示文件。**

​        **格式：nl  [选项] [文件名]**


​        **使用说明：**

​        **nl命令和cat命令很像，不过nl命令会输出行号。**

​        **选项：**

​        **-b指定行号指定的方式，主要有两种：**

　　    **-b a：表示不论是否为空行，也同样列出行号（类似 cat -n）**

　　    **-b t：如果有空行，空的那一行不要列出行号（默认值）**

　　**-n列出行号表示的方法，主要有三种：**

　　    **-n ln ：行号在萤幕的最左方显示**

　　    **-n rn ：行号在自己栏位的最右方显示，且不加 0**


　　    **-n rz ：行号在自己栏位的最右方显示，且加 0**


　　**-w行号栏位的占用的位数**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/rdHvjPTGy7wI.png?imageslim)**









### **man 指令**

**作用：manual，手册（包含了Linux中全部命令手册，英文）**

**语法：#man 命令  （退出按下q键）**

****

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/nIiyIOtyg8JK.png?imageslim)**





### **uptime**指令

**作用：输出计算机的持续在线时间（计算机从开机到现在运行的时间）**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/2sYva5VOCB66.png?imageslim)**



### **ifconfig**指令

**作用：用于操作网卡相关的指令。**


![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/TrmUVxT02Ert.png?imageslim)**





### **uname 指令**

**获取计算机操作系统相关信息**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/K2JXkGeT1E8N.png?imageslim)**



### netstat 指令**

**查看网络的连接状态**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/ic4CHhNyx2ex.png?imageslim)**



**-t 表示只列出tcp协议的连接**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/2ACyo1qmF5lC.png?imageslim)**





**-p：表示显示发起连接的进程pid和进程名称；**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/yzHUNpJBx7P0.png?imageslim)**



**-n：表示将地址从字母组合转化成ip地址，将协议转化成端口号来显示**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/xF1semWtsJOO.png?imageslim)**



### **指令file(确定文件类型)**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/z81qoUUWGBSe.png?imageslim)



### **find**指令****

**作用：用于查找文件（其参数有55个之多）**

**语法：#find 路径范围 选项 选项的值**

**选项：**

​         **-name：按照文档名称进行搜索（支持模糊搜索）**

​         **-type：按照文档的类型进行搜索**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/pwrBAzHxhNFM.png?imageslim)**



**-name 根据文件名查找文件**

**![1560824116988](![mark](http://ptagesjik.bkt.clouddn.com/blog/20190618/qYVomylHY0kc.png?imageslim))**



**-name '*.txt' 搜索目录下所有txt后戳的文件。**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/Jl43B91KhNo3.png?imageslim)**



**使用find来搜索目录下所有的文件夹**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/6aLoXNQCifER.png?imageslim)**



**搜索文件夹下所有文件**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/HVnojs3n9vhV.png?imageslim)**

### **which**指令        

**作用：**

**查看可执行文件的位置**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/1jLhuMBvMN8R.png?imageslim)**



### **locate**指令



​        **功能：查看文件位置。![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/pLsTOTr7STYk.png?imageslim)**



### **df**指令

**作用：查看磁盘的空间**

**语法：**#df -h  -h表示以可读性较高的形式展示大小****

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/VxBz0zvdm2yT.png?imageslim)**



**df -h**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/sSUgY4cbCDQc.png?imageslim)** 



### **free**指令

**作用：查看内存使用情况**


**语法：**#free -m   -m表示以mb为单位查看，-h表示以可读性较高的形式展示大小****


![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/UdVG85G35DLJ.png?imageslim)**



**-m 以mb的形式查看**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/OUeOqCfoOu1X.png?imageslim)**



**-h 以高可读性形式显示**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/fcwGscp9HRom.png?imageslim)**



### **head**指令

**作用：查看一个文件的前n行，如果不指定n，则默认显示前10行。**


**语法：**#head  -n**  文件路径   【n**表示数字】****


![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/2OyBE9HBqAKN.png?imageslim)**





### **tail**指令

**作用1：查看一个文件的未n行，如果n不指定默认显示后10行**

**语法：**#tail  -n**  文件的路径    n**同样表示数字****

**![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/eB5y2oev0mJE.png?imageslim)**



**tail -f**

**该命令一般用于查看系统的日志比较多。**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/7yQNT7ll4G6b.png?imageslim)**



### **less指令**

**查看文件，以较少的内容进行输出，按下辅助功能键（数字+回车、空格键+上下方向键）查看更多**

**语法：**#less**  需要查看的文件路径**

**在退出的只需要按下q键即可。**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/wgtf12Q2qI26.png?imageslim)**



### **wc**指令

**作用：统计文件内容信息（包含行数、单词数、字节数）**

**语法：#**wc**  -**lwc** 需要统计的文件路径**

  **-l**：表示lines，行数****


  **-w：表示words，单词数   依照空格来判断单词数量**

  **-c：表示bytes，字节数**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/aubqUpxkgzMs.png?imageslim)**



### **date指令**

**作用：表示操作时间日期（读取、设置）**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/U0OkDDI0FOL5.png?imageslim)**

**#date  +%F**

**![1560828119770](assets/1560828119770.png)**

**\**



**#date  “+%F %T”    引号表示让“年月日与时分秒”成为一个不可分割的整体**

**%F：表示完整的年月日			 %d：表示日期（带前导0）**

**%T：表示完整的时分秒			%H：表示小时（带前导0）**

**%Y：表示四位年份				%M：表示分钟（带前导0）**

**%m：表示两位月份（带前导0）	 %S：表示秒数（带前导0）	![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/KQ2btu8LUaDu.png?imageslim)**





### **cal**指令****

**作用：用来操作日历的**


**#**cal**    等价于 #**cal**  -1  直接输出当前月份的日历**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/A3nTulbBn2Xv.png?imageslim)**

******

**cal**  -3**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/PJlw7gNCufj3.png?imageslim)**



**cal -y 年份**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/pRj7mBWbl11C.png?imageslim)**



### grep指令

**grep命令用于查找文件中包含有指定字符串的行。**

**常用的选项：**


**•-v：列出不匹配的行**


**•-c：对匹配的行计数**

**•-l：只显示包含匹配模式的文件名**


**•-h：抑制包含匹配模式的文件名的显示**


**•-n:每个匹配行只按照相对的行号显示**


**•-i:对匹配模式不区分大小写**


![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/FWzsSS9kHmnq.png?imageslim)**



### tar指令

**Linux中的打包文件一般是以.tar结尾的，压缩的命令一般是以.gz结尾的。** 
**而一般情况下打包和压缩是一起进行的，打包并压缩后的文件的后缀名一般.tar.gz**

**选项：**

​        **1. 主选项**

​        **-c 创建压缩文档。相当于打包**

​        **-x 解压**

​        **-t 列出文档的内容，查看已经备份了哪些文件**

​        **注意，在参数的下达中， c/x/t 仅能存在一个，不可同时存在，因为不可能同时压缩与解压缩。**

​        **2. 辅选项**

​        **-z 具有 gzip 的属性一般格式为xx.tar.gz或xx. tgz**


​        **-j 具有 bzip2 的属性一般格式为xx.tar.bz2**  


​        **-v 压缩的过程中显示文件**

​        **-f 将文件打包生成到一个文件里，这个选项通常是必选项**


![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/idIakAKa01oh.png?imageslim)**



**解压压缩包** 
**命令：tar [-zxvf] 压缩文件** 
**其中：x：代表解压** 
**可以不用写**z，写z代表指定压缩方式，可以自动识别**** 
**示例：将/test下的txt.tar.gz解压到当前目录下** 

**示例：txt.tar.gz解压**
**tar -**xvf** txt.tar.gz -C /**usr——C代表指定解压的位置****



![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/iyLjjKNY5yHG.png?imageslim)**



### gzip指令

**gzip命令用于对文件进行压缩，生成的文件以“.gz”结尾**

**语法：**
**gzip –v 文件名**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/G9RPqHu3TcDF.png?imageslim)**

**gunzip命令是对以“.gz”结尾的文件进行解压缩。**

**gunzip** 
**-v 文件名**

![mark](http://ptagesjik.bkt.clouddn.com/blog/20190619/z84j44fd9VLa.png?imageslim)**