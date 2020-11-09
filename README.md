# Mini-spider

1. 功能描述：多线程网络爬虫，爬取网页图片地址。使用python开发一个迷你定向抓取器mini_spider.py，实现对种子链接的广度优先抓取，并把URL长相符合特定pattern的网页保存到磁盘上。

2. 程序运行: 
python mini_spider.py -c spider.conf 

3. 配置文件spider.conf: 
[spider] 
feedfile: ./urls          # 种子文件路径 
result: ./result.data     # 抓取结果存储文件, 一行一个
max_depth: 6              # 最大抓取深度(种子为0级) 
crawl_interval: 1         # 抓取间隔. 单位: 秒 
crawl_timeout: 2          # 抓取超时. 单位: 秒 
thread_count: 8           # 抓取线程数 

4. 种子文件urls:
http://xxx.xxx.com

5. 抓取策略
- 广度优先的网页抓取策略
- 多线程抓取要求
- 获取图片文件地址并存储到文件(gif|png|jpg|bmp为扩展格式的 url, 绝对路径存储到result.data文件中, 一行一个)  
