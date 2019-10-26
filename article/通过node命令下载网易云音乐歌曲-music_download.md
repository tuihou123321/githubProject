# 通过node命令下载网易云音乐歌曲-music_download


## 项目说明 
通过node命令行下载网易云音乐中的歌曲、歌词文件到本地；


**项目地址**：[https://github.com/8qewt/music_download](https://github.com/8qewt/music_download)



### 技术栈
- node    //通过node搭建服务，并通过fs模块下载
- iconv-lite    //解决node中文支持的问题


### 启动
```javascript
node main.js  https://music.163.com/#/song?id=1363948882     //下载指定音乐，歌词文件到本地
node main.js -l  https://music.163.com/#/song?id=1363948882     //下载指定音乐到本地
```

**更多参数**：

必选参数对长短选项同时适用。
- -a, --download-max-count  并行下载的最高数量，默认为5
- -c, --lyric-charset       设置保存歌词文件的字符集
- -d, --translate-offset    将翻译与歌词放在不同的行中，并设置翻译的偏移度，单位为秒
- -f, --filename_format     设置文件名与歌词的格式字符串，可用的替换字符串：name：歌名 subname：歌曲附加名 artist：艺术家
- -k, --translate-format    设置下载歌词的格式字符串，可用的替换字符串：original：原歌词 translate：翻译（将翻译与歌词放在同一行）
- -l, --lyric-disable       不保存歌词文件
- -m, --lyric-no-translate  不使用歌词翻译
- -n, --norename            禁用文件名替换，保持原有的文件名，即使包含/，可能会造成错误
- -r, --lyric-compress      启用歌词压缩，将重复的歌词合并为一行，可能会造成不兼容
- -w, --windowsize          将下载的文件名中\/:*?"<>|这些符号替换为空格



### 目录结构

```$xslt

│  asyncControl.js                //
│  lyric.js                       //
│  main.js                        // 入口文件
│  package.json                   //
│  parsers.js                     //
│  stringReplacer.js              //
│                                 
├─netease                         //
│      playlist.js                //
│      song.js                    //
│                                 
└─test                            //
        asyncTest.js              //
        stringReplaceTest.js      //

```
