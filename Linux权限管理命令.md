## 权限管理命令<br/>
**1.** 命令名称：chmod——change the permission mode of a file<br/>
功能描述：改变文件或目录权限<br/>
语法：chmod[{ugoa}{+ - =}{rwx}][文件或目录]<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[mode=421][文件或目录]<br/>
&emsp;&emsp;&emsp;-R 递归修改<br/>
范例：chmod u+x GuiZhou.list 对GuiZhou.list文件的User加上X权限<br/>
&emsp;&emsp;&emsp;chmod g+w，o+r GuiZhou.list<br/>
>权限的数字表示<br/>
r——4;w——2；x——1<br/>
rwxrw_r_ _<br/>
7&emsp;6&emsp;4<br/>
chmod 640 GuiZhou.list<br/>
删除文件的条件是对这个文件所在的目录有写权限<br/>
文件的写权限只是能修改文件内容<br/>

![权限含义](https://github.com/Sudin-Sophy/Linux-Note/blob/master/1.png?raw=true)

