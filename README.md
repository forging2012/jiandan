# 煎蛋分布式文章爬虫

多浏览器持久化cookie分布式爬虫爬取数据，使用到redis，mysql，将网页数据保存在磁盘中，详情页解析后存入数据库。

爬虫工程师进阶必备!高级示例！依赖核心库：[土拔鼠Golang爬虫包](https://github.com/hunterhug/GoSpider)

环境安装请查看：[个人博客](http://www.lenggirl.com/tool/gospider-env.html)或者

Look at: [https://github.com/hunterhug/GoSpider-docker](https://github.com/hunterhug/GoSpider-docker)

结果，总共抓取了58,097 篇文章

获取代码：

```
go get -u -v github.com/hunterhug/jiandan
```

1.cont.go编辑配置，`RootDir = "E:\\jiandan"`为数据目录,然后改数据库配置，redis密码请留空

```
	RootDir = "E:\\jiandan"

	// Redis配置
	RedisConfig = myredis.RedisConfig{
		DB:       0,
		Host:     "127.0.0.1:6379",
		Password: "smart2016",
	}

	// mysql config
	mysqlconfig = mysql.MysqlConfig{
		Username: "root",
		Password: "smart2016",
		Ip:       "127.0.0.1",
		Port:     "3306",
		Dbname:   "jiandan",
	}
```

2.进main文件夹运行`go run main.go`

3.数据保存在data文件夹和数据库中

4.重抓要删除Redis数据库和文件夹

5.如果只是接力，即是增量抓取，那么不需要删redis并且文件夹data/detail可不删，其他文件要删。

详细说明见[http://www.lenggirl.com/spider/jiandan.html](http://www.lenggirl.com/spider/jiandan.html)

![](/doc/jiandan/xx.png)
![](/doc/jiandan/redis.png)
![](/doc/jiandan/file.png)
![](/doc/jiandan/mysql.png)

如果你觉得项目帮助到你,欢迎请我喝杯咖啡

微信
![微信](https://raw.githubusercontent.com/hunterhug/hunterhug.github.io/master/static/jpg/wei.png)

支付宝
![支付宝](https://raw.githubusercontent.com/hunterhug/hunterhug.github.io/master/static/jpg/ali.png)
