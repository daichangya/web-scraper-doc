# Development Instructions

## Selector Development

本节演示了为卷筒纸刮板创建或扩展选择器所需的所有步骤。在此示例中,我们将创建“全选”选择器。

### 创建选择器逻辑
如果您打算扩展具有功能的其他选择器,则可以跳过文件创建步骤。

-在`scripts/Selector/`中复制文件`SelectorElementStyle.js`
-将重复的文件重命名为`SelectorAll.js`
-修改`getData`方法以返回所有内容
-指定您希望在`getFeatures`功能中启用的功能
-实现已启用功能的逻辑(功能`textmanipulation`可以直接使用)

### 创建选择器控件

-将一个部分添加到`devtools/views/`中的`SelectorEdit.html`文件中
-添加节类`form-group feature feature-AllSelector`
-您可以使用`{{#selectorName}}`和`{{/selectorName}}`防止显示内容(用于checkobx控件)
-使用`{{selector.selectorAll}}`定义变量


### 设置对选择器的引用

#### 控制器

-在`scripts/`中打开`Controler.js`
-在函数`getCurrentlyEditedSelector`中添加变量以选择您的HTML部分值
-将变量添加到`newSelector`对象(在`scripts/Selector/`中引用此功能的每个选择器都可以访问该值)
-将验证规则添加到函数`initSelectorValidation`中的变量中


#### 文件参考

-在`content_scripts`和`scripts`部分的`extension/manifest.json`中添加引用
-添加对`extension\devtools\devtools_scraper_panel.html`的引用
-向`playgrounds\extension\index.html`添加参考
-添加对`tests\SpecRunner.html`的引用


### 测试

为了进行测试,您需要运行Web服务器。我个人使用[Chrome浏览器的Web服务器](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb)并引用该项目的工作目录。

-在`tests/Selector`中复制测试文件并重命名
-为选择器编写测试
-通过打开`tests/SpecRunner.html`运行测试
-通过打开`playgrounds/extension/index.html`尝试实现
-如果无法满足您的情况,请扩展操场

### 文档

-在`docs/selectors`中创建`md`文件
-描述用法,选项等