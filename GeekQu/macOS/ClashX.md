## 应用概述

ClashX 是一个拥有 GUI 界面基于 Clash 可自定义规则的 macOS 代理应用。

支持 Shadowsocks 协议和其 simple-obfs 插件、v2ray-plugin 插件以及 VMess 协议和其 TCP、WebSocket 等传输方式。

## 应用下载

以下是各平台该应用的下载地址。

- macOS：[ClashX](https://github.com/yichengchen/clashX/releases)
- ...

## 获取订阅

此处将显示您的订阅链接，请注意为登录状态：

[cinwell website](/sublink?type=clash ':include :type=markdown')

!> 这个 **订阅链接** 非常重要，你应当把它当做密码一样妥善保管。

## 配置 ClashX

打开 ClashX，此时会提示您需要安装一个小工具，点击 **安装** 随后输入 macOS 账户密码即可。

![1](https://i.loli.net/2019/02/12/5c624d9f8a0cc.png ':size=400')

点击菜单栏中 ClashX 的图标，选择 配置 => 托管配置 => 设置地址，粘贴上方 **[获取订阅](#获取订阅)** 中的订阅链接。

![2](https://i.loli.net/2019/02/12/5c624f10ac02e.png ':size=400')

![3](https://i.loli.net/2019/02/12/5c624f85dd92b.png ':size=400')

点击菜单栏中 ClashX 的图标，出站模式选择 **规则**，勾选下方的 **设为系统代理** 以及 **开机启动**。

![4](https://i.loli.net/2019/02/12/5c625043035e2.png ':size=200')

## 开始使用

点击菜单栏中 ClashX 的图标，然后在下方的 **Proxy 策略组** 中选择 AUTO 或者你中意的节点即可。

## 其他注意

请不要修改 `~/.config/clash/config.yml` 中的端口配置，否则会导致应用异常。

