## 应用概述

Quantumult 是在 iOS 平台上的客户端软件，支持 Shadowsocks、ShadowsocksR 以及 VMess 协议。

目前 Quantumult 已经被 Apple 根据政府要求从中国大陆区的 App Store 移除，之前在中国大陆商店购买此软件的用户将不能获得更新或重新下载。

!> 这是一个付费软件，你需要购买才能使用。

## 应用下载

以下是各平台该应用的下载地址。

- Apple iOS：[App Store](https://itunes.apple.com/us/app/quantumult/id1252015438?ls=1&mt=8)
- ...

## 配置方案

此文中讲述在 Quantumult 中配置 SSR、V2ray、分流规则订阅。

如您需要更细化的配置，如使用策略组等，请 **[点此查阅](/iOS/Quantumult_conf.md)** 相关的使用方案，否则请往下继续。

## 获取订阅

此处将显示您的订阅链接，请注意为登录状态：

[cinwell website](/sublink?type=quantumult_sub ':include :type=markdown')

!> 这个 **订阅链接** 非常重要，你应当把它当做密码一样妥善保管。

## 配置 Quantumult

打开 Quantumult，点击底部导航栏的「设置」进入设置页面。

![1](https://i.loli.net/2019/01/11/5c382573c80a9.jpeg ':size=200')

进入「订阅」子页面并点击右上角的加号，从弹出菜单中选择第一个「服务器」。

![3](https://i.loli.net/2019/01/11/5c3828b395d90.png ':size=200')

在「名称」中输入本站名称并保存，随后在「链接」中粘贴上方 **[获取订阅](#获取订阅)** 中您需要使用的订阅类型并保存。

![4](https://i.loli.net/2019/01/11/5c382b0171a12.jpeg ':size=600')

随后点击右上角保存，此时会自动更新获取服务器。

### 分流规则

同样在「订阅」页面，点击右上角加号，从弹出菜单中选择第二个「分流」。

在名称中输入「Hackl0us Rules」，链接中输入「<https://raw.githubusercontent.com/Hackl0us/Surge-Rule-Snippets/master/LAZY_RULES/Quantumult.conf>」可长按链接拷贝，并保存。

![5](https://i.loli.net/2019/01/11/5c382e0a2969c.jpeg ':size=600')

随后左划「Hackl0us Rules」分流规则并点击替换。

![6](https://i.loli.net/2019/01/11/5c382ec662425.jpeg ':size=400')

## 开始使用

回到 Quantumult 主页，点击底部导航栏的 **圆 logo** 图标，选择您需要的节点，随后打开右上角开关即可。

如提示添加 VPN 配置，请点击 Allow 并验证您的 密码、Touch ID、Face ID 。
