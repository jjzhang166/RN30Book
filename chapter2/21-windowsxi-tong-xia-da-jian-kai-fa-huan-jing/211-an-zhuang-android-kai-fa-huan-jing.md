##2.1.1 安装 Android 开发环境

###安装JDK

搭建 Android 开发环境需要 Java Development Kit [JDK] 1.8或更高版本。你可以在命令行中输入 javac -version 来查看你当前安装的JDK版本。如果版本不合要求，则可以到官网上下载或百度搜索安装包。

JDK官网下载地址：
http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

###安装Android Studio

React Native目前需要 Android Studio2.0 或更高版本。Android Studio包含了运行和测试 React Native 应用所需的 Android SDK 和模拟器。

下载地址：https://developer.android.google.cn/studio/index.html

第一次安装的时候，选择 Custom 选项如图2-1所示

![](/assets/图2-1.png)图2-1自定义安装

勾选以下选项：
* Android SDK
* Android SDK Platform
* Performance (Intel ® HAXM)
* Android Virtual Device

注意:
* 除非特别注明，请不要改动安装过程中的选项。比如Android Studio默认安装了 Android Support Repository，而这也是React Native必须的（否则在react-native run-android 时会报 appcompat-v7 包找不到的错误）。
* 确定所有安装都勾选了，尤其是 Android SDK 和 Android Device Emulator。

Android Studio 默认安装最新的 SDK，但是 React Native 需要安装 Android 6.0 (Marshmallow) SDK 。
在Android Studio的欢迎界面中选择Configure | SDK Manager，如图2-2所示。或者进入 Android Studio后， 选择"Preferences" 菜单依次进入 Appearance & Behavior → System Settings → Android SDK。
![](/assets/图2-2.png)图2-2 选择SDK Manager

如图2-3所示，勾选 "Show Package Details" 确保以下选项被勾选：
* Google APIs
* Android SDK Platform 23
* Intel x86 Atom_64 System Image
* Google APIs Intel x86 Atom_64 System Image

![](/assets/图2-3.png)图2-3 安装SDK23

然后点击 SDK Tools选项卡，继续勾选"Show Package Details"，展开"Android SDK Build Tools" 确保"Android SDK Build-Tools 23.0.1" 被选中，如图2-4所示。
![](/assets/图2-4.png) 图2-4 安装SDK Build Tools

都勾选好了，点击 "Apply" 按钮开始安装。
