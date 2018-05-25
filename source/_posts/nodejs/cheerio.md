---
layout:     article
title:      "Cheerio Base On The CoffeeScript"
date:       2015-07-08
excerpt:    ""
tags:
    - JavaScript
---

爬虫
![image](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1527247415516&di=8b0aecad7363e94fa85027de5039cb14&imgtype=0&src=http%3A%2F%2Fff.topitme.com%2Ff%2Fb8%2Fae%2F111023110111caeb8fo.jpg)
<!-- more -->
###### cheerio安装
```
npm install cheerio
```
###### request-promise 安装
```
npm install request-promise
```

#### 初始化配置

```
cheerio = require('cheerio');
request = require('request-promise')

uri = 'http://www.baidu.com'
options =
  uri:uri,
  transform:(body)->
    return cheerio.load(body)

```

#### 使用

```
request(options).then(
  ($)->
    console.log($.html())
).catch(
  (err)->
    console.log("error==>"+err.message)
)

```
