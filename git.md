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

## git命令
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