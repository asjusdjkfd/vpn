1. 安装 wget
    ```
    yum install wget
    ```
2. 执行安装shadowsocks
```
wget –no-check-certificate -O shadowsocks.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh
```
3. 获取shadowsocks.sh读取权限
```
chmod +x shadowsocks.sh
```
4. 设置密码和端口号
当你输入`./shadowsocks.sh 2>&1 | tee shadowsocks.log`后就可以设置密码和端口号了：

![搭建ss](https://wistbean.github.io/images/ss1.png)

5. 选择加密方式
设置完密码和端口号之后，我们选择加密方式，这里选择 7：

![搭建ss](https://wistbean.github.io/images/ss2.png)

接着按任意键进行安装。

6. 安装完成
等一会之后，就安装完成了，它会给你显示你需要连接vpn的信息：

![搭建ss](https://wistbean.github.io/images/ss3.png)

可以看到需要连接ss的ip地址，密码，端口，和加密方式。

将这些信息保存起来，那么这时候你就可以使用它们来科学上网啦。


# 使用Shadowsocks

打开 Shadowsocks 客户端，输入ip地址，密码，端口，和加密方式。接着点击确定，右下角会有个小飞机按钮，右键-->启动代理。

![搭建ss](https://wistbean.github.io/images/ss4.png)

这时候就可以科学上网了。

访问以下 Youtube 和 Google 试试看，速度还可以的：
![搭建ss](https://wistbean.github.io/images/ss5.png)
![搭建ss](https://wistbean.github.io/images/ss6.png)


# 使用BBR加速器

让访问速度加速，飞起来！使用 BBR 加速工具。

## 安装 BBR

    wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh

## 获取读写权限

    chmod +x bbr.sh

## 启动BBR安装

    ./bbr.sh

接着按任意键，开始安装，坐等一会。安装完成一会之后它会提示我们是否重新启动vps，我们输入 y 确定重启服务器。

重新启动之后，输入 `lsmod | grep bbr` 如果看到 tcp_bbr 就说明 BBR 已经启动了。

再访问一下 Youtube，1080p 超高清，很顺畅不卡顿！

![搭建ss](https://wistbean.github.io/images/ss7.png)


# 相关文章

- [购买搬瓦工VPS省钱攻略：获取搬瓦工优惠码](https://wistbean.github.io/banwagong-coupon.html)
- [使用搬瓦工快速搭建自己的VPN](https://wistbean.github.io/banwagong-vpn.html)
- [CentOS快速搭建一个属于自己的IPsec/L2TP VPN](https://wistbean.github.io/ipsec,l2tp_vpn.html)
