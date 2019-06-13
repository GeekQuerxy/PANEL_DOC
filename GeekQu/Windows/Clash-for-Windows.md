## 应用概述

Clash for Windows 是一个拥有 GUI 界面基于 Clash 可自定义规则的 Windows 代理应用。

支持 Shadowsocks 协议和其 simple-obfs 插件、v2ray-plugin 插件以及 VMess 协议和其 TCP、WebSocket 等传输方式。

## 应用下载

以下是各平台该应用的下载地址。

- Windows：[Clash for Windows](https://github.com/Fndroid/clash_for_windows_pkg/releases)
- ...

## 获取订阅

此处将显示您的订阅链接，请注意为登录状态：

[cinwell website](/sublink?type=clash ':include :type=markdown')

!> 这个 **订阅链接** 非常重要，你应当把它当做密码一样妥善保管。

## 配置 Clash for Windows

打开 Clash for Windows，从任务栏点击 Clash for Windows 图标以显示主页面。

![1](https://i.loli.net/2019/02/13/5c63d6ccd2460.png ':size=600')

随后按 1 -> 2 -> 3 的顺序从侧边栏进入配置管理页面，并在该输入框中粘贴上方 **[获取订阅](#获取订阅)** 中的订阅链接并点击 **Download**。

![2](https://i.loli.net/2019/02/13/5c63d79cd7854.png ':size=600')

待下载完成后单击刚刚下载的配置文件，它会变成橙色，表示当前正在使用。

![3](https://i.loli.net/2019/02/13/5c63d9b12aa2b.png ':size=600')

随后从侧边栏回到 **General**，勾选下方的 **System Proxy** (设为系统代理) 以及 **Auto Launch** (开机自启)。

![4](https://i.loli.net/2019/02/13/5c63dbfe7e45e.png ':size=600')

## 开始使用

打开 Clash for Windows，从侧边栏进入 **Proxies**，上方选择 **Rule**，然后在下方的 **Proxy 策略组** 中选择 AUTO 或者你中意的节点即可。

## 其他注意

请不要修改 `~/.config/clash/config.yml` 中的端口配置，否则会导致应用异常。

