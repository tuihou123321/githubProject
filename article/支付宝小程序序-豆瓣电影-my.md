# 支付宝小程序序-豆瓣电影-my


## 项目说明 
支付宝小程序原生语言开发的豆瓣电影项目
相关文件介绍
- css,wxcss->acss
- 模板文件(jsx,vue)->axml

支付宝小程序开放的接口

- 生命周期事件函数
- 界面操作
- 多媒体库
- 缓存
- 文件
- 位置
- 网络
- 设备
- 数据安全
- 分享
- 自定义通用菜单


**项目地址**：[https://github.com/openfe-openfe/my](https://github.com/openfe-openfe/my)

**支付宝小程序接口文档**：[https://docs.alipay.com/mini/api/vzt2xm](https://docs.alipay.com/mini/api/vzt2xm)


## 支付宝小程序对象

项目中使用的my相关api:
- navigateTo  //路由跳转 
- httpRequest //http请求
- previewImage  //多图预览
- setNavigationBar //设置标题
- ...


## 目录结构

```$xslt

│  app.acss                          //顶层样式文件
│  app.js                            //app全局数据配置
│  app.json                          //支付宝小程序配置文件（路由，全局基本样式-背景颜色/标题文字/标题字颜色/）                              
│                              
├─images                            //图片资源  
│                                    
├─pages                             //项目文件夹
│  │                                
│  ├─index                         //路由入口一
│  │      index.acss                //支付宝小程序样式文件
│  │      index.axml                //支付宝小程序模板文件（只做数据的渲染）
│  │      index.js                  //路由的入口文件
│  │      index.json                //*
│                                    
└─utils                             //工具类

```
