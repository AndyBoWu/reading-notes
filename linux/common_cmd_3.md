## DevOps 和 SRE 工程师必备的 60 个 Linux 命令 - 3

[Medium](https://andybowu.medium.com/)

在处理分布式系统时，了解如何执行网络诊断和远程操作是至关重要的。

本篇文章专注于介绍一系列关键的 Linux 命令，这些命令帮助 DevOps 和 SRE 工程师有效地管理网络配置、进行远程登录、文件传输以及数据包跟踪。

从基本的网络连接检查到高级的网络配置和安全性管理，这些命令都是确保系统连续性和性能的重要工具。

掌握这些命令将帮助你优化网络操作，确保数据的安全传输，并高效地解决网络相关问题。

# ssh 命令：用于远程登录
```
ssh user@host  # 使用用户名和主机地址进行远程登录
ssh -i /path/to/private_key user@host  # 使用指定的私钥文件进行远程登录
```

# scp 命令：安全复制文件
```
scp file.txt user@remotehost:/remote/path  # 将本地文件 file.txt 复制到远程主机
scp -P 2222 file.txt user@remotehost:/remote/path  # 使用非标准端口 2222 复制文件
```

# wget 命令：从网上下载文件
```
wget http://example.com/file.txt  # 从网址下载文件
wget -c http://example.com/file.txt  # 断点续传，从上次中断处继续下载文件
```

# curl 命令：从或向服务器传输数据
```
curl http://example.com  # 显示指定 URL 的内容
curl -o localfile.html http://example.com  # 将 URL 的内容下载到本地文件
```

# ip 命令：管理 IP 地址和网络设置
```
ip addr show  # 显示所有网络接口的 IP 地址
ip route show  # 显示路由表
```

# ifconfig 命令：配置网络接口（已过时）
```
ifconfig  # 显示所有接口的网络配置
ifconfig eth0 192.168.1.4 netmask 255.255.255.0  # 设置 eth0 接口的 IP 地址和子网掩码
```

# netstat 命令：网络统计（已过时）
```
netstat -tuln  # 列出所有 TCP 和 UDP 端口的监听状态
netstat -r  # 显示路由表
```

# traceroute 命令：追踪数据包的网络路由
```
traceroute example.com  # 显示数据包到达 example.com 的路由
traceroute -I example.com  # 使用 ICMP 数据包进行追踪
```

# nc (Netcat) 命令：用于网络任务
```
nc -zv example.com 80  # 检查对 example.com 端口 80 的 TCP 连接
nc -l 1234  # 在本地 1234 端口监听连接
```

# dig 命令：DNS 查询
```
dig example.com  # 查询 example.com 的 DNS 信息
dig +trace example.com  # 追踪查询 example.com 的完整路径
```

# nslookup 命令：查询名称服务器
```
nslookup example.com  # 查询 example.com 的 DNS 服务器和 IP 地址
nslookup -type=mx example.com  # 查询 example.com 的邮件交换记录
```

# iptables 命令：配置网络防火墙规则
```
iptables -L  # 列出所有 iptables 规则
iptables -A INPUT -p tcp --dport 80 -j ACCEPT  # 允许所有进入端口 80 的 TCP 流量
```

# ss 命令：调查套接字
```
ss -t -a  # 显示所有 TCP 套接字
ss -u -a  # 显示所有 UDP 套接字
```

# tnc 命令：测试网络连接
```
tnc example.com 80  # 测试到 example.com 端口 80 的 TCP 连接
tnc -udp example.com 53  # 测试到 example.com 端口 53 的 UDP 连接
```

# ping 命令：检查网络连通性
```
ping example.com  # 检查与 example.com 的网络连通性
ping -c 4 example.com  # 发送 4 个 ICMP 回显请求到 example.com 并显示结果
```
