# WBAFNetworkingLogger

`WBAFNetworkingLogger` 是 [AFNetworking](http://github.com/AFNetworking/AFNetworking/) 3.x 的扩展,原库中已经将原来2.x中的`AFNetworkActivityLogger`移除.

为方便使用,自己根据2.x中`AFNetworkActivityLogger`的内容,修改为AFNetworking3.x 可用的辅助类.

`WBAFNetworkingLogger `会监听

* `AFNetworkingTaskDidResumeNotification`
* `AFNetworkingTaskDidCompleteNotification`

然后打印出请求和响应的关键信息.

## 使用方法

和AFNetworking2.x中的使用方法一样:

直接在程序启动以后调用:

``` objective-c
[[WBAFNetworkingLogger sharedLogger] startLogging];
```

默认情况下使用的是Info模式,可以通过下面方法设置具体模式,一般使用Debug模式较多:

``` objective-c
[[WBAFNetworkingLogger sharedLogger] setLevel:WBLoggerLevelDebug];
```

## License

MIT license.
