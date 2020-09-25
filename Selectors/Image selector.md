# Image selector

图像选择器可以提取图像的`src`属性(URL)。
您也可以选择存储图像。图像将存储在您的
下载目录:

`~/Downloads/<sitemap-id>/<selector-id>/<image filename.jpg>`

注意!为图像选择器选择CSS选择器时,
网站移到顶部。如果此功能以某种方式破坏了网站布局,请
将其报告为错误。

## Configuration options

- 选择器-图片元素的[CSS selector][css-selector]。
- 多个-正在提取多个记录。通常不应该
    检查图像选择器。
- 下载映像-下载映像并将其存储在本地驱动器上。当CouchDB
    使用存储后端,图像也存储在本地。
- 延迟-延迟提取

## Use cases

请参阅[Text selector][text-selector]用例。

[text-selector]: Text%20selector.md
[css-selector]: ../CSS%20selector.md