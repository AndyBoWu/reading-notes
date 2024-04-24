## DevOps 和 SRE 工程师必备的 60 个 Linux 命令 - 2

[Medium](https://andybowu.medium.com/)

在现代 DevOps 和 SRE 工作中，熟练掌握文件和目录管理命令是极其重要的。

这些基础命令不仅帮助工程师有效地操作和维护文件系统，还是自动化和脚本编写不可或缺的工具。

本篇文章将介绍一系列核心 Linux 命令，涵盖从基本的文件查看与操作到高级的文件同步和权限管理。

无论是日常的数据处理还是复杂的系统配置，这些命令都将助你轻松应对，提高工作效率。

# ls 命令：列出目录内容
```bash
ls            # 列出当前目录下的文件和目录
ls -l /path/to/directory  # 以长格式列出指定目录的内容，显示详细信息
```

# cd 命令：改变当前目录
```bash
cd /path/to/directory  # 切换到指定目录
cd ..                  # 返回上级目录
```

# mkdir 命令：创建目录
```
mkdir new_directory    # 在当前位置创建一个新目录
mkdir -p /path/to/directory/structure  # 创建一个目录结构，包括所有必需的父目录
```

# rm 命令：删除文件或目录
```bash
rm file.txt          # 删除名为 file.txt 的文件
rm -rf /path/to/directory  # 递归删除指定目录及其内容
```

# cp 命令：复制文件或目录
```
cp file1.txt file2.txt  # 将 file1.txt 复制为 file2.txt
cp -r dir1 dir2        # 递归复制 dir1 目录到 dir2（如果 dir2 不存在，则创建）
```

# mv 命令：移动文件或目录
```
mv file1.txt /path/to/directory  # 将 file1.txt 移动到指定目录
mv dir1 dir2   # 将 dir1 目录重命名为 dir2，或移动到 dir2 目录下
```

# touch 命令：创建一个空文件
```
touch newfile.txt  # 创建一个名为 newfile.txt 的空文件
touch -t 202401010830 newfile.txt # 更改 newfile.txt 的时间戳为 2024 年 1 月 1 日 8:30
```

# chmod 命令：更改文件权限
```
chmod 755 script.sh  # 更改 script.sh 的权限为 755
chmod -R 644 /path/to/directory  # 递归更改指定目录中所有文件的权限为 644
```

# chown 命令：更改文件所有权
```
chown user file.txt  # 将 file.txt 的所有者更改为 user
chown user:group file.txt  # 更改 file.txt 的所有者为 user，组为 group
```

# find 命令：在目录层级中搜索文件
```
find /path/to/directory -name "*.txt"  # 在指定目录下搜索所有 .txt 文件
find / -type f -size +2M  # 在整个系统中查找大于 2MB 的文件
```

# grep 命令：搜索文本中的模式
```
grep "pattern" file.txt  # 在 file.txt 中搜索文本 "pattern"
grep -r "pattern" /path/to/directory  # 递归搜索指定目录中文件内容包含 "pattern" 的文件
```

# diff 命令：逐行比较文件
```
diff file1.txt file2.txt  # 比较 file1.txt 和 file2.txt 的不同
diff -u file1.txt file2.txt  # 以统一格式显示两个文件的差异
```

# tar 命令：归档文件和目录
```
tar cvf archive.tar /path/to/directory  # 创建一个名为 archive.tar 的归档，包含指定目录
tar xvf archive.tar -C /path/to/extract  # 解压 archive.tar 到指定目录
```

# scp 命令：在主机间安全复制文件
```
scp localfile.txt user@remotehost:/remote/path  # 将本地文件复制到远程主机
scp -r /local/dir user@remotehost:/remote/path  # 递归复制本地目录到远程主机
```

# rsync 命令：远程同步文件和目录
```
rsync -a /local/dir user@remotehost:/remote/dir  # 同步本地目录到远程主机目录
rsync -a --delete /local/dir user@remotehost:/remote/dir  # 同步本地目录到远程，并删除在本
```

#文件管理 #目录管理 #Linux命令 #系统文件操作 #权限修改 #文件搜索 #文本搜索 #文件比较 #数据备份 #远程同步 #FileManagement #DirectoryManagement #LinuxCommands #FilesystemManipulation #PermissionChange #FileSearch #TextSearch #FileComparison #DataBackup #RemoteSynchronization
