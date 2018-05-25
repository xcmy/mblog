
---
layout:     article
title:      "setup-ipsec-vpn Setting"
date:       2015-07-08
excerpt:    ""
tags:
    - Linux
---

使用setup-ipsec-vpn在服务器完成VPN简易配置，翻墙。
<!-- more -->
### setup-ipsec-vpn   配置

[setup-ipsec-vpn](https://github.com/hwdsl2/setup-ipsec-vpn/blob/master/README-zh.md)

环境CentOS 7

```
yum update #(推荐)
```


```
wget https://git.io/vpnsetup-centos -O vpnsetup.sh && sudo sh vpnsetup.sh
```

执行完会有一个随机的 秘钥、用户名、密码，你可以直接连接，或者自行在`/vpnsetup.sh`配置

```
VPN_IPSEC_PSK='你的IPsec预共享密钥' \
VPN_USER='你的VPN用户名' \
VPN_PASSWORD='你的VPN密码' sh vpnsetup.sh
```


如若连接失败，看看服务器是否开启了防火墙。关闭防火墙后再试




