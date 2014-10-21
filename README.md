# Tinysou Android Library

想在项目中学习，查看 [demo](https://github.com/tinysou/tinysou-android-demo)

## 介绍

微搜索 Android 库，通过调用 public 接口，实现发送搜索请求、接收处理搜索响应等功能。目前支持的接口有：

* 搜索 API
* 自动补全 API

## 如何使用

* 导入 tinysou-android-library-v1.00.jar 到 Android project 的 libs 目录中
* 在 Android Studio 中，鼠标右击 jar 文件，选择 Add As Library

## 如何在应用中进行搜索

* 搜索 API

  填写微搜索的 engine_key

```java
    String engine_key = "YOUR_ENGINE_KEY";
```

  发送搜索请求，获得搜索结果

```java
    // 初始化客户端
    TinySouClient client = new TinySouClient(engine_key);
    // 设置搜索结果来自于第几页
    client.setPage(searchPage);
    // 获得 String 格式的搜索结果
    String result = client.Search(search_content);
```

* 自动补全 API

  填写微搜索的 engine_key （同上）

  发送自动补全请求，获得自动补全结果

```java
    // 初始化客户端
    TinySouClient client = new TinySouClient(engine_key);
    // 获得 String 格式的自动补全结果
    String result = client.AutoSearch(search_content);
```

其他参数的获取方法请参考API文档。
