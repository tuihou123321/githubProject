## github开源推荐项目：ant-design-icons



### 项目介绍：

通过请求 github上ant-design-mobile项目中引用的[icon文件](https://github.com/ant-design/ant-design-mobile/blob/master/components/icon/loadSprite.tsx),
单独导出icon，供其他框架使用，比如vue;

支持多种引入方式：svg、webFont

**项目地址**：<https://github.com/fjc0k/ant-design-icons>




### 技术栈：
- vue+vuepress  搭建web基本框架，使用md来生成网页

- webfonts-generator 把svg文件转成font字体图标

- element-ui 样式支持

- vue-clipboards  点击复制文件名

- axios 发起请求，动态获取ant design的css文件中引用的icon

  


### 项目启动

```
cnpm i   //安全装依赖包
npm run serve   //启动服务
npm run build  //打包项目，供其他项目引入使用
```



### 项目架构：

#### vuepress框架优点介绍

- [x]  通过markdown文件，自动创建路由，生成静态网页
- [x]  支持关键词搜索：md三级目录内的标题
- [x]  特殊的vue+md语法： <script></script>标签是vue语法， 其他部分=vue模板渲染语法+markdown语法；
- [x] 内置样式模板配置文件，json文件，可以修改导航栏
- [x] 支持热更新



### 项目结构

```


│  package.json                          //项目依赖包
├─dist                                  //打包后的文件
│  │  anticons.css                      //通过样式引入文件
│  │  anticons.json                     //所有支持的图标列表
│  │  anticons.min.css                  //通过样式引入文件min版本              
│  │  index.js                          //项目引用文件入口/列表
│  │
│  ├─font                              //打包后的svg可以使用font字体引入
│  ├─mobile                            //引入到项目中的文件
│  │  │  anticons.json                 //所有svg,json对象名称
│  │  │  index.js                      //所在导出地svg引用列表
│  │  │
│  │  └─svg                           //引要导出的svg文件列表
│  │          check-circle-o.svg        //svg文件
│  │
│  ├─standalone                             
│  └─svg                               //项目中所有svg文件
│          alipay-circle.svg│
├─docs                                  //docs下的md文件会自动生成路由，同时支持vue+md语法
│  │  guide.md
│  │  README.md                         //默认是首页                                   
│  └─.vuepress                         //vuepress框架自带配置文件
│      │  app.styl                      //框架样式文件,vuepress框架集成了，可以在/yarn.lock 文件查看到依赖
│      │  config.js                     //可以配置导航相关信息，KWD相关信息
│      │  enhanceApp.js                 //vuepress框架入口文件，功能：引入依赖库，引入样式，全局注册组件，为原型添加新方法
│      │
│      └─public                        //资源文件夹
│              hero.png
│
├─scripts                               //脚本命令：导出指定的icon图标到文件夹中
│  │  config.js
│  │  extractIcons.js                   //导出icon   
│  │  extractMobileIcons.js             //导出mobile icon
│  │  extractStandaloneIcons.js         //导出独立的icon
│  │  generateFonts.js                  //生成字体，主要通过webfonts-generator 库来把svg文件转成font字体文件
│  │
│  └─templates                         //build之后，导出css文件的模板，内置变量
│          anticons.hbs
│
└─src                                   //主要目录工程文件夹
    │  anticons.json                     //svg名称，unicode，id对应表
    │  index.js                          //导出所有的svg文件
    │
    ├─mobile                            //移动端独立的svg文件夹
    │  │  anticons.json
    │  │  index.js
    │  │
    │  └─svg                          //移动端所的svg文件
    │          check.svg
    │
    ├─standalone
    └─svg                             //所有svg文件列表
            alipay.svg
    
```
