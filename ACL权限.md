## ACL权限<br>
###### 查询分区是否开启ACL权限<br>
>dumpe2fs命令可查询指定分区详细文件系统信息的命令<br>
dumpe2fs -h /dev/sda3 查询分区是否开启了ACL<br>
-h 仅显示超级块中信息，不显示磁盘块组的详细信息<br>
现今Linux一般都已开启<br>

###### 临时开启分区ACL权限<br>
mount -o remount acl /<br>
重新挂载根分区，并挂载加入ACL权限<br>
###### 永久开启分区ACL权限<br>
**1.** vim /etc/fstab 系统开机自动挂载文件<br>
在要启动的分区语句后的default后加上“，acl”<br>
**2.** 执行mount -o remount /（重新挂载文件系统）或者重启系统<br>
***
### ACL权限的查看与设定<br>
**1.** 命令名称：getfacl<br>
功能描述：查看文件ACL权限<br>
语法：getfacl 文件名<br>
***
**2.** 命令名称：setfacl <br>
功能描述：设置ACL权限<br>
语法：setfacl [选项] 文件名<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;-m：设定ACL权限<br>
>范例：setfscl -m u：st：rx /project/<br>
给用户st分配rx权限。<br>
其中u代表user，st为用户名，rx为权限<br>
setfacl -m g:tgroup2:rwx /project/<br>
为组tgroup2分配rwx权限<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;-x：删除指定的ACL权限<br>
>范例：setfacl -x g：tgroup2 /project/<br>
删除组tgroup2的ACL权限<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;-b：删除所有的ACL权限<br>
>范例：setfacl -b /project/<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;-d：设置默认ACL权限<br>
>范例：setfacl -m d：u：用户名：权限 文件名<br>
设置了默认ACL权限后之后，对于新创建的文件，设置的用户都具有相应的权限<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;-k 删除默认ACL权限<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;-R 递归设定ACL权限<br>
>范例：setfacl -m u：用户名：权限 -R 文件名<br>
该命令执行后，对于文件及其子文件，设置的用户都会具有相应的ACL权限，但该命令之后创建的文件不生效<br>
###### 最大有效权限<br>
* mask是用来指定最大有效权限的，若给用户赋予ACL权限，需和mask的值“相与”才能得到用户的真正权限<br>
* 设置mask值：setfacl -m m:rx /project/ 将/project/的mask权限设置为rx<br>
>注：该设置不影响所有者的权限，只影响ACL权限和所属组权限 <br>