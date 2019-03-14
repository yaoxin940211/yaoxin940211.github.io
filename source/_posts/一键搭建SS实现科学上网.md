---
title: 一键搭建SS实现科学上网
date: 2019-03-09 20:35:57
tags: [SS, SSR]
categories: 科学上网
---
<!-- toc -->

# 搭建SS
## 下载一键搭建ss脚本
```
git clone https://github.com/flyzy2005/ss-fly

git安装
Centos： yum -y install git
Ubuntu/Debian： apt-get -y install git
```
<!--More-->
## 运行搭建脚本
```
ss-fly/ss-fly.sh -i [passwd] [port]
```
## 相关ss操作
```
修改配置文件：vim /etc/shadowsocks.json
停止ss服务：ssserver -c /etc/shadowsocks.json -d stop
启动ss服务：ssserver -c /etc/shadowsocks.json -d start
重启ss服务：ssserver -c /etc/shadowsocks.json -d restart
卸载ss服务：ss-fly/ss-fly.sh -uninstall
```
# 开启BBR加速
## 开启BBR加速
```
ss-fly/ss-fly.sh -bbr


验证加速是否开启成功
sysctl net.ipv4.tcp_available_congestion_control
如果返回值有bbr，说明开启成功
net.ipv4.tcp_available_congestion_control = bbr cubic reno
```

---
# shadowsocks.json配置
## 单用户配置
```
{
    "server":"0.0.0.0",
    "server_port":1024,
    "local_address": "127.0.0.1",
    "local_port":1080,
    "password":"mypassword",
    "timeout":300,
    "method":"aes-256-cfb"
}
```
## 多用户配置
```
{
    "server":"0.0.0.0",
    "local_address":"127.0.0.1",
    "local_port":1080,
    "port_password":{
        "1314":"yaoxin",
    	"1315":"yaoxin",
    	"1316":"yaoxin",
    	"1317":"yaoxin",
    	"2010":"yaoxin",
    	"2011":"yaoxin",
    	"2012":"yaoxin",
    	"2013":"yaoxin",
    	"2015":"yaoxin",
    	"3010":"yaoxin",
    	"3011":"yaoxin"
    },
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open":false
}
```
---

# 搭建SSR
> 如果要安装SSR，需要先卸载SS！！！

## 下载一键搭建ssr脚本
```
git clone https://github.com/flyzy2005/ss-fly
```
## 运行搭建脚本
```
ss-fly/ss-fly.sh -ssr
```
## 输入相关参数
## 相关ssr操作
```
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status
卸载：./shadowsocksR.sh uninstall
 
配置文件路径：/etc/shadowsocks.json
日志文件路径：/var/log/shadowsocks.log
代码安装目录：/usr/local/shadowsocks
```

