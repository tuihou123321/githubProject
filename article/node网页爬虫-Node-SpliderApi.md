# node网页爬虫- Node-SpliderApi

## 项目说明 
基于node的前端爬虫系统，API支持列表
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

### 启动
```javascript
npm i 
npm run dev
```
访问： http://localhost:3001/
