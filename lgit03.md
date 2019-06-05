
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

