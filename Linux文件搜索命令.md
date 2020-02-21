## Linux文件搜索命令
**1.** 命令名称：find
功能描述：文件搜索
语法：find[搜索范围][匹配条件]
范例：find /etc -name init 在目录/etc中查找文件init(精准搜索)
&emsp;&emsp;&emsp;find /etc -name *init\*（模糊搜索，\*对应任意字符）
&emsp;&emsp;&emsp;find /etc -name init???(?对应单个字符)
&emsp;&emsp;&emsp;find /etc -iname init（i表示不区分大小写）
&emsp;&emsp;&emsp;find [目录] -size +204800 在目录下查找大于100MB的文件
>在Linux中1数据块=512字节（0.5k）
100MB=102400KB=204800数据块
+n大于&emsp;-n小于&emsp;n等于

find /home -user Sudin
在根目录下查找所有者为Sudin的文件
-group 和根据所属组查找
find /etc -cmin -5 在/etc下查找5分钟内被修改过属性的文件和目录（+n -n =n）
&emsp;&emsp;&emsp;-amin 访问时间（access）
&emsp;&emsp;&emsp;-cmin 文件属性（change）
&emsp;&emsp;&emsp;-mmin 文件内容（modify）
&emsp;&emsp;&emsp;find /etc -size +163840 -a -size -204800 在/etc目录下查找大于80MB小于100MB的文件
>-a：两个条件同时满足
-o：两个条件满足任意一个即可

find /etc -name inittab -exec ls -l {} \；
在/etc下查找inittab文件并显示其详细信息
>-exec/ok（依次询问是否操作）
{} \:对搜索结果执行操作

-type 按类型查找（f文件；d目录；l软链接文件）（可与-a；-o结合使用）
-inum 根据i节点查找

