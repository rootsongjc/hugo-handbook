# hugo-universal主题配置说明

该主题包括以下几个分模块，用来配置登录页面上的六个模块，其中有四个模块的自定义配置在`data`目录下，下面的模块顺序按出现在主页上的顺序排列：

- carousel：登录页面上的以风车形式显示的背景也页面以及页面上的文字
- features：功能特性模块
- clients：参与者配置
- see_more：查看更多/参与进来，在`config.toml`中配置
- recent_posts：最新博客，在`config.toml`中配置
- testimonials：最新活动与客户评价

## carousel

![风车模块](https://ws1.sinaimg.cn/large/00704eQkgy1frnoluj5z8j32520pmwvi.jpg)

示例配置如下：

```yaml
weight: 1
title: "Envoy proxy"
description: >
  <ul class="list-style-none">
    <li>开源</li>
    <li>专为云原生应用而设计</li>
    <li>边缘和服务间代理</li>
    <li>Istio 默认的数据平面</li>
    <li><a href="https://servicemesher.github.io/envoy">访问 Envoy 中文文档</a></li>
  </ul>
image: "img/carousel/envoy-gitbook.png"
```

- weight：权重，决定显示顺序
- title：标题
- description：支持HTML
- image：显示的图片

可以配置多个页面，每个页面分别在一个YAML文件中配置，可以配置多个，建议是偶数个，因为这样当在大页面中显示会比较好看。

## features

![](https://ws1.sinaimg.cn/large/00704eQkgy1frnp9ss738j32360xajuj.jpg)

示例配置如下：

```yaml
weight: 1
name: "智能路由和负载均衡"
icon: "fa fa-exchange"
description: "控制服务间流量并进行动态负载均衡"
```

- weight：图标的权重
- name：显示的标题
- icon：使用[awesome-font](www.bootcss.com/p/font-awesome/) CSS中的icon
- description：描述

每个图标的配置都在一个单独的YAML中，可以配置多个，建议是偶数个，因为这样当在大页面中显示会比较好看。

## testimonials

![testimonials模块](https://ws1.sinaimg.cn/large/00704eQkgy1frnoobj2wcj32580uunin.jpg)

示例配置如下：

```yaml
text: "Envoy 最新版的官方文档中文版翻译活动正在进行中，赶快参与进来吧！参与翻译和校对，为社区贡献力量！[查看参与方式](https://github.com/servicemesher/envoy/blob/master/CODE_OF_CONDUCT.md)"
name: "Jimmy Song"
position: "发起者"
avatar: "https://ws1.sinaimg.cn/large/00704eQkgy1frmobjwmuoj31z21z61ky.jpg"
```

- text：支持HTML
- name：发布者名字
- position：发布者头衔（SM capital即网站管理员）
- avatar：发布者头像，使用微博图床，图片为正方形，至少200*200像素

## see_more

![see more模块](https://ws1.sinaimg.cn/large/00704eQkgy1frnox9lwmfj32520ky1kx.jpg)

示例配置如下：

```yaml
[params.see_more]
    enable = true
    icon = "fa fa-pagelines"
    title = "参与进来"
    subtitle = "加入 Service Mesh 爱好者群体"
    link_url = "/contact"
    link_text = "查看加入方式"
```

- icon：图标配置，图标来自[awesome-font](www.bootcss.com/p/font-awesome/) CSS
- title：标题
- subtitle：副标题
- link_url：链接URL
- link_text：按钮上的文字

## recent_posts

![](https://ws1.sinaimg.cn/large/00704eQkgy1frnpesf006j320c1461kx.jpg)

配置项如下：

```yaml
[params.recent_posts]
    enable = true
    title = "最新博客"
    subtitle = "社区参与者的博客与最 in 的新闻都在这里"
```

该配置是在`config.toml`中配置的。

## 图片说明

除了PNG格式的图片，其它图片都使用微博图床，默认的本地图片位置在`static/img`目录下，该目录下包括如下图片：

| 文件/目录名称        | 说明                                                         | 大小（像素） | 是否透明 |
| -------------------- | ------------------------------------------------------------ | ------------ | -------- |
| apple-touch-icon.png | 在苹果触摸设备上（如iPhone和iPad上）显示的网站favicon        | 128*128      | 是       |
| carousel目录         | 风车中的图片                                                 | 800*400      | 是       |
| clients              | 参与者配置中的图片，图片中间显示为原型                       | 320*180      | 是       |
| favicon.ico          | favicon                                                      | 128*128      | 是       |
| logo-small.png       | 在小屏幕上（如手机）显示的logo图片，现在默认使用图片根logo.png，可以再弄个小点的图片 | 187*42       | 是       |
| logo.png             | 默认的网站logo，显示在页面左上角                             | 187*42       | 是       |

以上图片是必须在网站中存储和使用的图片，还有一些地方使用图床中的图片，不需要在本地保存，请参考`config.toml`中的说明。

## 其它配置

其它配置都在 `config.toml` 中，请参考[hugo-universal主题模块说明](hugo-universal-templates.md)。