## 应用概述

ClashR for Windows 是基于 Clash 上修改的代理软件，功能上跟clash没区别，增加了对SSR的支持。

支持 Shadowsocks 、ShadowsocksR协议和其 simple-obfs 插件、v2ray-plugin 插件以及 VMess 协议和其 TCP、WebSocket 等传输方式。

## 应用下载

以下是各平台该应用的下载地址。

- Windows：[ClashR for Windows](https://raw.githubusercontent.com/aipeach/ssr-download/master/ClashR-Windows.7z)
- ...

## 获取订阅

此处将显示您的订阅链接，请注意为登录状态：

[cinwell website](/sublink?type=clashr ':include :type=markdown')

!> 这个 **订阅链接** 非常重要，你应当把它当做密码一样妥善保管。

## 配置 ClashR for Windows

打开 ClashR for Windows，从任务栏点击 ClashR for Windows 图标以显示主页面。

![1](https://i.loli.net/2020/02/07/uIbnVJtsChfc1zA.png ':size=600')

随后按 1 -> 2 -> 3 的顺序从侧边栏进入配置管理页面，并在该输入框中粘贴上方 **[获取订阅](#获取订阅)** 中的订阅链接并点击 **Download**。

![2](https://i.loli.net/2020/02/07/8TxAsSi5QGYogZc.png ':size=600')

当Download变成Success，表示已经下载完成，选中刚刚下载的配置文件。

![3](https://i.loli.net/2020/02/07/2L4nwsTJqDIgdUu.png ':size=600')

随后从侧边栏回到 **General**，勾选下方的 **System Proxy** (设为系统代理) 以及 **Auto Launch** (开机自启)。

![4](https://i.loli.net/2020/02/07/WAS5R8yln3sUpc7.png ':size=600')

## 开始使用

打开 ClashR for Windows，从侧边栏进入 **Proxies**，上方选择 **Rule**，然后在下方的 **Proxy 策略组** 中选择 AUTO 或者你中意的节点即可。

## 其他注意

请不要修改 `~/.config/clash/config.yml` 中的端口配置，否则会导致应用异常。

