##1.4.2 Mac系统下 React Native 开发环境搭建 

Mac 系统下安装完 React Native开发环境既可以调试 Android 程序又可以调试 iOS 程序。

###安装Xcode
首先将苹果操作系统升级到最新版本，然后可以通过 App Store 安装最新版本的 Xcode。这一步骤会同时安装Xcode IDE和Xcode的命令行工具。

###安装Homebrew
Homebrew是Mac系统的包管理器，用于安装NodeJS和一些其他必需的工具软件。在终端中执行命令。
```py
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
：在 Max OS X 10.11（El Capitan) 版本中，Homebrew 在安装软件时可能会碰到 /usr/local 目录不可写的权限问题。可以使用下面的命令修复：
```py
sudo chown -R `whoami` /usr/local
```

###安装Node
使用 Homebrew 来安装 Node。
```py
brew install node
```
安装完 Node 后，多了一个 npm 指令，npm 是 node 的包管理和分发工具，可以通过 npm 构建React Native 项目。安装完 node 后建议设置npm 国内镜像以加速后面的过程。执行命令：
```py
npm config set registry https://registry.npm.taobao.org --global
npm config set disturl https://npm.taobao.org/dist --global
```
###安装Yarn、React Native的命令行工具（react-native-cli）
Yarn 是Facebook提供的替代npm的工具，可以加速 Node 模块的下载。React Native 的命令行工具用于执行创建、初始化、更新项目、运行打包服务（packager）等任务。
```
npm install -g yarn react-native-cli
```
安装完yarn后同理也要设置镜像源：
```
yarn config set registry https://registry.npm.taobao.org --global
yarn config set disturl https://npm.taobao.org/dist --global
```
###Watchman
Watchman是由Facebook提供的监视文件系统变更的工具。安装此工具可以提高开发时的性能（packager可以快速捕捉文件的变化从而实现实时刷新）。
通过 Homebrew 安装
```
brew install watchman
```

###测试安装

安装完成后，激动人心的时刻来的，我们可以在命令行中创建 React Native 项目了。
执行命令：
```py
react-native init RNCode30
```
上述命令，会初始化一个名叫“RNCode30”的项目。该命令需要执行一段时间。
进入项目中，运行 iOS 程序，执行如下命令。
```gradle
cd RNCode30
react-native run-ios
```
如果能够正常运行，显示图2-8所示内容，表示环境安装成功。

![](/assets/图2-8.png)图2-8 测试运行

运行的时候会新打开一个命令窗口，这其实是打开调试环境的服务，如果不小心关闭了，需要执行 "react-native start" 重新打开。
###修改项目

现在你已经成功运行了项目，我们可以开始尝试动手改一改了:
1. 使用你喜欢的文本编辑器打开index.ios.js并随便改上几行;
2. 在iOS Emulator中按下⌘-R就可以刷新APP并看到你的最新修改。

###搭建Android开发环境
Mac系统自带 JDK 不需要像 Windows 操作系统一样额外安装，关于Android Studio 和 Android SDK 的安装参考1.4.1章节。

###ANDROID_HOME环境变量

在 Mac 系统中环境变量和Windows系统的配置方式也不一样。
确保 ANDROID_HOME 环境变量正确地指向了你安装的Android SDK的路径。具体的做法是把下面的命令加入到`~/.bash_profile`文件中。(`~`表示用户目录，即`/Users/你的用户名/`，而小数点开头的文件在 Finder 中是隐藏的，并且这个文件有可能并不存在。请在终端下使用vi ~/.bash_profile命令创建或编辑。

```
export ANDROID_HOME=~/Library/Android/sdk
```
然后使用下列命令使其立即生效（否则重启后才生效）：
```
source ~/.bash_profile
```
可以使用`echo $ANDROID_HOME`检查此变量是否已正确设置。


