## DevOps 和 SRE 工程师必备的 60 个 Linux 命令 - 1

[Medium](https://andybowu.medium.com/)

这些 Linux 命令对于 DevOps 或 SRE 工程师来说极为实用，它们覆盖了从系统和进程管理到服务控制和性能监控的多个关键领域。

熟练掌握这些命令可以帮助工程师高效地解决运维中的各种问题，优化系统性能，以及保证服务的稳定运行。

无论是进行日常的任务自动化，还是处理紧急的系统故障，这些命令都是工程师们日常工作中不可或缺的工具。

通过这些命令，工程师能够快速并准确地收集系统信息，进行故障排查，和执行必要的维护任务。

# ps 命令：显示当前运行的进程
```
ps            # 显示与当前用户相关的进程
ps aux        # 显示所有进程的详细信息，包括用户、PID、CPU和内存使用情况等
```

# top 命令：实时监控系统进程
```
top           # 实时显示系统中的进程状态
top -u username  # 实时显示指定用户的进程状态
```


# systemctl 命令：管理通过 systemd 控制的服务
```
systemctl status nginx  # 查看名为 nginx 的服务的状态
systemctl restart nginx # 重启名为 nginx 的服务
```


# journalctl 命令：查看由 systemd 的日志系统收集的日志
```
journalctl -u nginx    # 查看名为 nginx 的服务的日志
journalctl --since yesterday # 查看从昨天起的所有系统日志
```

# kill 命令：终止进程
```
kill 1234            # 终止进程 ID 为 1234 的进程
kill -9 1234         # 强制终止进程 ID 为 1234 的进程
```

# sudo 命令：以超级用户的身份执行命令
```
sudo apt update      # 以超级用户权限更新软件包列表
sudo systemctl restart nginx  # 以超级用户权限重启 nginx 服务
```

# crontab 命令：管理定时任务
```
crontab -l          # 列出当前用户的定时任务
(crontab -l; echo "0 5 * * * /path/to/script.sh") | crontab -  # 添加每天凌晨5点执行 script.sh 的定时任务
```

# at 命令：一次性定时任务
```
echo "echo hello" | at now + 1 minute # 一分钟后执行 echo hello
at 5pm tomorrow -f /path/to/script.sh # 明天下午5点执行 script.sh
```

# free 命令：显示内存使用情况
```
free           # 显示内存和交换空间的使用情况
free -h        # 显示内存和交换空间的使用情况，单位更易读
```

# df 命令：显示磁盘空间使用情况
```
df             # 显示所有文件系统的磁盘使用情况
df -h          # 以易读的格式显示磁盘空间使用情况
```

# du 命令：显示文件和目录的磁盘使用情况
```
du /path/to/directory  # 显示指定目录的磁盘使用情况
du -sh /path/to/directory  # 显示指定目录的总磁盘使用量，格式简洁
```

# lsof 命令：列出打开的文件及其进程
```
lsof             # 列出所有打开的文件和使用它们的进程
lsof /path/to/file  # 列出打开指定文件的所有进程
```

# hostname 命令：显示或设置系统的主机名
```
hostname         # 显示当前系统的主机名
hostname new-hostname  # 设置系统的主机名为 new-hostname
```

# uptime 命令：显示系统运行时间
```
uptime           # 显示系统从启动到现在的时间、用户数及负载
```

# ping 命令：检查与主机的网络连接
```
ping example.com    # 检查与 example.com 的网络连接
ping -c 4 example.com  # 发送4个包到 example.com 并显示结果
```
#Linux命令 #系统管理 #进程管理 #性能监控 #系统进程 #服务管理 #系统日志 #进程终止 #超级用户 #任务调度 #内存信息 #磁盘空间 #文件大小 #开放文件 #系统主机名 #系统运行时间 #网络连通性 #LinuxCommands #SystemManagement #ProcessManagement #PerformanceMonitoring #SystemProcesses #ServiceManagement #SystemLogs #ProcessTermination #Superuser #TaskScheduling #MemoryInfo #DiskSpace #FileSize #OpenFiles #Hostname #Uptime #NetworkConnectivity
