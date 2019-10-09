# 后端人员开发的基于antdDesign的后台管理系统-react-antd-admin

## 项目说明 
以后端的视角来做前端的后台管理项目，核心项目思路是用写配置的方式替代写代码，
符合数据驱动的原则，数据与逻辑分离。
接口文档，版本更新记录文档比较详细；
代码注释中写了比较多关于作者的学习心得；
对于后端常用的表单数据查询功能进行了封装，主模块进行拆分：查询组件，搜索操作组件，table展示组件，分页组件；
通过配置项动态创建查询项，复用性强；


**项目地址**: [https://www.github.com/jiangxy/react-antd-admin](https://www.github.com/jiangxy/react-antd-admin)

### 技术栈
- react+react-router+redux  //react全家桶
- ant design  //ui框架
- superagent  //基于promise的轻量级ajax api，适用于client/node
- moment    //日期处理类库 


### 技术点
- [x] 使用webpack.optimize.CommonsChunkPlugin来提取公用模块 verdor.min.js，放入cdn可加速  
- [x] 使用react的getComponent 动态//react-router3.x老版本的方案
- [x] 自定义了logger.js 来设置不同环境下的日志输出级别,debug,info,warn,error


### 功能点
- [x] 登陆
- [x] 多级导航菜单
- [x] 表格数据的选择、增/删/改/查、分页

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
    ├─schema                            //数据配置项
    │      test.config.js               //是不是显示导出按钮
    │      test.dataSchema.js           //数据查询层配置：传给后端的值/数据类型，组件类型/数据/样式，表格内是否展示
    │      test.querySchema.js          //数据展示层配置：展示的字段/顺序，默认值，类型定义及字符转换，扩展接口/改变渲染结果
    │                                   
    └─utils                             //工具类方法
            ajax.js                     //通过配置项来切换请求数据类型（mock,real）
            index.js                    //工具类方法汇总：日期处理，url参数获取，是不是字符串
            Logger.js                   //自定义日志输出级别
            MockAjax.js                 //mock数据请求
            RealAjax.js                 //基于superagent的ajax请求方法，接口数据

```
