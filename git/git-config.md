# 不同的文件夹读取不同的配置文件

> 在日常使用中，我们会有在不同的仓库配置不同的提交信息的需求，下面介绍基于 `路径` 的 `.gitconfig` 的使用方法

```shell
# ~/.gitconfig
[includeIf "gitdir:~/personal/"]
  path = ~/.gitconfig-personal
[includeIf "gitdir:~/work/"]
  path = ~/.gitconfig-work
...
其他配置
...

# ~/.gitconfig-personal
[user]
  name = personal
  email = personal@gmail.com
  signingkey = ABC
 
#  ~/.gitconfig-work
[user]
  name = work
  email = work@gmail.com
  signingkey = CBD
  
```
