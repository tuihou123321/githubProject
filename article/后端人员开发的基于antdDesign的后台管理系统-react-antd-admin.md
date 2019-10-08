# 后端人员开发的基于antdDesign的后台管理系统-react-antd-admin.md

## 项目说明 
以后端的视角来做前端的后台管理项目，核心项目思路是用写配置的方式替代写代码，
符合数据驱动的原则，数据与逻辑分离。接口文档，版本更新记录文档比较详细；
代码注释中写了比较多关于作者的学习心得；


**项目地址**: (github.com/jiangxy/react-antd-admin)[https://www.github.com/jiangxy/react-antd-admin]

### 技术栈
- react+react-router+redux  //react全家桶
- ant design  //ui框架
- superagent  //基于promise的轻量级ajax api，适用于client/node


### 技术点
- [x] 使用webpack.optimize.CommonsChunkPlugin来提取公用模块 verdor.min.js，放入cdn可加速  
- [x] 使用react的getComponent 动态//react-router3.x老版本的方案
- [x] 自定义了logger.js 来设置不同环境下的日志输出级别,debug,info,warn,error


### 启动
```javascript
npm i 
npm run dev
```

启动：localhost:8080  <br/>
账号：guest  <br>
密码: guest


### 目录结构
```$xslt

│  CHANGELOG.md                         //项目更新记录
│  index.html.template                  //渲染模板，支持ejs语法，通过html-webpack-plugin插件引入
│  package.json                         //依赖安装
│  README.md                            //文档说明
│  webpack.config.js                    //通用webpack配置
│  webpack.config.prod.js               //webpack生产配置文件
│                                                  
├─docs                                  //文档、接口文档，界面截图
│                                                  
└─src                                   //工程文件
    │  config.js                        //代码可配置化：log level,api，upload相关设置，项目名，图标，侧边栏配置
    │  index.js                         //react出口文件：路由配置，redux
    │  menu.js                          //左侧菜单枚举
    │                                   
    ├─components                        //组件库
    │  ├─App                            //
    │  │      index.js                  //
    │  │      index.less                //
    │                                   
    ├─redux                             //store设计
    │      Login.js                     //
    │      Sidebar.js                   //
    │      store.js                     //
    │                                   
    ├─schema                            //
    │      test.config.js               //
    │      test.dataSchema.js           //
    │      test.querySchema.js          //
    │      testAction.config.js         //
    │      testAction.dataSchema.js     //
    │      testAction.querySchema.js    //
    │      testSms.config.js            //
    │      testSms.dataSchema.js        //
    │      testSms.querySchema.js       //
    │                                   
    └─utils                             //
            ajax.js                     //
            index.js                    //
            Logger.js                   //自定义日志输出级别
            MockAjax.js                 //
            RealAjax.js                 //

```
