## git语法
####概念
 - 工作区:Workspace
 - 暂存区：Index/Stage
 - 本地仓库区：Repository
 - 远程仓库区：Remote


##个人开发

#### 新建代码库
 - cd到指定目录
 - 在当前目录新建一个git代码仓库<br>git init

####配置
- 配置用户名和邮箱（目的是知道谁提交和提交人的邮箱）
  - 配置当前目录的用户名和邮箱(以下两个命令会将用户信息保存在当前代码仓库中)
<br> git config user.name "lwq"<br>git config user.email "lwq@163.com"
  - 配置全局用户名和邮箱（以下两个命令会将用户信息保存全局配置里，以后就不用配置了）<br>git config --global user.name "lwq"<br>git config --global user.email "lwq@163.com
 - 查看当前所有配置<br>git config -l

#### 查看配置
 - 查看当钱

####增加修改删除文件

 - 创建代码<br> touch mian.c
 - 打开代码<br> open main.c

#### 代码提交
 - 把工作区代码提交到暂存区
   - 把单个文件提交到暂缓区<br>git add 文件 例如:git add main.c
   - 把当前目录下全部文件提交到暂存区 git add .
 - 暂存区的代码提交到本地仓库区 git commit -m "提交的信息"


####版本回退

 - 回退到当前版本：git reset --hard HEAD
 - 回退到上一个版本:git reset --hard HEAD^
 - 回退到之前的第N个修订版本:git reset --hard HEAD~N (N是一个整数)
 - 回退到指定版本号的版本:git reset --hard 版本号（版本号用7位即可，也可用全部）





####个人开发

 - git命令行帮助<br>git help


 - 创建代码<br> touch mian.c
 - 打开代码<br> open main.c
 - 将代码添加到代码库
   - 查看当前代码库状态<br>git status
   - 将文件添加到代码库<br>git add main.c
   - 将文件


##团队开发

####创建共享版本库
- （github, 本地共享仓库，git.oschina, U盘）

#### 新建代码库
 - cd到指定目录
 - 下载远程代码到当前路径 git clone  远程仓库URL 例如：git clone https://github.com/impressionapple/weibo.git

####配置
- 配置用户名和邮箱（目的是知道谁提交和提交人的邮箱）
  - 配置当前目录的用户名和邮箱(以下两个命令会将用户信息保存在当前代码仓库中)
<br> git config user.name "lwq"<br>git config user.email "lwq@163.com"
  - 配置全局用户名和邮箱（以下两个命令会将用户信息保存全局配置里，以后就不用配置了）<br>git config --global user.name "lwq"<br>git config --global user.email "lwq@163.com
 - 查看当前所有配置<br>git config -l


####增加修改删除文件

 - 创建代码<br> touch mian.c
 - 打开代码<br> open main.c

#### 代码提交
 - 把工作区代码提交到暂存区
   - 把单个文件提交到暂缓区<br>git add 文件 例如:git add main.c
   - 把当前目录下全部文件提交到暂存区 git add .
 - 暂存区的代码提交到本地仓库区 git commit -m "提交的信息"
 - 本地仓库区代码提交到远程仓库去 git pull

####版本回退
- 本地版本回退
 - 回退到当前版本：git reset --hard HEAD
 - 回退到上一个版本:git reset --hard HEAD^
 - 回退到之前的第N个修订版本:git reset --hard HEAD~N (N是一个整数)
 - 回退到指定版本号的版本:git reset --hard 版本号（版本号用7位即可，也可用全部）
- 远程仓库版本回退




