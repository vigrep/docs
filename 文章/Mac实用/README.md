

## 连接上VPN后自动添加静态路由

1. 编辑ip-up文件：sudo vim /etc/ppp/ip-up （如果没有ip-up文件，则新建)
2. ip-up授予可执行权限

ip-up文件内容：
```
#!/bin/sh
/sbin/route -n add -net 192.168.0.0 -netmask 255.255.0.0 192.168.9.220
```
