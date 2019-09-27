## 网易云音乐-react-cloud-music

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
- styled-components  使用样式组件化，区分全局/局部样式
- express 开启node服务
- compression  node中间件，在服务端压缩代码


### 项目优点

- 使用react16.8的新语法特性，lazy,Suspense异步加载组件
- 使用React.memo来避免函数组件的重复渲染，通过判断props状态是否改变，相当于组件的PureComponet
- 使用hook来写组件
- 使用  <></> 来代替 ,<div></div>，<Fragment></Fragment>包裹层
- 使用jest+enzyme做了单元测试
- 使用concurrently同时启动多个命令
- 基本使用的都是函数纯组件

  
### 总结
styled-components虽然可以把样式封装成一个组件的形式把元素包裹起来，但是IDE的不支持语法高亮，自动补全，个人不太喜欢；
项目中基本使用的是纯函数组件，性能上比较好；


  
  

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
│                                                       
├─NeteaseCloudMusicApi                                 // 接口存放的文件夹，要通过命令单独下载
├─public                                               // 公用资源文件夹                         
│      favicon.ico
│      index.html                                       // 模板文件
│      manifest.json                                    // 将站点添加至主屏幕配置文件
│                                                       
├─scripts                                              // 脚本启动文件夹
│      build.js                                         // 打包命令
│      start.js                                         // 启动命令
│      test.js                                          // 单元测试
│
└─src
    │  App.js                                           // 路由配置、全局样式，redux注入
    │  fix.css                                          // 移动端兼容高清屏的样式写法
    │  index.js                                         // 项目入口文件
    │  serviceWorker.js                                 // 实现离线浏览
    │  style.js                                         // 通过引入createGlobalStyle来创建全局样式
    │
    ├─api                                              //
    │      config.js                                    // axios基本的配置、拦截器等
    │      lyric-parser.js                              // 解析歌词一个方法
    │      request.js                                   // 把api接口封装成一个个方法
    │      script.js                                    // axios基本配置，拦截器2，初始化请求一堆接口数据
    │      utils.js                                     // 工具类方法
    │
    ├─application                                      // 应用程序页面
    │  │
    │  ├─Home                                         // 首页模块
    │  │      index.js                                 // 首页模块入口文件
    │  │      style.js                                 // 首页模块样式文件
    │  │
    │  └─User                                         // 用户模块
    │      └─Login                                    // 登陆模块
    │          │  index.js                             // 登陆模块入口文件
    │          │  style.js                             // 用户登陆模块样式
    │          │
    │          ├─components                           // 用户模块组件文件夹（子内容同上）
    │          │
    │          └─store                                // 用户模块的store文件夹 
    │                  actionCreators.js                //
    │                  constants.js                     //
    │                  index.js                         //
    │                  reducer.js                       //
    │
    ├─assets                                           // 静态资源文件
    │
    ├─baseUI
    │  ├─confirm
    │  │      index.js
    │  │
    │  ├─header
    │  │      index.js
    │
    ├─components
    │  │
    │  ├─list
    │  │      index.js
    │  │      music.png
    │  │      style.js
    │   
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


