# CSS selector

Web Scraper使用CSS选择器在网页中查找HTML元素并提取
来自他们的数据。当选择一个元素时,Web Scraper会尝试使其
最好猜测一下所选元素的CSS选择器。但是你
也可以自己编写并通过单击“元素预览”进行测试。您
可以使用CSS版本1-3中可用的CSS选择器,也可以使用伪
jQuery中另外可用的选择器。这里有一些
文档链接可能会帮助您:
 
 * [CSS Selectors][css-selectors-wikipedia]
 * [jQuery CSS selectors][css-selectors-jquery]
 * [w3schools CSS selector reference][w3schools-css-selector-reference]

## Additional Web Scraper selectors
可以向Web Scraper添加新的伪CSS选择器。现在在那里
仅添加了一个CSS选择器。

#### 父选择器

CSS选择器`_parent_`允许使用
*元素选择器*,用于选择*元素选择器*返回的元素。对于
例如,当您需要提取一个
* Element选择器*返回的元素的属性。

 [css-selectors-wikipedia]: http://en.wikipedia.org/wiki/Cascading_Style_Sheets#Selector
 [css-selectors-jquery]: http://api.jquery.com/category/selectors/
 [w3schools-css-selector-reference]: http://www.w3schools.com/cssref/css_selectors.asp