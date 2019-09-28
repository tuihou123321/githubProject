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
│  app.js
│  package.json
│  README.md
│
├─public
│  ├─images
│  │      node-email-server.webp
│  │
│  └─stylesheets
│          style.css
│
├─routes
│      index.js
│
├─test
│      test.unit.js
│
└─views
    │  error.jade
    │  layout.jade
    │
    └─submit
        │  index.html
        │
        └─assets
            ├─bootstrap
            └─js
                    jquery.backstretch.js
                    jquery.backstretch.min.js
                    jquery.blockUI.js
                    placeholder.js
                    retina-1.1.0.js
                    retina-1.1.0.min.js
                    scripts.js

```
