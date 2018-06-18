title: git常见命令
date: 2018-06-18 21:58:10
tags: 
---
#### git版本

```javascript
打开命令行工具 git bush
// 查看git版本
git --version
```

#### repository

```javascript
// 初始化仓库  创建的文件夹中有一个隐藏的.git文件夹，就是仓库
git init
查看状态
git status
// 提交所有
git add --all  或者 git add .
// 提交单个
git add 文件名 提交一个
// 备注信息
git commit -m ":tada: Initial commit"
// 查看日志
git log 或者 git log--pretty=online
```

`git status`命令用来 查看文件的状态 如果是红色的代表在工作区，使用了git add . 文件变成了绿色说明在暂存区 

使用了 `git commit -m ""` 在查看状态 `git status` 显示的是 `nothing to commit,working treeclean` 说明暂存区已经添加到了历史记录中，暂存区已经干净了。 

#### 版本回退

- 把版本回退到前面的版本，当前版本HEAD上一个版本HEAD^  

```javascript
git reset --hard HEAD^
```

- 查看自己的每一次命令的记录    如果回退到某一个版本之后又后悔了，n那么可以再回到某一次提交，这时可以查看自己的写过的命令

```javascript
git reflog
```

- 回到某一次的提交 回到某一次提交就要找到某一次提交的id，使用git reflog可以查看自己的命令id 


```javascript
git reset --hard id号
```

#### 添加远程库

拉代码

新建一个文件家用来存放 cd 进入该文件，输入命令

```javascript
git clone 后面附上https复制的地址
// 加限制
// (-- git clone --depth=1 下载最新的历史记录，设限制)
```

#### 创建分支

```
创建分支 github flow
git branch +分支名称
git branch 查看分支状态
git checkout +分支名称 切换分支
```

####push到线上

- 在git上创建一个远程仓库
- git push + 复制地址

```javascript
// push到远程仓库
git remote add origin https://github.com/你的GitHub用户名/admin-vue.git

git push -u origin master
```

或者

```javascript
git push --set-upstream origin +分支名称
```

