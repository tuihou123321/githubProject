## 网易云信PC版-基于vue的在线聊天平台-NIM_Web_Demo.md

### 项目介绍
网易云信的在线聊天
<br>
**项目地址**： https://github.com/netease-im/NIM_Web_Demo 


### 主要功能：
- 账号登陆/登陆
- 在线聊天
- 查看好友列表
- 查看用户信息
- 设置黑名单


### 启动
```js
npm i 
npm run start
```
http://127.0.0.1:8182/webdemo/im/login.html


### 技术栈
- vue



### 项目优点


  
### 总结


    

### 项目结构

```

│  app.js
│  package.json
│  README.md
│
├─ssh
│      cert.pem
│      key.pem
│
└─webdemo
    │  index.html
    │  main.html
    │  package-lock.json
    │
    ├─3rd
    │  │  DrawPlugin.js
    │  │  jquery-1.11.3.min.js
    │  │  nim_server_conf.js
    │  │  NIM_Web_Chatroom_v6.1.0.js
    │  │  NIM_Web_Netcall_v6.1.0.js
    │  │  NIM_Web_NIM_v6.1.0.js
    │  │  NIM_Web_NRTC_v6.1.0.js
    │  │  NIM_Web_SDK_v6.1.0.js
    │  │  NIM_Web_WebRTC_v6.1.0.js
    │  │  NIM_Web_WhiteBoard_v6.1.0.js
    │  │  platform.js
    │  │  polyfill.js
    │  │  rangeslider.min.js
    │  │  recorder.js
    │  │  rtcSupport.js
    │  │  vue.min.js
    │  │  zepto.min.js
    │  │
    │  ├─chrome
    │  │      gapafbpmfemleaplicdhhcikajbogpkf_main.crx
    │  │      yunxin-Web-Screensharing.crx
    │  │
    │  ├─es5-shim
    │  │  │  bower.json
    │  │  │  CHANGES
    │  │  │  component.json
    │  │  │  CONTRIBUTORS.md
    │  │  │  es5-sham.js
    │  │  │  es5-sham.map
    │  │  │  es5-sham.min.js
    │  │  │  es5-shim.js
    │  │  │  es5-shim.map
    │  │  │  es5-shim.min.js
    │  │  │  LICENSE
    │  │  │  Makefile
    │  │  │  package.json
    │  │  │  README.md
    │  │  │  shims.json
    │  │  │
    │  │  └─tests
    │  │      │  .eslintrc
    │  │      │  index.html
    │  │      │  index.min.html
    │  │      │  native.html
    │  │      │
    │  │      ├─helpers
    │  │      │      h-matchers.js
    │  │      │
    │  │      ├─lib
    │  │      │      jasmine-html.js
    │  │      │      jasmine.css
    │  │      │      jasmine.js
    │  │      │      jasmine_favicon.png
    │  │      │
    │  │      └─spec
    │  │              helpers-jasmine.js
    │  │              s-array.js
    │  │              s-date.js
    │  │              s-error.js
    │  │              s-function.js
    │  │              s-global.js
    │  │              s-number.js
    │  │              s-object.js
    │  │              s-regexp.js
    │  │              s-string.js
    │  │
    │  ├─EventEmitter
    │  │      EventEmitter.js
    │  │      EventEmitter.min.js
    │  │
    │  ├─jQuery-ajaxTransport-XDomainRequest
    │  │      bower.json
    │  │      jQuery.XDomainRequest.js
    │  │      jQuery.XDomainRequest.min.js
    │  │      LICENSE.txt
    │  │      package.json
    │  │      README.md
    │  │
    │  ├─video-js-5.8.7
    │  │  │  video-js.css
    │  │  │  video-js.min.css
    │  │  │  video-js.swf
    │  │  │  video.js
    │  │  │  video.js.map
    │  │  │  video.min.js
    │  │  │  video.min.js.map
    │  │  │
    │  │  ├─alt
    │  │  │      video-js-cdn.css
    │  │  │      video-js-cdn.min.css
    │  │  │      video.novtt.js
    │  │  │      video.novtt.min.js
    │  │  │      video.novtt.min.js.map
    │  │  │
    │  │  ├─examples
    │  │  │  ├─shared
    │  │  │  │      example-captions.vtt
    │  │  │  │
    │  │  │  └─simple-embed
    │  │  │          index.html
    │  │  │
    │  │  ├─font
    │  │  │
    │  │  ├─ie8
    │  │  │      videojs-ie8.js
    │  │  │      videojs-ie8.min.js
    │  │  │
    │  │  └─lang
    │  │          zh-CN.js
    │  │          zh-TW.js
    │  │
    │  └─videojs-hls-2.0.1
    │          videojs-contrib-hls.js
    │          videojs-contrib-hls.min.js
    │
    ├─im
    │  │  cloudMsg.html
    │  │  createTeam.html
    │  │  index.html
    │  │  login.html
    │  │  main.html
    │  │  netcall_meeting.html
    │  │  register.html
    │  │  selectCallMethod.html
    │  │  speakBan.html
    │  │  teamInfo.html
    │  │  teamMember.html
    │  │
    │  ├─audio
    │  │      avchat_connecting.mp3
    │  │      avchat_no_response.mp3
    │  │      avchat_peer_busy.mp3
    │  │      avchat_peer_reject.mp3
    │  │      avchat_ring.mp3
    │  │
    │  ├─chatroom
    │  │  │  anchor.html
    │  │  │  gulpfile.js
    │  │  │  list.html
    │  │  │  login.html
    │  │  │  package.json
    │  │  │  room.html
    │  │  │  roomManage.html
    │  │  │
    │  │  ├─dist
    │  │  │  ├─css
    │  │  │  │      chartroom.css
    │  │  │  │
    │  │  │  └─js
    │  │  │          emoji.js
    │  │  │          link.js
    │  │  │          room.js
    │  │  │          title.js
    │  │  │          util.js
    │  │  │
    │  │  ├─font
    │  │  │  │  demo.html
    │  │  │  │  Read Me.txt
    │  │  │  │  selection.json
    │  │  │  │  style.css
    │  │  │  │
    │  │  │  ├─demo-files
    │  │  │  │      demo.css
    │  │  │  │      demo.js
    │  │  │  │
    │  │  │  └─fonts
    │  │  │
    │  │  ├─images
    │  │  │  │  bg.png
    │  │  │  │
    │  │  │  └─emoji
    │  │  │          emoji_0.png
    │  │  │
    │  │  └─src
    │  │      ├─css
    │  │      │  │  config.css
    │  │      │  │  emoji.css
    │  │      │  │  font.css
    │  │      │  │  index.css
    │  │      │  │  reset.css
    │  │      │  │  util.css
    │  │      │  │
    │  │      │  ├─list
    │  │      │  │      list.css
    │  │      │  │
    │  │      │  ├─manager
    │  │      │  │      manager.css
    │  │      │  │
    │  │      │  └─room
    │  │      │          room.css
    │  │      │
    │  │      └─js
    │  │              emoji.js
    │  │              link.js
    │  │              room.js
    │  │              title.js
    │  │              util.js
    │  │
    │  ├─css
    │  │  │
    │  │  ├─contextMenu
    │  │  │  │  jquery.contextMenu.css
    │  │  │  │  jquery.contextMenu.min.css
    │  │  │  │  jquery.contextMenu.min.css.map
    │  │  │  │
    │  │  │  └─font
    │  │  │
    │  │  └─images
    │  │          ui-bg_flat_0_aaaaaa_40x100.png
    │  │
    │  ├─images
    │  │  │  addFriend.png
    │  │
    │  └─js
    │      │  cache.js
    │      │  config.js
    │      │  emoji.js
    │      │  link.js
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


