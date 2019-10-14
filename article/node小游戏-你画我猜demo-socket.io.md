## node小游戏-你画我猜demo-socket.io

### 项目说明 

简易你画我猜小游戏

**项目地址**：[https://github.com/Wscats/socket.io](https://github.com/Wscats/socket.io)

### 技术栈

- node         //在node层http服务，并保持长链接
- socket.io    //实时数据链接
- vue          //客户端逻辑处理


### 启动
```javascript
npm i socket.io
node index
```

http服务下打开： index.html

**画图窗口（粉红色）**：
功能：
- 设置关键词
- 开始画图
- 清空画布
- 显示对方是否回答正常的提示

**猜图窗口（淡蓝色）**：
- 实时显示画图的内容
- 发送答案+提示答案是否正常


**技术点**
- [x] socket.io 数据实时同步


### 目录结构

```$xslt

│  index.html          //入口文件，可以切换用户状态
│  index.js            //node启动文件
│  UDrawIGuess.html    //两种状态合在一个页面上
│                      
├─chat                 //
│      chat.html       //
│      chat.js         //
│                      
└─js                   //util js库
        socket.js      //socket.js库
        vue.js         //vue.js库

```
