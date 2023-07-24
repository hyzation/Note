## windows设置手动清理
- **查看C盘使用空间情况** 设置=>系统=>存储=>显示更多类别
- **清理休眠文件** 点击***系统和保留***， 以管理员身份打开cmd（C:\Windows\System32），执行 `powercfg -h off` 以关闭休眠功能并删除休眠文件
- **清理其他** 点击相应占用存储空间的类目进行清理
- **本地应用程序临时文件** （C:\Users\用户名\AppData\Local）中存放着程序相关的配置文件与临时文件，逐一进行查看清理


## 使用 Dism++ 
- **下载** https://github.com/Chuyu-Team/Dism-Multi-language