#1.2 React Native的特点

React Native是基于React实现的跨平台开发框架，既拥有Native (原生)的良好人机交互体验，又保留了 React 框架的开发效率。

##1.2.1 一次学习,随处编写
因为 Android,iOS 俩平台的交互方式有些差异，但是开发思路基本一致，所以React Native小组并没有狂妄的喊出 "Write once，run anywhere (一次编写，到处运行)" ，而是提出了 “Learn once，write anywhere (一次学习到处编写)”。没错，就是明确告诉你学一次就可以同时开发两个平台了。这一点可一直都是移动端开发人员和创业公司的理想。

##1.2.2 React Native运行机制
React Native 使用 JSX 语法开发，所谓 JSX，是 JavaScript 的语法扩展，让我们在 JavaScript 中可以编写类似 HTML 一样的代码。React Native 利用 JavascriptCore 引擎对 JS 文件进行解析，并利用 Bridge 映射到对应的 Native 方法和 UI 控件。得到的效果是：

1. 同样的 React Native 代码，下发到 Android 和 iOS 不同平台中，会自动调用对应 Native 的 UI 控件，保证了各平台用户体验的连贯性； 
2. 开发者就算是移动端小白，只要有React Native基础，通过编写一套React Native 端代码就可以同时完成 Android 与 iOS App 的开发；
3. 由于可以利用 JS bundle 同时下发数据和业务逻辑，这意味着你可以像 Web 开发一样，实时迭代更新你的移动端 App，无需在了解各自平台的热修复技术。

##1.2.3 React Native的扩展性

React Native扩展性还非常强，可以直接调用原生代码，使用原生的组件，避免了重复制作轮子：
1. Native Modules，这是 React Native 强大的一个扩展性，允许你通过简单的代码就能实现在 JS 里直接调用你自己的原生方法；
2.Native Components，如果你自己实现了一些复杂的原生UI组件，而这些组件尚未被 React Native 支持，你可以利用 Native Components 快速把原生组件引入到 React Native 中并可以直接在 JS 里更新这些组件的状态。
3. 同一个项目中，React Native开发的界面和原生代码开发的界面可以丝滑自如的切换，我们完全可以在现有的原生项目中集成 RN 来开发一些特定的功能。

