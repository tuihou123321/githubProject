# mpvue开发的顺风车微信小程序-service-mpvue-mini


## 项目说明 
基于mpvue开发的顺风车平台，目前做适配了微信小程序；
没有做信息判断，可以通过打包后来转换；


**项目地址**：[https://github.com/chengzhx76/service-mpvue-mini](https://github.com/chengzhx76/service-mpvue-mini)



### 技术栈
- mpvue   //vue语法的跨平台小程序开发框架
- vuex   //数据状态管理
- loadsh //模块化的js工具库
- font-awesome   //字体图标库
- flyio   //支持多平台(node.js、小程序、RN、web)的http请求库
- vuex-persistedstate   //结合本地存储做状态管理



### 启动
```javascript
cnpm i  //依赖安装
cnpm run dev //启动开发模式   //默认微信
npm run build  //打包，默认微信
```

主要调用的微信api

wx
- login  //登陆
- request //接口请求
- showToast   //信息弹层
- getStorageSync/setStorageSync/clearStorage  //本地数据存/取/清除
- getLocation //定位


### 主要实现的功能
-[x] 登录功能
-[x] 轮播功能
-[x] 地图上查看行程，调用的腾讯地图api
-[x] 地点模糊搜索
-[x] 时间选择插件
-[x] 自定义滚动栏
-[x] 分享图片生成,调用系统保存图片功能
-[x] 分享功能
-[x] 顺风车搜索
-[x] 顺风车信息添加
-[x] 个人中心


### 目录结构

```$xslt

│  index.html                        //模板文件
│  package.json                      //npm配置文件
│  project.config.json               //项目配置信息
│                                    
├─build                             //mpvue相关打包命令
│                                    
├─config                            //mpvue环境变量配置信息
│                                    
├─src                               //工程文件
│  │  app.json                      //路由，页面全局属性设置
│  │  App.vue                       //vue模板文件
│  │  main.js                       //vue顶层文件注入全局vuex数据
│  │                                
│  ├─api                           //接口封装
│  │      admin.js                  //管理员权限相关接口
│  │      api.js                    //通用接口
│  │      config.js                 //配置接口
│  │                                
│  ├─components                    //组件
│  │                                
│  ├─iconfont                      //字体库
│  │                                
│  ├─img                           //图片资源
│  │                                
│  ├─libs                          //库
│  │      qqmap-wx-jssdk.js         //腾讯地图sdk
│  │                                
│  ├─pages                         //页面
│  │  │                            
│  │  ├─index                     //首页
│  │  │      index.vue             //vue页面（模板/js/样式）
│  │  │      main.js               //页面入口文件
│  │  │      main.json             //首页body信息配置（title标题/开启下拉刷新）
│  │                                
│  ├─store                         //vuex相关文件
│  │                                
│  ├─styles                        //样式文件
│  │      index.scss                //全局样式文件
│  │      mixin.scss                //样式
│  │      variables.scss            //变量
│  │                                
│  └─utils                         //工具类
│          config.js                 //配置文件
│          index.js                  //共用方法
│          request.js                //基于flyio的请求库封装
│          validate.js               //正则验证库
│
└─static                            //静态文件

```
