## Linux下的shell命令



#### 目录信息查看 ls

##### （1）格式

```shell
ls 【选项】【参数】 
```

##### （2）常用参数选项

- -a：显示所有的文件夹及文件，包括以 “.” 开头的文件
- -l：显示文件的详细信息，比如文件的形态、权限、所有者、大小等信息
- -t：将文件按照创建时间排序列出
- -A：和 -a 一样，但是不列出 “.” （）当前目录和 “.” （）父目录
- -R：递归列出所有的文件，包括子目录中的文件

```shell
ls -a   #显示当前目录下所有目录与文件，包括隐藏目录与文件
...
```

#### 目录切换 cd

##### （1）格式

```shell
cd <路径/文件夹名>
```

##### （2）示例

```shell
cd /	#进入到根目录 "/" 下，Linux 系统的根目录为 "/"
cd /usr	#进入到目录 "/usr" 里面
cd ..	#退出当前目录到上一级目录中
cd ~	#切换到当前用户的主目录
```

#### 显示当前路径 pwd

#### 系统信息查看 uname

##### （1）格式

```shell
uname 【选项】
```

##### （2）常用参数选项

- -r ：列出当前系统的具体内核版本号
- -s ：列出系统内核名称
- -o ：列出系统信息

#### 清理屏幕 clear

#### 显示文件内容 cat

##### （1）格式

```shell
cat 【选项】【文件】
```

##### （2）常用参数选项

- -n ： 由 1 开始对所有输出的行进行编号。
- -b ： 和-n 类似，但是不对空白行编号。
- -s ： 当遇到连续两个行以上空白行的话就合并为一个行空白行

#### 切换用户执行身份 sudo

##### （1）格式

```shell
sudo 【选项】【命令】
```

##### （2）常用参数选项

- -h ：显示帮助信息
- -l ：列出当前用户可执行与不可执行的命令
- -p ：改变询问密码的提示符

##### $\color{#F00}{注意：sudo是临时切换用户为root}$

#### 添加用户 adduser

##### （1）格式

```shell
adduser 【选项】【用户名】
```

##### （2）常用参数选项

- -system ：添加一个系统用户
- -home DIR ：DIR 表示用户的主目录路径
- uid ID ：ID 表示用户的 uid
- ingroup GRP ：表示用户所属的组名

##### $\color{#F00}{注意：此命令需要 root 身份去运行}$

#### 删除用户 deluser

##### （1）格式

```shell
deluser 【选项】【用户名】
```

##### （2）常用参数选项

- -system ： 当用户是一个系统用户的时候才能删除。
- -remove-home ： 删除用户的主目录
- -remove-all-files ： 删除与用户有关的所有文件。
- -backup ： 备份用户信息

##### $\color{#F00}{注意：此命令需要 root 身份去运行}$

#### 切换用户 su

##### （1）格式

```shell
su 【选项】【用户名】
```

##### （2）常用参数选项

- -c –command ： 执行指定的命令，执行完毕以后恢复原用户身份。
- -login ： 改变用户身份，同时改变工作目录和 PATH 环境变量。
- -m ： 改变用户身份的时候不改变环境变量
- -h ： 显示帮助信息

##### $\color{#F00}{注意}$

```shell
#切换到root用户
sudo su
```

```shell
#切换回原来用户
sudo su 【原来的用户名】
```

#### 拷贝文件 cp

#### 移动文件 mv

#### 创建目录 mkdir

#### 创建文件 touch

#### 删除目录/文件 rm



#### 显示和配置网络属性 ifconfig

##### （1）格式

```shell
ifconfig 【选项/address】
```

##### （2）常用参数选项

- interface ： 网络接口名称，比如 eth0 等。
- up ： 开启网络设备。
- down ： 关闭网络设备。
- add ： IP 地址，设置网络 IP 地址。
- netmask add 子网掩码。

#### 系统帮助 man

##### （1）格式

```shell
man 【命令】
```

#### 系统重启 reboot

#### 系统关闭 poweroff

#### 软件安装 install

#### 设置命令别名 alias

##### （1）格式

```shell
alias 【参数】【别名】=【命令】
```

##### （2）常用参数选项

- -p ：查看系统中已有的命令别名信息

##### $\color{#F00}{注意：此方法设置的别名只对当前登录有效}$

#### 取消命令别名 unalias

##### （1）格式

```shell
unalias 【参数】 别名
```

##### （2）常用参数选项

- -a：删除所有的别名定义
