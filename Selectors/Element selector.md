# Element selector

元素选择器用于包含多个数据元素的元素选择。
例如,元素选择器可能用于选择列表中的项目列表
电子商务网站。选择器将返回每个选定的元素作为父元素
元素的子选择器。元素选择器子选择器将是
仅在元素选择器提供的元素内提取数据。

注意!如果页面在向下滚动或单击后动态加载新项目
在按钮上,那么您应该尝试使用以下选择器:

- [Element scroll down selector][element-scroll-selector]
- [Element click selector][element-click-selector]

## Configuration options

- 选择器-[CSS selector][css-selector]用于将要包装的元素
    用作子选择器的父元素。
- 多个-正在提取多个记录(几乎总是
    选中)。通常不应选中子选择器的多个选项。
- 延迟-延迟提取

## Use cases

#### 从页面中选择多个电子商务项目

例如,一个电子商务站点的页面带有项目列表。带元素
选择器,您可以选择包装这些项目的元素,然后添加
多个子选择器可在项目包装器中提取数据
元件。图1显示了如何在其中使用元素选择器
情况。

![Fig. 1: Multiple items selected with element selector][multiple-elements-with-text-selectors]

#### 从表中提取数据

与电子商务项目选择类似,您还可以选择表行并添加
子选择器,用于从表单元格提取数据。
尽管[Table selector][table-selector]可能是更好的解决方案。

[css-selector]: ../CSS%20selector.md
[element-scroll-selector]: Element%20scroll%20down%20selector.md
[element-click-selector]: Element%20click%20selector.md
[table-selector]: Table%20selector.md
[multiple-elements-with-text-selectors]: ../images/selectors/text/text-selector-multiple-elements-with-text-selectors.png?raw=true