## Linux各目录的作用<br/>
目录名 | 目录作用
-|-
/bin/ | 存放系统命令的目录，普通用户和超级用户都可以执行。不过放在/bin下的命令在单用户模式下也可执行。
/sbin/ | 保存和系统环境设置相关的命令，只有超级用户可以使用这些命令进行系统环境设置，但是有些命令可以允许普通用户查看。
/usr/bin/ | 存放系统命令的目录，普通用户和超级用户都可以执行。这些命令和系统启动无关，在单用户模式（安全模式）下不能执行。
/usr/sbin/ | 存放根文件系统不必要的系统管理命令，例如多数服务程序。只有超级用户可以使用。
/boot/ | 系统启动目录，保存系统启动相关的文件，如内核文件和启动引导程序（grup）文件等。
/dev/ | 设备文件保存位置。
/etc/ | 配置文件保存位置。系统内所有采用默认安装方式（rpm安装）的服务的配置文件全部都保存在这个目录当中。
/home/ | 普通用户的家目录。建立每个用户时，每个用户要有一个默认登陆位置，这个位置就是这个用户的家目录，所有普通用户的家目录就是在/home下建立一个和用户<br>名相同的目录。
/lib/ | 系统调用的函数库保存位置。
/lost+found/ | 当系统意外崩溃或机器意外关机，而产生一些文件碎片放在这里。当系统启动的过程<br>中fsck工具会检查这里，并修复已经损坏的文件系统。这个目录只在每个分区中出现。分别代表每个不同分区的备份恢复目录。
/media/ | 挂载目录。系统建议是用来挂载媒体设备的，例如软盘和光盘。
/mnt/ | 挂载目录。建议挂载额外设备，如U盘，移动硬盘和其他操作系统的分区。
/misc/ | 挂载目录。系统建议用来挂载NFS服务的共享目录。
/opt/ | 第三方安装的软件保存位置。
/proc/ | 虚拟文件系统，该目录中的数据并不保存到硬盘当中，而是保存到内存当中（只能读不能写），主要保存系统的内核，进程，外部设备状态和网络状态灯。
/sys/ | 虚拟文件系统。和/proc目录相似，都是保存在内存当中的，主要是保存内核相关信息的。
/root/ | 超级用户的家目录。普通用户的家目录在“/home”下，超级用户家目录直接在“/”下。
/srv/ | 服务数据目录。一些系统服务启动后，可以在这个目录中保存所需要的数据。
/tmp/ | 临时目录。系统存放临时文件的目录，该目录下所有用户都可以访问和写入。
/usr/ | 系统软件资源目录。usr是Unix Software Resource的缩写，是存放系统软件资源的目录。
/var/ | 动态数据保存位置。主要保存缓存，日志以及软件运行所产生的文件。