
[参考](http://blog.csdn.net/chenyufeng1991/article/details/48930471)

1.git上新建仓库

2.本地文件夹下执行```git init``` 并不会格式化文件夹，就算里面有文件了，也可以执行
（这一步必须做）


3.```git status``` 用来展示文件状态

4.```git add .```

5.```git commit```

6.

```
git remote add origin git@github.com:lmwshow/netty.git
```
这一步与远程仓库建立联系

7.
```
git pull origin master

如果有问题:
git pull origin master --allow-unrelated-histories
```
该命令是先把github上的文件拉下来，注意在每次提交之前要首先进行pull，这是防止冲突。

>上述执行成功后，发现在项目目录下多了一个“README.md”文件，这个文件就是从github上拉下来的。因为我们在github上创建repository的时候就创建了这个“README.md”文件，该文件是对这个repository的说明。


8.
```
git push -u origin master
这一步是真正向github提交，执行完成后，github上的repository就有和你本地一样的代码文件了。
```
