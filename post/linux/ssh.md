# Ubuntu用SSH远程工具默认用root用户连接；解决SSH不能用root用户连接

#  ROOT是什么意思？

> Root，也称为**根用户**，是Unix (如 Solaris 、 AIX 、 BSD ）和类UNIX系统 (如 Linux 、 QNX 等)，及Android和iOS移动设备系统中的唯一的超级用户，因其可对根目录执行读写和执行操作而得名。 其相当于 Windows 系统中的 SYSTEM (XP及以下)/ TrustedInstaller (Vista及以上)用户。



# **默认用普通用户连接没问题**

![img](https://img-blog.csdnimg.cn/700ff74486794f058a4a3b555a156254.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

 

# **默认用root用户连接就会失败**

![img](https://img-blog.csdnimg.cn/066d4ea760944183ba7612e9bb38337e.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

# 

#  解决方法

因为Ubuntu系统会默认锁用户使用root远程连接；我们只需要**添加一行允许代码**即可。

CenOS系统不会锁用户；因为我试过。

### **第一、给root用户设置一个密码**

```bash
sudo passwd root
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

### **第二、修改SSH服务的配置文件（记得要安装SSH服务哦）**

进入配置文件目录

```bash
dbw@dbw:~$ cd /etc/ssh
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

修改sshd_config这个文件！

（需要root权限才能修改）

```bash
vi sshd_config
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

![img](https://img-blog.csdnimg.cn/b6a380550fac4bad81869c4992395282.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

添加红色区域代码；添加完成后保存；[vi命令教程](https://www.runoob.com/linux/linux-vim.html)👈不会vi命令的可以自己点击链接自学一下！

```bash
PermitRootLogin yes
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

 在终端运行SSH重启命令

```bash
service ssh restart
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

------

### 第三、用SSH工具默认使用root用户连接linux

![img](https://img-blog.csdnimg.cn/9f78e1f478b84fd4a4101e828f99b636.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

# 

# **为什么我要默认用ROOT用户连接？👈👈👈**

- **不想输入超级用户密码**
- **拥有最高权限；便于增加或删除文件**
- **可以借助SSH工具修改系统代码。（如果不是root登录；则无法保存修改过的文件）**

不过root用户权限太高；可能导致手滑删除系统配置文件或重要数据！！！谨慎！！！

![img](https://img-blog.csdnimg.cn/5cda6bff937a41f7a369e86b60d5b342.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

 nshll远程连接工具；直接在wind系统远程修改Linux的代码。（支持复制粘）

反正让我老老实实敲那么多代码；不可能；绝对不可能。

![img](https://img-blog.csdnimg.cn/f20145c362944f309f3900d3e7400622.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)