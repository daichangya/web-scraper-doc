# Link selector

链接选择器用于链接选择和网站导航。如果您使用
_Link选择器_,不带任何子选择器,则它将提取链接并
链接的href属性。如果您将子选择器添加到_Link选择器_
那么这些子选择器将在此链接引导的页面中使用
至。如果要选择多个链接,请检查_multiple_属性。

注意!链接选择器仅适用于具有`href`属性的`<a>`标记。如果
链接选择器不适合您,那么您可以尝试以下解决方法:

1. 单击某项后,检查网址栏中的链接是否已更改(更改
    仅在哈希标记不计算在内之后)。如果链接没有更改,则该站点
    可能正在使用ajax进行数据加载。而不是使用链接选择器
    应该使用[Element click selector][element-click]。
2. 如果该站点打开一个弹出窗口,则应使用
    [Link popup selector][link-popup]
3. 该站点可能正在使用JavaScript `window.location`更改URL。网页
    Scraper目前无法处理这种导航。

## Configuration options

- 选择器-[CSS selector][css-selector]用于链接元素
    导航链接将被提取。
- 多个-正在提取多个记录。通常应检查。
- 延迟-延迟提取

## Use cases

**通过多级导航进行导航**

例如,一个电子商务网站具有多级导航-
`categories -> subcategories`。从所有类别中抓取数据和
子类别中,您可以创建两个_Link选择器_。一个选择器将选择
类别链接,另一个选择器将选择以下子类别链接
在类别页面中可用。子类别_Link选择器_应该是
作为_Link选择器_类别的子级。数据提取的选择器
子类别页面中的内容应作为子类别的子选择器
选择器。

![Fig. 1: Multiple link selectors for category navigation][multiple-level-link-selectors]

**手柄分页**

例如,一个电子商务网站具有多个类别。每个类别都有一个
项目列表和分页链接。另外有些页面无法直接访问
在类别中,但在分页页面中可用(您可以看到
分页链接1-5,但不是6-8)。您可以先建立一个
访问每个类别并从类别页面提取项目。该站点地图将
仅从第一个分页中提取项目。从所有项目中提取项目
分页链接,包括开始时不可见的分页链接
您需要创建另一个_Link选择器_来选择分页链接。
图2显示了应如何在站点地图中创建链接选择器。什么时候
刮板将打开一个类别链接,它将提取可用于
这一页。之后,它将找到分页链接并也访问这些链接。如果
分页链接选择器成为其自身的子级,它将递归
发现所有分页页面。图3显示了一个选择器图,您可以在其中选择
了解分页链接如何发现更多的分页链接和更多数据。

![Fig. 2: Sitemap with Link selector for pagination][pagination-link-selectors]
![Fig. 3: Selector graph with pagination][pagination-selector-graph]

[multiple-level-link-selectors]: ../images/selectors/link/multiple-level-link-selectors.png?raw=true
[pagination-link-selectors]: ../images/selectors/link/pagination-link-selectors.png?raw=true
[pagination-selector-graph]: ../images/selectors/link/pagination-selector-graph.png?raw=true
[element-click]: Element%20click%20selector.md
[link-popup]: Link%20popup%20selector.md
[css-selector]: ../CSS%20selector.md