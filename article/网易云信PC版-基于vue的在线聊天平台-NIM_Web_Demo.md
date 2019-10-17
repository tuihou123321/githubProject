## 网易云信PC版-基于vue的在线聊天平台-NIM_Web_Demo.md

### 项目介绍
基于websocket技术实现的h5在线聊天功能,项目内大量jquery,vue代码混用,猜测可能是遗留代码没有迁移完成造成的;
虽然引入了jquery,但是很多dom的操作还是使用原生语法；
eg:
- 元素获取
- dom元素创建、属性添加
- dom插入

页面与js完全分离，通过事件监听的方式来执行事件响应；

<br>
**项目地址**： https:    //github.com/netease-im/NIM_Web_Demo 


### 主要功能：
- 账号登陆/注册/退出
- 在线聊天(私聊,群聊)
- 发送文字/表情/图片/文本
- 用户状态显示(在线/离线)
- 个人资料修改(头像,昵称,性别,生日,手机,邮箱,签名)
- 查看好友列表/好友详情
- 设置黑名单
- 消息云记录(默认7天)
- 发送语音/视频
- 直播间
- 白版演示


### 启动
```js
npm i 
npm run start
```
http:    //127.0.0.1:8182/webdemo/im/login.html


### 技术栈
- vue
- jquery


###  技术点

    

### 项目结构

```

│  app.js                                            //
│  package.json                                      //
│                                                    
├─ssh                                               //证书,用于加密通讯
│      cert.pem                                      //
│      key.pem                                       //
│                                                    
└─webdemo                                           //
    │  index.html                                    //入口文件
    │                                                
    ├─3rd                                           //核心模块实现的sdk,主要的库
    │
    ├─im                                            //页面
    │  │  cloudMsg.html                             //云消息html代码片段,通过jquery.load方法动态载入页面,再把data通过dom插入的方式渲染出来
    │  │  createTeam.html                           //
    │  │  index.html                                //项目实际入口文件(可配置私有化环境)
    │  │  login.html                                //登陆页面
    │  │  main.html                                 //私聊页面(聊天界面逻辑使用vue处理,其他使用jquery)
    │  │  netcall_meeting.html                      //
    │  │  register.html                             //
    │  │  selectCallMethod.html                     //
    │  │  speakBan.html                             //
    │  │  teamInfo.html                             //
    │  │  teamMember.html                           //
    │  │
    │  ├─audio                                     //消息提示音资源文件
    │  │                                            
    │  ├─chatroom                                  //聊天室
    │  │                                           
    │  └─js                                       //
    │      │  cache.js                             //缓存数据，通过构造函数来创建一个Cache对象
    │      │  config.js                            //环境配置文件（可私有化环境）
    │      │  emoji.js                             //表情包配置文件
    │      │  link.js                              //SDK封装，消息订阅，发送，云记录消息获取，踢下线，添加/删除好友，黑名单等
    │      │  login.js                             //登陆相关的方法
    │      │  main.js                              //判断是不是私有化环境，来初始化yunxin对象
    │      │  md5.js                               //md5加密库
    │      │  register.js                          //注册用到的JS方法
    │      │  ui.js                                //聊天窗口view层html  
    │      │  util.js                              //工具类（cookies处理，日期格式化，数组功能扩展，包含其他页面逻辑代码）
    │      │                                       
    │      ├─3rd                                  //库
    │      │  │  jquery-ui.min.js                 //jquery ui库
    │      │  │  jquery.Jcrop.min.js              //jquery图片裁剪库
    │      │  │  whiteboard.js                    //白板演示库
    │      │  │                                   
    │      │  └─contextMenu                      //
    │      │      │  jquery.contextMenu.css       //
    │      │      │  jquery.contextMenu.js        //
    │      │      │  jquery.contextMenu.min.css   //
    │      │      │  jquery.contextMenu.min.js    //
    │      │      │  jquery.ui.position.js        //
    │      │      │  jquery.ui.position.min.js    //
    │      │      │                               
    │      │      └─font                         //
    │      │                                       //
    │      ├─module                               //
    │      │      base.js                          //
    │      │      cloudMsg.js                      //
    │      │      dialog_call_method.js            //
    │      │      dialog_team.js                   //
    │      │      friend.js                        //
    │      │      message.js                       //
    │      │      netcall.js                       //
    │      │      netcall_meeting.js               //
    │      │      netcall_ui.js                    //
    │      │      notification.js                  //
    │      │      personCard.js                    //
    │      │      session.js                       //
    │      │      sysMsg.js                        //
    │      │      team.js                          //
    │      │      whiteboard.js                    //
    │      │                                       
    │      └─widget                               //自定义封装的组件
    │              minAlert.js                      //弹窗
    │              uiKit.js                         //轻量级UI组件库

```


