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

##建好后hexo写博客## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```
title: postName #文章页面上的显示名称，可以任意修改，不会出现在URL中
date: 2013-12-02 15:30:16 #文章生成时间，一般不改，当然也可以任意修改
categories: example #分类
tags: [tag1,tag2,tag3] #文章标签，可空，多标签请用格式，注意:后面有个空格
description: 附加一段文章摘要，字数最好在140字以内。



