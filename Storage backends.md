# Storage backends

可以将Web scraper配置为使用本地存储或CouchDB。通过
默认情况下,所有数据都存储在本地存储中。

## Local storage

本地存储后端使用内置于数据库的浏览器来存储数据。这个数据
不会从一个chrome实例复制到另一个。

## CouchDB

[CouchDB][couchdb]是RESTful NoSQL JavaScript数据库。您可以配置
该数据库中存储站点地图和抓取数据的扩展名。数据
然后可以从您所有的chrome实例中访问。要做到这一点
您需要在选项页面中对其进行配置。您可以通过右键单击将其打开
扩展程序图标和选择选项。在那里您可以在存储之间切换
后端。对于CouchDB,您需要在站点地图上添加配置数据库
将被存储,并且将存储抓取数据的couchdb数据库服务器。
例如,您可以这样配置它:

-网站地图数据库-http://localhost:5984/scraper-sitemaps
-数据数据库-http://localhost:5984/

[couchdb]: http://couchdb.apache.org/

## Rest Api

如果要在自己的rest api和自己的数据库中实现站点地图存储,则使用此存储。
只需在您的API中实现以下方法即可:

- `GET/sitemaps/`-返回存储站点地图JSON中可用列表。
- `POST/sitemaps/`(主体中包含Sitemap JSON)-在存储中创建新的Sitemap。
- `PUT/sitemaps/:sitemap_id`(主体中包含Sitemap JSON)-更新存储中的现有站点地图。
- `DELETE/sitemaps/:sitemap_id`-从存储中删除站点地图。