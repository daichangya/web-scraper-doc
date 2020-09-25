# Element style selector

元素样式选择器可以提取HTML元素的样式值。
例如,您可以使用此选择器从中提取with属性
这个div:`<div style="width: 20px;"><div>`。

## Configuration options

- 选择器-元素的[CSS selector][css-selector]。
- 多个-正在提取多个记录。
- 样式名称-将要提取的属性。例如
    `width`,`background-image`。
- 删除HTML
- 修剪文字
- 替换文字-可能在替换字段中使用正则表达式
- 文字前缀/后缀
- 延迟-延迟提取

## Use cases

请参阅[Text selector][text-selector]用例。

[text-selector]: Text%20selector.md
[css-selector]: ../CSS%20selector.md