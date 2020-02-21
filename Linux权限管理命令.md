## 权限管理命令
**1.** 命令名称：chmod——change the permission mode of a file
功能描述：改变文件或目录权限
语法：chmod[{ugoa}{+ - =}{rwx}][文件或目录]
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[mode=421][文件或目录]
&emsp;&emsp;&emsp;-R 递归修改
范例：chmod u+x GuiZhou.list 对GuiZhou.list文件的User加上X权限
&emsp;&emsp;&emsp;chmod g+w，o+r GuiZhou.list
>权限的数字表示
r——4;w——2；x——1
rwxrw_r_ _
7&emsp;6&emsp;4
chmod 640 GuiZhou.list
删除文件的条件是对这个文件所在的目录有写权限
文件的写权限只是能修改文件内容

![权限含义](http://baidu.com/pic.png)

