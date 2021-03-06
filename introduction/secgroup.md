# 安全组简介

安全组是可以应用在云主机、云数据库、负载均衡、弹性网卡等资源上的有状态的虚拟防火墙，用于云资源的出入向的网络访问控制。支持一个云资源绑定一个或者多个安全组。一旦安全组的规则被更新，安全组绑定的所有云资源的实际访问规则会秒级更新。

> 外网防火墙和ACL将会被安全组替代，建议逐步将现有配置转移到安全组上。

## 外网防火墙、ACL与安全组

||网络ACL|外网防火墙|安全组|说明|
|---|---|---|---|---|
|作用维度|子网|资源|资源||
|作用范围|外网流量|内网流量|全部流量|
|封堵是否有状态|无|有|有|有状态指连接建立后，返回流量会被自动放行。|
|是否支持绑定多个|不支持|不支持|支持|

说明：

1、开启安全组后，支持安全组的实例将不再支持绑定外网防火墙。

## 产品限制

支持的产品：云主机（仅限快杰机型）


## 产品配额

|名称|配额|
|---|---|
|同一地域下可创建的安全组数量|1000|
|同一安全组的单向规则数量|1500|
|同一资源可绑定的安全组数量|5|
