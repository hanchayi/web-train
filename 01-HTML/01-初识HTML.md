## HTML的概述

### HTML的概念

**HTML** 全称为 HyperText Markup Language，译为<font color=#0000ff>**超文本标记语言**</font>。

HTML 不是一种编程语言，是一种描述性的**标记语言**。

**作用**：HTML是负责描述文档**语义**的语言。

### 概念：超文本

所谓的超文本，有两层含义：

（1）图片、音频、视频、动画、多媒体等内容，成为超文本，因为它们超出了文本的限制。

（2）不仅如此，它还可以从一个文件跳转到另一个文件，与世界各地主机的文件进行连接。即：超级链接文本。

### 概念：标记语言

HTML 不是一种编程语言，是一种描述性的**标记语言**。这主要有两层含义：

（1）**标记语言是一套标记标签**。比如：标签`<a>`表示超链接、标签`<img>`表示图片、标签`<h1>`表示一级标题等等，它们都是属于 HTML 标签。

说的通俗一点就是：网页是由网页元素组成的，这些元素是由 HTML 标签描述出来，然后通过浏览器解析，就可以显示给用户看了。

（2）编程语言是有编译过程的，而标记语言没有编译过程，HTML标签是直接由浏览器解析执行。

### HTML是负责描述文档语义的语言

HTML 格式的文件是一个纯本文文件（就是用txt文件改名而成），用一些标签来描述语义，这些标签在浏览器页面上是无法直观看到的，所以称之为“超文本标记语言”。

接下来，我们需要学习 HTML 中的很多“标签对儿”，这些“标签对儿”能够给文本不同的语义。

关乎“语义”的更深刻理解，等接下来我们学习了各种标签，就明白了。

## HTML的历史

![html中标签发展趋势](https://img.smyhvae.com/20151001_1001.png)

其中，我们专门来对XHTML做一个介绍。

**XHTML介绍：**
XHTML：Extensible Hypertext Markup Language，可扩展超文本标注语言。
XHTML的主要目的是为了<font color="blue">**取代HTML**</font>，也可以理解为HTML的升级版。
HTML的标记书写很不规范，会造成其它的设备(ipad、手机、电视等)无法正常显示。
XHTML与HTML4.0的标记基本上一样。
XHTML是<font color="blue">**严格的、纯净的**</font>HTML。

我们稍后将对XHTML的编写规范进行介绍。

## HTML的专有名词

- 网页 ：由各种标记组成的一个页面就叫网页。
- 主页(首页) : 一个网站的起始页面或者导航页面。
- 标记：  比如`<p>`称为开始标记 ，`</p>`称为结束标记，也叫标签。每个标签都规定好了特殊的含义。
- 元素：比如`<p>内容</p>`称为元素.
- 属性：给每一个标签所做的辅助信息。
- XHTML：符合XML语法标准的HTML。
- DHTML：dynamic，动态的。`javascript + css + html`合起来的页面就是一个 DHTML。
- HTTP：超文本传输协议。用来规定客户端浏览器和服务端交互时数据的一个格式。SMTP：邮件传输协议，FTP：文件传输协议。

## 书写第一个 HTML 页面

我们打开 VS Code 软件，新建一个文件，名叫`test.html`（注意，文件名是`test`，后缀名是`html`），保存到本地。

紧接着，在文件里，输入`html:5`，然后按一下键盘上的`Tab`键，就可以自动生成如下内容：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

上面的内容，就是 html 页面的骨架。我们在此基础之上，新增几个标签，完整代码如下：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h3>我是三级标题</h3>
    <img src="" alt="">
    <a href="https://www.jd.com">我是超链接，可以点击一下</a>
</body>
</html>

```

标签写完之后，我们用 chrome 浏览器打开上面这个`test.html`文件，看看页面效果：

到此，第一个简单的 HTML 页面就写完了。是不是很有成就感？


## HTML结构详解

HTML标签通常是成对出现的（<font color="blue">**双边标记**</font>），比如 `<div>` 和 `</div>`；也有少部分单标签（<font color="blue">**单边标记**</font>），如：`<br />`、`<hr />`和`<img src="images/1.jpg" />`等。

属性与标记之间、各属性之间需要以空格隔开。属性值以双引号括起来。


#### html骨架标签分类

| 标签名              |   定义   | 说明                             |
| ---------------- | :----: | :----------------------------- |
| `<html></html>`    | HTML标签 | 页面中最大的标签，我们成为根标签             |
| `<head></head>`    | 文档的头部  | 注意在head标签中我们必须要设置的标签是title     |
| `<title></title>` | 文档的标题  | 让页面拥有一个属于自己的网页标题               |
| `<body></body>`    | 文档的主体  | 元素包含文档的所有内容，页面内容 基本都是放到body里面的 |


### 1、文档声明头

任何一个标准的HTML页面，第一行一定是一个以`<!DOCTYPE ……>`开头的语句。这一行，就是文档声明头，即 DocType Declaration，简称DTD。

**DTD可告知浏览器文档使用哪种 HTML 或 XHTML 规范**。

#### HTML4.01有哪些规范呢？

**HTML4.01**这个版本是IE6开始兼容的。**HTML5是IE9开始兼容的**。如今，手机、移动端的网页，就可以使用HTML5了，因为其兼容性更高。

说个题外话，html1 至 html3 是美国军方以及高等研究所用的，并未对外公开。

HTML4.01里面有两大种规范，每大种规范里面又各有3种小规范。所以一共6种规范（见下图）。

HTML4.01里面规定了**普通**和**XHTML**两大种规范。HTML觉得自己有一些规定不严谨，比如，标签是否可以用大写字母呢？`<H1></H1>`所以，HTML就觉得，把一些规范严格的标准，又制定了一个XHTML1.0。在XHTML中的字母X，表示“严格的”。

总结一下，HTML4.01一共有6种DTD。说白了，HTML的第一行语句一共有6种情况：

![](https://img.smyhvae.com/20170629_1600.png)

下面对上图中的三种小规范进行解释：

**strict**：

表示“严格的”，这种模式里面的要求更为严格。这种严格体现在哪里？有一些标签不能使用。
比如，u标签，就是给一个本文加下划线，但是这和HTML的本质有冲突，因为HTML最好是只负责语义，不要负责样式，而u这个下划线是样式。所以，在strict中是不能使用u标签的。

那怎么给文本增加下划线呢？今后将使用css属性来解决。

XHTML1.0更为严格，因为这个体系本身规定比如标签必须是小写字母、必须严格闭合标签、必须使用引号引起属性等等。

**Transitional**：表示“普通的”，这种模式就是没有一些别的规范。

**Frameset**：表示“框架”，在框架的页面使用。

在sublime输入的html:xt，x表示XHTML，t表示transitional。

在HTML5中极大的简化了DTD，也就是说HTML5中就没有XHTML了。HTML5的DTD（文档声明头）如下：

```
<!DOCTYPE html>
```

### 2、页面语言 `lang`

下面这行标签，用于指定页面的语言类型：

```html
<html lang="en">
```

最常见的语言类型有两种：

- en：定义页面语言为英语。

- zh-CN：定义页面语言为中文。

### 3、头标签 `head`

#### html5 的比较完整的骨架：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
	<meta name="Author" content="">
    <meta name="Keywords" content="厉害很厉害" />
    <meta name="Description" content="网易是中国领先的互联网技术公司，为用户提供免费邮箱、游戏、搜索引擎服务，开设新闻、娱乐、体育等30多个内容频道，及博客、视频、论坛等互动交流，网聚人的力量。" />
    <title>Document</title>
</head>
<body>

</body>
</html>
```

## HTML的规范

- HTML不区分大小写，但HTML的标签名、类名、标签属性、大部分属性值建议统一用小写。
- HTML页面的后缀名是html或者htm(有一些系统不支持后缀名长度超过3个字符，比如dos系统)

### 1、编写XHTML的规范：

（1）所有标记元素都要正确的嵌套，不能交叉嵌套。正确写法举例：`<h1><font></font></h1>`

（2）所有的标记都必须小写。

（3）所有的标签都必须闭合。

- 双标签：`<span></span>`

- 单标签：`<br>` 建议写成 `<br />`   `<hr>` 建议转成 `<hr />`，还有`<img src=“URL” />`

（4）所有的属性值必须加引号。`<font  color="red"></font>`

（5）所有的属性必须有值。`<hr noshade="noshade">`、`<input  type="radio" checked="checked" />`

（6）XHTML文档开头必须要有DTD文档类型定义。

### 2、HTML的基本语法特性

#### （1）HTML对换行不敏感，对tab不敏感

HTML只在乎标签的嵌套结构，嵌套的关系。谁嵌套了谁，谁被谁嵌套了，和换行、tab无关。换不换行、tab不tab，都不影响页面的结构。

也就是说，HTML不是依靠缩进来表示嵌套的，而是看标签的嵌套关系。但是，我们发现有良好的缩进，代码更易读。建议大家都正确缩进标签。

百度为了追求极致的显示速度，所有HTML标签都没有换行、都没有缩进（tab），HTML和换不换行无关，标签的层次依然清晰，只不过程序员不可读了。如下图所示：

![](https://img.smyhvae.com/20170629_2226.png)

#### （2）空白折叠现象

HTML中所有的**文字之间**，如果有空格、换行、tab都将被折叠为一个空格显示。

举例如下：

![](https://img.smyhvae.com/20170629_2230.jpg)

#### （3）标签要严格封闭

标签不封闭的结果是灾难性的。

标签不封闭的举例如下：

![](https://img.smyhvae.com/20170629_2245.jpg)

