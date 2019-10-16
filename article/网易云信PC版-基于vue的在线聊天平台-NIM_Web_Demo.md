## 网易云信PC版-基于vue的在线聊天平台-NIM_Web_Demo.md

### 项目介绍
基于websocket技术实现的h5在线聊天功能
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
    │  ├─audio                                     //
    │  │      avchat_connecting.mp3                 //
    │  │      avchat_no_response.mp3                //
    │  │      avchat_peer_busy.mp3                  //
    │  │      avchat_peer_reject.mp3                //
    │  │      avchat_ring.mp3                       //
    │  │                                            
    │  ├─chatroom                                  //聊天室
    │  │                                           //
    │  └─js                                       //
    │      │  cache.js                             //
    │      │  config.js                            //
    │      │  emoji.js                             //
    │      │  link.js                              //
    │      │  login.js
    │      │  main.js
    │      │  md5.js
    │      │  register.js
    │      │  ui.js
    │      │  util.js
    │      │
    │      ├─3rd
    │      │  │  jquery-ui.min.js
    │      │  │  jquery.Jcrop.min.js
    │      │  │  whiteboard.js
    │      │  │
    │      │  └─contextMenu
    │      │      │  jquery.contextMenu.css
    │      │      │  jquery.contextMenu.js
    │      │      │  jquery.contextMenu.min.css
    │      │      │  jquery.contextMenu.min.css.map
    │      │      │  jquery.contextMenu.min.js
    │      │      │  jquery.contextMenu.min.js.map
    │      │      │  jquery.ui.position.js
    │      │      │  jquery.ui.position.min.js
    │      │      │
    │      │      └─font
    │      │
    │      ├─module
    │      │      base.js
    │      │      cloudMsg.js
    │      │      dialog_call_method.js
    │      │      dialog_team.js
    │      │      friend.js
    │      │      message.js
    │      │      netcall.js
    │      │      netcall_meeting.js
    │      │      netcall_ui.js
    │      │      notification.js
    │      │      personCard.js
    │      │      session.js
    │      │      sysMsg.js
    │      │      team.js
    │      │      whiteboard.js
    │      │
    │      └─widget
    │              minAlert.js
    │              uiKit.js
    │              uiKit.min.js

```


