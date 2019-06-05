
### 常用术语
1)、仓库（Repository）
受版本控制的所有文件修订历史的共享数据库

2)、工作空间（Workspace) 
本地硬盘或Unix 用户帐户上编辑的文件副本

3)、工作树/区（Working tree）
工作区中包含了仓库的工作文件。您可以修改的内容和提交更改作为新的提交到仓库。

4)、暂存区（Staging area）
暂存区是工作区用来提交更改（commit）前可以暂存工作区的变化。


### 查看配置

```bash
# 使用可以查看现在的git环境详细配置
git config -l 

# 查看系统config
git config --system --list

# 查看当前用户（global）配置
git config --global --list

# 查看当前仓库配置信息
git config —local --list

# 查看从最近到最远的提交日志
git log

```


### 文件4种状态

* Untracked: 

未跟踪, 此文件在文件夹中, 但并没有加入到git库, 不参与版本控制. 通过git add 状态变为Staged.

* Unmodify: 

文件已经入库, 未修改, 即版本库中的文件快照内容与文件夹中完全一致. 
这种类型的文件有两种去处
1. 如果它被修改, 而变为Modified. 
2. 如果使用git rm移出版本库, 则成为Untracked文件

* Modified: 

文件已修改, 仅仅是修改, 并没有进行其他的操作. 
这个文件也有两个去处, 
1. 通过git add可进入暂存staged状态,
2. 使用git checkout 则丢弃修改过, 返回到unmodify状态, 这个git checkout即从库中取出文件, 覆盖当前修改

* Staged: 

暂存状态. 
1. 执行git commit则将修改同步到库中, 这时库中的文件和本地文件又变为一致, 文件为Unmodify状态. 
2. 执行git reset HEAD filename取消暂存, 文件状态为Modified


### 添加 & 提交 & 删除

```bash
##### 添加 #####

# 添加指定文件到暂存区
$ git add [file1] [file2] ...

# 添加指定目录到暂存区，包括子目录
$ git add [dir]

# 添加当前目录的所有文件到暂存区
$ git add .


##### 提交 #####

# 通过add只是将文件或目录添加到了index暂存区，使用commit可以实现将暂存区的文件提交到本地仓库。

# 提交暂存区到仓库区
$ git commit -m [message]

# 撤销提交，1：代表上一次提交，以此类推
git reset --hard HEAD~1


##### 删除 #####

# 删除已提交文件
git rm -rf filename

# 查看已提交文件
git ls-files

# 撤销删除
git checkout -- filename

```



