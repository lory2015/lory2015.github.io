---
title: git hexo blog
date: 2016-05-01 14:41:19
tags: [git, hexo, blog]
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

``` bash
npm install hexo-deployer-git --save
```
在_config.yam里修改添加
deploy:
  type: git
  repo: git@github.com:lory2015/lory2015.github.io.git
  branch: master
就可以方便的使用 hexo g  -d 生成和部署博客

##建好后hexo写博客## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
16：08现在在desktop上 write blog
```

