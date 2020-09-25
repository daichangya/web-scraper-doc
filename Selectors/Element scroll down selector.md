# Element scroll down selector

这是另一个与元素选择器相似的元素选择器,但
另外,它向下滚动页面多次以查找那些元素
当页面向下滚动到底部时添加。使用延迟
属性配置滚动和元素搜索之间的等待间隔。
没有找到新元素后,滚动将停止。如果页面可以滚动
然后,该选择器将陷入无限循环。

## Configuration options

- 选择器-元素的[CSS selector][css-selector]。
- 多个-正在提取多个记录(几乎总是
    选中)。通常不应选中子选择器的多个选项。
- 延迟-元素选择之前的延迟和滚动之间的延迟。这个
    通常应指定,因为不会立即从中加载数据
    向下滚动后的服务器。如果超过2000毫秒可能是一个不错的选择
    您不想因为服务器响应速度不够快而丢失数据。
- 分页限制-您希望选择器执行的点击次数。

## Use cases

请参阅[Element selector][element-selector]用例。

[element-selector]: Element%20selector.md
[css-selector]: ../CSS%20selector.md