

```bash
# 目录创建
sudo mkdir -pv /codebase/{java,web}
sudo chown -R ops:ops /codebase

# git初始化
cd /codebase/java
git init

# 设置后端远程仓库地址
git remote add origin http://gitlab.example.com/java/projectName.git

# git fetch 获取并创建所有分支信息
# (1)创建并更新本地远程分支。即创建并更新origin/xxx 分支，拉取代码到origin/xxx分支上。
# (2)在FETCH_HEAD中设定当前分支-origin/当前分支对应，如直接到时候git merge就可以将origin/abc合并到abc分支上。
git fetch

# 切换到对应分支（这里会创建本地的这个分支）
git checkout dev

# 查看当前分支和远程分支关联关系
git branch -vv

# 拉代码
git pull

```

