##2.1.3 测试安装

安装完成后，激动人心的时刻来的，我们可以在命令行中创建 React Native 项目了。
执行命令：
```py
react-native init RNCode30
```
上述命令，会初始化一个名叫“RNCode30”的项目。该命令需要一段时间。请不要在命令行默认的System32目录中init项目，会有各种权限限制导致不能运行。
进入项目中，运行 Android 程序，执行如下命令。
```gradle
cd RNCode30
react-native run-android
```
如果能够正常运行，显示图2-7所示内容，表示环境安装成功。

![](/assets/图2-7.png)图2-7 测试运行

###修改项目

现在你已经成功运行了项目，我们可以开始尝试动手改一改了:
1. 使用你喜欢的文本编辑器打开index.android.js并随便改上几行;
2. 按两下R键，或是用Menu键（快键键ctrl+M）打开开发者菜单，然后选择 Reload JS 就可以看到你的最新修改。