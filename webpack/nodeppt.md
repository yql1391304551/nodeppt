
# Nodeppt简述

+ Nodeppt是基于Markdown语法编辑生成的网页ppt

+ 在编写时相对传统的PowerPoint较为不直观，编写对于初学者也没那么友好，但是他更为契合程序员，而且编辑时对于代码区块的处理比PowerPoint更好，也便于对他的重复利用。在转载时无需U盘，只要将它发布到网上即可在任意地方使用。

+ 对于我来说，Nodeppt的学习让我学会了使用Markdown和Github的使用，对于HTML的结构和js的使用也有了一定的理解。

+ 在学习过程中也遇到了一些问题，通过小组讨论和网上学习解决了大部分问题。我们在改变页面背景色上遇到了问题，即便是与网上的代码一样也无法实现，最后在我们一直忽略的js和css文件的导入上找到了答案，可以导入一个简单的js文件，在按钮后面执行其中的函数就可以实现了。同时我们也想到了在处理图片是也可以用相似的方法来处理。

## 下载

npm install -g nodeppt

## 使用

+ new：使用线上模板创建一个新的 md 文件
+ serve：启动一个 md 文件的 webpack dev server
+ build：编译产出一个 md 文件

# create a new slide with an official template
$ nodeppt new slide.md

# create a new slide straight from a github template
$ nodeppt new slide.md -t username/repo

# start local sever show slide
$ nodeppt serve slide.md

# to build a slide
$ nodeppt build slide.md

## 帮助

nodeppt -h

## 演讲者模式

nodeppt 有演讲者模式，在页面 url 后面增加?mode=speaker 既可以打开演讲者模式，双屏同步

## 查看ppt时的快捷键

翻页: ↑/↓/←/→ Space Home End
全屏: F

## public 文件夹

如果项目文件夹下，存在public文件夹，可以直接通过 url 访问，参考webpack dev server的 contentBase 选项。
在build的时候，public 文件夹中的文件会完全 copy 到dist文件夹中

## 编写教程

**此教程由王韬智、姚黔龙共同制作**

**王韬智：图片处理、布局控制**

**姚黔龙：动画效果、文字格式**

**合力：样式**

[在线演示](https://borisfwyy.github.io/dist/nodebook.html)

