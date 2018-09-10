## Git的基础命令系列-01

### 1.git add
git add 表示对相应的文件进行Git追踪，也可以说是添加本地的修改到暂存区，常用的git add命令有</br>
```
1.git add demo.html  // 将demo.html文件添加到暂存区
2.git add .          // 将本地所有的修改或者新增的文件添加到暂存区
```

### 2.git commit -m 'message about commit'
git commit表示将git add增加的本地修改和变动，提交到版本区。其中-m后面所带的信息，是本次提交相关的信息，由提交者自己书写。只有在git add .操作后提交到暂存区的文件，才可以进行git commit操作。

### 3.git commit -a -m 'message about commit'
这个是git add和git commit -m操作的合并写法。本地修改过的文件，原本需要先经过git add添加到暂存区，然后再经过git comm -m添加到版本区，但是这样略显麻烦。git commit -a -m就是这两个操作的合并写法。