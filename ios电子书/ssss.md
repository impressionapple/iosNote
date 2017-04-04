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
 - 查看当前所有配置<br>git config -l
 - 查看当前代码库状态<br> git status

####增加修改删除文件

 - 创建代码<br> touch mian.c
 - 打开代码<br> open main.c

#### 代码提交
 - 把工作区代码提交到暂存区
   - 把单个文件提交到暂缓区<br>git add 文件 例如:git add main.c
   - 把当前目录下全部文件提交到暂存区 git add .
 - 暂存区的代码提交到本地仓库区 git commit -m "提交的信息"


####版本回退

 - 回退到当前版本,放弃没有提交到本地代码仓库（在 git commite -m "",之前所有操作都还原到最初）：git reset --hard HEAD
 - 回退到上一个版本(回到提交到本地仓库的最后一个之前的):git reset --hard HEAD^
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
- 创建网络仓库
  - github
  - oschian
- 创建U盘仓库
- 创建本地仓库
  - cd到指定目录
  - 在当前目录新建一个本地共享仓库：git init --bare

#### 新建代码库经理初始化文件，并添加忽略文件
 - cd到指定目录
 - clone共享库代码到该目录下
    - 下载本地共享仓库到该目录下 git clone 共享仓库路径
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

#### 代码提交到本地代码仓库
 - 把工作区代码提交到暂存区
   - 把单个文件提交到暂缓区<br>git add 文件 例如:git add main.c
   - 把当前目录下全部文件提交到暂存区 git add .
 - 暂存区的代码提交到本地仓库区 git commit -m "提交的信息"

#### 把代码提交到远程代码仓库
 - 下载最新的共享仓库的代码到该目录下:git pull
 - 本地仓库区代码提交到远程仓库去 git push

####版本回退
- 本地版本回退
 - 回退到当前版本：git reset --hard HEAD
 - 回退到上一个版本:git reset --hard HEAD^
 - 回退到之前的第N个修订版本:git reset --hard HEAD~N (N是一个整数)
 - 回退到指定版本号的版本:git reset --hard 版本号（版本号用7位即可，也可用全部）


- 远程仓库版本回退


#### 代码冲突
- 情况一：a 提交代码到本地仓库后，再提交(push)本地仓库到远程仓库
b提交代码到本地仓库，然后在提交(push)本地仓库到远程仓库<br>导致结果：b无法提交提交（push）本地仓库到远程仓库，会提示提交过期的错误<br>解决方案：每次把修改后的代码提交到本地后，如果想提交本地代码仓库到远程代码仓库之前都要拉取（pull）远程代码仓库的代码到本地代码仓库，然后处理（合并，删除）后，再提交（push）本地代码仓库到远程仓库

- 情况二：


- 原因 ： 张三修改代码后提交到本地代码然后再提交到远程仓库， 经理 提交代码代码到本地仓库，如果直接提交到远程代码仓库会出问题。所以必须先pull一下，如果有代码冲突的话解决冲突（合并代码，删除张三代码，删除经理代码）然后提交到本地仓库，在提交到远程仓库，
-


#### 静态路的处理
 git add.


#### 版本备份
 - 1.0版本开发完毕，将1.0版本上传到appstore。对1.0版本进行备份（打上标签）
   - git tag -a weibo1.0 -m "这是1.0版本"
   - 查看当前tag: git tag
 - 需要将标签push到共享版本库
   - 经理
   - git push origin weibo1.0
   - 张三
   - git pull
   - git tag
   -
 - 开始2.0版本的开发
 - 发现1.0版本有bug，在经理的文件夹下面创建一个文件夹，用于修复bug，将共享版本库所有内容clone
   - 经理创建一个新的文件夹
   - cd 到这个文件夹下
   - 克隆远程服务器代码：git clone
   -
 - 将当前的代码转为1.0标签，创建分支，并切换到该分支
   - git checkout weibo1.0 :转为1.0标签
   - 创建分支名字叫weibo1.1fixbug
     - git checkout -b weibo1.1fixbug
 - 在分支中修复bug,上传到appstore,将修复好的版本，打上tag,并上传到共享版本库：
  - git tag -a weibo1.1 -m "修复了bug" (注意打的tag名不能和以前的重复)
  - git push origin weibo1.1
 -
 - 跟当前正在开发的2.0版本进行合并
  - 经理切换到张三创建的分支
  - pull下张三创建的分支的代码
 - 删除分支
  - 查看分支本地
    - git branch (查看当前在哪个分支)或者 git branch -r（查看本地版本库的分支）
  - 切换分支
    - git chechout master
  - 删除分支
    - 删除缓存的分支
     - git branch -d 分支的简称（weibo1.1fixbug）
    - 删除本地仓库分支
     - git branch -r -d 分支的全称（origin/weibo1.1fixbug）
    - 删除远程服务器代码
      - git push origin --delete 分支的简称（weibo1.1fixbug）
      -

#### 分支


