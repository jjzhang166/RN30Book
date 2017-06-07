##2.1.1 安装依赖软件

React Native 前需要安装 Node，Python2。

###安装Chocolatey
Chocolatey并不是 React Native必须的软件，它是一个Windows上的包管理器，只需要一条简单的命令，就可以完成软件的安装、更新和卸载等操作。使用这个软件可以方便的安装 Node 和 Python2。别单独去对应的官方网站下载安装即可。

以管理员的身份来运行命令提示符窗口，在命令行中输入:
```py
@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin
```
Chocolatey 的网站可能在国内访问困难，导致上述安装命令无法正常完成。 如果你实在装不上这个工具，也不要紧。所需的 Python2 和 Node 你可以分别单独去对应的官方网站下载安装即可。

###安装Python2
安装完 Chocolatey，可以在命令提示符窗口，使用Chocolatey来安装Python2，在命令行中输入：
```py
choco install python2
```
目前Python最新版本是3.X ，但是并不兼容 Python2。目前React Native 不支持 Python 3版本。

###安装Node
使用Chocolatey来安装Node
```py
choco install nodejs.install
```
询问是否允许脚本时，输入“Y” 并按下Enter键。

安装完 Node 后，多了一个 npm 指令，npm 是 node 的包管理和分发工具，可以通过 npm 构建React Native 项目。安装完 node 后建议设置npm 国内镜像以加速后面的过程。执行命令：
```py
npm config set registry https://registry.npm.taobao.org --global
npm config set disturl https://npm.taobao.org/dist --global
```
###安装Yarn、React Native的命令行工具（react-native-cli）
Yarn 是 Facebook 提供的替代 npm 的工具，可以加速 node 模块的下载。React Native 的命令行工具用于执行创建、初始化、更新项目、运行打包服务（packager）等任务。
执行命令:
```py
npm install -g yarn react-native-cli
```
安装完 yarn 后同理也要设置镜像源：
```py
yarn config set registry https://registry.npm.taobao.org --global
yarn config set disturl https://npm.taobao.org/dist --global
```

