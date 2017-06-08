##2.3.3 Sublime Text 3

Sublime Text 3 是一款广泛使用的代码编辑器，支持 Windows、Mac OS X、Linux 三大桌面平台，它是付费应用，但目前可以无限期的试用。它支持多种编程语言的语法高亮、拥有优秀的代码自动完成功能，还拥有代码片段（Snippet ）的功能，可以将常用的代码片段保存起来，在需要时随时调用，极大的提高编程效率。

Sublime Text 3 强大功能的支撑在于它的插件机制，通过 Package Control 功能，开发者可以安装各种需要的插件，默认情况下，Sublime Text 3 没有集成 Package Control，我们需要自己安装。

###安装Package Control
打开Sublime Text 3，Windows系统选择 Tools 菜单项“Install Package Conrol”。Mac 系统选择 Tools 菜单项的 “Command Palette ..” 再输入“Package Conrol”， 然后选择 “Install Package”

安装完成后，可以在 Preferences 菜单下找到 Package Settings 和 Package Control 两个子菜单。

###安装相关插件
在 Sublime Text 3 中，React Native 开发相关的插件主要有：
* babel-sublime：支持 Javascript，ES6 和 JSX 语法高亮
* react-native-snippets：支持 React Native 代码片段

在 Package Control 对话框中选择 Package Control:Install Packages 并在弹出的对话框中输入 Babel，即可找到 babel-sublime，如图2-11。
![](/assets/图2-11.png)图2-11 安装Babel

react-native-snippets 插件同样通过 Package Control 进行安装，在 Install Package 对话框中搜索 react-native-snippets 安装即可。