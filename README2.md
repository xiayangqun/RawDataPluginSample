### 替换头文件
本插件的编译依赖 Agora Rtc 的 C++ 头文件。所以请务必要保持住 C++头文件的一致性。比如说你现在使用的是Unity SDK 4.5.2.6。那么你需要为这个 4.5.2.6 的 Unity SDK编译插件的时候。就去
https://github.com/AgoraIO-Extensions/terra_shared_configs/tree/main/headers
去下载对应版本的 SDK C++头文件。复制到 include 文件夹下去替换。

非常有可能日后Unity SDK 做了升级，但是这个插件没有使用升级后的C++头文件重新编译。直接导致内存错位。崩了。

非常有可能日后Unity SDK 做了升级，但是这个插件没有使用升级后的C++头文件重新编译。直接导致内存错位。崩了。

非常有可能日后Unity SDK 做了升级，但是这个插件没有使用升级后的C++头文件重新编译。直接导致内存错位。崩了。

### 填写逻辑代码
打开cxx/AudioFrameObserver.cpp文件去
putAudioFrameData(void* buffer, int length) 函数里缓存数据
onPlaybackAudioFrame 函数里去填充数据

### 编译动态库
1. README.md文件里写了怎么编译。怎么把生成的动态库拷贝到Unity Rtc SDK对应的目录地方
2. C++的部分这就改完了，很简单


