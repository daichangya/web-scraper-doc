## 微信公众号

扫码关注微信公众号,分布式编程。
![分布式编程](http://www.images.mdan.top/qrcode_for_gh_1e2587cc42b1_258_1587996055777.jpg)

[https://zthinker.com/](https://zthinker.com/)

中文文档网址:https://daichangya.github.io/web-scraper-doc/#/

# Web Scraper

Web Scraper是chrome浏览器扩展程序,用于从Web提取数据
页面。使用此扩展程序,您可以创建网站的计划(站点地图)
应该遍历并提取什么。使用这些站点地图
Web Scraper将相应地导航该站点并提取所有数据。Scraped
以后可以将数据导出为CSV或JSON行。

#### 最新版本

在[安装页面](./Installation.md)上了解有关安装过程的信息。

## 更新日志

### v0.3.6

- 更新了对表的支持(更新了垂直表支持并添加了复杂的标题和数据行)
- 添加了从文件导出和导入站点地图
- 添加了俄语翻译和对i18n的支持,从而可以添加每种语言的翻译
- 添加了用于站点地图的Rest Api CRUD存储
- 移至webpack捆绑器
- 添加了来自预定义模型的ID提示
- 添加了常量和文档选择器
- 重构预览数据并在抓取数据中添加搜索
- 将返回的项目模型重构为JSON
- 添加了保存JSON行的功能

### v0.3

- 启用了多个起始URL的粘贴(通过[@jwillmer](https://github.com/jwillmer))
- 添加了对动态表列的抓取(通过[@jwillmer](https://github.com/jwillmer))
- 添加了样式提取类型(通过[@jwillmer](https://github.com/jwillmer))
- 添加了文本操作(修剪,替换,前缀,后缀,删除HTML)(通过[@jwillmer](https://github.com/jwillmer))
- 添加了图像改进功能,可在div背景中查找图像(通过[@jwillmer](https://github.com/jwillmer))
- 添加了对垂直表的支持(通过[@jwillmer](https://github.com/jwillmer))
- 在请求之间添加了随机延迟功能(通过[@Euphorbium](https://github.com/Euphorbium))
- 起始URL现在也可以是本地URL(通过[@ 3flex](https://github.com/3flex))
- 添加了CSV导出选项(通过[@mohamnag](https://github.com/mohamnag))
- 添加了供选择的Regex组(通过[@RuneHL](https://github.com/RuneHL))
- 设置的JSON导出/导入(通过[@haisi](https://github.com/haisi))
- 在网址中添加了日期和数字模式(通过[@codoff](https://github.com/codoff))
- 添加了分页选择器限制(通过[@codoff](https://github.com/codoff))
- 改进了CSV导出(通过[@haisi](https://github.com/haisi))
- 添加了点击限制选项(由[@ panna-ahmed](https://github.com/panna-ahmed))

### v0.2

- 添加了元素点击选择器
- 添加了元素向下滚动选择器
- 添加了链接弹出选择器
- 改进的表格选择器可与任何html标记一起使用
- 添加了图像下载
- 选择元素时添加了键盘快捷键
- 在使用选择器之前增加了可配置的延迟
- 增加了页面访问之间的可配置延迟
- 添加了多个起始网址配置
- 添加了表单字段验证
- 修正了很多错误

### v0.1.3

- 添加了表格选择器
- 添加了HTML选择器
- 添加了HTML属性选择器
- 添加了数据预览
- 添加了远程起始网址
- 修复了使选择器树无法在某些操作系统上显示的错误

#### 错误

提交错误时,请尽可能附上导出的站点地图。

#### 开发

在开始之前,请阅读[开发说明](/Development.md)。

## 执照

LGPLv3

[chrome-store]: https://chrome.google.com/webstore/detail/web-scraper/jnhgnonknehpejjnehehllkliplmbmhn
[webscraper.io]: http://webscraper.io/
[google-groups]: https://groups.google.com/forum/#!forum/web-scraper
[github-issues]: https://github.com/martinsbalodis/web-scraper-chrome-extension/issues
[get-started-chrome]: https://developer.chrome.com/extensions/getstarted#unpacked
[latest-releases]: https://github.com/ispras/web-scraper-chrome-extension/releases