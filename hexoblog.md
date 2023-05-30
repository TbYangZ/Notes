# HexoBlog

## 什么是 Hexo

> Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

具体而言，Hexo 是基于 Node.js 所编写的一个静态博客网站生成器，非常方便。

官方文档：[Hexo](https://hexo.io/zh-cn/docs/)

## 准备

使用 Hexo 需要安装 Git 和 Node.js。

之后使用指令

```shell
npm install -g hexo-cli
```

安装 Hexo。

然后在指定文件夹下创建 Hexo 文件。

```shell
hexo init <folder>
cd <folder>
npm install
```

之后会生成如下格式的文件夹：

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

具体每个文件或目录的作用或功能如下：

 `_config.yml` 是配置文件，对博客的大部分配置都在此进行。

`package.json` 是应用程序的信息。可以自由移除。

  `scaffolds` 是模版文件夹。当新建文章时，Hexo 会根据 scaffold 来建立文件。

> Hexo的模板是指在新建的文章文件中默认填充的内容。例如，如果您修改scaffold/post.md中的Front-matter内容，那么每次新建一篇文章时都会包含这个修改。

`source` 是源文件等存放的地方。文章的源文件和相关的图片等都可以存储在这里。

> 资源文件夹是存放用户资源的地方。除 `_posts` 文件夹之外，开头命名为 `_` (下划线)的文件 / 文件夹和隐藏的文件将会被忽略。Markdown 和 HTML 文件会被解析并放到 `public` 文件夹，而其他文件会被拷贝过去。

`themes` 是主题文件夹。Hexo 会根据主题来生成静态页面。

## 配置文件

这里选一些比较重要的配置信息。

更多详情 [配置 | Hexo](https://hexo.io/zh-cn/docs/configuration)。

### 网站 Site

这部分是网站的基本配置。

其中 `language` 中文使用 `zh-CN` 或 `zn-hans`；`timezone` 为时区，国内一般用 `Asia/Shanghai`。

### 网址 URL

这部分是对网站的网址的相关配置。

这里有一个永久链接的概念：

> **固定链接**（**PermaLink**，**Permanent Link**的缩写）或称“**永久链接**”或“**静态链接**”，意指向一个特定网络日志（WebLog ，Blog）的永久固定标识符。一般情况下，固定链接指向的均为一个网络日志条目（Entry）的独立网页。默认存档设置包含基于数据库的存档和单独文件存档。默认情况下，固定链接被设置为链接到一个条目的单独存档页面中。你可以在网络日志的下方，或者在“发布时间”之后，看到 Permalink。点击 Permalink 将会把访问者导向到专属于该条目 (Entry) 的独立网页中，一般包含“添加评论”等功能。

### 目录 Directory

大概率不太会触碰。

### 文章 Writing

这部分是对文章的配置。

`auto_spacing` 在中文和英文中添加空格。

`titlecase:(true/false)` 将标题转化为 title case 的形式。

> Title Case是一种英语文本格式，它表示将每个单词的首字母大写，其余字母小写的写法。Title Case通常用于书籍、文章、标题、广告宣传语等需要突出显示的文字内容中。对于每个单词的首字母大写，除了冠词、介词和连词等较短的词以外，其他的单词都要大写。例如，Title Case将"The Quick Brown Fox Jumps Over the Lazy Dog"转化为"The Quick Brown Fox Jumps over the Lazy Dog"。在不同的英语国家和地区，Title Case的具体规则可能会略有不同，但基本原则是将每个单词的首字母大写。

`filename_case` 将文件名转化为小写（1）或大写（2）。

`highlight` 代码块的高亮设置。

`prismjs` 代码块的高亮设置。

### 分页 Pagination

`per_page` 每页的文章数量，为 0 关闭分页功能。

### 扩展 Extensions

`theme` 主题名称。

`theme_config` 对主题的配置文件，会覆盖当前的配置文件。

## 基本命令

```plain
hexo init [folder]
```

新建一个网站。如果没有设置 `folder` ，Hexo 默认在目前的文件夹建立网站。

```plain
hexo new [layout] <title>
```

新建一篇文章。`layout` 为版面设计。如果没有，默认为 ``default_layout``。

`-p` 参数表示文章的位置。默认是在 `source/_post/` 下创建新的文章。

```plain
hexo generate
hexo g
```

生成静态文件。

参数 `-d` 表示生成完之后立刻部署。

```plain
hexo server
```

启动本机服务器。默认访问网址为 `http://localhost:4000/`。

```plain
hexo deploy
hexo d
```

部署网站。

参数 `-g` 表示部署前先生成静态文件。

```plain
hexo render <file1> [file2] ...
```

渲染文件。将 Markdown 文件渲染为 Html 文件

参数 `-o` 表示输出文件。具体用法  `hexo render <file1> -o <file2>` 将 `file1` 的渲染结果输出到 `file2` 中。




