# 基于vue+MongoDB+爬虫的全栈后台项目-Girl

## 项目说明 
爬虫后台管理系统，可视化查看爬虫配置状态，代理IP配置，响应式设计支持手机端
数据来源于爬虫


**项目地址**：https://github.com/Xu-Angel/Girl  <br/>
**在线演示**：http://girl.xutianshi.top/admin/index.html#/dashboard

### 技术栈
- vue+vuex            //vue全家桶   
- express             //最流行的node web应用框架  
- MongoDB             //面向文档存储的数据库 
- mongoose            //在node环境下，对mongoDB便捷操作的对象模型工具 
- element-ui          //UI组件库 
- cookie-parser       //express中间件，解析cookies，用在服务端
- js-cookie           //客户端的cookies库
- crypto              //node加密模块，支持MD5,SHA
- formidable          //上传文件处理模块的插件
- mockjs              //mock数据 
- nprogress           //实现网页顶部进度条
- node                //后端语言                
  - path              //路径模块
  - fs                //文件处理模块



### 后台功能
- [x] 登陆
- [x] 数据查询
- [x] 路由权限管理
- [x] 图片上传

### 服务端功能
- [x] 代理IP爬取、使用、导出、导入
- [x] 定时爬去任务
- [x] 日志类

### 实现的API
- [x] 登录功能


### 启动
```javascript

```


### 目录结构

server文件夹：服务端模块
```$xslt                                    
                                             
│  index.html                                //浏览器访问入口文件
│  package.json                              //npm配置文件，依赖包，启动命令，项目说明
│                                            
├─build                                      //webpack构建文件
│      build.js                              //
│      check-versions.js                     //
│      utils.js                              //
│      vue-loader.conf.js                    //
│      webpack.base.conf.js                  //基本通用配置
│      webpack.dev.conf.js                   //测试环境构建配置
│      webpack.prod.conf.js                  //生产环境构建配置
│                                            //
├─config                                     //环境变量、baseURL配置
│      dev.env.js                            //测试
│      index.js                              //
│      prod.env.js                           //生产
│                                            
├─mock                                       //使用mock.js来模拟数据
│      index.js                              //入口文件，通过引入子文件来处理不同参数的返回状态
│                                            
├─src                                        //业务项目源码目录
│  │  App.vue                                //路由顶层包括文件
│  │  main.js                                //webpack打包入口文件，的顶层注入store,router配置
│  │  permission.js                          //
│  │                                         
│  ├─api                                     //
│  │      admin.js                           //
│  │                                         //
│  ├─assets                                  //
│  │                                         //
│  ├─components                              //
│  │  ├─Breadcrumb                           //
│  │  │      index.vue                       //
│  │                                         //
│  ├─icons                                   //
│  │  │  index.js                            //
│  │  │  svgo.yml                            //
│  │  │                                      //
│  │  └─svg                                  //
│  │                                         //
│  ├─router                                  //
│  │      index.js                           //
│  │                                         //
│  ├─store                                   //
│  │  │  getters.js                          //
│  │  │  index.js                            //
│  │  │                                      //
│  │  └─modules                              //
│  │          app.js                         //
│  │          tagsView.js                    //
│  │          user.js                        //
│  │                                         //
│  ├─styles                                  //
│  │                                         //
│  ├─utils                                   //
│  │      auth.js                            //
│  │      regulation.js                      //
│  │      request.js                         //基于axios封装的请求库
│  │      validate.js                        //
│  │                                         //
│  └─views                                   //
│      │  404.vue                            //
│      │                                     //
│      ├─center                              //
│      │      index.vue                      //
│      │                                     //
│      ├─dashboard                           //
│      │  │  index.vue                       //
│      │  │                                  //
│      │  └─components                       //
│      │          PanGroup.vue               //
│      │                                     //
│      ├─layout                              //
│      │  │  Layout.vue                      //
│      │  │                                  //
│      │  ├─components                       //
│      │  │  │  AppMain.vue                  //
│      │  │  │  index.js                     //
│      │  │  │  Navbar.vue
│      │  │  │  TagsView.vue
│      │  │  │
│      │  │  └─Sidebar
│      │  │          index.vue
│      │  │          Item.vue
│      │  │          Link.vue
│      │  │          SidebarItem.vue
│      │  │
│      │  └─mixin
│      │          ResizeHandler.js
│      │
│      ├─list
│      │  │  index.vue
│      │  │
│      │  ├─chart
│      │  │      index.vue
│      │  │
│      │  └─detail
│      │          dna.scss
│      │          index.vue
│      │
│      ├─log
│      │  ├─error
│      │  │      index.vue
│      │  │
│      │  ├─file
│      │  │      index.vue
│      │  │
│      │  └─visit
│      │          index.vue
│      │
│      ├─login
│      │      index.vue
│      │
│      ├─nested
│      │  ├─menu1
│      │  │  │  index.vue
│      │  │  │
│      │  │  ├─menu1-1
│      │  │  │      index.vue
│      │  │  │
│      │  │  ├─menu1-2
│      │  │  │  │  index.vue
│      │  │  │  │
│      │  │  │  ├─menu1-2-1
│      │  │  │  │      index.vue
│      │  │  │  │
│      │  │  │  └─menu1-2-2
│      │  │  │          index.vue
│      │  │  │
│      │  │  └─menu1-3
│      │  │          index.vue
│      │  │
│      │  └─menu2
│      │          index.vue
│      │
│      ├─permission
│      │  ├─admin
│      │  │      index.vue
│      │  │
│      │  └─role
│      │          index.vue
│      │
│      ├─spider
│      │  │  index.vue
│      │  │
│      │  ├─config
│      │  │      index.vue
│      │  │
│      │  └─ip
│      │          index.vue
│      │
│      └─tree
│              index.vue
│
└─static
        .gitkeep



```
