---
layout: default
title:  如何利用github写博客
---

也算是摸索了大半天，记录下这个过程，用来回忆或者帮助后来人
---

#为什么用github写博客
* 酷炫?
* markdown！
* 没广告!!
* 版本控制!! 
* 其他...


#github page
对于每个项目，github都有个主页，列出项目的源代码。

同时github还提供了pages功能，允许自定义项目首页以替换默认的源码列表。

于是我们可以用这个页面做一些事了。
#一个特殊的项目username.github.io
例如我的就是ZiWee.github.io，该项目的page可以通过http://username.github.io来直接访问（而不是github.com/ziwee/xx项目）.

项目分支名使用master。

#关于jekyll
这是一个静态站点生成器，根据一些代码生成静态页面。

github上可以利用jekyll生成页面。
##如何使用jekyll
###参考目录结构

```
.
├── _config.yml
├── index.html
├── _layouts
│   └── default.html
├── _posts
│   ├── 2015-11-20-beginning.md
│   └── 2015-11-20-how_to_create_blog_at_github.md
└── _site
    ├── 2015
    │   └── 11
    │       └── 20
    │           ├── beginning.html
    │           └── how_to_create_blog_at_github.html
    └── index.html
```

* **_site**是生成的站点文件
* **_posts**是我们写的文章,用md或者html都可以
* **_layouts**模板,利用了一些变量,参考jekyll文档
* **index.html**主页
* **_config.yml**配置文件
* 这仅是一个demo的目录结构,还可以有一些插件等等,但不是必须

如果要在本地测试(需先安装jekyll,见下文),切换到该目录下执行`jekyll serve`,即可在本地4000端口上通过浏览器预览效果,如果效果不错push到github即可

##安装jekyll
首先需要安装ruby,似乎是需要ruby2.0以上版本,如果在国内,你可以切换源到taobao的源,速度会快点

然后gem install jekyll,可能需要sudo提高权限

#不再在本地预览了
前面提到ZiWee.github.io项目, 在github上创建该项目,自然内容如上述jekyll目录结构下的东西了.

#细节
我很懒,有些具体细节没写出来

然后我也很水,还没给主页加上评论功能

对于有些文件的内容,可以直接fork过去

如上...

其实如果不想折腾,还可以简单的随便找几个别人的很棒的github.io,fork一些,直接写就行







