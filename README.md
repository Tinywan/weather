
<h1 align="center">Weather</h1>

<p align="center">:rainbow: 基于高德开放平台的 PHP 天气信息组件。</p>

[![Build Status](https://travis-ci.org/Tinywan/weather.svg?branch=master)](https://travis-ci.org/tinywan/weather)

## 安装

```sh
$ composer require tinywan/weather -vvv
```

## 配置

在使用本扩展之前，你需要去 [高德开放平台](https://lbs.amap.com/dev/id/newuser) 注册账号，然后创建应用，获取应用的 API Key。

## 使用

```php
use Tinywan\Weather\Weather;

$key = 'xxxxxxxxxxxxxxxxxxxxxxxxxxx';

$weather = new Weather($key);
```
###  获取实时天气

```php
$response = $weather->getLiveWeather('深圳');
```
示例：

```json
{
    "status": "1",
    "count": "1",
    "info": "OK",
    "infocode": "10000",
    "lives": [
        {
            "province": "广东",
            "city": "深圳市",
            "adcode": "440300",
            "weather": "中雨",
            "temperature": "27",
            "winddirection": "西南",
            "windpower": "5",
            "humidity": "94",
            "reporttime": "2018-08-21 16:00:00"
        }
    ]
}
```

### 获取近期天气预报

```
$response = $weather->getForecastsWeather('深圳');
```
示例：

```json
{
    "status": "1", 
    "count": "1", 
    "info": "OK", 
    "infocode": "10000", 
    "forecasts": [
        {
            "city": "深圳市", 
            "adcode": "440300", 
            "province": "广东", 
            "reporttime": "2018-08-21 11:00:00", 
            "casts": [
                {
                    "date": "2018-08-21", 
                    "week": "2", 
                    "dayweather": "雷阵雨", 
                    "nightweather": "雷阵雨", 
                    "daytemp": "31", 
                    "nighttemp": "26", 
                    "daywind": "无风向", 
                    "nightwind": "无风向", 
                    "daypower": "≤3", 
                    "nightpower": "≤3"
                }, 
                {
                    "date": "2018-08-22", 
                    "week": "3", 
                    "dayweather": "雷阵雨", 
                    "nightweather": "雷阵雨", 
                    "daytemp": "32", 
                    "nighttemp": "27", 
                    "daywind": "无风向", 
                    "nightwind": "无风向", 
                    "daypower": "≤3", 
                    "nightpower": "≤3"
                }, 
                {
                    "date": "2018-08-23", 
                    "week": "4", 
                    "dayweather": "雷阵雨", 
                    "nightweather": "雷阵雨", 
                    "daytemp": "32", 
                    "nighttemp": "26", 
                    "daywind": "无风向", 
                    "nightwind": "无风向", 
                    "daypower": "≤3", 
                    "nightpower": "≤3"
                }, 
                {
                    "date": "2018-08-24", 
                    "week": "5", 
                    "dayweather": "雷阵雨", 
                    "nightweather": "雷阵雨", 
                    "daytemp": "31", 
                    "nighttemp": "26", 
                    "daywind": "无风向", 
                    "nightwind": "无风向", 
                    "daypower": "≤3", 
                    "nightpower": "≤3"
                }
            ]
        }
    ]
}
```