---
title: A new beginning by hexo
date: 2016-05-11 10:36:13
tags: [hexo]
---

以前的博客用的wordpress
11年开始用的，好久了，后来迁移到了阿里云，也不什么经营了，年久失修，变得很慢了，最近想要改造，但是又觉得过去太沉重，于是一键删除了，过去并不值得留恋，如果是好的东西或者思想，我们总会不经意就会回忆到，到时候再写写就好了。

过去写博客之初就想说要是有人问我问题，我甩给他一个我写的文章，省了沟通的成本。不想开始之后就越发懒散，不过总算是开始了，很多事开始了就有东西推动你，想想自己有个博客一年总得写点什么吧，要不每年续费之时又得感概这钱白花了。

<!--more-->

这次不用Wordpress了，用的是hexo，为了不被误导，直接去看[官方的文档](https://github.com/hexojs/hexo)。
下面的指引是在Mac下，首先得安装node环境，由于机器本来就装好了。直接装hexo:

``` bash
$ npm install hexo-cli -g
```

然后新建个目录，进去

``` bash
$ hexo init
```
下载相关的东西好后

``` bash
$ hexo server
```
然后提示你在浏览器里输入：` http://localhost:4000/ `查看，然后在浏览器里就看到一个Hello World
页面，它告诉你如何建文章，运行，发布等。因为我想发布都`ftp`,所以就点了，`deploy`下的more info链接。按照提示：
``` bash
$ npm install hexo-deployer-ftpsync --save
```
然后在文件夹下找到`_config.yml`按介绍填写相关信息。

坑1:因为右边导航不是英文的，所以我设置了以下两项。
``` xml
language: zh-CN
timezone: Asia/Shanghai
```
发布到FTP,我只发布静态文件，所以要先生成静态文件
``` bash
$ hexo generate
```
然后 
``` bash
$ hexo deploy
```
TIP:

* 写文章要要多个标签怎么办？因为hexo使用了[YAML](https://zh.wikipedia.org/wiki/YAML),所以要用相应的格式[[1]](#tip)

``` yaml
tags:
- 耕书录
- stanley小立
```
也可以这样 `tags:[耕书录,stanley小立]`

* markdown要加页内跳转怎么加？因为markdown没有相应的语法，所以只能是一个链接`[开始跳转](#jump)`然后是一段html代码带上跳转的id，如`<span id="jump">跳到此处</span>`

* 脚注(跳转到参考文献)如何添加？这个markdown语法里没有，不过有很多编辑器有支持 `[^footnotes]` 然后页尾使用 `[^footnotes]:`来呼应。

其它不会的可以参考[hexo docs](https://hexo.io/docs/deployment.html) 官网的文档还是比较全面的。

添加评论

国内一般是使用多说的来做的，首先需要注册一个多说的账号，接着[按这里](http://dev.duoshuo.com/threads/541d3b2b40b5abcd2e4df0e9)来配置。

参考文献：

<span id="tip">[1]</span>:  [https://github.com/hexojs/hexo/issues/320](https://github.com/hexojs/hexo/issues/320)

官方文档 [https://hexo.io/docs/deployment.html](https://hexo.io/docs/deployment.html)


