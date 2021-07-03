## 检查git版本

git --version	//可以用这个检查是否安装git



## 初始化

​	git init	//初始化



## 设置基本信息

git config --gobal user.name "Eric"	//开发者的名字

--gobal	//全局配置

git config user.email "uwizeyeeric@icloud.com"	//开发者邮箱



## 工作流

![trees](/Users/ericuwizeye/Desktop/trees.png)

*你的本地仓库由 git 维护的三棵"树"组成。第一个是你的 `工作目录`，它持有实际文件；第二个是 `暂存区（Index）`，它像个缓存区域，临时保存你的改动；最后是 `HEAD`，它指向你最后一次提交的结果。*



## 写完代码，git管理

git add script.js	//暂存script.js

git add .				//暂存所有

git status			//查看暂存区的内容

git rm  --cached script.js	//从暂存区移走



## 评论/提交 comment/commit

git commit -m "使用终端提交的"	//提交



git config --list	//配置状态...



## 创建/关联远程仓库

*GitHub和本地文件关联*

git remote add origin https://github.com/McQueen5258/gitOperation.git 	//创建新的origin，origin是名字，给远程仓库的名字。



## 推送push

git push origin master //把本地文件push到orgin库里面，在master分支



## 分支

![branches](/Users/ericuwizeye/Desktop/branches.png)

*分支是用来将特性开发绝缘开来的。在你创建仓库的时候，**master** 是"默认的"分支。在其他分支上进行开发，完成后再将它们合并到主分支上。*



### 1.创建/删除分支

git checkout -b b1	//创建分支b1。如果想删除分支把-b换成-d



### 2.切换分支

git checkout master	//切换到master分支

### 更多关于分支操作

#### 查看当前所在分支

git branch -vv 

#### 查看分支情况

git branch -a

#### 获取所有分支

git fetch



## 更新与合并

1. 先到主分支 git checkout master 

2. git merge b1     //merge是命令
3. git push origin master 

如果有文件冲突，需要手动改。

## 拉pull

git pull origin master	//把远端的master分支的内容拉下来如果有冲突，就要手动修复冲突



## 标签

*可以设置版本号*

git log	//提交记录



### 创建标签

git tag 1.0.0 7b142f08678	//穿件了版本号。后面的code是从提交记录里面的commit后面复制的

git push origin master --tags	//直接push，不需要commit提交。

## Clone克隆

gi t clone https://github.com/McQueen5258/gitOperation.git



## 删除本地的git的隐藏文件

rm -rf .git



## GitHub网页链接

https://mcqueen5258.github.io/gitOperation/A/



## 实用小贴士

内建的图形化 git：
`gitk`
彩色的 git 输出：
`git config color.ui true`
显示历史记录时，每个提交的信息只显示一行：
`git config format.pretty oneline`
交互式添加文件到暂存区：
`git add -i`





TODO:

- [ ] git diff <source_branch> <target_branch>

在合并改动前，可以使用以上命令预览差异

- [ ] 确认是不是学会了“创建远程仓库”	
- [x] 在本地尝试把主分支master跟b1分支合并的权限问题。//不是权限问题，是有一个分支缺少文件。