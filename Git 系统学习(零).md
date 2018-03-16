# Git 系统学习(零)

## SVN 与 Git 的不同之处

### 1.**集中式 vs 分布式**  

svn 为集中化的版本控制系统 (Centralized Version Control Systems，简称 CVCS),只有 server 上才有版本库.一旦 server 出问题,历史数据丢失.  git 为分布式版本控制系统(Distributed Version Control System，简称 DVCS),只要是 clone 过的机器上有完整版本库, 即使充当交换的 "server" 出问题, 其他机器上仍然有历史数据.

### 2.**有无暂存区** 

 git 的工作区中有一个隐藏目录 `.git` ,为 git 的版本库. 暂存区 index 就存在于版本库中.

Q:暂存区的作用? 如何把改动更新到暂存区?   
A:暂存区可以看做: 工作区与版本库的中间区. `git add` 添加改动到暂存区. `git commit`, 提交改动到仓库.

## git 指令

* git add  [.]/[file]
* git commit -m ["contens"]

## 参考链接

[git 官网](https://git-scm.com)  
[git - 简明指南](http://rogerdudler.github.io/git-guide/index.zh.html)  
[图形化学习 git 分支](https://learngitbranching.js.org/?NODEMO)