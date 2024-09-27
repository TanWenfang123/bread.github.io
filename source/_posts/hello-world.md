---
title: 版本管理基本操作
---
# Git命令流程
### 1. 安装Git
### 2 .配置Git用户信息

```
git config --global user.name "你的用户名"  
git config --global user.email "你的邮箱地址"
```
### 3. 初始化Git仓库
##### 初始化一个新的Git仓库。

```
1. cd 项目目录路径  
2. git init
```
### 4. 添加文件到Git仓库
##### 将项目文件添加到Git的暂存区（或称为暂存索引）。

```
git add 文件名  
# 或者添加所有文件  
git add .
```
### 5. 提交文件到Git仓库
##### 将暂存区的更改提交到Git仓库中，并附上提交信息。

```
git commit -m "提交信息"
```
### 6. 查看提交历史
##### 使用git log命令查看项目的提交历史。

```
git log
```
### 7. 标签
##### 为特定的提交打上标签，以便于版本管理和发布

```
git tag -a v1.0 -m "Version 1.0"
git push orgin --tags
```

