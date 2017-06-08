#2.4 熟悉项目

以初始化的 RN30Code 项目为例，我们来简单熟悉下项目。


##2.4.1 认识项目结构
我们主要关心和开发密切的项目结构。

```
RN30Code
    |-- android
    |-- ios
    |-- node_modules
    |-- index.android.js
    |-- index.ios.js
    |-- package.json

```
* android 和 ios 对应的就是原生代码，分别可以通过 Android Studio 和 Xcode打开，如果不涉及到混合开发，一般用不到。
* node_modules 里面内容非常多，这是我们项目依赖文件。
* package.json 是项目说明文件。里面可以看到
 ```
 ...
 "dependencies": {
	"react": "16.0.0-alpha.6",
	"react-native": "0.44.2"
 },
 ...
 ```
 这个代码的是当前项目的依赖。


* index.ios.js 和 index.android.js 分别是 iOS/Android 程序入口文件，当我们调用 "react native run ios/android" 命令时，就会执行该文件。在实际React Native项目中经常会看到 xxx.ios.js 或者 xxx.android.js，这表明该文件不是两个平台通用的文件，只针对其中一个平台。

##2.4.2 熟悉代码





