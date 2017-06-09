##1.5.1 Atom＋Nuclide

Atom 是由 Github 打造的下一代编程开发利器，支持 Windows、Mac、Linux 三大桌面平台，免费且开源。Atom 支持各种编程语言的代码高亮，同时具备强大的代码补全功能，能够极大的提高编程效率，Atom 本质上是一个文本编辑器，而不是一个 IDE，因此在用来开发 React Native 时需要配合 Nuclide 一起使用。

Nuclide 是 Facebook 基于 Atom 的基础上开发的一个插件 IDE，可以用来开发 React Native，iOS 和 Web 应用，Nuclide 对 Windows 平台并不是友好，支持 Mac OS X 和 Linux平台。

Nuclide 内置了对 React Native 的支持，包括代码自动补全，代码诊断等。

###安装Atom

Atom下载地址: https://atom.io/
这个没什么难的，解压缩之后，把Atom从下载目录，拖到应用程序目录即可。

###安装Nuclide
这里，我们在Atom中，用图形化界面来安装。
点击菜单栏：Atom->Preferences 
然后，在Install Packets的输入框中，输入 nuclide，出现的第一个就是我们想要安装的，点击 install 。如图2-9所示
![](/assets/图2-9.png) 图2-9 安装Nuclide

安装完之后，重新进入 Atom 点击 Add Project Folder 打开 RN 项目工程即可开始开发。 