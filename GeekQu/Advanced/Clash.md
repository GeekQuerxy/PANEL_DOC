
我们发现部分用户对该应用的配置存在更高需求，所以现在我们提供可由您自定义 Clash 配置。

!> 请注意，自定义配置不提供技术支持服务。

## 请求方式 （GET）

示例：`https://www.gov.com/link/123456789?clash=1&source=GIST_URL`

其中 **GIST_URL** 为您的 YAML 配置地址。

## 配置文件 （示例）

``` yaml
# 自定义 Clash 配置示例
---
General:
  port: 7890
  socks-port: 7891
  redir-port: 7892
  allow-lan: true
  mode: Rule
  log-level: silent
  external-controller: '0.0.0.0:9090'
  secret: ''
  dns:
    enable: true
    ipv6: false
    # listen: 0.0.0.0:53
    # enhanced-mode: redir-host
    nameserver:
      - 1.2.4.8
      - 223.5.5.5
      - 114.114.114.114
      - tls://dns.rubyfish.cn:853
    fallback:
      - tls://dns.rubyfish.cn:853
      - tls://dns.google

Proxy:  # 添加额外节点，但请注意，ProxyGroup 中所有的筛选并不会获取此处提供的额外节点
- name: "韩国自建 1"
  type: ss
  server: server
  port: 443
  cipher: AEAD_CHACHA20_POLY1305
  password: "password"
  plugin: obfs
  plugin-opts:
    mode: tls # or http
    # host: bing.com
- { name: "韩国自建 2", type: vmess, server: server, port: 443, uuid: uuid, alterId: 32, cipher: auto }
- { name: "自购国内中继", type: vmess, server: server, port: 443, uuid: uuid, alterId: 32, cipher: auto }

ProxyGroup:
# 请注意，class 和 noclass 不能同时使用
- name: '香港' # 策略组名
  type: url-test # 支持 Clash 所有的 type 类型
  content:  # 从 3 级的节点中筛选香港节点
    class: 3
    regex: '(香港)'
  url: http://www.qualcomm.cn/generate_204
  interval: 3600

- name: '日本'
  type: url-test
  content:  # 从非 0 级的节点中筛选日本节点
    noclass: 0
    regex: '(日本)'
  url: http://www.qualcomm.cn/generate_204
  interval: 3600

- name: '坡坡'
  type: url-test
  content:  # 从所有节点中筛选新加坡节点
    regex: '(新加坡)'
  url: http://www.qualcomm.cn/generate_204
  interval: 3600

- name: '美国'
  type: url-test
  content:
    regex: '(美国)'
  url: http://www.qualcomm.cn/generate_204
  interval: 3600

- name: '台湾'
  type: url-test
  content:
    regex: '(台湾)'
  url: http://www.qualcomm.cn/generate_204
  interval: 3600

- name: '韩国'
  type: url-test
  content:  # 从所有节点中筛选韩国节点，并在筛选的节点后面加上 right-proxies 中的节点
    regex: '(韩国)'
    right-proxies:
      - '韩国自建 1'
      - '韩国自建 2'
  url: http://www.qualcomm.cn/generate_204
  interval: 3600

- name: '中继'
  type: fallback
  content:  # 从所有节点中筛选中继节点，并在筛选的节点前面加上 left-proxies 中的节点
    regex: '(中国|回国)'
    left-proxies:
      - '自购国内中继'
  url: http://www.qualcomm.cn/generate_204
  interval: 3600

- name: "PROXY"
  type: select
  content:
    left-proxies:
      - '香港'
      - '日本'
      - '坡坡'
      - '台湾'
      - '美国'
      - '韩国'
      - '中继'

- name: "Final"
  type: select
  content:
    left-proxies:
      - "PROXY"
      - "DIRECT"

- name: "ForeignMedia"
  type: select
  content:
    left-proxies:
      - PROXY
      - '香港'
      - '日本'
      - '坡坡'
      - '台湾'
      - '美国'
      - '韩国'
      - '中继'

- name: "DomesticMedia"
  type: select
  content:
    left-proxies:
      - DIRECT
      - PROXY
      - '中继'

- name: "Apple"
  type: select
  content:
    left-proxies:
      - DIRECT
      - PROXY

- name: "Hijacking"
  type: select
  content:
    left-proxies: 
      - DIRECT
      - REJECT

Rule:
  # 加载远程规则，仅支持一个远程规则
  # 使用神机规则或从其他完整配置中获取规则，需为标准 YAML 格式
  # source: https://github.com/ConnersHua/Profiles/raw/master/Clash/Pro.yaml
  # 或自行提供规则
  source: https://gist.github.com/GeekQu/6fdb445a02035ed972c360e3511fa113/raw/Rule.yaml
```