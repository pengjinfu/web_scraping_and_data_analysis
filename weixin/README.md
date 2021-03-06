# 微信
## 网络爬虫
### 获取公众号的所有文章
`scraping.py`
- 使用说明
    - 1、替换代码开始部分的微信公众平台的用户名、密码和要爬的公众号名称。
    - 2、get_articles_list()用于获取公众号文章清单。
    - 3、get_articles()根据get_articles_list生成的csv逐个访问文章固定链接，并导出把保存为一份pdf和一份仅文本的txt。
    - 4、运行`python3 scraping.py`即可，爬取过程会通过`weixin.log`文件记录。

`analysis.py`
- 使用说明
    - 1、需先完成信息抓取，有`articles.csv`文件。
    - 2、运行`python3 analysis.py`即可。

- 坑与建议
    - 1、由于腾讯的反爬做的相当好，建议酌情增加sleep延迟，如果被禁，需要等待较长时间，或更换公众平台账号。
    - 2、由于增加的sleep延迟较长，整个爬取过程耗时比较长。
    - 3、保存pdf耗时也长，可采用debug方式，随时暂停。
