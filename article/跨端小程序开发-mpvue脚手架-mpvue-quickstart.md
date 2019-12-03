# 跨端小程序开发-mpvue脚手架-mpvue-quickstart


## 项目说明 
mpvue是美团团队开源的一款小程序开发框架。

**项目地址**：[https://github.com/Meituan-Dianping/mpvue](https://github.com/Meituan-Dianping/mpvue)

特点：
- 完整的vue.js开发体验 （包括使用vuex状态管理）
- 支持多端小程序（微信，支付宝，百度，头条）
- 使用vue.js命令行工具vue-cli快速初始化项目(默认配置信息wx-appid)
- h5代码转换编译成小程序目标代码的能力
- 支持使用npm外部依赖

## 快速开始
使用vue-cli快速搭建脚手架

```js

cnpm i -g vue-cli  //全局安装vue cli
vue init mpvue/mpvue-quickstart mpvue-demo   //使用vue cli创建mpvue的脚手架
cd mpvue-demo  //进入项目目录
cnpm i   //安装依赖   
npm run dev //启动->打开微信小程序开发工具->导入项目/build/wx

```
 
 ## 基本命令
 
 ```js
npm run dev:wx     //测试启动，实时编译
npm run build:wx   //打包文件
npm run start:wx   //
```
简写
- wx 微信
- my 蚂蚁金服（支付宝小程序）
- swan 百度智能小程序
- tt 今日头条

 

### mpvue-quickstart架手架技术栈

- mpvue
- cssnano  //优化压缩css文件
- glob  //通配符匹配文件名，递归读取指定类型文件
- html-webpack-plugin  //webpack打包时，创建一个html文件，并把webpack打包后的插入到html文档中
- http-proxy-middleware  //nodejs请求代理中间件，解决开发中跨域、鉴权、图片防盗链等问题
- optimize-css-assets-webpack-plugin  //webpack的css压缩插件
- postcss-mpvue-wxss  //css转wxss库（清除微信小程序不支持的选择器/注释，rem转rpx,标签选择器到小程序的class选择器）
- px2rpx-loader  //把px转换成rpx单位，将宽度number按比例缩小
- mkdirp //递归创建，以包的形式包装mkdir -p命令
- webpack-hot-middleware  //webpack热更新中间件，相比webpack-dev-server更底层，可以编写后端服务使用


### mp-vue脚手架目录结构

```$xslt

│  index.html                        //html模板文件
│  package.json                      //npm配置文件，依赖包，启动命令
│  package.swan.json                 //百度小程序配置文件
│  project.config.json               //小程序配置文件
│  project.swan.json                 //百度小程序项目文件
│                                    
├─build                             //打包命令文件
│      build.js                      //打包编译命令
│      check-versions.js             //版本检查
│      dev-client.js                 //开发模式下，客户端事件监听，自动刷新
│      dev-server.js                 //dev启动命令
│      utils.js                      //打包命令使用的工具类
│      vue-loader.conf.js            //
│      webpack.base.conf.js          //webpack基础配置
│      webpack.dev.conf.js           //webpack开发环境配置
│      webpack.prod.conf.js          //webpack打包环境配置
│                                    
├─config                            //配置文件
│      dev.env.js                    //测试环境配置文件
│      index.js                      //外部配置文件
│      prod.env.js                   //生产环境配置文件
│                                    
└─src                               //项目目录
    │  app.json                      //app配置文件（路由，tabBar设置-位置/颜色/列表/背景，全局window属性-字体颜色/背景/文本）
    │  App.vue                       //主路由引入的vue入口文件，用来打印启动信息
    │  main.js                       //app.json中配置的一个主路由
    │                                
    ├─components                    //vue组件库
    │      card.vue                  //组件一
    │                                
    ├─pages                         //主要的页面
    │  ├─counter                   //计数器页面
    │  │      store.js              //vuex使用
    │  │                            
    │  ├─index                     //首页页面
    │  │      index.vue             //vue文件（包含template,script,style）
    │  │      main.js               //路由中配置的入口文件（每配置一个路由就实例化一次），实例化vue文件，配置异常处理
    │                                
    └─utils                         //工具类

```
