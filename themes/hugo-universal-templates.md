# hugo-universal主题模块说明

使用该主题的网站的`config.toml`配置文件示例如下（以<https://servicemesher.github.io/>为示例）：

```toml
# 网站的根URL
baseurl = "https://servicemesher.github.io/"
# 首页的标题
title = "ServiceMesher"
# 设置使用的主题
theme = "hugo-universal-theme"
# 设置网站默认的语言，所有的语言翻译文件在i18n目录下，文件名于此处配置的语言代码相同
languageCode = "zh"
defaultContentLanguage = "zh"
# 值为空的话则不启用disqus，因为需要翻墙才能访问，所以我们不启用
disqusShortname = ""
# 取消默认的代码高亮，我们使用prism代码高亮
pygmentsUseClasses = false
pygmentCodeFences = true

# 每页显示的文章数量用于分页
paginate = 10

[menu]

# 板块化分
# 权重对应在页面上显示的次序

[[menu.main]]
    name = "主页"
    url  = "/"
    weight = 1

[[menu.main]]
    name = "博客"
    url  = "/blog/"
    weight = 2

[[menu.main]]
    name = "活动"
    identifier = "activity"
    url  = "/activity/"
    weight = 3

[[menu.main]]
    name="黄页"
    url = "/awesome-servicemesh/"
    weight = 4

[[menu.main]]
    name = "联系我们"
    url  = "/contact/"
    weight = 5

# 顶栏，可选择显示

[[menu.topbar]]
    weight = 1
    name = "GitHub"
    url = "https://github.com/servicemesher"
    pre = "<i class='fa fa-2x fa-github'></i>"

[[menu.topbar]]
    weight = 4
    name = "Email"
    url = "mailto:jimmysong@jimmysong.io"
    pre = "<i class='fa fa-2x fa-envelope'></i>"

# 配置参数，HTML中可以引用
[params]
    viewMorePostLink = "/blog/"
    author = "ServiceMesher"
    # 文章默认的SEO设置
    defaultKeywords = ["service mesh"]
    defaultDescription = "Service Mesh爱好者网站"
    
    # 浏览器中看到每一页的后缀，与原文标题使用·分隔
    description = "Service Mesh爱好者"
    # 留空，不启用谷歌地图
    googleMapsApiKey = ""
    # Baidu统计的token
    baiduKey="761ec5e305f799778975c1f71c47a520"
    
    # 选用的 CSS，可选的有：default（浅蓝）、blue、green、marsala,、pink、red、turquoise、violet（我用的这个）
    style = "violet"

    # 404页面显示的图片
    errorimage = "https://ws1.sinaimg.cn/large/00704eQkgy1frkahxdca2j30hd08wq52.jpg"
	# 页脚显示的关于信息
    about_us = "<p>Service Mesh 爱好者</p>"
    copyright = "Copyright ©️ 2018, ServiceMesher all rights reserved."

    # Go语言格式的时间模板
    date_format = "2006-01-02"
	# 网站logo
    logo = "img/logo.png"
    address = """<p><strong>ServiceMesher.</strong>
      """

[Permalinks]
	# 博客中文章的URL规则，可以为/blog/2018/05/24/mypost/
    #blog = "/blog/:year/:month/:day/:filename/"
    blog = "/blog/:filename/"

# 是否启用顶层通知栏
[params.topbar]
    enable = false 
    text = """<p class="hidden-sm hidden-xs">欢迎来到 Service Mesh 爱好者网站</p>
      """

# 是否启用右侧的小工具
[params.widgets]
    categories = true
    tags = true
    search = true

[params.carousel]
    enable = true
    # 设置首页大风车的背景图片
    background = "https://ws1.sinaimg.cn/large/00704eQkgy1frlkpcfzt4j30zk0k0at2.jpg" 

# 功能显示栏目
[params.features]
    enable = true

# 社区活动栏目
[params.testimonials]
    enable = true
    title = "社区活动"
    subtitle = "我们会不定期得在线上和线下举办精彩的活动，敬请关注，下面是历史活动记录"

# 参与进来栏目
[params.see_more]
    enable = true
    icon = "fa fa-pagelines"
    title = "参与进来"
    subtitle = "加入 Service Mesh 爱好者群体"
    link_url = "/contact"
    link_text = "查看加入方式"

# 参与者栏目
[params.clients]
    enable = true
    title = "参与者"
    subtitle = "Envoy官方文档中文版卓越贡献者"

# 最新博客栏目
[params.recent_posts]
    enable = true
    title = "最新博客"
    subtitle = "社区参与者的博客与最 in 的新闻都在这里"
```

## 资源目录

所有的静态资源保存在`static`目录下。

所有的自定义模块的配置都在`data`目录下，使用YAML格式配置。

JPG格式的图片使用微博图床保存。

因为微博图床只能保存JPG格式的图片，主题中使用了部分PNG格式（图片支持透明）保存在GitHub中。