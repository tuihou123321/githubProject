# node网页爬虫- Node-SpliderApi

## 项目说明 
基于node的邮件服务系统，可在线发送邮件，邮件服务器的权限信息使用了加密方式处理，
如果想使用自己的服务器，要把加密方式删除，并且使用官方原始代码；核心代码演示如下

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

### 核心代码

```javascript

const nodemailer = require('nodemailer')  

// 设置服务器基本信息
var mailTransport = nodemailer.createTransport({
  host : 'smtp.sina.com',
  secureConnection: true, // use SSL
  auth : {
    user : 'konkadigital@sina.cn',
    pass : 'xxxx'
  },
});

//发送邮件的方法
  mailTransport.sendMail(options, function (err, msg) { // eslint-disable-line
    if (err) {
      res.status(500).render('error', {
        title: err.response,
        error: {
          status: err.responseCode,
          stack: err
        }
      })
    } else {
      res.status(200).send({
        msg: '邮件已经发送至：' + msg.accepted,
        title: '邮件发送成功',
        type: 'success',
        status: 200,
        data: new Date()
      }).end()
    }
  })

```


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
