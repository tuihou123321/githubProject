# 网易云音乐nodejsApi服务-NeteaseCloudMusicApi

## 项目说明 
使用node.js开发的 网易云音乐 api服务；
目前开发的接口多达100+，文档完善；
核心技术：跨站请求伪造CSRF,伪造请求头，调用官方API

**项目地址**：[https://github.com/Binaryify/NeteaseCloudMusicApi](https://github.com/Binaryify/NeteaseCloudMusicApi)

**api文档地址**：[api文档](https://binaryify.github.io/NeteaseCloudMusicApi/#/?id=neteasecloudmusicapi)


## 技术栈
- express    //node web应用程序框架
- apicache   //express中间件，缓存用
- pac-proxy-agent //接口请求代理
- querystring  //处理http请求参数，string与object互转
- node //使用的node子模块
  - fs  //文件模块
  - path //路径
  - child_process //子程序模块



## 启动
```javascript
npm i
npm start
```
歌曲搜索：http://127.0.0.1:3000/search?keywords=%E6%B5%B7%E9%98%94%E5%A4%A9%E7%A9%BA

## 主要完成的接口
-[x] 登陆相关
-[x] 电台相关
-[x] 通知类
-[x] 设置类
-[x] 用户信息相关/操作类
-[x] 歌曲类
-[x] 评论类
-[x] 推荐类
-[x] FM
-[x] 歌手相关
-[x] more...

其他问题：
issues修复：https://github.com/Binaryify/NeteaseCloudMusicApi/issues/462

