# Scraping a site

打开您要抓取的网站。

## Create Sitemap

创建_sitemap_时,您需要做的第一件事就是指定
起始网址。这是开始抓取的网址。你也可以
如果抓取应从多个位置开始,请指定多个起始网址。
例如,如果您要抓取多个搜索结果,则可以创建
每个搜索结果的单独起始网址。

### 指定多个带有范围的网址

如果网站在页面URL中使用编号,则创建起来要简单得多
范围起始网址,而不是创建用于浏览网站的_Link选择器_。
要指定范围网址,请用范围替换起始网址的数字部分
定义- `[1-100]`。如果网站在网址中使用零填充,则添加零
填充到范围定义- `[001-100]`。如果您想跳过一些网址
那么您还可以像这样`[0-100:10]`指定增量。

像这样`http://example.com/page/[1-3]`使用范围网址来链接如下:

- `http://example.com/page/1`
- `http://example.com/page/2`
- `http://example.com/page/3`

像这样`http://example.com/page/[001-100]`使用零填充的范围网址
对于这样的链接:

- `http://example.com/page/001`
- `http://example.com/page/002`
- `http://example.com/page/003`

像这样`http://example.com/page/[0-100:10]`使用范围网址递增
像这样的链接:

- `http://example.com/page/0`
- `http://example.com/page/10`
- `http://example.com/page/20`

## Create selectors

创建_sitemap_之后,您可以向其添加选择器。在里面
_Selectors_面板中,您可以添加新的选择器,对其进行修改并在
选择器树。
可以以树型结构添加选择器。网页刮板将
按照选择器在树中的排列顺序执行选择器
结构体。例如,有一个新闻网站,您想抓取所有文章
其链接在第一页上可用。在图1中,您可以看到
示例网站。

![Fig. 1: News site][image-news-site]

要抓取该网站,您可以创建一个_Link选择器_,它将提取所有
第一页中的文章链接。然后,作为子选择器,您可以添加
_Text选择器_将从以下文章页面中提取文章:
_链接选择器_找到了链接。下图说明了_sitemap_
应该为新闻站点而构建。

![Fig. 2: News site sitemap][image-news-site-sitemap]

请注意,在创建选择器时,请使用“元素预览”和“数据预览”功能
以确保您选择了具有正确数据的正确元素。

选择器中提供了有关选择器树构建的更多信息。
文档。您应该至少了解以下核心选择器:

- [Text selector][text-selector]
- [Link selector][link-selector]
- [Element selector][element-selector]

### 检查选择器树

为_sitemap_创建选择器后,您可以检查树
选择器图形面板中选择器的结构。下图显示了
示例选择器图。

![Fig. 3: News site selector graph][image-news-site-selector-graph]

## Scrape the site

为_sitemap_创建选择器后,即可开始抓取。打开
_Scrape_面板并开始抓取。一个新的弹出窗口将打开,其中
刮板将加载页面并从中提取数据。刮完后
弹出窗口将关闭,并且将弹出消息通知您。您可以查看
通过打开_Browse_面板来抓取数据,并通过打开
_导出数据_面板。

[image-news-site]: images/scraping-a-site/news-site.png?raw=true
[image-news-site-sitemap]: images/scraping-a-site/news-site-sitemap.png?raw=true
[image-news-site-selector-graph]: images/scraping-a-site/news-site-selector-graph.png?raw=true
[text-selector]: Selectors/Text%20selector.md
[link-selector]: Selectors/Link%20selector.md
[element-selector]: Selectors/Element%20selector.md