
### 在github创建账号

### 在github创建仓库(repo)

### github官方指引内容

```bash
# 本地创建一个仓库目录
mkdir /Users/ronny/Dropbox/lgit
cd /Users/ronny/Dropbox/lgit

echo "# lgit" >> README.md

# 初始化
git init

# 提交到暂存区
git add README.md

# 提交到仓库，-m表示备注信息
git commit -m "first commit"

# 远程库的名字就是origin
git remote add origin https://github.com/tyler9453111623/lgit.git

# 本地库master分支的内容推送到远程
git push -u origin master

# -u 作用：
# ① git不但会把本地的master分支内容推送的远程新的master分支
# ② 还会把本地的master分支和远程的master分支关联起来


# 后期提交到远程只需要
git push origin master

# 创建本地分支
git branch 分支名

# 切换到本地分支
git checkout 分支名

# 提交本地分支到远程仓库
git push origin 本地分支名

# 新建本地分支与远程分支关联
git branch –set-upstream 本地新建分支名 origin/远程分支名

# 查看本地分支和远程分支关联关系
git branch -vv

```

> 这里如果遇到报错，需要设置下git用户名和密码;  
"Please make sure you have the correct access rights and the repository exists."

### 解决办法：

##### ① 在git设置一下身份的名字和邮箱
```bash
git config --global user.name "tyler9453111623"
git config --global user.email "tyler9453111623@gmail.com"

```

##### ② 把本机的公钥填到github上；
github > 右上角头像 > setting > SSH and GPG keys > New SSH key > 粘贴


```bash
# 再次尝试
[ronny@MacPro2018.local:~/Dropbox/lgit]$ git push -u origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 218 bytes | 218.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:tyler9453111623/lgit.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.

```

