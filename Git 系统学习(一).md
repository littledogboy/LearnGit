# Git 系统学习(一)

## 文件状态变化周期
### status 
![文件状态变化周期](https://ws4.sinaimg.cn/large/006tNc79gy1fmohui82yzj31800k2jvm.jpg)

查看详细状态: `git status`  

查看简单状态: `git status -s`
![状态概览](https://ws2.sinaimg.cn/large/006tNc79gy1fmoj0bofpaj318w0a8q5j.jpg)

### 状态之间的切换

#### add

仓库中, 新创建的文件处于 `untracked` 状态. 使用 `git add <file>` 或者 `git add *`, 追踪文件,并添加到 stage(暂存区).

#### commit

`git commit -m "提交内容"`  将提交信息与命令放在同一行

`git commit` 启动文本编辑器输入本次提交的说明

`git commit -a` 跳过使用暂存区域,省略掉 git add, 直接提交


## diff

查看已暂存和未暂存的修改.

要查看工作区修改, 没有 `add` 的修改. `git diff`

![](https://ws4.sinaimg.cn/large/006tKfTcgy1fmqowj71uwj31dg0uwdm2.jpg)

**注意:** git diff 本身只显示尚未暂存的改动，而不是自上次提交以来所做的所有改动。所以有时候你一下子暂存了所有更新过的文件后，运行git diff后却什么也没有，就是这个原因。

查看已 `add`,没有 `commit` 的修改. `git diff --staged`

可以选用一款合适的 diff 比较工具. [diff-tools-mac](https://www.git-tower.com/blog/diff-tools-mac/)

### Beyond Compare 下载和破解

[Beyond Compare 下载链接](TODO)  
[Beyond Compare 破解](TODO)

### Beyond Compare Line Tool 使用

[Git 配置](http://www.scootersoftware.com/support.php?zz=kb_vcs_osx#git)


## 忽略文件 

`.gitignore`

```
$ .gitignore
  *.[oa]
  *~
```

1. 在仓库的根目录下常见一个 `.gitignore` 文件. `touch .gitignore`
2. 打开文件 `vim .gitignore`
3. 编写规则, 并保存退出.

[github忽略规则](https://github.com/github/gitignore)  
[Git忽略规则](https://www.cnblogs.com/kevingrace/p/5690241.html)

## 工作流

![](https://ws2.sinaimg.cn/large/006tNc79gy1fmoijnttm8j317u0hyaf0.jpg)

## 配置
如果遇到中文文件名乱码,修改下配置 

`git config --global core.quotepath false`

