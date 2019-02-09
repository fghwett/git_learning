# Git学习使用

[TOC]

## 入门篇

### 教程1 Git基础

#### 新建数据库

把该目录移动到本地Git数据库。

```git
$ git init
```

```git
$ mkdir tutorial
$ cd tutorial
$ git init
Initialized empty Git repository in /Users/yourname/Desktop/tutorial/.git/
```

#### 提交文件

请使用status命令确认工作树和索引的状态

```git
$ git status
```

```git
$ git status
# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#     sample.txt
nothing added to commit but untracked files present (use "git add" to track)
```

文件加入到索引，要使用add命令。在<file>指定加入索引的文件。用空格分割可以指定多个文件。

```git
$ git add .
```

>指定参数「.」，可以把所有的文件加入到索引。

提交文件了。请执行如下显示的commit命令。

```git
$ git commit -m ""
```

```git
$ git commit -m "first commit"
[master (root-commit) 116a286] first commit
 0 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 sample.txt

$ git status
# On branch master
nothing to commit (working directory clean)
```

使用log命令，我们可以在数据库的提交记录看到新的提交。

```git
$ git log
commit ac56e474afbbe1eab9ebce5b3ab48ac4c73ad60e
Author: eguchi <eguchi@nulab.co.jp>
Date:   Thu Jul 12 18:00:21 2012 +0900

    first commit
```