## Linux文件处理命令2<br/>
**1.** 命令名称：touch<br/>
功能描述：创建空文件<br/>
语法：touch [文件名]<br/>
范例：touch GuiZhou.list<br/>
***
**2.** 命令名称：cat<br/>
功能描述：显示文件内容<br/>
语法：cat [文件名]<br/>
&emsp;&emsp;&emsp;-n 显示行号<br/>
范例：cat &ensp;/etc/issue<br/>
&emsp;&emsp;&emsp;cat -n /etc/services<br/>
***
**3.** 命令名称：tac<br/>
功能描述：显示文件内容（反向列出）<br/>
语法于用法与cat相同（不支持-n）<br/>
***
**4.** 命令名称：more<br/>
功能描述：分页显示文件内容<br/>
语法：more [文件名]<br/>
&emsp;&emsp;&emsp;（空格）或f&emsp;翻页<br/>
&emsp;&emsp;&emsp;（ENTER）&emsp;换行<br/>
&emsp;&emsp;&emsp;&emsp;Q&emsp;退出<br/>
***
**5.** 命令名称：less<br/>
功能描述：分页显示文件内容（可向上翻页）<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;“↑”：向上换行<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;“PageUp”：向上翻页<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;其余与more相同<br/>
可在less语句中进行关键词搜索，例如：/service<br/>
搜索后用N（next）向下查找<br/>
***
**6.** 命令名称：head<br/>
功能描述：显示文件前面几行<br/>
语法：head[文件名]<br/>
&emsp;&emsp;&emsp;-n 指定行数，默认10行<br/>
范例：head -n 20 /etc/services<br/>
***
**7.** 命令名称：tail<br/>
功能描述：显示文件后面几行<br/>
语法：tail [语法]<br/>
&emsp;&emsp;&emsp;-n 指定行数<br/>
&emsp;&emsp;&emsp;-f 动态显示文件末尾内容<br/>
***
**8.** 命令名称：ln——link<br/>
功能描述：生成链接文件<br/>
语法：ln -s[原文件][目标文件]<br/>
&emsp;&emsp;&emsp;-s 创建软链接<br/>
范例：ln&ensp;-s&ensp;/etc/issue&ensp;/tmp/issue.soft<br/>
创建文件/etc/issue的软链接/tmp/issue.soft（类似Windows的快捷方式）<br/>
&emsp;&emsp;&emsp;ln&ensp;/etc/issue&ensp;/tmp/issue.hard<br/>
创建文件/etc/issue的硬链接/tmp/issue.hard<br/>
> 对于软链接：<br/>
>* 权限：lrwxrwxrwx<br/>
>* 文件大小——只是符号链接<br/>
>* /tmp/issue.soft——>/etc/issue<br/>
>对于硬链接：<br/>
>* 相当于cp -p+同步更新<br/>
>* 通过i结点识别是硬链接还是软链接（硬链接的i结点与原文件相同）<br/>
>* 不能跨分区<br/>
>* 不能针对目录使用<br/>
