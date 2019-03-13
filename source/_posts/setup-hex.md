---
title: 如何使用Hexo建站
date: 2019-03-12 11:10:24
categories:
- 杂项

tags:
- hexo
---



# 如何使用Hexo建站

## 一、安装Hexo

``$ sudo npm install -g hexo-cli --unsafe-perm=true --allow-root``

由于我是在macbook上建站，在安装hexo-cli时总会提示

`WARN Hit error EACCES: permission denied, mkdir '/usr/local/lib/node_modules/hexo-cli/node_modules/fsevents/lib'``

解决办法，就是在npm install命令中加上参数``--unsafe-perm=true --allow-root``即可



## 二、初始化站点

```
$ hexo init blog
$ cd blog
```

blog下目录如下

```
.
├── _config.yml
├── package.json
├── scaffolds
├── source
|   ├── _drafts
|   └── _posts
└── themes
```



## 三、新建文章

```
$ hexo new [layout] <title>
```

其中layout参数为文章的类型，可选值为post, page和draft，默认为post

Hexo 有三种默认布局：`post`、`page` 和 `draft`，它们分别对应不同的路径，而您自定义的其他布局和 `post` 相同，都将储存到 `source/_posts` 文件夹。

| 布局    | 路径             |
| ------- | ---------------- |
| `post`  | `source/_posts`  |
| `page`  | `source`         |
| `draft` | `source/_drafts` |
