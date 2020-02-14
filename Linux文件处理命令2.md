## Linux文件处理命令2
**1.** 命令名称：touch
功能描述：创建空文件
语法：touch [文件名]
范例：touch GuiZhou.list
***
**2.** 命令名称：cat
功能描述：显示文件内容
语法：cat [文件名]
&emsp;&emsp;&emsp;-n 显示行号
范例：cat &ensp;/etc/issue
&emsp;&emsp;&emsp;cat -n /etc/services
***
**3.** 命令名称：tac
功能描述：显示文件内容（反向列出）
语法于用法与cat相同（不支持-n）
***
**4.** 命令名称：more
功能描述：分页显示文件内容
语法：more [文件名]
&emsp;&emsp;&emsp;（空格）或f&emsp;翻页
&emsp;&emsp;&emsp;（ENTER）&emsp;换行
&emsp;&emsp;&emsp;&emsp;Q&emsp;退出
***
**5.** 命令名称：less
功能描述：分页显示文件内容（可向上翻页）
&emsp;&emsp;&emsp;&emsp;&emsp;“↑”：向上换行
&emsp;&emsp;&emsp;&emsp;&emsp;“PageUp”：向上翻页
&emsp;&emsp;&emsp;&emsp;&emsp;其余与more相同
可在less语句中进行关键词搜索，例如：/service
搜索后用N（next）向下查找
***
**6.** 命令名称：head
功能描述：显示文件前面几行
语法：head[文件名]
&emsp;&emsp;&emsp;-n 指定行数，默认10行
范例：head -n 20 /etc/services
***
**7.** 命令名称：tail
功能描述：显示文件后面几行
语法：tail [语法]
&emsp;&emsp;&emsp;-n 指定行数
&emsp;&emsp;&emsp;-f 动态显示文件末尾内容
***
**8.** 命令名称：ln——link
功能描述：生成链接文件
语法：ln -s[原文件][目标文件]
&emsp;&emsp;&emsp;-s 创建软链接
范例：ln&ensp;-s&ensp;/etc/issue&ensp;/tmp/issue.soft
创建文件/etc/issue的软链接/tmp/issue.soft（类似Windows的快捷方式）
&emsp;&emsp;&emsp;ln&ensp;/etc/issue&ensp;/tmp/issue.hard
创建文件/etc/issue的硬链接/tmp/issue.hard
> 对于软链接：
>* 权限：lrwxrwxrwx
>* 文件大小——只是符号链接
>* /tmp/issue.soft——>/etc/issue
>对于硬链接：
>* 相当于cp -p+同步更新
>* 通过i结点识别是硬链接还是软链接（硬链接的i结点与原文件相同）
>* 不能跨分区
>* 不能针对目录使用
