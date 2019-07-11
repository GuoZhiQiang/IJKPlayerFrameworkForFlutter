### 背景
在开发 flutter 视频播放器组件时，ijkplayer 没有提供 PixelBuffer，导致播放器白屏，只有声音没有画面输出。
因此对 ijkplayer 做了修改，以满足需求，并打包成 framework 可以集成使用

### 使用
1. 根据 ijkplayer 官网的介绍 导入依赖的库;
2. 为 `IJKFFMoviePlayerController` 提供了 `framePixelbuffer` api :

```
- (CVPixelBufferRef)copyPixelBuffer {
    return [(IJKFFMoviePlayerController *)_player framePixelbuffer];
}
```
`copyPixelBuffer` 可以换成你自定的方法名。

### Note
使用时，播放器依赖的库，要安装 ijkplayer 官网的介绍进行添加

### 下载地址
https://pan.baidu.com/s/1P7NAS3eCPKEmq5h6PkxZxw  github 有包大小限制，放在了网盘上，解压缩使用。
