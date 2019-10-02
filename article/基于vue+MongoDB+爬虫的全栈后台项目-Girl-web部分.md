# 基于vue+MongoDB+爬虫的全栈后台项目-Girl-web部分

## 项目说明 
本项目是一个全栈爬虫项目，包含三大独立部分：
- /admin   //管理后台
- /server  //服务端
- /app     //app端

项目设计思路，通过服务端去爬取web数据，存在mongoDB中，再把数据提供成接口，供admin、app模块调用展示；
同时web平台提供用户、日志模块管理管理；


**项目地址**：https://github.com/Xu-Angel/Girl  <br/>
**在线演示**：http://girl.xutianshi.top/admin/index.html#/dashboard


### 管理后台技术栈
- vue+vuex            //vue全家桶   
- element-ui          //UI组件库 
- js-cookie           //客户端的cookies库
- mockjs              //mock数据 
- nprogress           //实现网页顶部进度条
- vue-count-to        //数字累加动画组件
- axios               //前端请求库
- socket.io           //即时通讯模块,基于websocket


### 后台web功能  /admin
- [x] 登陆、注册
- [x] 权限管理
- [x] 妹子数据查询
- [x] 爬虫设置（爬取状态-爬虫进度展示动画，代理IP查看，参数配置-去重）
- [x] 管理员列表、操作
- [x] 日志记录（访问日志，日志分类查看/管理）
- [x] 我的信息（头像上传，密码修改）
- [x] 自适应移动端


### 启动
```javascript

```

### 目录结构

```$xslt                                    
                                             
│  index.html                                //浏览器访问入口文件
│  package.json                              //npm配置文件，依赖包，启动命令，项目说明
│                                            
├─build                                      //webpack构建文件
│      build.js                              //
│      check-versions.js                     //
│      utils.js                              //
│      vue-loader.conf.js                    //
│      webpack.base.conf.js                  //基本通用配置
│      webpack.dev.conf.js                   //测试环境构建配置
│      webpack.prod.conf.js                  //生产环境构建配置
│                                            
├─config                                     //webpack配置文件夹
│      dev.env.js                            //测试配置
│      index.js                              //设置webpack不同环境下的配置文件（静态服务器，跨域代理，资源路径，打包输出文件...）
│      prod.env.js                           //生产配置
│                                            
├─mock                                       //使用mock.js来模拟数据
│      index.js                              //入口文件，通过引入子文件来处理不同参数的返回状态
│                                            
├─src                                        //业务项目源码目录
│  │  App.vue                                //路由顶层包括文件
│  │  main.js                                //webpack打包入口文件，的顶层注入store,router配置
│  │  permission.js                          //路由拦截，未登陆重定向到登陆页，并在路由切换时注入顶部加载条动画
│  │                                         
│  ├─api                                     //封装好的api文件夹，封装好url,method,接收data
│  │      admin.js                           //用户信息模块（其他模块：女孩信息、ip、日志、爬虫、通用）
│  │                                         
│  ├─assets                                  //静态资源
│  │                                         
│  ├─components                              //组件文件夹
│  │  ├─Breadcrumb                           //封装的组件包括：svg图片，
│  │  │      index.vue                       
│  │                                         
│  ├─icons                                   //所有的icon列表
│  │  │  index.js                            //把svg文件批量导出，并全局注册
│  │  └─svg                                  //svg文件夹
│  │                                         //
│  ├─router                                  //使用vue-router 配置全局路由表
│  │      index.js                           
│  │                                         
│  ├─store                                   //vuex配置文件夹
│  │  │  getters.js                          //
│  │  │  index.js                            //实例化vuex
│  │  │                                      
│  │  └─modules                              //
│  │          app.js                         //
│  │          tagsView.js                    //
│  │          user.js                        //
│  │                                         
│  ├─styles                                  //样式
│  │                                         
│  ├─utils                                   //工具方法
│  │      auth.js                            //权限验证
│  │      regulation.js                      //正则
│  │      request.js                         //基于axios封装的请求库
│  │      validate.js                        //验证方法
│  │                                         
│  └─views                                   //视图层
│      │                                     
│      ├─layout                              //布局模块
│      │  │  Layout.vue                      //布局模块文件
│      │  │                                  
│      │  ├─components                       //此模块自己的组件库
│      │  │
│      │  └─mixin                            //混入文件夹（组件逻辑复用模块）
│      │          ResizeHandler.js           //监控屏幕宽度变化，自动切换classname,来实现响应式设计
│      │
│

```
