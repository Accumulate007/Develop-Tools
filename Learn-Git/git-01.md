## Git基础命令系列-01

### 1.git add
git add 表示对相应的文件进行Git追踪，也可以说是添加本地的修改到暂存区，常用的git add命令有</br>
```
1.git add demo.html  // 将demo.html文件添加到暂存区
2.git add .          // 将本地所有的修改或者新增的文件添加到暂存区
```

### 2.git commit -m 'message about commit'
git commit表示将git add增加的本地修改和变动，提交到版本区。其中-m后面所带的信息，是本次提交相关的信息，由提交者自己书写。只有在git add .操作后提交到暂存区的文件，才可以进行git commit操作。
当提交的是文件夹类型的文件时，提交的信息不需要用引号，否则无法提交。

### 3.git commit -a -m 'message about commit'
这个是git add和git commit -m操作的合并写法。本地修改过的文件，原本需要先经过git add添加到暂存区，然后再经过git commit -m添加到版本区，但是这样略显麻烦。git commit -a -m就是这两个操作的合并写法。

### 4.git status
git status可以查看当前git管理的状态。
a.如果当前工作区是干净的，没有可提交的修改变动，则git status会提示：nothing to commit, working tree clean
b.如果当前工作区有了变动，但还没有进行git add操作，则git status会红色提示相应修改的文件
c.如果当前工作区的修改文件已经进行了git add提交，则git status会绿色文字提醒相应的提交文件
git status还有一个简略版的状态说明: git status -s。这个命令会显示简略版的git当前状态说明，免得看一大堆英文说明。但是需要对简略的状态说明规则需要有一定了解。

### 5.git diff
git diff命令可以对比本地的工作区和暂存区文件的差异。如果本地的修改文件都进行了git add操作，则本地工作区和暂存区的差异就不存在了，git diff也就不会显示任何信息。

### 6.git log
查看当前项目的提交记录。当进入git log模式后，需要通过Q按键退出。

### 7.git branch
查看当前项目的分支情况

### 8.git branch my-branch-01
创建一个叫做my-branch-01的分支

### 9.git checkout my-branch-01
切换到my-branch-01分支上

### 10.git merge my-branch-01
将my-branch-01与当前的分支进行合并

### 11.git merge --abort
取消两个分支的合并。在两个分支存在冲突，并且合并失败的情况下，可以使用这个命令进行合并操作的撤销。

### 12.git reset HEAD a.txt
取消a.txt文件在暂存区的提交

### 13.git commit -m 'some new words' --amend
这次的提交的说明信息，会覆盖上一次commit提交的说明信息。运用这条命令可进行commit提交信息的修改，但是要注意的是只能修改上一次提交的信息。

### 14.git reset "HEAD^"
撤销上一次的commit提交，这条信息还有一个类似的用法，可以指定撤销之前N次的commit提交：
git reset HEAD~N

### 15.git reset hash
可以撤销本次hash值所代表的commit提交，需要知道当次commit提交的hash值。
