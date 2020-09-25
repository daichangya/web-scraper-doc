# Installation

## Requirements

该扩展程序至少支持Chrome和Mozilla Firefox等不同的浏览器。Opera也可以用于浏览器。

# Install Chrome

要安装该程序,您必须执行以下操作:

1. 使用从[release page][latest-release]下载的插件“ web-scraper-chrome-extension-v <版本号> .zip”解压缩文件。
2. 转到Google Chrome浏览器中的扩展程序页面-[chrome://extensions/](chrome://extensions/)。
3. 使用右上角的开关启用开发人员模式(如果未启用)。(您可以在这里https://developer.chrome.com/extensions/getstarted#unpacked阅读更多信息)。
4. 您可以通过以下方式向浏览器添加扩展:
    1. 使用拖放系统,将从解压缩的文件中获得的文件夹`web-scraper-chrome-extension-v<version number>`移动到扩展名页面;
    2. 从从解压缩的文件获得的文件夹`web-scraper-chrome-extension-v<version number>`中下载解压缩的扩展名。作为执行操作的结果,新的Web Scraper扩展名应出现在Google Chrome浏览器扩展名列表中:
5. 为使扩展名正常工作,请在安装后重新启动chrome,以使扩展名正常工作。
   ![Fig. Installing the program in Google Chrome][install-chrome]

# Install Mozilla Firefox

要安装该程序,您必须执行以下操作:

1. 转到Mozilla Firefox浏览器设置页面。关于:配置。
2. 在搜索栏中,输入xpinstall.signatures.required设置,然后按Enter。
3. 将此设置的值设置为false(在设置行上双击)。
   ![Fig. Modifying Mozilla Firefox][change-config]
4. 转到Mozilla Firefox浏览器的加载项页面(扩展名)。关于:插件
5. 单击相应的图标打开设置菜单。
6. 在下拉列表中选择菜单项“从文件安装插件”。
   ![Fig. Install Add-on][install-addon]
7. 在带有程序分发包的磁盘上,选择带有插件“ web-scraper-chrome-extension-v <版本号> . zip”的文件。
8. 单击文件选择确认按钮。
   ![Fig. Selecting a program distribution file][choose-addon-file]
9. 在弹出窗口中确认扩展的安装。

    ![Fig. Confirm install extension][confirm-install]

[install-chrome]: images/installation/chrome_scraper_1.png
[change-config]: images/installation/Firefox_scraper_1.png
[install-addon]: images/installation/Firefox_scraper_2.png
[choose-addon-file]: images/installation/Firefox_scraper_3.png
[confirm-install]: images/installation/Firefox_scraper_4.png
[latest-release]: https://github.com/ispras/web-scraper-chrome-extension/releases