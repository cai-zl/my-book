# Linux

## 运维命令

### 查看服务器出口IP（互联网）

```shell

curl ipinfo.io/ip

```

### 查看端口占用情况

```shell

lsof -i:8080

```

### 修改IP

- Centos

```shell

vim /etc/sysconfig/network-scripts/ifcfg-em1

# TYPE="Ethernet"
# PROXY_METHOD="none"
# BROWSER_ONLY="no"
# BOOTPROTO="static"
# DEFROUTE="yes"
# IPV4_FAILURE_FATAL="no"
# IPV6INIT="yes"
# IPV6_AUTOCONF="yes"
# IPV6_DEFROUTE="yes"
# IPV6_FAILURE_FATAL="no"
# IPV6_ADDR_GEN_MODE="stable-privacy"
# NAME="em1"
# UUID="e1cd63bb-ae8f-4b19-ac82-a169a3942368"
# DEVICE="em1"
# ONBOOT="yes"
# IPADDR=192.168.50.207
# PREFIX=23
# GATEWAY=192.168.50.254
# NETMASK=255.255.255.0
# IPV6_PRIVACY=no
# DNS1=8.8.8.8

```

### 删除60分钟之前的文件

```shell

find /home/logs -mmin +60 -delete

```

### cron示例

```shell

# 目录: /var/spool/cron/root

# 每小时清理一次日志
0 * * * * find /home/logs -mmin +60 -delete

```
