> 华为悦盒EC6108V9C刷成小型服务器和NAS！没想到吧，我的盒子是ubuntu服务器!


# 华为悦盒EC6108V9C刷成小型服务器和NAS

![在这里插入图片描述](https://img-blog.csdnimg.cn/e9f36c25f33e457a9d500a72822a92f4.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/10d42da606494f59ad85751e21ba351d.jpeg#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/87621580235e415698731dde6d58f0fd.jpeg#pic_center)

---

# 机顶盒参数
架构：arm7
系统：ubuntu 20.04.5 32位
CPU：hi3798mv100
内存:1G
存储：8G

![在这里插入图片描述](https://img-blog.csdnimg.cn/9c31d4f5b2e44983809ab0360035a2d7.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/576d7581ced1434d83488eb1f84a60cb.png)
---
# 重点！！！


### [刷机视频 ！！！](https://www.bilibili.com/video/BV1wd4y1d7BR/?spm_id_from=333.999.0.0&vd_source=d603bafbe46aebcff52c457fbe607bb4)👈

### [系统固件！！！](https://www.ecoo.top/)👈


---

# 这是我在盒子上挂的博客；看起来不错吧

[博客地址（欢迎访问）](http://dengbowang.fgimaxl2.vipnps.vip/)👈

![在这里插入图片描述](https://img-blog.csdnimg.cn/f72902e2e0124d02b7e1b256602eb59f.png)



# 盒子固件刷好之后的软件安装
## 一、安装docker管理工具

```shell
curl -fsSL https://get.casaos.io | sudo bash
```
[CasaOs](https://casaos.io/)
![在这里插入图片描述](https://img-blog.csdnimg.cn/8f221382036e45529da0fec135dd4c0a.png)


## 二、安装各种软件

[halohub/halo - Docker容器地址](https://hub.docker.com/r/halohub/halo)

[Halo博客官网](https://docs.halo.run/)


![在这里插入图片描述](https://img-blog.csdnimg.cn/763eee3eed194417b0f4375cb87f5768.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/069162b245a44e169325c6fa39a8a05c.png)

## 三、内网穿透

[Linux -启动方式 · 飞鸽内网穿使用教程 (fgnwct.com)](https://www.fgnwct.com/help/linux.html)

```sh
#解压
tar -zxvf linux_amd64_client.tar.gz
#进入到目录
cd linux_amd64_client
#赋予权限
sudo chmod +x npc 
#启动命令
./npc -server=xxxxx -vkey=xxxx
```


## 设置自启
可以看他

[Ubuntu20.04--开机自动运行脚本(命令)-- 自动启动脚本\]](https://blog.csdn.net/feiying0canglang/article/details/124695749)

