# Text selector

文本选择器用于文本选择。文本选择器将提取文本
从所选元素及其所有子元素开始。HTML将是
剥离,将仅返回文本。选择器将忽略其中的文本
`<script>`和`<style>`标签。新行`<br>`标签将替换为
换行符。您还可以将正则表达式应用于
结果数据。

## Configuration options

- 选择器-[CSS selector][css-selector]表示要从中获取数据的元素
    将被提取。
- 多个-正在提取多个记录。通常不应该
    检查。如果要在一页中使用多个文本选择器,请使用
    多个检查,那么您实际上可能需要
    [Element selector][element-selector]。
- 正则表达式-从结果中提取子字符串的正则表达式。
- 删除HTML
- 修剪文字
- 替换文字-可能在替换字段中使用正则表达式
- 文字前缀/后缀
- 延迟-延迟提取

### 正则表达式

正则表达式属性可用于提取文本的子字符串
选择器提取的内容。使用正则表达式时,整个匹配项
(第0组)将作为结果返回[www.regexr.com][regex-site]是一个
一个不错的网站,您可以在其中了解正则表达式并进行尝试。

以下是一些可能会有用的示例:

|文本|正则表达式|结果|
| ---------------- | ------------------------------ |- --------- |
|价格:14.99 \ $ | `[0-9]+\.[0-9]+` | 14.99 |
| ID:H83JKDX4 | `[A-Z0-9]{8}` | H83JKDX4 |
|日期:2014-08-20 | `[0-9]{4}\-[0-9]{2}\-[0-9]{2}` | 2014-08-20 |

## Use cases

**使用多个文本选择器每页提取一条记录**

例如,您正在抓取每页只有一篇文章的新闻网站。这一页
可能包含文章,标题,发布日期和作者。一个
_链接选择器_可以将刮板导航到这些文章页面中的每个页面。
多个文本选择器可以提取标题,日期,作者和文章。
对于文本选择器,应不选中_Multiple_选项,因为每个页面
仅提取一条记录。

![Fig. 1: Multiple text selectors per page][text-selector-multiple-single-text-selectors-in-one-page]

**每页使用多个文本选择器提取多个项目**

电子商务网站通常每页有多个项目。如果要刮
这些项目,您将需要一个_Element选择器_来选择项目包装器
元素和多个文本选择器,用于在每个项目包装器中选择数据
元件。

![Fig. 2: Multiple elements with text selectors. Some arrows are skipped.][text-selector-multiple-elements-with-text-selectors]

**每页提取多个文本记录**

例如,您要提取文章的评论。有多个
在单个页面中添加注释,则只需要注释文本(如果需要
其他评论属性,请参见上面的示例)。您可以使用
_文本选择器_以提取这些注释。_Text选择器_多个
应该检查属性,因为您将提取多个记录。

![Fig. 3: Text selector selects multiple comments][text-selector-multiple-per-page]

[regex-site]: http://www.regexr.com/
[text-selector-multiple-single-text-selectors-in-one-page]: ../images/selectors/text/text-selector-multiple-single-text-selectors-in-one-page.png?raw=true
[text-selector-multiple-elements-with-text-selectors]: ../images/selectors/text/text-selector-multiple-elements-with-text-selectors.png?raw=true
[text-selector-multiple-per-page]: ../images/selectors/text/text-selector-multiple-per-page.png?raw=true
[element-selector]: Element%20selector.md
[css-selector]: ../CSS%20selector.md