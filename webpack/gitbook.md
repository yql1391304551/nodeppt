## 环境要求

`NodeJS`(v4.0.0及以上)

## 通过`NPM`安装

`npm install gitbook-cli -g` gitbook-cli是gitbook的一个命令行工具, 通过它可以在电脑上安装和管理gitbook的多个版本.

## 编写书籍

### book.json

存放配置信息
记录Gitbook的一些配置信息

---

* title - 标题
* author - 作者信息
* description - 书本描述
* language - 使用的语言
* gitbook - 指定gitbook版本
* root - 指定存放 GitBook 文件的根目录
* links - 在侧边栏添加链接
* styles - 自定义样式
* plugins - 插件
* pluginsConfig - 插件配置
* structure - 设置 Readme, Summary, Glossary等对应的文件
---

#### title

设置书本的标题

"title" : "gitbook使用"
#### author

作者的相关信息

"author" : "姚黔龙"

#### description

本书的简单描述

"description" : "记录Gitbook的使用"

#### language

Gitbook使用的语言, 版本2.6.4中可选的语言如下：
en, ar, bn, cs, de, en, es, fa, fi, fr, he, it, ja, ko, no, pl, pt, ro, ru, sv, uk, vi, zh-hans, zh-tw



"language" : "zh-hans" 配置使用简体中文

#### gitbook

指定使用的gitbook版本

"gitbook" : "3.2.2",
"gitbook" : ">=3.0.0"

#### root

指定存放 GitBook 文件（除了 book.json）的根目录

"root": "..."

#### links

在左侧导航栏添加链接信息

"links" : {
    "sidebar" : {
        "Home" : "http://zhangjikai.com"
    }
}

#### styles

自定义页面样式， 默认情况下各generator对应的css文件

"styles": {
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
    "pdf": "styles/pdf.css",
    "mobi": "styles/mobi.css",
    "epub": "styles/epub.css"
}
例如使<h1> <h2>标签有下边框， 可以在website.css中设置

h1 , h2{
    border-bottom: 1px solid #EFEAEA;
}

#### plugins

配置使用的插件

"plugins": [
    "disqus"
]
添加新插件之后需要运行gitbook install来安装新的插件

Gitbook默认带有5个插件：

* highlight
* search
* sharing
* font-settings
* livereload
如果要去除自带的插件， 可以在插件名称前面加-

"plugins": [
    "-search"
]
pluginsConfig
配置插件的属性

"pluginsConfig": {
    "fontsettings": {
        "theme": "sepia",
        "family": "serif",
        "size":  1
    }
}

#### structure

指定 Readme、Summary、Glossary 和 Languages 对应的文件名，下面是这几个文件对应变量以及默认值：

| 变量 |  含义和默认值 |
| :-----| :---- |
| structure.readme | Readme file name (defaults to README.md) |
| structure.summary	| Summary file name (defaults to SUMMARY.md) |
|structure.glossary	| Glossary file name (defaults to GLOSSARY.md) |
| structure.languages | Languages file name (defaults to LANGS.md) |

### Summary

概要文件主要存放 GitBook 的文件目录信息，左侧的目录就是根据这个文件来生成的，默认对应的文件是 SUMMARY.md，可以在 book.json 重新定义该文件的对应值。它通过 Markdown 中的列表语法来表示文件的父子关系，下面是一个简单的示例：

# Summary
* [Introduction](README.md)
* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)

再在相应的文件中用`markdown`写上文字即可

## 预览书籍

`gitbook serve` 使用下列命令会运行一个服务器, 通过http://localhost:4000/可以预览书籍
`gitbook build` 运行该命令后会在书籍的文件夹中生成一个 _book 文件夹, 里面的内容即为生成的 html 文件. 我们可以使用下面命令来生成网页而不开启服务