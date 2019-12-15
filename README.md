dart_server
========
this start a http server for flutter web, it can also proxy api requests for Cross-Origin Request.

Feature
--------
1. Start a http server at local static directory.
2. Proxy api requests for Cross-Origin Request.

Run
--------
> need install dart sdk,can execute dart command
```java
# install dependence
flutter pub get
# start
dart lib/server.dart
```
Config
--------
- Config port,  for example:
```java
var server = await http.startServer('127.0.0.1', 3000);
```
- Config api proxy,  for example:
```java
var pubProxy = Proxy(
    'https://pub.dev',
    publicPath: '',
    timeout: timeout,
  );
```
- Config local static directory ,  for example:
```java
var fs = const LocalFileSystem();
  var vDir = CachingVirtualDirectory(
    app,
    fs,
    allowDirectoryListing: true,
    source: fs.currentDirectory.parent.childDirectory("build").childDirectory("web"),
    maxAge: const Duration(days: 24).inSeconds,
  );
```


中文：
---------

dart_server
========
为flutter web启动一个http服务器，并且可以代理api请求，解决跨域请求问题。

功能
--------
1. 为本地文件夹启动一个http服务，例如为flutter web的产物启动http服务
2. 通过接口代理 解决flutter web调用接口时跨域问题

执行
--------
> 需要安装dart sdk，可以运行dart命令
```java
# 安装依赖
flutter pub get
# 启动服务
dart lib/server.dart
```
配置
--------
- 配置端口号,  例如:
```java
var server = await http.startServer('127.0.0.1', 3000);
```
- 配置接口代理,  例如:
```java
var pubProxy = Proxy(
    'https://pub.dev',
    publicPath: '',
    timeout: timeout,
  );
```
- 配置本地文件夹地址 ,  例如:
```java
var fs = const LocalFileSystem();
  var vDir = CachingVirtualDirectory(
    app,
    fs,
    allowDirectoryListing: true,
    source: fs.currentDirectory.parent.childDirectory("build").childDirectory("web"),
    maxAge: const Duration(days: 24).inSeconds,
  );
```

# Contact me:

- Blog:http://blog.csdn.net/masonblog
- Email:MasonLiuChn@gmail.com

License
=======

    Copyright 2019 MasonLiu, Inc.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
