## 如何创建远程库并与本地库相连

* 创建远程库的时候不要点Initial this repository with a README

## 在eclipse可以创建Git项目也可以import

## 如何在Eclipse中修改Git项目

    * 先在Eclipse创建一个要上传的项目。
    * 创建一个Git仓库并与远程仓库相连
    * 将Eclipse创建的项目复制到创建好的Git仓库
    * 将Eclipse新建项目删除重新import已经存在于Git仓库中的项目
    这样修改了Eclispe中的项目时，在Git仓库中提交与上传

## Git多人协作

找到想要新建项目的位置，打开Git Bush输入:

```
git clone git@github.com:Bihanghang/JavaWebNotes.git
```

默认情况下，只能看到本地的master分支。不信可以用git branch命令看看

要在dev分支上开发,先创建本地dev分支，再创建远程origin的dev分支到本地：

```
git checkout -b dev
git checkout -b dev origin/dev
```

上传项目

```
git add env.txt
git commit -m "add env"
git push --set-upstream origin dev
```

**报错remote origin already exist，就需要先删除**

```
git remote rm origin
```

**报错 src refspec master does not match an报,就需要先拉取**

```
git pull
```

**合并分支**

```
git checkout master
git merge dev
```
## GitLab本地新建的分支与远程分支相关联
```
git branch --set-upstream-to=origin/develop develop
```
可以先用`git pull`查看当前分支是否与远程分支相关联.
