## Git的基础命令系列-01

### 1.git add
git add 表示对相应的文件进行Git追踪，也可以说是添加本地的修改到暂存区，常用的git add命令有</br>
```
1.git add demo.html  // 将demo.html文件添加到暂存区
2.git add .          // 将本地所有的修改或者新增的文件添加到暂存区
```

### 2.git commit -m 'message about commit'
git commit表示将git add增加的本地修改和变动，提交到版本区。其中-m后面所带的信息，是本次提交相关的信息，由提交者自己书写。