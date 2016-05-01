---
title: git hexo blog
date: 2016-05-01 14:41:19
tags: [git, hexo, blog]
description: "多台电脑同写一个gitblog"
---

先github创建一个库名为lory2015.github.io， github它规定了此命名方式
命令终端里建立库作为博客用[如下](https://github.com/lory2015/aaaaa)
``` bash
echo "# aaaaa" >> README.md
git init
git add README.md
git commit -m "first commit"
 git remote add origin git@github.com:lory2015.github.io
 if
  fatal: remote origin already exists. 
 first
  git remote rm origin
  then 
 git remote add origin git@github.com:lory2015.github.io
 git push -u origin master
```
输入用户和密码 开始上传add内容如果上传整个文件的 add . 其它一样。
git add .
git commit -m "folder now"
git remote add origin git@github.com:lory2015.github.io
git push -u origin master
第3可以省略如果报错了
接着用其它电脑就可以 git clone git@github.com:lory2015.github.io到电脑本地接着写同一个博客

``` bash
npm install hexo-deployer-git --save
```
在_config.yam里修改添加
deploy:
  type: git
  repo: git@github.com:lory2015/lory2015.github.io.git
  branch: master
就可以方便的使用 hexo g  -d 生成和部署博客

##建好后hexo写博客Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
16：08现在在desktop上 write blog
```
ssh git@github.com
hexo d 就不会有 host key的报错了  github 里的SSH里对应电脑的SHH钥匙会变亮了。
最后把变化更新备份到例外一个blog库里
git add .
git commit -m "this new change for blog"
git push -u origin master

台式机写博客，先执行下面一种把笔记的更新合并到本地
``` bash
down vote
One approach is to commit that file first then pull.

git add filename
git commit 
//enter your commit message and save 
git pull 

Another approach is stash your changes then pull. Then apply stash.

git stash
git pull
git stash apply stash@{0}
```
然后台式电脑写好博客 hexo g -d 
