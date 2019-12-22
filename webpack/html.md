

## `<html>`标签

`<html>` 元素定义了整个 HTML 文档.

这个元素拥有一个开始标签 `<html>`，以及一个结束标签 `</html>`。

## 主体

HTML主体是通过 `<body>` 标签进行定义的，，要用`</body>`表示主体结束 .
实例

---
    <html>
    <body>
    <p>This is my first paragraph.</p>
    </body>

    </html>

## HTML 标题
HTML 标题是通过 `<h1> - <h6>` 标签进行定义的，要在结束时加上`</h1>-</h6>`.

<h6>这是标题</h6>

`<h6>这是标题</h6>`

## HTML 段落

HTML 段落是通过 `<p>` 标签进行定义的，要用`</p>`表示段落结束.

<p>这是个段落</p>

`<p>这是个段落</p>`

## HTML 链接
HTML 链接是通过 `<a> `标签进行定义的,要用`</a>`表示段落结束.

<a href="http://www.baidu.com">百度</a>

`<a href="http://www.baidu.com">百度</a>`

在 href 属性中指定链接的地址.

## HTML 图像
HTML 图像是通过 `<img> `标签进行定义的.

<img src="https://www.baidu.com/img/bd_logo1.png" width="400" height="150" />

`<img src="https://www.baidu.com/img/bd_logo1.png" width="400" height="150" />`

## 换行

`<br>` 或者` <br />`

可以用在段落内部，只要加入他们即可实现换行.

## 表格

+ 表格由 `<table>` 标签来定义。每个表格均有若干行（由 `<tr>` 标签定义），每行被分割为若干单元格（由 `<td>` 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等.

+ 表格中的空单元格，有的浏览器会使一些的单元格的边框没有被显示出来。为了避免这种情况，在空单元格中添加一个空格占位符`&nbsp;`，就可以将边框显示出来.

+ 表格标题 `<caption>标题</caption>`

+ 跨行 `rowspan="2"`或者跨列 `colspan="2"`

+ 在`table`标签中可以调整表格表框粗细`border`、背景图片`background`背景色`bgcolor`等.

<table border="1">
<caption>标题</caption>
<tr>
<th>表头</th>
<th>表头</th>
</tr>
<tr>
<td> 1,  1</td>
<td> 1,  2</td>
</tr>
<tr>
<td> &nbsp;</td>
<td> 2,  2</td>
</tr>
</table>

    <table border="1">
    <caption>标题</caption>
    <tr>
    <th>表头</th>
    <th>表头</th>
    </tr>
    <tr>
    <td> 1,  1</td>
    <td> 1,  2</td>
    </tr>
    <tr>
    <td> &nbsp;</td>
    <td> 2,  2</td>
    </tr>
    </table>

## 列表
+ 无序列表始于 `<ul>` 标签。每个列表项始于 `<li>`,都要有结束符.

+ 有序列表始于 `<ol>` 标签。每个列表项始于 `<li>` 标签,都要有结束符.

+ 列表项内部可以使用段落、换行符、图片、链接以及其他列表等等.

## HTML块
大多数 HTML 元素被定义为块级元素或内联元素,例如`<h1>`、`<p>`、`<ul>`、`<table>`.

HTML `<div> `元素是块级元素，它是可用于组合其他 HTML 元素的容器.

如果与 CSS 一同使用，`<div>`元素可用于对大的内容块设置样式属性.

`<div> `元素的另一个常见的用途是文档布局.

## HTML`<base>` 元素

`<base>` 标签为页面上的所有链接规定默认地址或默认目标

## HTML `<link>` 元素

`<link>` 标签定义文档与外部资源之间的关系,最常用于连接样式表：

## HTML `<style>` 元素

`<style>` 标签用于为 HTML 文档定义样式信息。

## HTML`<script>` 元素

`<script>`标签用于定义客户端脚本，比如 JavaScript。
