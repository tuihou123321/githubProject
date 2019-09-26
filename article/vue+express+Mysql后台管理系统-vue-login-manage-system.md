# vue+express+Mysql后台管理系统-vue-login-manage-system

## 项目说明 
基于vue+express+mysql的全栈后台管理系统


**项目地址**：https://github.com/sakila1012/vue-login-manage-system

### 页面功能
- [x] 登陆


### 实现的API
- [x] 登录功能


### 技术栈
- vue
- express
- Mysql
- element ui

### 启动
```javascript
npm i 
npm run dev
```
访问： http://localhost:3001


### 目录结构
```$xslt
│  index.html
│  package.json
│  README.md
│
├─build
│      build.js
│      check-versions.js
│      dev-client.js
│      dev-server.js
│      utils.js
│      vendor-manifest.json
│      vue-loader.conf.js
│      webpack.base.conf.js
│      webpack.dev.conf.js
│      webpack.dll.conf.js
│      webpack.prod.conf.js
│
├─config
│      dev.env.js
│      index.js
│      prod.env.js
│
├─dist
│  └─static
│      │  data.json
│      │  datasource.json
│      │  vuetable.json
│      │
│      ├─css
│      │  │  color-dark.css
│      │  │  datasource.css
│      │  │  main.css
│      │  │
│      │  └─theme-green
│      │      │  color-green.css
│      │      │  index.css
│      │      │
│      │      └─fonts
│      │              element-icons.ttf
│      │              element-icons.woff
│      │
│      ├─img
│      │      img.jpg
│      │
│      └─js
│              vendor.dll.js
│
│
├─service                                          //服务端代码
│  │  app.js                                       //入口文件，node服务端口配置
│  │
│  ├─api                                           //服务端路由
│  │      userApi.js                               //用户模块
│  │
│  └─db                                            //数据库相关
│          db.js                                   //数据库配置信息
│          sqlMap.js                               //Mysql查询语句
│
├─src                                              //
│  │  App.vue                                      //
│  │  main.js                                      //
│  │                                               
│  ├─components                                    //组件
│  │  ├─common                                     //通用组件
│  │  │      Home.vue                              //首页组件
│  │  │                                            
│  │  └─page                                       //网页
│  │          Login.vue                            //页面
│  │                                               
│  ├─router                                        //路由配置文件夹
│  │      index.js                                 //路由
│  │                                               
│  └─utils                                         //工具类
│          utils.js                                //工具类方法，常用的正则表达示
│
└─static                                           //静态资源文件夹

```
