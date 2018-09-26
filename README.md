# get_data_from_taobao
**[refer from here](https://blog.csdn.net/BF02jgtRS00XKtCx/article/details/82836020)**<br/>
## 主要思路就是：<br/>
### 1.获取淘宝url规则<br/>
### 2.获取url下的编码<br/>
```
def get_html_text(url):
    try:
        res = requests.get(url,timeout=30)
        res.raise_for_status()
        res.encoding = res.apparent_encoding
        return res.text
    except:
        return ""
```
### 3.从编码中提取自己所需要的数据，比如价格，标题，产地，销量<br/>
### 4.将这些数据存入txt文件中<br/>
### 5.读取数据，清理数据<br/>
### 6.待续-
