# GitBook插件

记录本人基于参考的几篇文档总结下来会用到的插件，更多插件可以到 [插件官网](https://plugins.gitbook.com) 去搜索。

- [search-plus](#search-plus)
- [github-buttons](#github-buttons)
- [ace](#ace)
- [splitter](#splitter)
- [sharing-plus](#sharing-plus)
- [ tbfed-pagefooter](#tbfed-pagefooter)
- [donate](#donate)
- [anchor-navigation-ex](#anchor-navigation-ex)
- [edit-link](#edit-link)
- [favicon](#favicon)
- [alerts](#alerts)
- [version-select](#version-select)



## search-plus

支持中文搜索，需要将默认的 `search`  和 `lunr`去掉。

[插件地址](https://plugins.gitbook.com/plugin/search-plus)

```sh
"plugins": [
    "-lunr",
    "-search",
    "search-plus"
]
```

## github-buttons

添加项目在github上的star，fork，watch情况。

[插件地址](https://plugins.gitbook.com/plugin/github-buttons)

```sh
"plugins": [
    "github-buttons"
],
"pluginsConfig": {
    "github-buttons": {
        "buttons": [{
            "user": "ks4na",
            "repo": "dafaERP-guide-Java",
            "type": "star",
            "size": "small",
            "count": true
        }, {
            "user": "ks4na",
            "type": "follow",
            "width": "230",
            "count": false
        }]
    }
}
```

## ace

代码编辑插件。

[插件地址](https://plugins.gitbook.com/plugin/ace)

>  默认情况下，line-height为1，显得比较挤，可以在 `styles/website.css` 中加入代码指定ace字体的大小：

```css
.aceCode {
    font-size: 14px !important;
}
```

```sh
"plugins": [
    "ace"
]
```

使用方法见插件地址中的介绍，效果如下：

{%ace edit=true, lang='javascript', theme="monokai"%}
function compare(a, b){
    return a > b ? 1 : a === b ? 0 : -1
}

compare(1, 2)
{%endace%}

## splitter

使侧边栏宽度可自由调节。

[插件地址](https://plugins.gitbook.com/plugin/splitter)

```sh
"plugins": [
    "splitter"
]
```

## sharing-plus

分享插件，比默认的 `share` 多了一些分享方式。

[插件地址](https://plugins.gitbook.com/plugin/sharing-plus)

```sh
"plugins": [
	"-share",
    "sharing-plus"
],
"pluginsConfig": {
    "sharing": {
        "qq": true,
        "weibo": true,
        "qzone": true,
        "google": true,
        "all": ["facebook", "google", "twitter", "weibo", "qq", "qzone"]
    }
}
```

## tbfed-pagefooter

页脚插件

[插件地址](https://plugins.gitbook.com/plugin/tbfed-pagefooter)

```sh
"plugins": [
    "tbfed-pagefooter"
],
"pluginsConfig": {
    "tbfed-pagefooter": {
        "copyright": "Copyright &copy; yumecoder.top 2018",
        "modify_label": "最后修改时间：",
        "modify_format": "YYYY-MM-DD HH:mm:ss"
    }
}
```

## donate

打赏插件

[插件地址](https://plugins.gitbook.com/plugin/donate)

```sh
"plugins": [
    "donate"
],
"pluginsConfig": {
    "donate": {
        "wechat": "/images/donation_img/wechat_qr.png",
        "alipay": "/images/donation_img/alipay_qr.jpg",
        "title": "",
        "button": "赏",
        "alipayText": "支付宝打赏",
        "wechatText": "微信打赏"
    }
}
```

##  anchor-navigation-ex

添加Toc到侧边悬浮导航以及回到顶部按钮。需要注意以下两点： 

- 只会提取 h[1-3] 标签作为悬浮导航 

- 只有按照以下顺序嵌套才会被提取 

  ```markdown
  # h1
  ## h2
  ### h3
  必须以h1开始，直接写h2不会被提取
  ```

[插件地址](https://plugins.gitbook.com/plugin/anchor-navigation-ex)

```sh
"plugins": [
    "anchor-navigation-ex"
],
"pluginsConfig": {
    "anchor-navigation-ex": {
        "multipleH1": false,
        "showLevel" : false
    }
}
```

## edit-link

如果将 GitBook 的源文件保存在 github 或者其他的仓库上，使用该插件可以链接到当前页的源文件上。 

[插件地址](https://plugins.gitbook.com/plugin/edit-link)

```sh
"plugins": [
    "edit-link"
],
"pluginsConfig": {
    "base": "https://github.com/ks4na/dafaERP-guide-Java/edit/master",
    "label": "Edit This Page"
}
```

## favicon

更改网站的favicon.ico

```sh
"plugins": [
    "favicon"
],
"pluginsConfig": {
    "favicon": {
    	"shortcut": "images/favicon/favicon.ico"
    }
}
```

## alerts

添加不同 alerts 样式的 blockquotes，目前包含 info, warning, danger 和 success 四种样式。 

[插件地址](https://plugins.gitbook.com/plugin/alerts)

```sh
"plugins": [
    "alerts"
]
```

使用示例：

```sh
Info styling
> **[info] For info**
>
> Use this for infomation messages.

Warning styling
> **[warning] For warning**
>
> Use this for warning messages.

Danger styling
> **[danger] For danger**
>
> Use this for danger messages.

Success styling
> **[success] For info**
>
> Use this for success messages.
```

效果如下：

Info styling
> **[info] For info**
>
> Use this for infomation messages.

Warning styling
> **[warning] For warning**
>
> Use this for warning messages.

Danger styling
> **[danger] For danger**
>
> Use this for danger messages.

Success styling
> **[success] For info**
>
> Use this for success messages.

## version-select

添加版本选择的下拉框，针对文档有多个版本的情况。

[插件地址](https://plugins.gitbook.com/plugin/versions-select)

```sh
"plugins": [
    "version-select"
],
"pluginsConfig": {
    "version-select": {
        "options": [
            {
                "value": "http://localhost:4000",
                "text": "v3.2.3"
            },
            {
                "value": "http://localhost:5000",
                "text": "v2.6.9"
            }
        ]
    }
}
```

