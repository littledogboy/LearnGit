# Git 系统学习(一)

## 文件状态变化周期
### status 
![文件状态变化周期](https://ws4.sinaimg.cn/large/006tNc79gy1fmohui82yzj31800k2jvm.jpg)

查看详细状态: `git status`  

查看简单状态: `git status -s`
![状态概览](https://ws2.sinaimg.cn/large/006tNc79gy1fmoj0bofpaj318w0a8q5j.jpg)

### untracted

仓库中, 新创建的文件处于 `untracked` 状态. 使用 `git add <file>` 或者 `git add *`, 追踪文件,并添加到 stage(暂存区).

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

