# 基于MIPSEL架构的梅林固件ss

merlin koolshare ss for mipsel

适用于merlin koolshare mipsel架构机型的改版固件，由于mipsel架构老旧且性能较低，此架构机型的科学上网插件已经不再维护，最后的版本是3.0.4，此处作为仓库搬迁后的备份留存。

因为老仓库的3.0.4的gfwlist以及chnroute还有CDN基本都不能用了，基于这个问题我改了一个版本，将其指向了一个正常更新的地方，从而正常工作

fancyss_mipsel支持机型（需刷梅林koolshare改版固件）：

华硕系列：RT-N66U RT-AC66U（非RT-AC66U-B1）
PS: mipsel机型的固件下载地址: http://koolshare.cn/forum-96-1.html

## 安装

#### 下载这个ss压缩包

先去release页面下载shadowsocks.tar.gz 

> https://github.com/elmagnificogi/merlin-koolshare-ss-for-mipsel/archive/v0.1.tar.gz

#### 匿名上传

> https://cowtransfer.com/

比如牛奶快传,然后拿到分享链接，进入并再次下载，拿到牛奶的真实下载链接,比如

> https://static.cowtransfer.com/anonymous/c06c0c3c-1db1-49f4-b40e-d405f2f7f488/shadowsocks.tar.gz?onett=b13f6a16c9a73ce35db66120e115517e&attname=shadowsocks.tar.gz 

然后才能用wget拿到这个文件

![SMMS](https://i.loli.net/2020/05/01/qfCJIBn2Nx1zFi7.png)



### SSH安装

进入路由ssh以后的修改命令如下：

```
wget --no-check-certificate  -O ./shadowsocks.tar.gz 刚才牛奶快传的链接
tar -zxvf ./shadowsocks.tar.gz -C ./shadowsocks
chmod +x ./shadowsocks/install.sh
sh /tmp/shadowsocks/install.sh
```

等待安装结束以后，刷新网页，填上ss，试一下更新gwflist，会发现正常更新了。



#### 其他

更新按钮无效-不会误触导致被老版ss覆盖掉



要用上面这么繁琐的方式来更新的原因是：

1. 路由中的wget无法获取到git的任何内容，ssl版本太低了，git封掉了低版本的wget命令
2. github.com或者是raw.githubusercontent.com在没有ss翻墙的情况下可能路由里不能直接wget到，当然如果还有上级路由可以翻墙，可以wget自然就不用这么麻烦了
3. 默认是没有sftp或者fpt服务的，所以上传文件稍微麻烦了点
4. 离线安装无效，缺少了一个js文件，当然如果你补上这个js也能通过离线安装，不过补上这个js文件可能还要从git拉取，所以...



其他临时匿名文件分享站

> https://bbs.itzmx.com/thread-59000-1-1.html



ARM 仓库参考：
> https://github.com/hq450/fancyss
