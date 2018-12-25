# GitBook配置

记录GitBook的一些配置信息

- [title - 标题](#title)
- [author - 作者](#author)
- [description - 描述](#description)
- [language - 语言](#language)
- [gitbook - 指定gitbook版本](#gitbook)
- [links - 侧边栏添加链接](#links)
- [styles - 自定义样式](#styles)
- [plugins - 插件](#plugins)
- [pluginsConfig - 插件配置](#pluginsconfig)
- [structure - 自定义默认文件的位置](#structure)

## title 

设置书籍的标题

```sh
"title": "GitBook Usage"
```

## author

作者的相关信息

```sh
"author": "_yuusha"
```

## description

本书的简单描述

```sh
"description": "GitBook的使用笔记"
```

## language

本文档使用的语言，如配置使用中文简体

```sh
"language": "zh-hans"
```

## gitbook

指定所使用的gitbook的版本

```sh
"gitbook": ">=3.0.0",
"gitbook": "3.2.3"
```

## links

为左侧导航栏添加链接

```sh
"links": {
    "sidebar": {
        "yumecoder": "http://m.yumecoder.top"
    }
}
```

## styles

自定义页面样式，默认情况下各generator对应的css文件

```sh
"styles": {
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
    "pdf": "styles/pdf.css",
    "mobi": "styles/mobi.css",
    "epub": "styles/epub.css"
}
```

例如使 `h1`, `h2` 标签有下边框，可以在 `styles/website.css` 中设置：

```css
h1, h2 {
    border-bottom: 1px solid #eee;
}
```

## plugins

配置使用的插件

> 可以在 [插件官网](https://plugins.gitbook.com) 上查找插件安装

```sh
"plugins": [
    "alerts",
    "donate"
]
```

添加了新的插件之后需要运行 `gitbook install`  来安装新的插件

GitBook默认带有5个插件：

- highlight
- search
- sharing
- font-settings
- livereload

如果需要去除自带的插件，可以在插件名称前面加上 `-` , 例如去除自带的 `search` ，替换成支持中文搜索的 `search-plus` ：

```sh
"plugins": [
    "-search",
    "search-plus"
]
```

## pluginsConfig

配置插件的属性

```sh
"pluginsConfig": {
    "fontSettings": {
        "theme": "sepia",
        "family": "serif",
        "size": 2
    }
}
```

## structure

指定README，SUMMARY，GLOSSARY，LANGS 等文件的位置，覆盖GitBook使用的默认路径。 

```sh
{
    "structure": {
        "readme": "INTRO.md"
    }
}
```

| 变量                | 默认值      |
| ------------------- | ----------- |
| structure.readme    | README.md   |
| structure.summary   | SUMMARY.md  |
| structure.glossary  | GLOSSARY.md |
| structure.languages | LANGS.md    |

