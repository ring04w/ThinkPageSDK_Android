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

# 更多信息
更多信息请访问心知天气网站： www.thinkpage.cn
