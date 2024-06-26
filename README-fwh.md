# 运行程序：
## 分支说明:
1. release: 服务器终端运行
2. master: 本地终端运行
3. dev: 本地开发程序运行 (由于引用依赖方式不同导致)

## 开发工具运行：
1. 打开spider.py文件。执行main
2. 优先配置config.json文件。设置Cookie，采集的用户
3. 
## 终端运行：


# 运行逻辑：
1. 先安装开发者存储json数据
2. 自己遍历json数据存储到Notionzhogn

## 自定义逻辑功能
1. 先获取数据，然后写入Notion中
2. 多个用户ID的时候, 查询完一个用户ID后就触发保存Notion数据

### Notion-util写入逻辑
1. 获取网络数据源
2. 本地存储一份json数据源
3. 对比数据源中的id数据(唯一值),确认是否有新的数据,再存储Notion中

## 常用运行命令：

- 首次终端运行,需要pip安装
```bash
$ python3 -m pip install weibo-spider
```

- 优先配置config.json文件

- 默认选择config.json文件 输出指定文件夹
```bash
cd /Users/fwh/A_FWH/GitHub/weiboSpider
#$ python3 -m weibo_spider --output_dir="/Users/fwh/Downloads/"
$ python3 -m weibo_spider --output_dir="/Users/fwh/fuwenhao/Github/weiboSpider/Weibo_data/"
"
```

- 定时任务执行脚本
```bash
crontab -e

# 每10分钟执行一次
#*/10 * * * * /Users/fwh/fuwenhao/Github/spider/T-Test/test.sh
*/10 * * * * /home/fwh/github/weiboSpider/fwh_start.sh
```
- 定时脚本查看:
```bash

当你使用crontab -e命令编辑cron任务并保存后，并不会直接生成一个文件。实际上，cron任务是保存在用户的cron表中，而不是保存在文件中。

crontab -e命令会打开一个文本编辑器，让你编辑当前用户的cron任务。当你保存并退出编辑器时，cron任务会被写入到用户的cron表中。

你可以使用crontab -l命令来查看当前用户的cron任务，它会将cron任务的内容输出到终端。

如果你想将cron任务保存到文件中，你可以使用crontab -l > filename命令将cron任务输出重定向到一个文件中。这样，你就可以将cron任务保存为一个文件。

```
## 用户对照列表：
- 链接: https://m.weibo.cn/u/1499104401
- 1499104401  新浪军事
- 2705169595    正能量量
- 5648162302    黄建同学
- 1727858283  宝玉




   "user_id_list": ["1865990891","2056277053","1253846303","1627825392","1658384301","1497035431","1400854834","1727858283","5648162302","2177169610"],

## 帮助文档
- 设置配置文件
    - https://github.com/dataabc/weiboSpider/blob/master/docs/settings.md
- 获取cookie信息
    - https://github.com/dataabc/weiboSpider/blob/master/docs/cookie.md
