# markdown静态站点生成工具-ydoc

## 项目说明 
去哪儿团队开源的一个文档生成工具，
通过ydoc脚手架命令把markdown/html文件打包成静态站点,支持移动端；

**项目地址**：[https://github.com/YMFE/ydoc](https://github.com/YMFE/ydoc)

### 支持各类插件：
- 在页面中引入js/css文件
- 全局搜索功能
- 根据代码结构和注释，生成react组件文档，基于react-styleguide
- 快速复制markdown生成页面的代码片段
- 点击markdown页面图片可以浏览原图
- 在页面尾巴添加‘编辑此页面’的链接到github/gitlab等页面
- 评论插件


## 使用说明

```
 ydoc init   //生成架子
 ydoc build  //自动打包 docs文件夹下所有文件，并生成 _site目录
 ydoc server  //启动静态服务，启动docs目录下的文档，可实时看到内容变化
```
