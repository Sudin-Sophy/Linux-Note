## Linux文件处理命令1<br/>
**1.** 命令名称：ls——list<br/>
功能描述：显示目录文件<br/>
语法：ls 选项[-ald] [文件或目录]<br/>
&emsp;&emsp;&emsp;&emsp;-a 显示所有文件，包括隐藏文件<br/>
&emsp;&emsp;&emsp;&emsp;-l 详细信息显示<br/>
&emsp;&emsp;&emsp;&emsp;-d 查看目录属性<br/>
&emsp;&emsp;&emsp;&emsp;-i 查看i结点<br/>
>u：所有者（只能有1个）：创建者<br/>
g：所属组（只有1个）：授权相同的一组用户<br/>
o：其他<br/>
\_（文件类型） \_ \_ \_（所有者权限） \_ \_ \_（所属者权限） \_ \_ \_（其他权限）<br/>
r：读&emsp;w：写&emsp;x：执行<br/>
***
**2.** 命令名称：mkdir——make directories<br/>
功能描述：创建新目录<br/>
语法：mkdir -p[目录名]<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;-p 递归创建<br/>
范例：mkdir -p/tmp/GuiZhou/LiuPanShui  依次创建GuiZhou和LiuPanShui目录<br/>
&emsp;&emsp;&emsp;mkdir /tmp/GuiZhou/LiuPanShui /tmp/GuiZhou/GuiYang  在GuiZhou目录下创建LiuPanShui和GuiYang目录。<br/>
***
**3.** 命令名称：cd——change directory<br/>
功能描述：切换目录<br/>
语法：cd [目录]<br/>
范例：cd /tmp/GuiZhou/Guiyang 切换到指定目录<br/>
&emsp;&emsp;&emsp;cp .. 返回上一级目录  “.”表示当前目录<br/>
***
**4.** 命令名称：pwd——print working directory<br/>
功能描述：显示当前目录<br/>
语法：pwd<br/>
***
**5.** 命令名称：rmdir——remove empty directories<br/>
功能描述：删除空目录<br/>
语法：rmdir[目录名]<br/>
范例：rmdir /tmp/GuiZhou/GuiYang<br/>
***
**6.** 命令名称：cp——copy<br/>
功能描述：复制文件目录（复制文件不需要加选项）<br/>
语法：cp -rp[原文件或目录]（可多个）[目标目录]（可改名）<br/>
&emsp;&emsp;&emsp;-r 复制目录<br/>
&emsp;&emsp;&emsp;-p 保留文件属性（备份时保留日志属性）<br/>
范例：cp -r /tmp/GuiZhou/LiuPanShui /root&emsp;将/tmp/GuiZhou/LiuPanShu目录复制到/root目录下<br/>
&emsp;&emsp;&emsp;cp -rp /tmp/GuiZhou/GuiYang /tmp/GuiZhou/LiuPanShui /root <br/>
将/tmp/GuiZhou目录下的GuiYang和LiuPanShui目录复制到/root下，保留目录属性<br/>
***
**7.**命令名称：mv——move<br/>
功能描述：截切文件、改名<br/>
语法：mv[原文件或目录][目标目录]（可改名，如mv /tmp/GuiZhou/GuiYang /root/guiyang）<br/>
范例：mv /tmp/GuiZhou/Guiyang /root&emsp;将/tmp/GuiZhou/GuiYang剪切到/root<br/>
***
**8.** 命令名称：rm——remove<br/>
功能描述：删除文件或目录<br/>
语法：rm -rf[文件或目录]<br/>
&emsp;&emsp;&emsp;-r 删除目录<br/>
&emsp;&emsp;&emsp;-f 强制执行<br/>