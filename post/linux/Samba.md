> Ubuntu20通过Samba工具与windows系统实现文件共享传输'



# Ubuntu20通过Samba工具与windows系统实现文件共享传输

> 实测可用！！！！踩过N个坑了！！！
>
> 你要是失败；那就是ubuntu系统问题；重装系统再试一遍

## Ubuntu

### 1、安装samba服务器

```shell
sudo apt-get install samba samba-common
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/f0b5e66445c74374843ae0291ed5db28.png)

&emsp;


### 2、配置需要共享的目录

```bash
sudo chmod 777 /home/ -R
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/bb18936ba0c440538e0fd16f5adec4e7.png)
&emsp;


### 3、添加Samba用户
![在这里插入图片描述](https://img-blog.csdnimg.cn/fd9956315ac74b4caf2b709e4805017e.png)

&emsp;

###  4、配置Samba（重点）

```bash
sudo vi /etc/samba/smb.conf
```

在末尾添加如下代码工作组的话查看你自己电脑的Windows下的工作组名

read only = no    //就是可读可写的含义
![在这里插入图片描述](https://img-blog.csdnimg.cn/676a3074491b4f65aa49f5c9edd7fb43.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/e6b2d7bacb9345a9814cb7f230eb0b2c.png)&emsp;


###  5、重启samba服务

```bash
sudo service smbd restart
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/75813a5fcc714964935fef11de303106.png)

&emsp;
### 6、查看IP
```sh
ip add
```

红色框内就是ubuntu的地址

Ubuntu和windows需要在同一网段内；虚拟机设置桥接就可以了
![在这里插入图片描述](https://img-blog.csdnimg.cn/81d73107b65b448cafa7e6965e075622.png)
	
**这是windows的IP地址**
![在这里插入图片描述](https://img-blog.csdnimg.cn/c54c9b0242df4b07b839df923c2d7a37.png)



---
&emsp;
## windows端

### 1、资源管理器访问

地址栏输入 `\\ + IP`地址回车就能看见ubuntu设置的共享文件夹了
![在这里插入图片描述](https://img-blog.csdnimg.cn/b80476ed0c674fa18e718c8e010b1742.png)
&emsp;


### 2、浏览器访问

把资源管理器地址栏的IP和路径复制粘贴到浏览器地址栏就可以了

![在这里插入图片描述](https://img-blog.csdnimg.cn/85443684ffeb4d419b6b5f8c6f5e3310.png)

---















