
### 报错

To https://github.com/tyler9453111623/lgit.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/tyler9453111623/lgit.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```bash
# 勾选强制覆盖已有的分支（可能会丢失改动），再点击上传，上传成功。
git push -u origin master -f 

```

### 当一台机器同时拉取两个git地址时

```bash
# 通过配置文件管理，只要cd 到这个目录，即拉取这个地址
[ronny@MacPro2018.local:~/Dropbox/lpython3.6]$ cat .git/config
[core]
    repositoryformatversion = 0
    filemode = true
    bare = false
    logallrefupdates = true
    ignorecase = true
    precomposeunicode = true
[remote "origin"]
    url = https://github.com/tyler9453111623/lpython3.6.git  # 这里配置地址
    fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
    remote = origin
    merge = refs/heads/master
```

### 每次拉取都要输入用户名密码
```bash

git config --global credential.helper store

```

### git远程库强制覆盖本地
```bash

# git强制覆盖本地命令（单条执行）：
git fetch --all && git reset --hard origin/master && git pull

```


