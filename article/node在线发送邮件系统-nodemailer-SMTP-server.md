# node网页爬虫- Node-SpliderApi

## 项目说明 
基于node的邮件服务系统，可在线发送邮件

**项目地址**：https://github.com/momodiy/nodemailer-SMTP-server

### 技术栈
- express     //搭建web服务器
- nodemailer  //node的邮件系统
- jade        //html模板引擎
- nodemon     //node进程监控，文件修改自动重启
- html5shiv   //让ie6-ie8支持html5标签
- respond     //让ie6-ie8支持css3标签 
- font-awesome  //icon图标库

### 启动
```javascript
npm i 
npm run start
```
访问： http://localhost:8888



### 目录结构

```$xslt
│  
│  app.js                          //express基本配置：端口监听、插件引入               
│  package.json                    //依赖包
│                                                 
├─public                           //公共资源文件夹
│                                  
├─bin                              //可执行文件夹               
│      start.js                    //启动文件                            
├─routes                           //路由配置文件夹              
│      index.js                    //路由配置，并引入nodemailer
│                                  
├─test                             //单元测试文件夹               
│      test.unit.js                //单元测试              
│                                     
└─views                            //视图层模板             
    │  error.jade                  //错误页模板             
    │  layout.jade                 //布局模板             
    │                              
    └─submit                       //视图层模板             
        │  index.html              //主入口模板             
        │                          
        └─assets                   //静态资源             
```
