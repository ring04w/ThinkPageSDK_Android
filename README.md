AndroidSDK
==========
# 简介

心知天气Android SDK 为第三方应用提供了简单易用的心知天气API调用服务，使第三方应用可以快速整合心知天气API的所有功能。v2.0版SDK主要有三大特点：

* 完美兼容：全面支持心知天气API 2.0，支持实时天气，预报天气，空气质量，生活指数的查询。 

* 简单使用：只需在您的应用中添加几行代码就能访问心知天气API 2.0版的全部服务。对API调用结果的解包封装，让您能抛开对心知天气API细节的研究，从而更加专注优化你的应用。 

* 专业性能：异步调用模式保证了你的应用程序的无延迟响应。对并发请求的高性能处理让你的应用开发更省心、高效。

# 下载使用
下载解压zip包，点击进入src目录，SDK源文件都在这里面。把loopj和thinkpage两个目录中的所有原文件添加到你的工程目录下，就可以使用SDK的全部功能了。

# TPWeatherManager 类
应用通过以下构造函数初始化一个TPWeatherManager实例：
```java
public TPWeatherManager(String apiKey, TPWeatherManagerDelegate delegate)
```
# 发送天气服务请求
在创建好TPWeatherManager对象实例后，调用以下几个fetch API，向心知天气服务器发起一个天气请求:
获取和城市当前的天气信息
```java
public void fetchCurrentWeather(TPCity city, TPWeatherReportLanguage language, TPTemperatureUnit unit)
```
获取城市未来几天的天气预报
```java
public void fetchFutureWeather(TPCity city, TPWeatherReportLanguage language, TPTemperatureUnit unit)
```
获取城市的空气质量信息
```java
public void fetchAirQuality(TPCity city, TPWeatherReportLanguage language, TPTemperatureUnit unit, TPAirQualitySource aqi)
```
获取城市的天气相关咨询（穿衣，洗车等）
```java
public void fetchWeatherSuggestions(TPCity city, TPWeatherReportLanguage language, TPTemperatureUnit unit)
```
获取和城市天气相关的所有信息
```java
public void fetchAllWeather(TPCity city, TPWeatherReportLanguage language, TPTemperatureUnit unit, TPAirQualitySource aqi)
```
这五个API和心知天气API对应，大家可以对照查看http://www.thinkpage.cn/weather/api/ API参数解释：

TPCity 代表一个城市，你可以用new TPCity("城市名); 创建一个临时的城市对象

inLanguage 返回结果的语言： kEnglish：英语 kSimplifiedChinese：简体中文 kTraditionalChinese：繁体中文

unit 单位： kCelsiu：摄氏度 kFahrenheit：华氏度

aqi 空气质量的数据源： kAQINone：无 kAQICity：城市检测站 kAQIAll：城市所有监测站

# 更多信息
更多信息请访问心知天气网站： www.thinkpage.cn
