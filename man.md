# Git 学习

## Git 初始化

在指定的文件夹中右键，打开 `git`，使用指令 `git init` 创建一个本地库并初始化。

这个文件夹下的文件就是命令所操作的文件。

## Git 中的文件状态

### 暂存状态

处于**暂存（staged）** 状态的文件意味着它可以被提交了。在这种状态下，所有必要的修改都已经完成，所以下一步就是把文件移到提交状态。

### 已经提交的状态

当一个文件的所有修改都被保存在本地的 repo 中时，该文件就处于**提交的（committed）** 状态。处于提交阶段的文件是可以被推送到远程 repo（在 GitHub 上）的文件。

### 已修改状态

处于**修改（modified）** 状态的文件已经做了一些修改，但还没有保存。这意味着该文件的状态与之前在提交状态下的状态有了改变。

## Git 中的文件上传操作

### 添加

用指令 `git add .` 将文件夹中的所有文件添加，使得文件处于暂存状态，保存在本地库中。对指定文件可以用 `git add <filename>` 添加文件。

### 提交

使用指令 `git commit`。

一般会在后面加参数 `-m "first commit"`，以表示提交的信息。

### 推送的 GitHub 仓库中

先将本地库与 GitHub 中的仓库进行连接。使用指令 `git remote add origin <url/ssh>` 进行连接。其中 `origin` 表示本地的版本库的名字。

用 `git remote rm <name>` 删除远程仓库。

用 `git remote renamte <old_name> <new_name>` 对仓库重新命名。

再使用指令 `git push -u origin main`。`main` 为分支名称。

### 查看文件的状态

使用指令 `git status`。

## Git 分支

创建分支：`git branch <name>`

切换分支：`git checkout <name>`

分支合并：`git merge` 将所有分支
