# Selectors

Web刮板具有多个选择器,可用于不同类型的数据
提取以及与网站的不同交互。选择器可以
分为三组:

-用于数据提取的数据提取选择器。
-用于网站导航的链接选择器。
-用于分隔多个记录的元素选择的元素选择器

### 数据提取选择器

数据提取选择器仅从所选元素返回数据。
例如[Text selector][text-selector]从中提取文本
选定的元素。这些选择器可用作数据提取选择器:

- [Text selector][text-selector]
- [Link selector][link-selector]
- [Link popup selector][link-popup-selector]
- [Image selector][image-selector]
- [Document selector][document-selector]
- [Constant Value][constant-value]
- [Table selector][table-selector]
- [Element attribute selector][element-attribute-selector]
- [Element style selector][element-style-selector]
- [HTML selector][html-selector]
- [Grouped selector][grouped-selector]

### 链接选择器

链接选择器从链接中提取URL,这些链接以后可打开以获取数据
萃取。例如,如果在站点地图树中有一个_Link选择器_
3个子文本选择器,然后Web爬网程序使用_Link提取所有URL
选择器_,然后打开每个链接并使用那些子数据提取选择器
提取数据。当然,链接选择器可能会将_Link selectors_作为子级
选择器,则这些子_Link选择器_将用于下一页
导航。这些是当前可用的_Link选择器_:

- [Link selector][link-selector]
- [Link popup selector][link-popup-selector]

### 元素选择器

元素选择器用于包含多个数据元素的元素选择。
例如,元素选择器可用于选择列表中的项目列表
电子商务网站。选择器将返回每个选定的元素作为父元素
元素的子选择器。元素选择器子选择器将
仅在元素选择器提供的元素内提取数据。
这些是当前可用的元素选择器:

- [Element selector][element-selector]
- [Element scroll down selector][element-scroll-selector]
- [Element click selector][element-click-selector]

### 输入值

该选择器用于与页面进行交互。例如,以搜索形式输入值。

- [Input Value][input-value]

## Selector configuration options

每个选择器都有配置选项。在这里您可以看到最常见的。
特定于选择器的配置选项在
选择器文档。

-选择器-CSS选择器,用于选择要使用的元素
    上。
-多个-当要访问多个记录(数据行)时应检查
    使用此选择器提取。从两个或多个选择器提取的数据
    多个选中项不会合并在单个记录中。
-延迟-使用选择器之前的延迟。
-父选择器-为此选择器配置父选择器以使
    选择器树。

注意!使用多个配置选项时的一个常见错误是创建
两个选择器以及多个选中项,并期望刮板将
成对连接选择器值。例如,如果您选择了分页链接,
导航链接这些链接不能成对逻辑连接。正确的
方法是使用元素选择器选择包装器元素并添加数据选择器
作为未选中具有多个选项的元素选择器的子选择器。

[text-selector]: Selectors/Text%20selector.md
[link-selector]: Selectors/Link%20selector.md
[link-popup-selector]: Selectors/Link%20popup%20selector.md
[image-selector]: Selectors/Image%20selector.md
[element-attribute-selector]: Selectors/Element%20attribute%20selector.md
[element-style-selector]: Selectors/Element%20style%20selector.md
[table-selector]: Selectors/Table%20selector.md
[grouped-selector]: Selectors/Grouped%20selector.md
[html-selector]: Selectors/HTML%20selector.md
[element-selector]: Selectors/Element%20selector.md
[element-click-selector]: Selectors/Element%20click%20selector.md
[element-scroll-selector]: Selectors/Element%20scroll%20down%20selector.md
[document-selector]: Selectors/Document%20selector%20.md
[constant-value]: Selectors/Constant%20value.md
[input-value]: Selectors/Input%20value.md