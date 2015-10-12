# Git 命令分类总结

## 撤销

### 撤销已发布提交

`git revert <SHA>`

使用 git push 将代码提交后撤销

git 会新建一个新的 commit 来执行提供的 对应 commit 的相反的更改，任何在该旧 commit 中删除的内容将会在新 commit 中添加进去，反之亦然

### 修改上次提交

`git commit --amend`

结合最新的文件修改情况和上一次提交信息更新并替换上一次提交。没有新的文件更改就直接覆盖上次提交

### 撤销本地修改

`git checkout -- <bad filename>`

撤销未commit的修改

会将该文件的内容恢复到上一次 git commit 的状态。可以提供一个分支名称或者直接提供要回到的 SHA

### 重置本地修改

`git reset <last good SHA> `

撤销本地没有 push的一些commit

`git reset` 历史会退到指定的 SHA，同时硬盘上的这些文件还是维持在被修改了的状态

添加--hard 同时撤销硬盘上的修改

### 撤销本地修改后重做

`git reflog` 和 `git reset` 或 `git checkout`

`git reflog`列出HEAD 修改的时间

### 提交到了另一个分支

`git branch feature`
`git reset --hard origin/master`
`git checkout feature`

一个分支的commit 移动到另一个分支

git branch feature 既可以创建一个 feature 新分支并且不会切换到那个分支

git reset --hard 去恢复 master 分支到 origin/master 的状态。

git checkout 到你的 feature 分支，你能看到所有的更改