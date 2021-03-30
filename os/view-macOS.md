# 查看系统内核和发行版本

## macOS

```shell
# 内核 & 处理器相关
$ uname -a

# 系统发行版本
$ sw_vers
```
## Linux

```shell
# 内核版本
# 方法一
$ cat /proc/version

# 方法二
$ uname -a

# 发行版本
# 方法一
$ lsb_release -a # 适用于所有发行版 Linux

# 方法二
$ cat /etc/issue # 适用于所有发行版 Linux

# 方法三
$ cat /etc/redhat-release # 只适用于 redhat 系列

```
