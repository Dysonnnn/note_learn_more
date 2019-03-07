@echo off      表示在此语句后所有运行的命令都不显示命令行本身 


### echo

@与echo off相像，但它是加在每个命令行的最前面，表示运行时不显示这一行的命令行（只能影响当前行）。


echo= 表示输出空白行


echo enter code directory     显示enter code directory

call 调用另一个批处理文件（如果不用call而直接调用别的批处理文件，那么执行完那个批处理文件后将无法返回当前文件并执行当前文件的后续命令）。


pause 运行此句会暂停批处理的执行并在屏幕上显示Press any key to continue...的提示，等待用户按任意键后继续
若输入PAUSE>NUL 则表示暂停且不提示“按下任意键继续”。


---


### 设置字体颜色和窗体大小：

设置字体颜色：COLOR 02 （0代表背景色，2代表前景色）

常用的颜色有以下值：0 黑色，1蓝色，2 绿色，3 浅绿色，4红色，5紫色，6黄色，7白色，8灰色，9浅蓝，A浅绿，B浅蓝色，C浅红色，D浅紫色，E浅黄色，F亮白色）。

### 设置窗体大小：
MODE CON: COLS=宽度 LINES=高度


--------------------- 
作者：苦逼的IT男 
来源：CSDN 
原文：https://blog.csdn.net/daoming1112/article/details/77197558 
版权声明：本文为博主原创文章，转载请附上博文链接！



rem 表示此命令后的字符为注释，不执行。


---


### 网络命令

<span style="font-size:14px;">@ECHO OFF
TITLE BAT脚本例子4
COLOR A
echo -----------BAT脚本例子4-----------
echo= 
PING www.baidu.com
echo=
echo -----------------------------------
IPCONFIG
echo=
echo -----------------------------------
ARP 
echo=
echo -----------------------------------
PAUSE</span>



--------------------- 
作者：苦逼的IT男 
来源：CSDN 
原文：https://blog.csdn.net/daoming1112/article/details/77197558 
版权声明：本文为博主原创文章，转载请附上博文链接！


```bat
@echo off
title 这是标题
color 03
mode con cols=40 lines=15
:: todo
echo hello world
pause

```

from  https://www.jianshu.com/p/8ef89220545f




[如何把bat文件的输出结果放到txt文件中](https://zhidao.baidu.com/question/153567116.html?qbl=relate_question_1&word=%D7%D4%B6%AF%B1%A3%B4%E6bat%CA%E4%B3%F6%D0%C5%CF%A2)

wkdxz 
推荐于2017-10-01

@echo off
call "批处理路径">D:\结果.txt
start notepad D:\结果.txt
如
@echo off
call "D:\procedure.bat">D:\结果.txt
start notepad D:\结果.txt
>用到了两个文件，
>一个是执行call的bat文件，
>另一个是执行实际代码，需要代码执行过程的bat文件

