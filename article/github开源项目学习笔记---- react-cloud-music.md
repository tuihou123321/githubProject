## github开源项目推荐---- react-cloud-music

### 项目介绍

一个仿网易云音乐的react h5项目，具有丰富的动画效果，使用了大量react的库，具有良好的单元测试；
使用了代码分割，图片懒加载技术来提高性能，tab栏点击后缓存了数据，避免重复请求

项目地址：https://github.com/sanyuan0704/react-cloud-music

接口地址：https://github.com/Binaryify/NeteaseCloudMusicApi/tree/dbd1d7ab02eea1b15d3a87f76e6ccd169e9167f3


### 主要功能：

- 全局音频播放组件
- 搜索功能
- banner轮播图
- 下拉加载


### 启动

```js
cnpm i

//下载子模块（启动api接口服务）
git submodule update --init --recursive
cd NeteaseCloudMusicApi
cd ..   

//开始运行
npm run start

```

### 打包发布到线上
```js
npm run build
```


### 技术栈

- react16.8 
- react-router5.0
- better-scroll   移动端滚动组件
- immutable，redux-immutable     不可变量数据，提高react组件diff性能
- react-lazyload    异步加载react组件
- react-router-config   来渲染路由，只要提供路由配置表
- react-transition-group  react动画，过渡组件
- redux-thunk   redux中间件
- styled-components  使用样式组件化
- express 开启node服务
- compression  node中间件，在服务端压缩代码


### 项目优点

- 使用react16.8的新语法特性，lazy,Suspense异步加载组件，提高性能im
- 使用hook来写组件
- 使用  <></> 来代替 ,<div></div>，<Fragment></Fragment>包裹层
- 使用jest+enzyme做了单元测试
- 使用concurrently同时启动多个命令

  

### 项目结构

```
│  package.json
│  server.js
│
├─config                                               // webpack基本配置项
│  │  env.js                                           // 环境变量
│  │  modules.js                                       // 模块化
│  │  paths.js                                         // 常用文件路径
│  │  pnpTs.js                                         // 
│  │  webpack.config.js                                // 通用webpack配置信息
│  │  webpackDevServer.config.js                       // webpack测试环境配置信息
│  │
│  └─jest                                             // 单元测试文件夹
│          cssTransform.js                              //
│          fileTransform.js                             //
│                                                       //
├─NeteaseCloudMusicApi                                 // 接口存放的文件夹，要通过命令单独下载
├─public                                               // 公用资源文件夹                         
│      favicon.ico
│      index.html
│      manifest.json
│                                                       //
├─scripts                                              //
│      build.js                                         // 打包命令
│      start.js                                         // 启动命令
│      test.js                                          // 单元测试
│
└─src
    │  App.js
    │  fix.css
    │  index.js
    │  logo.svg
    │  serviceWorker.js
    │  style.js
    │  tree.txt
    │
    ├─api
    │      config.js
    │      lyric-parser.js
    │      request.js
    │      script.js
    │      utils.js
    │
    ├─application
    │  ├─Album
    │  │  │  index.js
    │  │  │  style.js
    │  │  │
    │  │  └─store
    │  │          actionCreators.js
    │  │          constants.js
    │  │          index.js
    │  │          reducer.js
    │  │
    │  ├─Home
    │  │      index.js
    │  │      style.js
    │  │
    │  ├─Player
    │  │  │  index.js
    │  │  │
    │  │  ├─mini-player
    │  │  │      index.js
    │  │  │      style.js
    │  │  │
    │  │  ├─normal-player
    │  │  │      index.js
    │  │  │      style.js
    │  │  │
    │  │  ├─play-list
    │  │  │      index.js
    │  │  │      style.js
    │  │  │
    │  │  └─store
    │  │          actionCreators.js
    │  │          constants.js
    │  │          index.js
    │  │          reducer.js
    │  │
    │  ├─Rank
    │  │  │  index.js
    │  │  │  style.js
    │  │  │
    │  │  └─store
    │  │          index.js
    │  │
    │  ├─Recommend
    │  │  │  index.js
    │  │  │  style.js
    │  │  │
    │  │  └─store
    │  │          actionCreators.js
    │  │          constants.js
    │  │          index.js
    │  │          reducer.js
    │  │
    │  ├─Search
    │  │  │  index.js
    │  │  │  music.png
    │  │  │  singer.png
    │  │  │  style.js
    │  │  │
    │  │  └─store
    │  │          actionCreators.js
    │  │          constants.js
    │  │          index.js
    │  │          reducer.js
    │  │
    │  ├─Singer
    │  │  │  index.js
    │  │  │  style.js
    │  │  │
    │  │  └─store
    │  │          actionCreators.js
    │  │          constants.js
    │  │          index.js
    │  │          reducer.js
    │  │
    │  ├─Singers
    │  │  │  index.js
    │  │  │  singer.png
    │  │  │  style.js
    │  │  │
    │  │  └─store
    │  │          actionCreators.js
    │  │          constants.js
    │  │          index.js
    │  │          reducer.js
    │  │
    │  ├─SongList
    │  │      index.js
    │  │      style.js
    │  │
    │  └─User
    │      └─Login
    │          │  index.js
    │          │  style.js
    │          │
    │          ├─components
    │          │  ├─LoginForm
    │          │  │      index.js
    │          │  │      style.js
    │          │  │
    │          │  └─PhoneForm
    │          │      │  index.js
    │          │      │  style.js
    │          │      │
    │          │      ├─step-one
    │          │      │      index.js
    │          │      │
    │          │      └─step-two
    │          │              index.js
    │          │              style.js
    │          │
    │          └─store
    │                  actionCreators.js
    │                  constants.js
    │                  index.js
    │                  reducer.js
    │
    ├─assets             //静态资源文件
    │  │  back.svg
    │  │  border.js
    │  │  music.png
    │  │
    │  └─iconfont     //字体图标
    │
    ├─baseUI
    │  ├─confirm
    │  │      index.js
    │  │
    │  ├─header
    │  │      index.js
    │
    ├─components
    │  ├─album-detail
    │  │      index.js
    │  │      style.js
    │  │
    │  ├─list
    │  │      index.js
    │  │      music.png
    │  │      style.js
    
    ├─layouts
    │      BlankLayout.js
    │      HomeLayout.js
    │      HomeLayout.style.js
    │
    ├─routes
    │      index.js
    │
    └─store
            index.js
            reducer.js
    
```


