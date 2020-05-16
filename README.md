
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