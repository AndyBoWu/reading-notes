## DevOps 和 SRE 工程师必备的 60 个 Linux 命令 - 4

[Medium](https://andybowu.medium.com/)

在 DevOps 和 SRE 的领域中，处理和操作文本数据是一项常见而关键的任务，特别是在处理日志文件和配置管理时。

本篇文章将介绍一系列Linux命令，这些命令对于高效处理文本文件非常有用。

从基础的文件查看和编辑，到复杂的文本过滤和数据处理，我们将探索如何使用这些命令来简化日常任务，提高工作效率。

这些命令的掌握不仅可以帮助您更好地管理和解析日志文件，还能有效地处理各种文本数据，从而支持复杂的自动化和脚本任务。

# cat 命令：连接并显示文件内容
```
cat file.txt  # 显示 file.txt 文件的内容
cat file1.txt file2.txt > merged.txt  # 将 file1.txt 和 file2.txt 的内容合并后输出到 merged.txt
```

# nano 命令：简单文本编辑器 
我个人强烈推荐 [SpaceVim](https://spacevim.org/cn/)
```
nano file.txt  # 使用 nano 编辑器打开 file.txt
```

# sed 命令：用于过滤和转换文本的流编辑器
```
sed 's/old/new/g' file.txt  # 将 file.txt 中所有的 "old" 替换为 "new"
sed -n '1,5p' file.txt  # 打印 file.txt 的第1到第5行
```

# awk 命令：模式扫描和文本处理
```
awk '{print $1}' file.txt  # 打印 file.txt 每行的第一列
awk '/pattern/ {print $0}' file.txt  # 打印 file.txt 中包含 "pattern" 的所有行
```

# cut 命令：从文件的每行中删除部分
```
cut -d':' -f1 file.txt  # 使用冒号作为分隔符，显示 file.txt 每行的第一字段
cut -c1-5 file.txt  # 显示 file.txt 每行的第1到第5个字符
```

# sort 命令：排序文本文件的行
```
sort file.txt  # 将 file.txt 的行按字母排序
sort -nr file.txt  # 将 file.txt 的行按数字进行逆序排序
```

# uniq 命令：报告或省略重复的行
```
uniq file.txt  # 从 file.txt 中删除相邻的重复行
sort file.txt | uniq  # 排序 file.txt 并删除所有重复行
```

# tr 命令：转换或删除字符
```
tr 'a-z' 'A-Z' < file.txt  # 将 file.txt 中的小写字母转换为大写
tr -d '0-9' < file.txt  # 删除 file.txt 中的所有数字
```

# grep 命令：在文件中搜索模式
```
grep "pattern" file.txt  # 在 file.txt 中搜索含有 "pattern" 的行
grep -r "pattern" /path/to/directory  # 递归搜索指定目录下含有 "pattern" 的文件
```

# wc 命令：字、行、字符和字节的统计
```
wc file.txt  # 显示 file.txt 的行数、单词数和字节数
wc -l file.txt  # 只显示 file.txt 的行数
```

# tail 命令：输出文件的最后部分
```
tail -n 10 file.txt  # 显示 file.txt 的最后10行
tail -f file.txt  # 动态显示 file.txt 新增的内容
```

# head 命令：输出文件的开始部分
```
head -n 10 file.txt  # 显示 file.txt 的前10行
head -n 5 file1.txt file2.txt  # 分别显示 file1.txt 和 file2.txt 的前5行
```

# diff 命令：逐行比较文件
```
diff file1.txt file2.txt  # 比较 file1.txt 和 file2.txt 的不同
diff -u file1.txt file2.txt  # 以统一格式显示两个文件的差异
```

# tee 命令：从标准输入读取并同时输出到文件和标准输出
```
echo "example" | tee file.txt  # 将 "example" 写入 file.txt 并同时输出到屏幕
command | tee file.txt  # 将命令的输出同时保存到 file.txt 并输出到屏幕
```

# echo 命令：显示一行文本/字符串
```
echo "Hello World"  # 显示 Hello World
echo -n "Hello World" > file.txt  # 将 Hello World 写入 file.txt，不新增换行
```

#Linux命令 #系统管理 #文本处理 #文件操作 #网络诊断 #远程登录 #DevOps工具 #SRE实践 #性能监控 #配置管理 #LinuxCommands #SystemManagement #TextProcessing #FileManagement #NetworkDiagnostics #RemoteAccess #DevOpsTools #SREPractices #PerformanceMonitoring #ConfigurationManagement

#SSH #SCP #下载文件 #数据传输 #IP管理 #网络配置 #网络统计 #路由追踪 #网络任务 #DNS查询 #命名服务器查询 #防火墙配置 #套接字调查 #网络测试 #网络连接 #SSH #SCP #Wget #Curl #IPManagement #NetworkConfiguration #NetworkStatistics #Traceroute #Netcat #DNSLookup #NSLookup #FirewallRules #SocketInvestigation #NetworkTesting #NetworkConnectivity
