##2.2.2 搭建Android调试环境

Mac系统自带 JDK 不需要像 Windows 操作系统一样额外安装，关于Android Studio 和 Android SDK 的安装参考2.1.2章节。

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

###测试安装 
参考2.1.3章节。