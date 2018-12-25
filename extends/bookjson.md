# book.json示例

我的`book.json` 模板，仅供参考，有注释，**使用时需要去掉注释**。

```json
{
	"title": "gitbook入门教程",
	"author": "_yuusha",
	"description": "记录学习gitbook过程中的总结...", // 本书的简单描述，默认是从 README（第一段）中提取
	"language": "zh-hans", // 指定文档语言为中文简体，左上角搜索会显示中文placeholder
	"gitbook": ">=3.0.0", // 指定gitbook版本
	"links" : { // 左侧导航栏添加链接
		"sidebar" : {
			"码梦人" : "http://m.yumecoder.top", 
		}
	},
	"styles": { // 添加自定义的页面样式
		"website": "styles/website.css",
		"ebook": "styles/ebook.css",
		"pdf": "styles/pdf.css",
		"mobi": "styles/mobi.css",
		"epub": "styles/epub.css"
	},
	"plugins": [ // 配置插件，gitbook默认自带5个:highlight，search，sharing，font-settings，livereload
		"-lunr", // 去除lunr
		"-search", //去除自带的search
		"search-plus", //添加支持中文搜索的search-plus
		"splitter", // 侧边栏宽度调节
		"-sharing", // 去除自带的分享插件，增加sharing-plus
		"sharing-plus",
		"tbfed-pagefooter", // 添加脚注
		"donate", // 添加打赏功能
		"anchor-navigation-ex", // 添加Toc到侧边悬浮导航以及回到顶部按钮
		"favicon", // 更改网站favicon
		"versions-select", // 文档版本选择
		"ace", // 支持代码在线编辑
		"github-buttons", //添加项目在 github 上的 star，watch，fork情况
		"alerts", // alerts样式，包含success，info，warning，danger
		"edit-link" // 编辑此页按钮
	],
	"pluginsConfig": { // 配置插件的属性
		"fontsettings": { // 设置gitbook自带的fontSettings插件的属性
			"theme": "white",
			"family": "sans",
			"size": 2
		},
		"sharing": { // 分享插件配置
			"qq": true,
			"weibo": true,
			"qzone": true,
			"google": true,
			"all": ["facebook", "google", "twitter", "weibo", "qq", "qzone"]
		},
		"tbfed-pagefooter": { // 脚注配置
			"copyright": "Copyright &copy; yumecoder.top 2018",
			"modify_label": "最后修改时间:",
			"modify_format": "YYYY-MM-DD HH:mm:ss"
		},
		"donate": { // 打赏插件配置
          "wechat": "/images/donation_img/wechat_qr.png",
          "alipay": "/images/donation_img/alipay_qr.jpg",
          "title": "",
          "button": "赏",
          "alipayText": "支付宝打赏",
          "wechatText": "微信打赏"
        },
		"anchor-navigation-ex": {
			"multipleH1": false, // 如果一个md文档中只有一个H1，设为false
			"showLevel" : false, // 是否在锚点导航的标题前展示层级序号
        },
		"favicon": {
			 "shortcut": "/images/favicon/favicon.ico"
		},
		"versions": {
			"gitbookConfigURL": "", // 绑定url，更改book.json自动更新
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
		},
		"github-buttons": {
			"buttons": [{
				"user": "ks4na",
				"repo": "gitbook-usage",
				"type": "star",
				"size": "small",
				"count": true
		    }, {
				"user": "ks4na",
				"type": "follow",
				"width": "230", // 自定义大小
				"count": false
		    }]
		},
		 "edit-link": {
            "base": "https://github.com/ks4na/gitbook-usage/edit/master",
            "label": "Edit This Page"
        }
	}
	
}
```

