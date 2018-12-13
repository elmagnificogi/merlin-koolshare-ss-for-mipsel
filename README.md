# 基于MIPSEL架构的梅林固件ss
merlin koolshare ss for mipsel

适用于merlin koolshare mipsel架构机型的改版固件，由于mipsel架构老旧且性能较低，此架构机型的科学上网插件已经不再维护，最后的版本是3.0.4，此处作为仓库搬迁后的备份留存。

因为老仓库的3.0.4的gfwlist以及chnroute还有CDN基本都不能用了，基于这个问题我改了一个版本，将其指向了一个正常更新的地方，从而正常工作

fancyss_mipsel支持机型（需刷梅林koolshare改版固件）：

华硕系列：RT-N66U RT-AC66U（非RT-AC66U-B1）
PS: mipsel机型的固件下载地址: http://koolshare.cn/forum-96-1.html

进入路由ssh以后的修改命令如下：

```
wget --no-check-certificate https://raw.githubusercontent.com/elmagnificogi/merlin-koolshare-ss-for-mipsel/master/shadowsocks.tar.gz
tar -zxvf /tmp/shadowsocks.tar.gz
chmod +x /tmp/shadowsocks/install.sh
sh /tmp/shadowsocks/install.sh
```

等待安装结束以后，刷新网页，填上ss，试一下更新gwflist，会发现正常更新了。

#####　已知问题

前往不要手贱去点ss更新，点了以后就坏了，就会需要重新做一遍上面的操作！！！
有空我再把ss更新的地方改了

ARM 仓库参考：
> https://github.com/hq450/fancyss
