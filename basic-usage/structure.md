# 目录结构

GitBook 的基本目录结构如下：

```sh
.
├── book.json
├── README.md
├── SUMMARY.md
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

下面主要介绍一下GitBook预定义的几个文件的作用。

## SUMMARY.md

概要文件存放GitBook的文件目录信息，左侧的目录就是根据这个文件来生成。 通过 Markdown 中的列表语法表示文件父子关系，下面是一个示例：

```markdown
# Summary
* [Introduction](README.md)
* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)
```

这个配置对应的目录结构如下图所示：

 ![summary1](../images/summary1.png)

> **[info] 提示**
>
> 可以使用 `---` 来在左侧导航中生成水平分割线。

## README.md

README文件存放整篇文档的概要介绍，生成的html文档首页就是README.md。

## book.json（可选）

存放配置信息，下一节中所讲的 [配置信息](./conf.md) 都是在这个文件里定义的。

## GLOSSARY.md（可选）

术语表文件， 允许你指定术语并且在术语表中显示它们各自的定义。基于这些术语，GitBook会自动建立索引并高亮这些在文中的术语。 

`GLOSSARY.md`  的格式非常简单： 

```sh
## Git
分布式版本控制软件

## Markdown
Aaron Swartz 跟John Gruber共同设计的排版语言
```

效果如下：

Git Markdown

## LANGS.md(可选)

GitBook支持使用多语言来构建书本。按照GitBook的标准格式，每个语言应该作为一个子目录，命名为 `LANGS.md` 的文件应该遵循下面的格式并出现在仓库的根目录下： 
```markdown
* [英语](en/)
* [法语](fr/)
* [西班牙语](es/)
```
可以从 [Learn Git](https://github.com/GitbookIO/git) 这本书中看到一个完整的例子。 

## 忽略文件和文件夹

GitBook会读取 `.gitignore`，`.bookignore`，`.ignore` 文件来获取忽略的文件和目录的列表。 

```sh
# 这是一个注释

# 忽略文件test.md
test.md

# 忽略文件夹 "bin" 中的所有内容
bin/*
```