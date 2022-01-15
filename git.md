# git
## git概述
### 三个区
工作区：存放代码的地方，git add添加到暂存区
暂存区：临时存储，git commit提交到本地库
本地库：一旦提交到本地库，就会生成历史版本
### 远程库
远程代码代码仓库 git push
局域网：gitlab
互联网：github、gitee

## git基本命令
### 设置用户签名
git config --gloabl user.name 用户名
git config --global user.email 邮箱
这里设置用户签名和将来登录 GitHub(或其他代码托管中心)的账号没有任何关系

### 初始化本地仓库
git init

### 查看本地库状态
git status

### 添加暂存区
git add 文件名

### 提交本地库
git commit -m  "日志信息"  文件名  
git reflog 查看简略日志  
git log 查看详细日志

### 历史版本

#### 查看历史版本

git log  
git reflog

#### 版本穿梭

git reset --hard 版本号

## git分支操作

### 查看分支
git branch -v （可以查看所有分支）

### 创建分支
git branch 分支名

### 切换分支
git checkout 分支名  
切换分支的本质是切换head指针

<img src=./img1.png  width=80%/>

### 删除分支
git branch -d 分支名

### 合并分支

把指定的分支合并到当前分支上 ：git merge 分支名

### 冲突合并
产生冲突后需要手动修改冲突文件，之后add，commit，commit时不能加冲突文件名

## github 操作

### 创建远程仓库别名
git remote -v 查看当前所有远程地址别名  
git remote add 别名 远程地址  （给远程地址其一个别名，方便push、pull等）

### 推送本地分支到远程仓库
git push 别名 分支  （注意最小单元是分支）  
git push 远程地址 分支

### 拉取远程库到本地库
git pull 远程库地址别名 远程分支名  
git pull 远程库地址 远程分支名

### 克隆远程库到本地
git clone 远程地址  
克隆下来以后会自动其一个别名叫origin