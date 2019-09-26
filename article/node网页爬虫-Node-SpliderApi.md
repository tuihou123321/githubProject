# node网页爬虫- Node-SpliderApi

## 项目说明 
基于node的前端爬虫系统，API支持列表如下，通过express架设web服务器，把接口通过ejs模板渲染成新的web站点
- 拉勾工作职位搜索
- 前端框架top100
- 视频数据列表

**项目地址**：https://github.com/ecitlm/Node-SpliderApi

### 技术栈
- express  //node服务层框架 
- request   //在node层发起请求
- cheerio   //node层中的dom选择器
- nodemon   //监控文件变化，自动重启node服务（不会自动重启，生产环境推荐使用pm2）
- iconv-lite // 解决node环境中gbk编码的问题
- ejs   //js模板语言
- docsify  //通过md快速生成文档网站

### 启动
```javascript
npm i 
npm run dev
```
访问： http://localhost:3001

###启动文档网站
```javascript
npm i docsify-cli -g
docsify serve docs
```
访问： http://localhost3000

### 目录结构
```$xslt
│  app.js                                        //express服务器配置信息：路由信息，端口设置
│  package.json                                  //依赖包
│                                                
├─bin                                            //
│      www                                       //
│                                                
├─config                                         //配置信息文件夹
│      dbs.js                                    //数据库账号配置信息
│      routes.js                                 //
│
├─docs                                           //基于docsify框架，通过md文件快速生成文档网站
│      .nojekyll                                 
│      api.png                                   //资源图片
│      index.html                                //模板
│      README.md                                 //主要内容，默认首页
│      sw.js                                     //离线访问所需文件
│      _coverpage.md                             //首屏内容设置（模板自带）
│
├─public                                         //静态资源文件                           
│  │  index.html                                 //
│
├─routes                                         //路由文件夹
│  ├─api                                         //api路由
│  │  ├─it                                       //api路由模块
│  │  │      daily_list.js                       //api路由子文件
│  │
│  └─web                                         //网页路由                    
│          index.js                              //网页路由子文件
│
├─utils                                         //工具类方法文件夹
│
└─views                                         //视图层
    └─web                                       //ejs模板文件夹
            index.ejs                           //ejs模板文件，相当于template，可以获取express中的变量
```
