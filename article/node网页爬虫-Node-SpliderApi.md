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

### 启动
```javascript
npm i 
npm run dev
```
访问： http://localhost:3001/


### 目录结构
```$xslt
│  app.js                                        //express服务器配置信息：路由信息，端口设置
│  package.json                                  //依赖包
│                                                
├─bin                                            //
│      www                                       //
│                                                //
├─config                                         //配置信息文件夹
│      dbs.js                                    //数据库账号配置信息
│      routes.js                                 //
│
├─docs                                           //
│      .nojekyll                                 //
│      api.png                                   //
│      index.html                                //
│      README.md                                 //
│      sw.js                                     //
│      _coverpage.md                             //
│
├─public
│  │  favicon.ico
│  │  index.html
│  │
│  ├─css
│  │
│  ├─fonts
│  │
│  └─js
│
├─routes
│  ├─api
│  │  ├─it
│  │  │      daily_info.js
│  │  │      daily_list.js
│  │  │      web_frame.js
│  │  │
│  │  ├─job
│  │  │      job_info.js
│  │  │      job_list.js
│  │  │
│  │  ├─joke
│  │  │      joke_img.js
│  │  │      joke_list.js
│  │  │      joke_photo.js
│  │  │
│  │  ├─music
│  │  │      new_songs.js
│  │  │      plist.js
│  │  │      plist_songs.js
│  │  │      rank_list.js
│  │  │      rank_list_info.js
│  │  │      search.js
│  │  │      singer_classify.js
│  │  │      singer_info.js
│  │  │      singer_list.js
│  │  │      song_info.js
│  │  │      song_lrc.js
│  │  │
│  │  ├─news
│  │  │      news_detail.js
│  │  │      news_list.js
│  │  │      video_list.js
│  │  │
│  │  └─photo
│  │          huaban.js
│  │          jandan.js
│  │          photo_list.js
│  │          photo_type.js
│  │          photo_view.js
│  │
│  └─web
│          daily_info.js
│          daily_list.js
│          index.js
│          jandan.js
│          photo.js
│
├─utils
│      decrypt.js
│      fetch.js
│      filter_sign.js
│      httpServer.js
│      log_color.js
│      md5.js
│
└─views
    └─web
            daily_info.ejs
            daily_list.ejs
            index.ejs
            jandan.ejs
            photo.ejs
```
