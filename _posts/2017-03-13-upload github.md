---
layout: post
title: "本地上传到github"
date: 2017-03-13
tag: 工具 
---

写点本地上传到github的方法，这里简单的记录一下，感觉用命令更方便点，这里全用命令行来实现，不了解Git命令的可以去了解下。

第一步：建立GIT仓库

cd到你的本地项目根目录下，执行git命令
```
git init
```
第二步：将项目的所有文件添加到仓库中
```
git add .
```
如果想添加某个特定的文件，只需把.换成特定的文件名即可

第三步：将ADD的文件COMMIT到仓库
```
git commit -m "注释语句"
```
第四步：去GITHUB上创建自己的REPOSITORY，创建页面如下图所示：

![tool-editor](http://www.072322.top/assets/images/gitupdata/img1.png)
点击下面的Create repository，就会进入到类似下面的一个页面，拿到创建的仓库的https地址，红框标示的就是


第五步：重点来了，将本地的仓库关联到GITHUB上
```
git remote add origin https://github.com/zgangjin/Babel-Browserify-ES6
```
后面的https链接地址换成你自己的仓库url地址，也就是上面红框中标出来的地址

第六步：上传github之前，要先pull一下，执行如下命令：

```
git pull origin master
```
第七步，也就是最后一步，上传代码到GITHUB远程仓库
```
git push -u origin master
```
执行完后，如果没有异常，等待执行完就上传成功了，中间可能会让你输入Username和Password，你只要输入github的账号和密码就行了