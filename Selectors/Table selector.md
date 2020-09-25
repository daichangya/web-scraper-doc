# Table selector

表选择器可以从表中提取数据。_Table选择器_具有3个可配置的CSS选择器。
选择器用于表格选择。
如果header是一列,则可以使用_This是vertical table_提示来选择垂直表类型。

您可以从复杂的标头(由多个行和子字符串组成)中提取数据,也可以从复杂的行(其单元格可以
包含子字符串)。
选择选择器之后,_Table selector_ scraper会自动为您建议标题的CSS
和基于表格HTML的行。
如果表头是由th或tbody标签定义的,则表的类型将自动确定(垂直或水平)。

您可以在这些选择器上单击“元素预览”,以查看_Table selector_是否正确找到了表头和数据行。
如果自动检测失败,则可以像使用表选择器一样自行选择标题和数据行选择器。
从多个页面提取数据时,标题行选择器用于标识表列。

您还可以在提取的数据中重命名表列,并仅在输出数据中包括所需的列。
如果在数据提取期间发现新列,则也可以将它们添加到提取的数据中。

图1显示了从表中提取数据时应选择的内容。
![Fig. 1: Selectors for table selector][table-selector-selectors]

图2显示了复杂标头的示例。

![Fig. 2: Header for table selector][table-selector-complex-header]

图3显示了复杂行的示例。

![Fig. 3: Rows for table selector][table-selector-complex-rows]

图4显示了重命名和从最终数据中排除的列标题的示例。

![Fig. 4: Column headers renaming][table-selector-column-headers]

## Configuration options

- 选择器-表元素的[CSS selector][css-selector]。
- 标题行选择器-[CSS selector][css-selector]用于表标题行。
- 数据行选择器-[CSS selector][css-selector]用于表数据行。
- 这是垂直表-暗示此表是垂直的(具有垂直的标题和行)
- 提取缺少的列-在站点地图创建过程中未提取的新列将添加到提取的数据中
- 多个-正在提取多个记录。通常应该是
    检查表选择器,因为要提取多行。
- 延迟-延迟提取

## Use cases

请参阅[Text selector][text-selector]用例。

[table-selector-selectors]: ../images/selectors/table/selectors.png?raw=true
[text-selector]: Text%20selector.md
[css-selector]: ../CSS%20selector.md
[table-selector-complex-rows]: ../images/selectors/table/ComplexRows.png?raw=true
[table-selector-complex-header]: ../images/selectors/table/ComplexHeader.png?raw=true
[table-selector-column-headers]: ../images/selectors/table/ColumnsHeaders.png?raw=true