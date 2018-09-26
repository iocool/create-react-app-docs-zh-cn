# 用户指南

英文版 [用户指南](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md)

该项目是使用 [Create React App](https://github.com/facebookincubator/create-react-app) 来引导的.

有关如何执行一些常见的任务信息,可以在下面的列表中找到. <br>
查看 [此处](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md) 可以找到本用户指南的最新版本(英文原版).

## 目录

- [更新到最新版](#更新到最新版)
- [发送反馈](#发送反馈)
- [文件结构](#文件结构)
- [script配置信息](#script配置信息)
  - [npm start](#npm-start)
  - [npm test](#npm-test)
  - [npm run build](#npm-run-build)
  - [npm run eject](#npm-run-eject)
- [浏览器支持](#浏览器支持)
- [支持的语法特点及 Polyfill](#支持的语法特点及-polyfill)
- [编辑器中的语法高亮](#编辑器中的语法高亮)
- [编辑器中 Lint 信息显示](#编辑器中-lint-信息显示)
- [编辑器中进行调试](#编辑器中进行调试)
- [代码自动格式化](#代码自动格式化)
- [修改页面标题 `<title>`](#修改页面标题)
- [安装依赖项](#安装依赖项)
- [组件引入](#组件引入)
- [代码拆分](#代码拆分)
- [样式添加](#样式添加)
- [CSS 处理](#css处理)
- [添加CSS 预处理器 (如Sass, Less 等)](#添加-css-预处理器如-sass-less-等)
- [图像, 字体和文件的添加](#图像字体和文件的添加)
- [`public` 文件夹的使用](#public-文件夹的使用)
  - [HTML 修改](#html修改)
  - [Adding Assets Outside of the Module System](#adding-assets-outside-of-the-module-system)
  - [什么时候该使用 `public` 文件夹](#什么时候该使用-public-文件夹)
- [全局变量的使用](#全局变量的使用)
- [添加 Bootstrap](#添加-bootstrap)
  - [使用自定义主题](#使用自定义主题)
- [添加 Flow](#添加-flow)
- [添加路由 Router](#添加路由-router)
- [添加自定义环境变量](#添加自定义环境变量)
  - [在 HTML 中引用环境变量](#在-html-中引用环境变量)
  - [在 Shell 中添加临时环境变量](#在-shell-中添加临时环境变量)
  - [在 `.env` 文件中添加开发环境的变量](#在-env-文件中添加开发环境的变量)
- [能否使用修饰器](#能否使用修饰器)
- [使用 AJAX 请求数据](#使用-ajax-请求数据)
- [与后端的 API 集成](#与后端的-api-集成)
  - [Node](#node)
  - [Ruby on Rails](#ruby-on-rails)
- [在开发中使用代理 API 请求](#在开发中使用代理-api-请求)
  - [配置代理后出现 Invalid Host Header 错误](#配置代理后出现-invalid-host-header-错误)
  - [手动配置代理](#手动配置代理)
  - [配置 WebSocket 代理](#配置-websocket-代理)
- [在开发中使用 HTTPS](#在开发中使用-https)
- [在服务器上生成动态 `<meta>` 标签](#在服务器上生成动态-meta-标签)
- [预加载静态 HTML 文件](#预加载静态-html-文件)
- [在服务器端添加数据到页面](#在服务器端添加数据到页面)
- [运行测试 TEST](#运行测试-test)
  - [文件命名约定](#文件命名约定)
  - [命令行界面](#命令行界面)
  - [版本控制集成](#版本控制集成)
  - [编写一个测试](#编写一个测试)
  - [测试组件](#测试组件)
  - [使用第三方 Assertion 库](#使用第三方-assertion-库)
  - [初始化测试环境](#初始化测试环境)
  - [关注及排除测试](#关注及排除测试)
  - [覆盖率报告](#覆盖率报告)
  - [持续集成](#持续集成)
  - [禁用 jsdom](#禁用-jsdom)
  - [快照测试](#快照测试)
  - [编辑器集成](#编辑器集成)
- [调试测试 TEST](#调试测试-test)
  - [在 Chrome 中调试测试](#在-chrome-中调试测试)
  - [在 Visual Studio Code 中调试测试](#在-visual-studio-code-中调试测试)
- [开发独立组件 Components](#开发独立组件-components)
  - [Storybook 入门](#storybook-入门)
  - [Styleguidist 入门](#styleguidist-入门)
- [发布组件 Components 到 npm](#发布组件-components-到-npm)
- [开发渐进式网页应用 (PWA,即 Progressive Web App)](#开发渐进式网页应用-pwa即-progressive-web-app)
  - [Opting Out of Caching](#opting-out-of-caching)
  - [优先考虑离线](#优先考虑离线)
  - [PWA(Progressive Web App) 元数据](#pwaprogressive-web-app-元数据)
- [对打包文件大小的分析](#对打包文件大小的分析)
- [部署](#部署)
  - [静态服务器](#静态服务器)
  - [其他方案](#其他方案)
  - [使用客户端路由的服务端配置](#使用客户端路由的服务端配置)
  - [在构建打包时相对路径的设置](#在构建打包时相对路径的设置)
  - [Azure](#azure)
  - [Firebase](#firebase)
  - [GitHub 页面](#github-页面)
  - [Heroku](#heroku)
  - [Netlify](#netlify)
  - [Now](#now)
  - [S3 和 CloudFront](#s3-和-cloudfront)
  - [Surge](#surge)
- [高级配置](#高级配置)
- [问题排查](#问题排查)
  - [`npm start` 后检测不到变化](#npm-start-后检测不到变化)
  - [`npm test` 在 macOS Sierra 运行被挂起](#npm-test-在-macos-sierra-运行被挂起)
  - [`npm run build` 提前退出](#npm-run-build-提前退出)
  - [`npm run build` 在 Heroku 执行失败](#npm-run-build-在-Heroku-执行失败)
  - [`npm run build` fails to minify](#npm-run-build-fails-to-minify)
  - [Moment.js 缺少语言支持](#moment.js-缺少语言支持)
- [Eject 替代方案](#eject-替代方案)
- [您觉得不足之处](#您觉得不足之处)

## 更新到最新版

Create React App 分为两个包:

* `create-react-app` 是一个全局的命令行程序,可用来创建新项目.
* `react-scripts` 是用来生成在具体项目的第三方依赖项及配置.

通常情况下,我们几乎不用去更新 `create-react-app`,因为 `react-scripts` 会承担起相应的安装及配置操作.

当运行 `create-react-app`时, `react-scripts` 始终会使用最新版本来创建项目,因此在项目创建时,将自动获取并应用最新特性及一些改进,更新等.

如要更新现有 `react-scripts` 的版本,请先浏览 [更新日志](https://github.com/facebookincubator/create-react-app/blob/master/CHANGELOG.md) ,找到你当前使用的版本,参照你对应的版本更新说明进行更新操作(如果你不清楚你所使用的版本,可以查看本地的 `package.json` 文件,找到版本信息).

大多数情况下,可以直接修改 `package.json` 文件中 `reac-scripts` 的版本再执行 `npm install` ,但是不建议这样做,可能会有一些潜在的风险,具体也可以查看 [更新日志](https://github.com/facebookincubator/create-react-app/blob/master/CHANGELOG.md) .

我们尽可能对项目不做重大调整,以便用户顺利的升级 `react-scripts`.

## 发送反馈

如有问题,可随时提交您的 [反馈](https://github.com/facebookincubator/create-react-app/issues) .

## 文件结构

当项目创建后,项目目录如下所示:

```
my-app/
  README.md
  node_modules/
  package.json
  public/
    index.html
    favicon.ico
  src/
    App.css
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
```

在构建项目( `build` )时,下面的文件 **必须存在并保证文件名及路径与下面要求一致**

* `public/index.html` 为模板页面;
* `src/index.js` 为 JavaScript 入口.

对于其他文件,可以进行删除及重命名.

也可以在 `src` 目录中创建子目录.为了保证最快的代码重构, Webpack 只会处理在 `src` 目录中的文件. <br>
所以需要把 **所有的 JS 和 CSS 文件** 放在 `src` 目录中,否则 Webpack 不会识别处理.

只有 `public` 目录下的文件才会被 `public/index.html` 引用. <br>
请阅读下面有关使用 JavaScript 和 HTML 静态资源的说明.

当然也可以创建多个与 `public` 同级的顶级目录. <br>
但这些目录不会包含在构建的项目中,我们可以使用这些目录存放项目说明文档.


## script配置信息

在项目目录中,可以运行以下命令:

### `npm start`

在开发模式 (development mode) 下运行应用.<br>
在浏览器中访问 [http://localhost:3000](http://localhost:3000) ,可以查看页面.

如果代码有修改,将自动重新加载页面.<br>
构建过程中,出现的错误信息和 lint 警告信息会显示在控制台中.

### `npm test`

在交互模式下运行测试监测 (test wathcer) .<br>
更多信息,请参阅 [运行测试 TEST](#运行测试-test) .

### `npm run build`

在构建 (build) 模式下,会在 `build` 文件目录中生成用以生产环境的应用.<br>
build 模式将会合理的将 react 项目打包,并进行足够的优化,以保证在生产环境中获得最佳的性能.

build 模式会尽可能的压缩打包文件,并在打包的文件名中加入文件内容的 hash.<br>
到这里,应用程序已经可以进行部署了.

查看更多关于 [部署](#部署) 的信息.

### `npm run eject`

注意: 该命令为单向操作,即 **只能运行一次** ` eject` ,一旦运行就无法撤回

如果对于构建工具和配置项不满意,可以随时运行 `eject` 命令.这个命令将会从项目中移除单个构建的依赖项.

取而代之的是,所有的配置文件和项目依赖(Webpack, Babel, ESLint 等)都会被导入到我们的项目中,这样我们就可以完全自主进行配置了.此时除了 `eject` 命令,其余的命令依然可用.

其实 `eject` 没有必要去使用,对于中小型应用来说,默认的配置项已经足够好用了,提供此功能是为了方便在一些特定的情况下进行自定义使用.

## 浏览器支持

默认情况下,生成的项目使用最新版本的 React.

更多有关支持的浏览器信息,请参阅 [React文档](https://reactjs.org/docs/react-dom.html#browser-support)

## 支持的语法特点及 Polyfill

支持最新的 JavaScript 标准的超集. <br>
除了 [ES6](https://github.com/lukehoban/es6features) 语法功能外,还支持:

* [指数运算符](https://github.com/rwaldron/exponentiation-operator) (ES2016).
* [Async/await](https://github.com/tc39/ecmascript-asyncawait) (ES2017).
* [Object Rest/Spread Properties](https://github.com/sebmarkbage/ecmascript-rest-spread) (第 3 阶段提案).
* [Dynamic import()](https://github.com/tc39/proposal-dynamic-import) (第 3 阶段提案)
* [Class Fields and Static Properties](https://github.com/tc39/proposal-class-public-fields) (第 3 阶段提案的一部分).
* [JSX](https://facebook.github.io/react/docs/introducing-jsx.html) 和 [Flow](https://flowtype.org/) 语法.

想要了解更多信息,可以查看[这里](https://babeljs.io/docs/plugins/#presets-stage-x-experimental-presets-).

我们建议谨慎使用这些实验性特型,但 Facebook 在产品代码中已较多使用这些新特性,如果这些提案中的特性以后有所变化,我们也会提供 [codemods](https://medium.com/@cpojer/effective-javascript-codemods-5a6686bb46fb).

请注意,项目中 **仅包含 ES6 的少量 [polyfills](https://en.wikipedia.org/wiki/Polyfill)** .


* [`Object.assign()`](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Object/assign) 使用 [`object-assign`](https://github.com/sindresorhus/object-assign).
* [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) 使用 [`promise`](https://github.com/then/promise).
* [`fetch()`](https://developer.mozilla.org/en/docs/Web/API/Fetch_API) 使用 [`whatwg-fetch`](https://github.com/github/fetch).

如果需要其他 **运行时支持** 的 ES6+ 功能(如 `Array.from()` 或 `Symbol`) ,需要自行手动添加相应的 polyfills ,或者项目运行目标浏览器已经支持这些特性.

另外还需要注意的是,使用较新的语法功能(如 `for...of` 或 `[...nonArrayValue]` ) 导致 Babel 生成依赖于 ES6 运行时的功能代码,如果不添加 polyfills ,代码运行可能会出错.如有疑问,可以使用 [Babel REPL](https://babeljs.io/repl/) 查看所有的特定的语法编译内容.

## 编辑器中的语法高亮

如需要在编辑器中配置语法高亮,请查看 [有关 Babel 的文档](https://babeljs.io/docs/editors) ,并按照文档说明进行操作配置.

## 编辑器中 Lint 信息显示

>注意: 此功能在 `react-scripts@0.2.0` 或更高版本中可用.<br>
>npm 版本在 3 或更高版本.

一些编辑器,包括 Sublime Text, Atom, 和 Visual Studio Code,都提供了 ESLint 插件.

编辑器的 Lint (代码风格检查)插件并不是必须的.我们同样可以在终端或浏览器控制台中,看到 lint 信息.如果希望在编辑器中就可以显示 lint 信息,则需要进行相应的安装配置等.

首先我们需要在在编辑器中安装 ESLint 插件.然后在项目的根目录下,创建一个名为 `.eslintrc` 的文件,文件内容如下:

```json
{
  "extends": "react-app"
}
```

此时,编辑器中应该会显示 lint 警告信息.

请注意,即使进一步配置 `.eslintrc` 文件,这些修改也 **只会影响编辑器集成** ,不会对终端和浏览器中的 lint 信息显示产生影响,因为 Create React App 本身提供了一些常见的错误检测.

如果想在项目中执行代码格式化操作,可以考虑使用 [Prettier](https://github.com/jlongster/prettier) 来替代 ESLint.

## 编辑器中进行调试

**目前只有 [Visual Studio Code](https://code.visualstudio.com) 和 [WebStorm](https://www.jetbrains.com/webstorm/) 支持该功能.**

Visual Studio Code 和 WebStorm 支持开箱即用,可直接调试 Create React App 应用.这使得作为开发者而言,直接在编辑器中就可以进行代码的编写及调试.最重要的是,能够拥有连续的开发工作流,使得在开发过程中,不必在多个工具窗口之间来回切换.

### Visual Studio Code

需要安装最新版本的 [VS Code](https://code.visualstudio.com) 和 VS Code 的扩展 [Chrome Debugger Extension](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)

然后将以下代码块添加到 `launch.json` 文件中,并将该文件放在应用根目录中的 `.vscode` 文件夹中.

```json
{
  "version": "0.2.0",
  "configurations": [{
    "name": "Chrome",
    "type": "chrome",
    "request": "launch",
    "url": "http://localhost:3000",
    "webRoot": "${workspaceRoot}/src",
    "sourceMapPathOverrides": {
      "webpack:///src/*": "${webRoot}/*"
    }
  }]
}
```
>注意: 如果通过 [HOST 或 PORT 环境变量](#高级配置) 进行了调整,则 url 需要修改.

通过运行 `npm start` 来启动应用,在 VS Code 中,使用 `F5` 快捷键或者点击绿色的调试按钮进行调试.之后,可以继续进行代码编写,设置断点,修改代码等操作,然后可以继续通过编辑器调试编辑后的代码.

在 VS Code 调试过程中出现问题,可参阅 [故障排除指南](https://github.com/Microsoft/vscode-chrome-debug/blob/master/README.md#troubleshooting)

### WebStorm

需要安装 [WebStorm](https://www.jetbrains.com/webstorm/) 和 Chrome 扩展程序 [JetBrains IDE Support](https://chrome.google.com/webstore/detail/jetbrains-ide-support/hmhgeddbohgjknpmjagkdomcpobmllji)

选择 WebStorm 菜单栏 `Run` 中的 `Edit Configurations...`,然后点击 `+` 并且选择 `JavaScript Debug` .然后将 `http://localhost:3000` 粘贴在 URL 字段栏中,并保存配置.

>注意: 如果通过 [HOST 或 PORT 环境变量](#高级配置) 进行了调整,则 url 需要修改.

通过运行 `npm start` 来启动应用,在 macOS 系统下,通过 `^D` 快捷键或者点击绿色的调试图标按钮,可以在 WebStorm 中开启调试功能.在 Windows 系统下,通过 `F9` 快捷键或者点击绿色的调试图标按钮,可以开启调试功能.


当然,在以下这些开发工具中,调试方式与 WebStorm 中相同:

IntelliJ IDEA Ultimate, PhpStorm, PyCharm Pro, 以及 RubyMine

## 代码自动格式化

Prettier 是一个代码格式化 (code formatter) 工具,支持 JavaScript, CSS 以及 JSON 等格式.它可以自动格式化代码,保证项目中代码格式统一.有关详细信息,请参阅 [Prettier 的 GitHub 页面](https://github.com/prettier/prettier) , 查看 [演示页面](https://prettier.github.io/prettier/).

如果我们想在 git 提交代码时自动进行格式化,可以安装下面的依赖项:

```sh
npm install --save husky lint-staged prettier
```

或者使用 `yarn`:

```sh
yarn add husky lint-staged prettier
```

* `husky` 使得使用 githooks 如同使用 npm scripts 一样简单.
* `lint-staged` 允许在使用 git 提交代码时,可以在处于 staged 状态(即待提交区)里的文件运行脚本. 查看这篇 [博客文章](https://medium.com/@okonetchnikov/make-linting-great-again-f3890e1ad6b8) ,可以了解更多关于 lint-staged 的信息.
* `prettier` 将在我们提交代码之前运行 JavaScript 脚本来格式化代码.

现在,我们可以修改项目根目录下的 `package.json` 文件,在该文件中添加以下代码,确保每个文件都可以被格式化处理.

将下面代码添加到 `scripts` 部分:

```diff
  "scripts": {
+   "precommit": "lint-staged",
    "start": "react-scripts start",
    "build": "react-scripts build",
```

接下来在 `package.json` 文件中添加 `lint-staged` 字段:

```diff
  "dependencies": {
    // ...
  },
+ "lint-staged": {
+   "src/**/*.{js,jsx,json,css}": [
+     "prettier --single-quote --write",
+     "git add"
+   ]
+ },
  "scripts": {
```

现在,只要进行代码提交, Prettier 就会自动格式化被修改的文件.另外,首次使用的时候,可以运行 `./node_modules/.bin/prettier --single-quote --write "src/**/*.{js,jsx,json,css}"` 对整个项目代码进行格式化.

当然如果你想要将 Prettier 集成到编辑器中,可以参照 Prettier 的 GitHub 页面上 [编辑器集成](https://prettier.io/docs/en/editors.html) 部分了解.

## 修改页面标题

你可以在生成的项目中的 `public` 文件夹中,找到 HTML 文件,编辑该文件中的 `<title>` 标签,将标签内容中的 "React App" 修改为你所需要的标题.

请注意,通常情况下 `public` 文件夹中的文件不用编辑的.例如你要[添加一个样式](#样式添加) ,是不需要操作 HTML 文件.

如果需要动态去修改页面的标题, 可以使用 [`document.title`](https://developer.mozilla.org/en-US/docs/Web/API/Document/title) 来修改.如果需要在复杂的应用场景下,通过 React 组件修改标题时,可以借助如 [React Helmet](https://github.com/nfl/react-helmet) 第三方插件来实现.

如果你在生产环境中使用自定义服务器,希望在用户浏览器接收到页面数据之前,就可以修改页面标题,可以参照 [这里](#在服务器上生成动态-meta-标签) ,也可以使用页面预加载,即当 JavaScript 加载后,页面会被构建为静态 HTML ,访问 [这里](#预加载静态-html-文件) 查看相关介绍.

## 安装依赖项

最终生成的项目包括 React 和 ReactDOM 作为依赖项.在开发环境下,还会包括 Create React App 的其他一些依赖项.可以使用 `npm` 命令来安装其他的依赖项,例如 React Router,则执行:

```sh
npm install --save react-router
```

当然也可以使用 `yarn`:

```sh
yarn add react-router
```

不仅仅是 `react-router` , 其他任何库都可以使用该方式安装.

## 组件引入

由于使用了 Babel ,所以项目支持 ES6
虽然你仍然可以使用 `require()` 和 `module.exports`,但我们鼓励使用 [`import` 和 `export`](http://exploringjs.com/es6/ch_modules.html) 来替代他们.

示例:

### `Button.js`

```js
import React, { Component } from 'react';

class Button extends Component {
  render() {
    // ...
  }
}

export default Button; // 这里不要忘记使用 export default !
```

### `DangerButton.js`


```js
import React, { Component } from 'react';
import Button from './Button'; // 从另一个文件 Import 组件 

class DangerButton extends Component {
  render() {
    return <Button color="red" />;
  }
}

export default DangerButton;
```

请注意 [默认导出和命名导出(`default exports`, `named exports`)的区别](http://stackoverflow.com/questions/36795819/react-native-es-6-when-should-i-use-curly-braces-for-import/36796281#36796281). 这会是一个常见的错误原因.

我们建议在模块仅导出单个内容(如组件)时,使用默认导入和导出( `imports` 和 `exports` ).如 `export default Button` 和 `import Button from './Button'`.

命名导出( `named exports` )在导出多个函数模块时很有用,一个模块( `module` )最多可以有一个默认导出( `default exports` )和多个命名导出( `named exports` ).

了解更多有关 ES6 模块的信息,请参照:

* [When to use the curly braces?](http://stackoverflow.com/questions/36795819/react-native-es-6-when-should-i-use-curly-braces-for-import/36796281#36796281)
* [Exploring ES6: Modules](http://exploringjs.com/es6/ch_modules.html)
* [Understanding ES6: Modules](https://leanpub.com/understandinges6/read#leanpub-auto-encapsulating-code-with-modules)

## 代码拆分

为避免用户在使用应用之前下载整个应用程序,将代码拆分成较小的代码块,实现代码的按需加载.

该功能是通过 [动态 `import()`](http://2ality.com/2017/01/import-operator.html#loading-code-on-demand) 来实现的.它的 [建议](https://github.com/tc39/proposal-dynamic-import) 在第三部分.The `import()` function-like form takes the module name as an argument and returns a [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) which always resolves to the namespace object of the module.

示例:

### `moduleA.js`

```js
const moduleA = 'Hello';

export { moduleA };
```
### `App.js`

```js
import React, { Component } from 'react';

class App extends Component {
  handleClick = () => {
    import('./moduleA')
      .then(({ moduleA }) => {
        // 使用 moduleA
      })
      .catch(err => {
        // 挂起 failure
      });
  };

  render() {
    return (
      <div>
        <button onClick={this.handleClick}>加载</button>
      </div>
    );
  }
}

export default App;
```

这将使的 `moduleA.js` 以及它所有的依赖项作为一个单独的模块,仅在用户点击 `加载` 按钮后才会加载.

也可以同 `async` / `await` 一起使用.

### 与 React 路由(Router) 一起使用

如果你使用的是 React 路由,请参照本 [教程](http://serverless-stack.com/chapters/code-splitting-in-create-react-app.html), 了解如何进行代码拆分,你也可以在 [此处](https://github.com/AnomalyInnovations/serverless-stack-demo-client/tree/code-splitting-in-create-react-app) 找到对应的 GitHub 示例.

另外也可以参照 React 文档中的 [Code Splitting](https://reactjs.org/docs/code-splitting.html) 部分.

## 样式添加

项目使用 [Webpack](https://webpack.js.org/) 来处理所有的资源. Webpack 提供了一种 JavaScript 的扩展方式,要表示 JavaScript 文件依赖于 CSS 文件, 需要 **在 JavaScript 文件中 `import` CSS 文件**.

### `Button.css`

```css
.Button {
  padding: 20px;
}
```

### `Button.js`

```js
import React, { Component } from 'react';
import './Button.css'; // 告诉 Webpack 当前 Button.js 使用该样式

class Button extends Component {
  render() {
    // 可以像使用普通 CSS 样式那样使用
    return <div className="Button" />;
  }
}
```

当然 **这些不是 React 必须的**,不过这个功能真的很方便,查看 [这里](https://medium.com/seek-blog/block-element-modifying-your-javascript-components-d7f99fcab52b) 可以了解到这种方法使用的好处.不过这样用,相比 Webpack 方式,移植到其他构建工具或平台会麻烦一点.

在开发环境,使用这种依赖引用方式,可以在编辑样式文件时动态的重新加载编辑后的样式.在生产环境,所有的 CSS 文件,都会被压缩并关联到一个单独的 `.CSS` 文件.

如果担心会使用到 Webpack-specific 语义,可以将所有的 CSS 正确引入到 `src/index.css` 文件中,这样仍然会在 `src/index.js` 文件中导入,但如果需要把项目迁移到其他构建工具中,也可以直接移除导入. 

## CSS处理

项目中 CSS 文件最终会被压缩,并通过 [Autoprefixer](https://github.com/postcss/autoprefixer) 自动添加不同浏览器兼容的前缀.

例如:

```css
.App {
  display: flex;
  flex-direction: row;
  align-items: center;
}
```

处理之后:

```css
.App {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: horizontal;
  -webkit-box-direction: normal;
      -ms-flex-direction: row;
          flex-direction: row;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
}
```

如果处于一些原因需要禁用该功能,可以参照 [这里](https://github.com/postcss/autoprefixer#disabling) 操作.

## 添加 CSS 预处理器(如 Sass, Less 等)

通常情况下,建议不要在不同的组件中使用相同的 CSS 类名.例如,在 `<AcceptButton>` 和 `<RejectButton>` 组件在,不建议使用 `.Button` 这样的 CSS 类名,我们建议,创建一个 `<Button>` 组件,并使用它自己私有的 `.Button` 样式,然后可以在 `<AcceptButton>` 和 `<RejectButton>` 中进行渲染(但 [不能继承](https://facebook.github.io/react/docs/composition-vs-inheritance.html) ).

遵循这样的规则可能会使 CSS 使用起来不那么灵活,因为混合以及嵌套功能会被组件自身样式所替代,当然如果你不是很介意,也可以使用一些 CSS 预处理工具,在这个例子里,我们使用 Sass ,当然你也可以使用 Less 或者其他预处理工具. 

首先,使用下面命令安装 Sass:

```sh
npm install --save node-sass-chokidar
```

当然也可以使用 `yarn`:

```sh
yarn add node-sass-chokidar
```

然后在 `packpage.json` 文件中,添加一下 `script`:

```diff
   "scripts": {
+    "build-css": "node-sass-chokidar src/ -o src/",
+    "watch-css": "npm run build-css && node-sass-chokidar src/ -o src/ --watch --recursive",
     "start": "react-scripts start",
     "build": "react-scripts build",
     "test": "react-scripts test --env=jsdom",
```

>注意: 要使用其他 CSS 预处理工具,请根据相关文档替换 `build-css` 和 `watch-css` 命令.

此时,你可以重命名 `src/App.css` 为 `src/App.scss` , 运行命令 `npm run watch-css` ,程序将自动监测根目录下的每一个 Sass 文件,并且在对应的 Sass 文件位置创建相应的 CSS 文件.在我们当前的示例中,将覆盖 `src/App.css` .由于 `src/App.js` 中依旧 imports 的是 `src/App.css` ,因此该 CSS 文件仍是项目的一部分,现在尝试编辑 `src/App.scss` ,对应的 `src/App.css` 将重新生成.

要在不同的 Sass 文件间共享变量,可以使用 Sass imports .例如, `src/App.scss` 可以使用其他组件的样式文件中,包含 `@import "./shared.scss"` 定义的变量.

如果在非相对路径下启用导入文件,需要在 `package.json` 文件中添加命令参数.

```
"build-css": "node-sass-chokidar --include-path ./src --include-path ./node_modules src/ -o src/",
"watch-css": "npm run build-css && node-sass-chokidar --include-path ./src --include-path ./node_modules src/ -o src/ --watch --recursive",
```

可以这样使用:

```scss
@import 'styles/_colors.scss'; // 假设在 src/ 下有 styles 这个文件夹
@import 'nprogress/nprogress'; // 在 nprogress 目录下导入 css 文件
```

此时你可能希望删除项目源目录中所有生成的 .CSS 文件,同时在 `.gitignore` 文件中添加 `src/**/*.css` 这样一条规则.因为通常我们都不会把构建的生产项目添加进源代码管理中.

最后,我们可能希望当我们运行 `npm start` 命令的时候,可以自动裕兴``运行 `watch-css` 命令,当我们运行 `npm build` 时,自动运行 `build-css` 命令.我们可以使用 `&&` 运算符按照顺序执行这2个脚本,然而并没有跨平台的方式允许我们同时运行这2个脚本,因此我们还需要安装一个依赖包:

```sh
npm install --save npm-run-all
```

当然也可以使用 `yarn`:

```sh
yarn add npm-run-all
```

然后我们就可以在 `start` 和 `build` 脚本中添加与 CSS 预处理工具相关的命令
Then we can change `start` and `build` scripts to include the CSS preprocessor commands:

```diff
   "scripts": {
     "build-css": "node-sass-chokidar src/ -o src/",
     "watch-css": "npm run build-css && node-sass-chokidar src/ -o src/ --watch --recursive",
-    "start": "react-scripts start",
-    "build": "react-scripts build",
+    "start-js": "react-scripts start",
+    "start": "npm-run-all -p watch-css start-js",
+    "build-js": "react-scripts build",
+    "build": "npm-run-all build-css build-js",
     "test": "react-scripts test --env=jsdom",
     "eject": "react-scripts eject"
   }
```

此时再运行 `npm start` 和 `npm build` 命令,也可以构建 sass 文件.


**为什么使用 `node-sass-chokidar`**

`node-sass` 已被证实有以下问题:

- `node-sass --watch` 在虚拟机或 docker 中使用时,在某些情况下会出现 *性能问题*.


- 样式无限编译问题 [#1939](https://github.com/facebookincubator/create-react-app/issues/1939)

- `node-sass` 监测目录中新增文件的问题 [#1891](https://github.com/sass/node-sass/issues/1891)

 在示例中使用的 `node-sass-chokidar` 已经解决以上问题.

## 图像,字体和文件的添加

在 Webpack 中,使用图像和字体等静态资源与 CSS 使用类似.

你可以 **在 JavaScript 模块中 `import` 文件**.这可以告诉 Webpack 将该文件包含在 bundle 中.与 CSS 导入不同,导入文件会转化为字符串值,这个值其实就是最终在代码中引用的路径,例如,作为图像的 `src` 属性或者链接到 PDF 文件的 `href` 地址链接.

有时候为了减少对于服务器的请求数,在导入小与 10,000 字节的图像时,会直接返回图像的 [data URI](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URIs),而非图像的路径.主要适用于以下文件扩展名: bmp, gif, jpg, jpeg, and png. 但 SVG 文件除外,详情参阅 [#1153](https://github.com/facebookincubator/create-react-app/issues/1153).

示例:

```js
import React from 'react';
import logo from './logo.png'; // 告诉 Webpack 该 JS 文件使用这个图像

console.log(logo); // /logo.84287d09.png

function Header() {
  // 最终导入结果是图片地址
  return <img src={logo} alt="Logo" />;
}

export default Header;
```

这样确保了在构建项目时, Webpack 将图像移动到合适的构建文件夹中,并为我们提供了正确的路径

同样适用于 CSS :

```css
.Logo {
  background-image: url(./logo.png);
}
```

Webpack 在 CSS 中找到所有相关的模块引用(从 `./` 开始),并路径替换为 bundle 中的最终路径.如果地址拼写错误或意外删除了重要的文件,你将在编译时看到错误提示,类似于导入了不存在的 JavaScript 模块.编译后,最终的文件名由 Webpack 根据文件哈希值生成.如果文件的内容发生了变化, Webpack 将自动重新打包并生成新的文件名,因此无需担心长时间的缓存问题.

请注意,这是 Webpack 的自定义功能.

**React 不需要该功能**,但是很多人喜欢这个功能(React Native 使用类似的图像机制). <br>
处理静态资源的另一个方法将在下一章节中介绍.

## public 文件夹的使用

>注意: 该功能只在 `react-scripts@0.5.0` 或者跟高的版本中提供

### HTML修改

`public` 文件夹中包含 HTML 文件,因此可以对其进行调整,例如, [修改页面标题](#修改页面标题).
编译后的代码将在构建过程中,自动添加进 `scrip` 标签中.

### 在模块之外添加静态资源

你也可以在 `public` 文件夹中添加其他资源.

请注意,通常我们会鼓励使用 `import` 在 JavaScript 文件中引入文件.例如,可参阅 [添加 CSS 预处理器(如 Sass, Less 等)](#添加-css-预处理器如-sass-less-等) 以及 [图像字体和文件的添加](#图像字体和文件的添加)

这种机制提供了很多好处:

* 脚本和样式被压缩并打包在一起以避免额外的网络请求.
* 缺少文件会引起编译错误,而不会导致用户的 404 错误信息.
* 最终打包文件名为文件的哈希值,因此不用担心会产生浏览器缓存的问题.

但是,可以使用 **escape hatch**在系统模块之外添加静态资源.

如果将文件放入 `public` 文件夹中, Webpack 将 **不会** 处理该文件.相反,该文件将会被复制到构建文件夹中.如果要引用 `public` 文件夹中的资源,需要使用一个名为 `PUBLIC_URL` 的变量.

在 `index.html` 文件中,可以这样使用:

```html
<link rel="shortcut icon" href="%PUBLIC_URL%/favicon.ico">
```
只有 `public` 文件夹中的文件才可以使用 `%PUBLIC_URL` 前缀.如果你需要使用 `src` 或 `node_modules` 文件夹里的文件,你需要新建一个明确表示该功能的文件夹,然后把所要引用的文件复制到该文件夹中,以确保可以作为构建文件的一部分.

当你运行 `npm run build` 时, Create React App 将会把 `%PUBLIC_URL%` 替换为正确的绝对路径.因此当使用客户端路由或将项目托管在非根 URL 上时,项目也可以正常的工作.

在 JavaScript 代码中, `process.env.PUBLIC_URL` 可以类似这样使用:

```js
render() {
  // 注意: 这是 escape hatc ,请谨慎使用
  // 通常我们建议使用 `import` 来获取资源 URL
  // 如本节上方 '图像字体和文件的添加' 中所述
  return <img src={process.env.PUBLIC_URL + '/img/logo.png'} />;
}
```

也请记住这样使会出现的一些问题:

* `public` 文件夹中文件并不会进行压缩和打包处理
* 在编译的时候,并不会调用丢失的文件,因此会导致用户出现 404 的错误
* 并不会使用打包后文件的哈希值作为文件名,因此这些文件每次有修改后,重命名或添加参数

### 什么时候该使用 public 文件夹

通常我们建议在 JavaScript 中进行 [添加 CSS 预处理器(如 Sass, Less 等)](#添加-css-预处理器如-sass-less-等) 以及 [图像字体和文件的添加](#图像字体和文件的添加)
该 `public` 文件夹可以在解决一些不常见的问题:

* 你需要在构建文件中输出特定名称的文件,如 [`manifest.webmanifest`](https://developer.mozilla.org/en-US/docs/Web/Manifest).
* 你有成百上千的图像,需要动态引用他们的路径.
* 你希望在 [`pace.js`](http://github.hubspot.com/pace/docs/welcome/) 捆绑一个小的脚本.
* 某些库可能与 Webpack 不兼容,只能使用 `<script>` 标签来引用.

请注意,如果要添加 `<script>` 全局变量声明,则请参阅下一章节.

## 全局变量的使用

When you include a script in the HTML file that defines global variables and try to use one of these variables in the code, the linter will complain because it cannot see the definition of the variable.

You can avoid this by reading the global variable explicitly from the `window` object, for example:

```js
const $ = window.$;
```

This makes it obvious you are using a global variable intentionally rather than because of a typo.

Alternatively, you can force the linter to ignore any line by adding `// eslint-disable-line` after it.

## 添加 Bootstrap

You don’t have to use [React Bootstrap](https://react-bootstrap.github.io) together with React but it is a popular library for integrating Bootstrap with React apps. If you need it, you can integrate it with Create React App by following these steps:

Install React Bootstrap and Bootstrap from npm. React Bootstrap does not include Bootstrap CSS so this needs to be installed as well:

```sh
npm install --save react-bootstrap bootstrap@3
```

Alternatively you may use `yarn`:

```sh
yarn add react-bootstrap bootstrap@3
```

Import Bootstrap CSS and optionally Bootstrap theme CSS in the beginning of your ```src/index.js``` file:

```js
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap/dist/css/bootstrap-theme.css';
// Put any other imports below so that CSS from your
// components takes precedence over default styles.
```

Import required React Bootstrap components within ```src/App.js``` file or your custom component files:

```js
import { Navbar, Jumbotron, Button } from 'react-bootstrap';
```

Now you are ready to use the imported React Bootstrap components within your component hierarchy defined in the render method. Here is an example [`App.js`](https://gist.githubusercontent.com/gaearon/85d8c067f6af1e56277c82d19fd4da7b/raw/6158dd991b67284e9fc8d70b9d973efe87659d72/App.js) redone using React Bootstrap.

### 使用自定义主题

Sometimes you might need to tweak the visual styles of Bootstrap (or equivalent package).<br>
We suggest the following approach:

* Create a new package that depends on the package you wish to customize, e.g. Bootstrap.
* Add the necessary build steps to tweak the theme, and publish your package on npm.
* Install your own theme npm package as a dependency of your app.

Here is an example of adding a [customized Bootstrap](https://medium.com/@tacomanator/customizing-create-react-app-aa9ffb88165) that follows these steps.

## 添加 Flow

Flow is a static type checker that helps you write code with fewer bugs. Check out this [introduction to using static types in JavaScript](https://medium.com/@preethikasireddy/why-use-static-types-in-javascript-part-1-8382da1e0adb) if you are new to this concept.

Recent versions of [Flow](http://flowtype.org/) work with Create React App projects out of the box.

To add Flow to a Create React App project, follow these steps:

1. Run `npm install --save flow-bin` (or `yarn add flow-bin`).
2. Add `"flow": "flow"` to the `scripts` section of your `package.json`.
3. Run `npm run flow init` (or `yarn flow init`) to create a [`.flowconfig` file](https://flowtype.org/docs/advanced-configuration.html) in the root directory.
4. Add `// @flow` to any files you want to type check (for example, to `src/App.js`).

Now you can run `npm run flow` (or `yarn flow`) to check the files for type errors.
You can optionally use an IDE like [Nuclide](https://nuclide.io/docs/languages/flow/) for a better integrated experience.
In the future we plan to integrate it into Create React App even more closely.

To learn more about Flow, check out [its documentation](https://flowtype.org/).

## 添加路由 Router

Create React App doesn't prescribe a specific routing solution, but [React Router](https://reacttraining.com/react-router/) is the most popular one.

To add it, run:

```sh
npm install --save react-router-dom
```

Alternatively you may use `yarn`:

```sh
yarn add react-router-dom
```

To try it, delete all the code in `src/App.js` and replace it with any of the examples on its website. The [Basic Example](https://reacttraining.com/react-router/web/example/basic) is a good place to get started.

Note that [you may need to configure your production server to support client-side routing](#serving-apps-with-client-side-routing) before deploying your app.

## 添加自定义环境变量

>Note: this feature is available with `react-scripts@0.2.3` and higher.

Your project can consume variables declared in your environment as if they were declared locally in your JS files. By
default you will have `NODE_ENV` defined for you, and any other environment variables starting with
`REACT_APP_`.

**The environment variables are embedded during the build time**. Since Create React App produces a static HTML/CSS/JS bundle, it can’t possibly read them at runtime. To read them at runtime, you would need to load HTML into memory on the server and replace placeholders in runtime, just like [described here](#injecting-data-from-the-server-into-the-page). Alternatively you can rebuild the app on the server anytime you change them.

>Note: You must create custom environment variables beginning with `REACT_APP_`. Any other variables except `NODE_ENV` will be ignored to avoid accidentally [exposing a private key on the machine that could have the same name](https://github.com/facebookincubator/create-react-app/issues/865#issuecomment-252199527). Changing any environment variables will require you to restart the development server if it is running.

These environment variables will be defined for you on `process.env`. For example, having an environment
variable named `REACT_APP_SECRET_CODE` will be exposed in your JS as `process.env.REACT_APP_SECRET_CODE`.

There is also a special built-in environment variable called `NODE_ENV`. You can read it from `process.env.NODE_ENV`. When you run `npm start`, it is always equal to `'development'`, when you run `npm test` it is always equal to `'test'`, and when you run `npm run build` to make a production bundle, it is always equal to `'production'`. **You cannot override `NODE_ENV` manually.** This prevents developers from accidentally deploying a slow development build to production.

These environment variables can be useful for displaying information conditionally based on where the project is
deployed or consuming sensitive data that lives outside of version control.

First, you need to have environment variables defined. For example, let’s say you wanted to consume a secret defined
in the environment inside a `<form>`:

```jsx
render() {
  return (
    <div>
      <small>You are running this application in <b>{process.env.NODE_ENV}</b> mode.</small>
      <form>
        <input type="hidden" defaultValue={process.env.REACT_APP_SECRET_CODE} />
      </form>
    </div>
  );
}
```

During the build, `process.env.REACT_APP_SECRET_CODE` will be replaced with the current value of the `REACT_APP_SECRET_CODE` environment variable. Remember that the `NODE_ENV` variable will be set for you automatically.

When you load the app in the browser and inspect the `<input>`, you will see its value set to `abcdef`, and the bold text will show the environment provided when using `npm start`:

```html
<div>
  <small>You are running this application in <b>development</b> mode.</small>
  <form>
    <input type="hidden" value="abcdef" />
  </form>
</div>
```

The above form is looking for a variable called `REACT_APP_SECRET_CODE` from the environment. In order to consume this
value, we need to have it defined in the environment. This can be done using two ways: either in your shell or in
a `.env` file. Both of these ways are described in the next few sections.

Having access to the `NODE_ENV` is also useful for performing actions conditionally:

```js
if (process.env.NODE_ENV !== 'production') {
  analytics.disable();
}
```

When you compile the app with `npm run build`, the minification step will strip out this condition, and the resulting bundle will be smaller.

### 在 HTML 中引用环境变量

>Note: this feature is available with `react-scripts@0.9.0` and higher.

You can also access the environment variables starting with `REACT_APP_` in the `public/index.html`. For example:

```html
<title>%REACT_APP_WEBSITE_NAME%</title>
```

Note that the caveats from the above section apply:

* Apart from a few built-in variables (`NODE_ENV` and `PUBLIC_URL`), variable names must start with `REACT_APP_` to work.
* The environment variables are injected at build time. If you need to inject them at runtime, [follow this approach instead](#generating-dynamic-meta-tags-on-the-server).

### 在 Shell 中添加临时环境变量

Defining environment variables can vary between OSes. It’s also important to know that this manner is temporary for the
life of the shell session.

#### Windows (cmd.exe)

```cmd
set "REACT_APP_SECRET_CODE=abcdef" && npm start
```

(Note: Quotes around the variable assignment are required to avoid a trailing whitespace.)

#### Windows (Powershell)

```Powershell
($env:REACT_APP_SECRET_CODE = "abcdef") -and (npm start)
```

#### Linux, macOS (Bash)

```bash
REACT_APP_SECRET_CODE=abcdef npm start
```

### 在 .env 文件中添加开发环境的变量

>Note: this feature is available with `react-scripts@0.5.0` and higher.

To define permanent environment variables, create a file called `.env` in the root of your project:

```
REACT_APP_SECRET_CODE=abcdef
```
>Note: You must create custom environment variables beginning with `REACT_APP_`. Any other variables except `NODE_ENV` will be ignored to avoid [accidentally exposing a private key on the machine that could have the same name](https://github.com/facebookincubator/create-react-app/issues/865#issuecomment-252199527). Changing any environment variables will require you to restart the development server if it is running.

`.env` files **should be** checked into source control (with the exclusion of `.env*.local`).

#### What other `.env` files can be used?

>Note: this feature is **available with `react-scripts@1.0.0` and higher**.

* `.env`: Default.
* `.env.local`: Local overrides. **This file is loaded for all environments except test.**
* `.env.development`, `.env.test`, `.env.production`: Environment-specific settings.
* `.env.development.local`, `.env.test.local`, `.env.production.local`: Local overrides of environment-specific settings.

Files on the left have more priority than files on the right:

* `npm start`: `.env.development.local`, `.env.development`, `.env.local`, `.env`
* `npm run build`: `.env.production.local`, `.env.production`, `.env.local`, `.env`
* `npm test`: `.env.test.local`, `.env.test`, `.env` (note `.env.local` is missing)

These variables will act as the defaults if the machine does not explicitly set them.<br>
Please refer to the [dotenv documentation](https://github.com/motdotla/dotenv) for more details.

>Note: If you are defining environment variables for development, your CI and/or hosting platform will most likely need
these defined as well. Consult their documentation how to do this. For example, see the documentation for [Travis CI](https://docs.travis-ci.com/user/environment-variables/) or [Heroku](https://devcenter.heroku.com/articles/config-vars).

#### Expanding Environment Variables In `.env`

>Note: this feature is available with `react-scripts@1.1.0` and higher.

Expand variables already on your machine for use in your `.env` file (using [dotenv-expand](https://github.com/motdotla/dotenv-expand)).

For example, to get the environment variable `npm_package_version`:

```
REACT_APP_VERSION=$npm_package_version
# also works:
# REACT_APP_VERSION=${npm_package_version}
```

Or expand variables local to the current `.env` file:

```
DOMAIN=www.example.com
REACT_APP_FOO=$DOMAIN/foo
REACT_APP_BAR=$DOMAIN/bar
```

## 能否使用修饰器

Many popular libraries use [decorators](https://medium.com/google-developers/exploring-es7-decorators-76ecb65fb841) in their documentation.<br>
Create React App doesn’t support decorator syntax at the moment because:

* It is an experimental proposal and is subject to change.
* The current specification version is not officially supported by Babel.
* If the specification changes, we won’t be able to write a codemod because we don’t use them internally at Facebook.

However in many cases you can rewrite decorator-based code without decorators just as fine.<br>
Please refer to these two threads for reference:

* [#214](https://github.com/facebookincubator/create-react-app/issues/214)
* [#411](https://github.com/facebookincubator/create-react-app/issues/411)

Create React App will add decorator support when the specification advances to a stable stage.

## 使用 AJAX 请求数据

React doesn't prescribe a specific approach to data fetching, but people commonly use either a library like [axios](https://github.com/axios/axios) or the [`fetch()` API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) provided by the browser. Conveniently, Create React App includes a polyfill for `fetch()` so you can use it without worrying about the browser support.

The global `fetch` function allows to easily makes AJAX requests. It takes in a URL as an input and returns a `Promise` that resolves to a `Response` object. You can find more information about `fetch` [here](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch).

This project also includes a [Promise polyfill](https://github.com/then/promise) which provides a full implementation of Promises/A+. A Promise represents the eventual result of an asynchronous operation, you can find more information about Promises [here](https://www.promisejs.org/) and [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise). Both axios and `fetch()` use Promises under the hood. You can also use the [`async / await`](https://davidwalsh.name/async-await) syntax to reduce the callback nesting.

You can learn more about making AJAX requests from React components in [the FAQ entry on the React website](https://reactjs.org/docs/faq-ajax.html).

## 与后端的 API 集成

These tutorials will help you to integrate your app with an API backend running on another port,
using `fetch()` to access it.

### Node
Check out [this tutorial](https://www.fullstackreact.com/articles/using-create-react-app-with-a-server/).
You can find the companion GitHub repository [here](https://github.com/fullstackreact/food-lookup-demo).

### Ruby on Rails

Check out [this tutorial](https://www.fullstackreact.com/articles/how-to-get-create-react-app-to-work-with-your-rails-api/).
You can find the companion GitHub repository [here](https://github.com/fullstackreact/food-lookup-demo-rails).

## 在开发中使用代理 API 请求

>Note: this feature is available with `react-scripts@0.2.3` and higher.

People often serve the front-end React app from the same host and port as their backend implementation.<br>
For example, a production setup might look like this after the app is deployed:

```
/             - static server returns index.html with React app
/todos        - static server returns index.html with React app
/api/todos    - server handles any /api/* requests using the backend implementation
```

Such setup is **not** required. However, if you **do** have a setup like this, it is convenient to write requests like `fetch('/api/todos')` without worrying about redirecting them to another host or port during development.

To tell the development server to proxy any unknown requests to your API server in development, add a `proxy` field to your `package.json`, for example:

```js
  "proxy": "http://localhost:4000",
```

This way, when you `fetch('/api/todos')` in development, the development server will recognize that it’s not a static asset, and will proxy your request to `http://localhost:4000/api/todos` as a fallback. The development server will **only** attempt to send requests without `text/html` in its `Accept` header to the proxy.

Conveniently, this avoids [CORS issues](http://stackoverflow.com/questions/21854516/understanding-ajax-cors-and-security-considerations) and error messages like this in development:

```
Fetch API cannot load http://localhost:4000/api/todos. No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'http://localhost:3000' is therefore not allowed access. If an opaque response serves your needs, set the request's mode to 'no-cors' to fetch the resource with CORS disabled.
```

Keep in mind that `proxy` only has effect in development (with `npm start`), and it is up to you to ensure that URLs like `/api/todos` point to the right thing in production. You don’t have to use the `/api` prefix. Any unrecognized request without a `text/html` accept header will be redirected to the specified `proxy`.

The `proxy` option supports HTTP, HTTPS and WebSocket connections.<br>
If the `proxy` option is **not** flexible enough for you, alternatively you can:

* [Configure the proxy yourself](#configuring-the-proxy-manually)
* Enable CORS on your server ([here’s how to do it for Express](http://enable-cors.org/server_expressjs.html)).
* Use [environment variables](#adding-custom-environment-variables) to inject the right server host and port into your app.

### 配置代理后出现 Invalid Host Header 错误

When you enable the `proxy` option, you opt into a more strict set of host checks. This is necessary because leaving the backend open to remote hosts makes your computer vulnerable to DNS rebinding attacks. The issue is explained in [this article](https://medium.com/webpack/webpack-dev-server-middleware-security-issues-1489d950874a) and [this issue](https://github.com/webpack/webpack-dev-server/issues/887).

This shouldn’t affect you when developing on `localhost`, but if you develop remotely like [described here](https://github.com/facebookincubator/create-react-app/issues/2271), you will see this error in the browser after enabling the `proxy` option:

>Invalid Host header

To work around it, you can specify your public development host in a file called `.env.development` in the root of your project:

```
HOST=mypublicdevhost.com
```

If you restart the development server now and load the app from the specified host, it should work.

If you are still having issues or if you’re using a more exotic environment like a cloud editor, you can bypass the host check completely by adding a line to `.env.development.local`. **Note that this is dangerous and exposes your machine to remote code execution from malicious websites:**

```
# NOTE: THIS IS DANGEROUS!
# It exposes your machine to attacks from the websites you visit.
DANGEROUSLY_DISABLE_HOST_CHECK=true
```

We don’t recommend this approach.

### 手动配置代理

>Note: this feature is available with `react-scripts@1.0.0` and higher.

If the `proxy` option is **not** flexible enough for you, you can specify an object in the following form (in `package.json`).<br>
You may also specify any configuration value [`http-proxy-middleware`](https://github.com/chimurai/http-proxy-middleware#options) or [`http-proxy`](https://github.com/nodejitsu/node-http-proxy#options) supports.
```js
{
  // ...
  "proxy": {
    "/api": {
      "target": "<url>",
      "ws": true
      // ...
    }
  }
  // ...
}
```

All requests matching this path will be proxies, no exceptions. This includes requests for `text/html`, which the standard `proxy` option does not proxy.

If you need to specify multiple proxies, you may do so by specifying additional entries.
Matches are regular expressions, so that you can use a regexp to match multiple paths.
```js
{
  // ...
  "proxy": {
    // Matches any request starting with /api
    "/api": {
      "target": "<url_1>",
      "ws": true
      // ...
    },
    // Matches any request starting with /foo
    "/foo": {
      "target": "<url_2>",
      "ssl": true,
      "pathRewrite": {
        "^/foo": "/foo/beta"
      }
      // ...
    },
    // Matches /bar/abc.html but not /bar/sub/def.html
    "/bar/[^/]*[.]html": {
      "target": "<url_3>",
      // ...
    },
    // Matches /baz/abc.html and /baz/sub/def.html
    "/baz/.*/.*[.]html": {
      "target": "<url_4>"
      // ...
    }
  }
  // ...
}
```

### 配置 WebSocket 代理

When setting up a WebSocket proxy, there are a some extra considerations to be aware of.

If you’re using a WebSocket engine like [Socket.io](https://socket.io/), you must have a Socket.io server running that you can use as the proxy target. Socket.io will not work with a standard WebSocket server. Specifically, don't expect Socket.io to work with [the websocket.org echo test](http://websocket.org/echo.html).

There’s some good documentation available for [setting up a Socket.io server](https://socket.io/docs/).

Standard WebSockets **will** work with a standard WebSocket server as well as the websocket.org echo test. You can use libraries like [ws](https://github.com/websockets/ws) for the server, with [native WebSockets in the browser](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket).

Either way, you can proxy WebSocket requests manually in `package.json`:

```js
{
  // ...
  "proxy": {
    "/socket": {
      // Your compatible WebSocket server
      "target": "ws://<socket_url>",
      // Tell http-proxy-middleware that this is a WebSocket proxy.
      // Also allows you to proxy WebSocket requests without an additional HTTP request
      // https://github.com/chimurai/http-proxy-middleware#external-websocket-upgrade
      "ws": true
      // ...
    }
  }
  // ...
}
```

## 在开发中使用 HTTPS

>Note: this feature is available with `react-scripts@0.4.0` and higher.

You may require the dev server to serve pages over HTTPS. One particular case where this could be useful is when using [the "proxy" feature](#proxying-api-requests-in-development) to proxy requests to an API server when that API server is itself serving HTTPS.

To do this, set the `HTTPS` environment variable to `true`, then start the dev server as usual with `npm start`:

#### Windows (cmd.exe)

```cmd
set HTTPS=true&&npm start
```

#### Windows (Powershell)

```Powershell
($env:HTTPS = $true) -and (npm start)
```

(Note: the lack of whitespace is intentional.)

#### Linux, macOS (Bash)

```bash
HTTPS=true npm start
```

Note that the server will use a self-signed certificate, so your web browser will almost definitely display a warning upon accessing the page.

## 在服务器上生成动态 `<meta>` 标签

Since Create React App doesn’t support server rendering, you might be wondering how to make `<meta>` tags dynamic and reflect the current URL. To solve this, we recommend to add placeholders into the HTML, like this:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta property="og:title" content="__OG_TITLE__">
    <meta property="og:description" content="__OG_DESCRIPTION__">
```

Then, on the server, regardless of the backend you use, you can read `index.html` into memory and replace `__OG_TITLE__`, `__OG_DESCRIPTION__`, and any other placeholders with values depending on the current URL. Just make sure to sanitize and escape the interpolated values so that they are safe to embed into HTML!

If you use a Node server, you can even share the route matching logic between the client and the server. However duplicating it also works fine in simple cases.

## 预加载静态 HTML 文件

If you’re hosting your `build` with a static hosting provider you can use [react-snapshot](https://www.npmjs.com/package/react-snapshot) or [react-snap](https://github.com/stereobooster/react-snap) to generate HTML pages for each route, or relative link, in your application. These pages will then seamlessly become active, or “hydrated”, when the JavaScript bundle has loaded.

There are also opportunities to use this outside of static hosting, to take the pressure off the server when generating and caching routes.

The primary benefit of pre-rendering is that you get the core content of each page _with_ the HTML payload—regardless of whether or not your JavaScript bundle successfully downloads. It also increases the likelihood that each route of your application will be picked up by search engines.

You can read more about [zero-configuration pre-rendering (also called snapshotting) here](https://medium.com/superhighfives/an-almost-static-stack-6df0a2791319).

## 在服务器端添加数据到页面

Similarly to the previous section, you can leave some placeholders in the HTML that inject global variables, for example:

```js
<!doctype html>
<html lang="en">
  <head>
    <script>
      window.SERVER_DATA = __SERVER_DATA__;
    </script>
```

Then, on the server, you can replace `__SERVER_DATA__` with a JSON of real data right before sending the response. The client code can then read `window.SERVER_DATA` to use it. **Make sure to [sanitize the JSON before sending it to the client](https://medium.com/node-security/the-most-common-xss-vulnerability-in-react-js-applications-2bdffbcc1fa0) as it makes your app vulnerable to XSS attacks.**

## 运行测试 TEST

>Note: this feature is available with `react-scripts@0.3.0` and higher.<br>
>[Read the migration guide to learn how to enable it in older projects!](https://github.com/facebookincubator/create-react-app/blob/master/CHANGELOG.md#migrating-from-023-to-030)

Create React App uses [Jest](https://facebook.github.io/jest/) as its test runner. To prepare for this integration, we did a [major revamp](https://facebook.github.io/jest/blog/2016/09/01/jest-15.html) of Jest so if you heard bad things about it years ago, give it another try.

Jest is a Node-based runner. This means that the tests always run in a Node environment and not in a real browser. This lets us enable fast iteration speed and prevent flakiness.

While Jest provides browser globals such as `window` thanks to [jsdom](https://github.com/tmpvar/jsdom), they are only approximations of the real browser behavior. Jest is intended to be used for unit tests of your logic and your components rather than the DOM quirks.

We recommend that you use a separate tool for browser end-to-end tests if you need them. They are beyond the scope of Create React App.

### 文件命名约定

Jest will look for test files with any of the following popular naming conventions:

* Files with `.js` suffix in `__tests__` folders.
* Files with `.test.js` suffix.
* Files with `.spec.js` suffix.

The `.test.js` / `.spec.js` files (or the `__tests__` folders) can be located at any depth under the `src` top level folder.

We recommend to put the test files (or `__tests__` folders) next to the code they are testing so that relative imports appear shorter. For example, if `App.test.js` and `App.js` are in the same folder, the test just needs to `import App from './App'` instead of a long relative path. Colocation also helps find tests more quickly in larger projects.

### 命令行界面

When you run `npm test`, Jest will launch in the watch mode. Every time you save a file, it will re-run the tests, just like `npm start` recompiles the code.

The watcher includes an interactive command-line interface with the ability to run all tests, or focus on a search pattern. It is designed this way so that you can keep it open and enjoy fast re-runs. You can learn the commands from the “Watch Usage” note that the watcher prints after every run:

![Jest watch mode](http://facebook.github.io/jest/img/blog/15-watch.gif)

### 版本控制集成

By default, when you run `npm test`, Jest will only run the tests related to files changed since the last commit. This is an optimization designed to make your tests run fast regardless of how many tests you have. However it assumes that you don’t often commit the code that doesn’t pass the tests.

Jest will always explicitly mention that it only ran tests related to the files changed since the last commit. You can also press `a` in the watch mode to force Jest to run all tests.

Jest will always run all tests on a [continuous integration](#continuous-integration) server or if the project is not inside a Git or Mercurial repository.

### 编写一个测试

To create tests, add `it()` (or `test()`) blocks with the name of the test and its code. You may optionally wrap them in `describe()` blocks for logical grouping but this is neither required nor recommended.

Jest provides a built-in `expect()` global function for making assertions. A basic test could look like this:

```js
import sum from './sum';

it('sums numbers', () => {
  expect(sum(1, 2)).toEqual(3);
  expect(sum(2, 2)).toEqual(4);
});
```

All `expect()` matchers supported by Jest are [extensively documented here](https://facebook.github.io/jest/docs/en/expect.html#content).<br>
You can also use [`jest.fn()` and `expect(fn).toBeCalled()`](https://facebook.github.io/jest/docs/en/expect.html#tohavebeencalled) to create “spies” or mock functions.

### 测试组件

There is a broad spectrum of component testing techniques. They range from a “smoke test” verifying that a component renders without throwing, to shallow rendering and testing some of the output, to full rendering and testing component lifecycle and state changes.

Different projects choose different testing tradeoffs based on how often components change, and how much logic they contain. If you haven’t decided on a testing strategy yet, we recommend that you start with creating simple smoke tests for your components:

```js
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

it('renders without crashing', () => {
  const div = document.createElement('div');
  ReactDOM.render(<App />, div);
});
```

This test mounts a component and makes sure that it didn’t throw during rendering. Tests like this provide a lot of value with very little effort so they are great as a starting point, and this is the test you will find in `src/App.test.js`.

When you encounter bugs caused by changing components, you will gain a deeper insight into which parts of them are worth testing in your application. This might be a good time to introduce more specific tests asserting specific expected output or behavior.

If you’d like to test components in isolation from the child components they render, we recommend using [`shallow()` rendering API](http://airbnb.io/enzyme/docs/api/shallow.html) from [Enzyme](http://airbnb.io/enzyme/). To install it, run:

```sh
npm install --save enzyme enzyme-adapter-react-16 react-test-renderer
```

Alternatively you may use `yarn`:

```sh
yarn add enzyme enzyme-adapter-react-16 react-test-renderer
```

As of Enzyme 3, you will need to install Enzyme along with an Adapter corresponding to the version of React you are using. (The examples above use the adapter for React 16.)

The adapter will also need to be configured in your [global setup file](#initializing-test-environment):

#### `src/setupTests.js`
```js
import { configure } from 'enzyme';
import Adapter from 'enzyme-adapter-react-16';

configure({ adapter: new Adapter() });
```

>Note: Keep in mind that if you decide to "eject" before creating `src/setupTests.js`, the resulting `package.json` file won't contain any reference to it. [Read here](#initializing-test-environment) to learn how to add this after ejecting.

Now you can write a smoke test with it:

```js
import React from 'react';
import { shallow } from 'enzyme';
import App from './App';

it('renders without crashing', () => {
  shallow(<App />);
});
```

Unlike the previous smoke test using `ReactDOM.render()`, this test only renders `<App>` and doesn’t go deeper. For example, even if `<App>` itself renders a `<Button>` that throws, this test will pass. Shallow rendering is great for isolated unit tests, but you may still want to create some full rendering tests to ensure the components integrate correctly. Enzyme supports [full rendering with `mount()`](http://airbnb.io/enzyme/docs/api/mount.html), and you can also use it for testing state changes and component lifecycle.

You can read the [Enzyme documentation](http://airbnb.io/enzyme/) for more testing techniques. Enzyme documentation uses Chai and Sinon for assertions but you don’t have to use them because Jest provides built-in `expect()` and `jest.fn()` for spies.

Here is an example from Enzyme documentation that asserts specific output, rewritten to use Jest matchers:

```js
import React from 'react';
import { shallow } from 'enzyme';
import App from './App';

it('renders welcome message', () => {
  const wrapper = shallow(<App />);
  const welcome = <h2>Welcome to React</h2>;
  // expect(wrapper.contains(welcome)).to.equal(true);
  expect(wrapper.contains(welcome)).toEqual(true);
});
```

All Jest matchers are [extensively documented here](http://facebook.github.io/jest/docs/en/expect.html).<br>
Nevertheless you can use a third-party assertion library like [Chai](http://chaijs.com/) if you want to, as described below.

Additionally, you might find [jest-enzyme](https://github.com/blainekasten/enzyme-matchers) helpful to simplify your tests with readable matchers. The above `contains` code can be written more simply with jest-enzyme.

```js
expect(wrapper).toContainReact(welcome)
```

To enable this, install `jest-enzyme`:

```sh
npm install --save jest-enzyme
```

Alternatively you may use `yarn`:

```sh
yarn add jest-enzyme
```

Import it in [`src/setupTests.js`](#initializing-test-environment) to make its matchers available in every test:

```js
import 'jest-enzyme';
```

#### Use `react-testing-library`

As an alternative or companion to `enzyme`, you may consider using `react-testing-library`. [`react-testing-library`](https://github.com/kentcdodds/react-testing-library) is a library for testing React components in a way that resembles the way the components are used by end users. It is well suited for unit, integration, and end-to-end testing of React components and applications. It works more directly with DOM nodes, and therefore it's recommended to use with [`jest-dom`](https://github.com/gnapse/jest-dom) for improved assertions.

To install `react-testing-library` and `jest-dom`, you can run:

```sh
npm install --save react-testing-library jest-dom
```

Alternatively you may use `yarn`:

```sh
yarn add react-testing-library jest-dom
```

Similar to `enzyme` you can create a `src/setupTests.js` file to avoid boilerplate in your test files:

```js
// react-testing-library renders your components to document.body,
// this will ensure they're removed after each test.
import 'react-testing-library/cleanup-after-each';

// this adds jest-dom's custom assertions
import 'jest-dom/extend-expect';
```

Here's an example of using `react-testing-library` and `jest-dom` for testing that the `<App />` component renders "Welcome to React".

```js
import React from 'react';
import { render } from 'react-testing-library';
import App from './App';

it('renders welcome message', () => {
  const { getByText } = render(<App />);
  expect(getByText('Welcome to React')).toBeInTheDOM();
});
```

Learn more about the utilities provided by `react-testing-library` to facilitate testing asynchronous interactions as well as selecting form elements from [the `react-testing-library` documentation](https://github.com/kentcdodds/react-testing-library) and [examples](https://codesandbox.io/s/github/kentcdodds/react-testing-library-examples).

### 使用第三方 Assertion 库

We recommend that you use `expect()` for assertions and `jest.fn()` for spies. If you are having issues with them please [file those against Jest](https://github.com/facebook/jest/issues/new), and we’ll fix them. We intend to keep making them better for React, supporting, for example, [pretty-printing React elements as JSX](https://github.com/facebook/jest/pull/1566).

However, if you are used to other libraries, such as [Chai](http://chaijs.com/) and [Sinon](http://sinonjs.org/), or if you have existing code using them that you’d like to port over, you can import them normally like this:

```js
import sinon from 'sinon';
import { expect } from 'chai';
```

and then use them in your tests like you normally do.

### 初始化测试环境

>Note: this feature is available with `react-scripts@0.4.0` and higher.

If your app uses a browser API that you need to mock in your tests or if you just need a global setup before running your tests, add a `src/setupTests.js` to your project. It will be automatically executed before running your tests.

For example:

#### `src/setupTests.js`
```js
const localStorageMock = {
  getItem: jest.fn(),
  setItem: jest.fn(),
  clear: jest.fn()
};
global.localStorage = localStorageMock
```

>Note: Keep in mind that if you decide to "eject" before creating `src/setupTests.js`, the resulting `package.json` file won't contain any reference to it, so you should manually create the property `setupTestFrameworkScriptFile` in the configuration for Jest, something like the following:

>```js
>"jest": {
>   // ...
>   "setupTestFrameworkScriptFile": "<rootDir>/src/setupTests.js"
>  }
>  ```

### 关注及排除测试

You can replace `it()` with `xit()` to temporarily exclude a test from being executed.<br>
Similarly, `fit()` lets you focus on a specific test without running any other tests.

### 覆盖率报告

Jest has an integrated coverage reporter that works well with ES6 and requires no configuration.<br>
Run `npm test -- --coverage` (note extra `--` in the middle) to include a coverage report like this:

![coverage report](http://i.imgur.com/5bFhnTS.png)

Note that tests run much slower with coverage so it is recommended to run it separately from your normal workflow.

#### Configuration

The default Jest coverage configuration can be overriden by adding any of the following supported keys to a Jest config in your package.json.

Supported overrides:
 - [`collectCoverageFrom`](https://facebook.github.io/jest/docs/en/configuration.html#collectcoveragefrom-array)
 - [`coverageReporters`](https://facebook.github.io/jest/docs/en/configuration.html#coveragereporters-array-string)
 - [`coverageThreshold`](https://facebook.github.io/jest/docs/en/configuration.html#coveragethreshold-object)
 - [`snapshotSerializers`](https://facebook.github.io/jest/docs/en/configuration.html#snapshotserializers-array-string)

Example package.json:

```json
{
  "name": "your-package",
  "jest": {
    "collectCoverageFrom" : [
      "src/**/*.{js,jsx}",
      "!<rootDir>/node_modules/",
      "!<rootDir>/path/to/dir/"
    ],
    "coverageThreshold": {
      "global": {
        "branches": 90,
        "functions": 90,
        "lines": 90,
        "statements": 90
      }
    },
    "coverageReporters": ["text"],
    "snapshotSerializers": ["my-serializer-module"]
  }
}
```

### 持续集成

By default `npm test` runs the watcher with interactive CLI. However, you can force it to run tests once and finish the process by setting an environment variable called `CI`.

When creating a build of your application with `npm run build` linter warnings are not checked by default. Like `npm test`, you can force the build to perform a linter warning check by setting the environment variable `CI`. If any warnings are encountered then the build fails.

Popular CI servers already set the environment variable `CI` by default but you can do this yourself too:

### On CI servers
#### Travis CI

1. Following the [Travis Getting started](https://docs.travis-ci.com/user/getting-started/) guide for syncing your GitHub repository with Travis.  You may need to initialize some settings manually in your [profile](https://travis-ci.org/profile) page.
1. Add a `.travis.yml` file to your git repository.
```
language: node_js
node_js:
  - 6
cache:
  directories:
    - node_modules
script:
  - npm run build
  - npm test
```
1. Trigger your first build with a git push.
1. [Customize your Travis CI Build](https://docs.travis-ci.com/user/customizing-the-build/) if needed.

#### CircleCI

Follow [this article](https://medium.com/@knowbody/circleci-and-zeits-now-sh-c9b7eebcd3c1) to set up CircleCI with a Create React App project.

### On your own environment
##### Windows (cmd.exe)

```cmd
set CI=true&&npm test
```

```cmd
set CI=true&&npm run build
```

(Note: the lack of whitespace is intentional.)

##### Windows (Powershell)

```Powershell
($env:CI = $true) -and (npm test)
```

```Powershell
($env:CI = $true) -and (npm run build)
```

##### Linux, macOS (Bash)

```bash
CI=true npm test
```

```bash
CI=true npm run build
```

The test command will force Jest to run tests once instead of launching the watcher.

>  If you find yourself doing this often in development, please [file an issue](https://github.com/facebookincubator/create-react-app/issues/new) to tell us about your use case because we want to make watcher the best experience and are open to changing how it works to accommodate more workflows.

The build command will check for linter warnings and fail if any are found.

### 禁用 jsdom

By default, the `package.json` of the generated project looks like this:

```js
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom"
```

If you know that none of your tests depend on [jsdom](https://github.com/tmpvar/jsdom), you can safely remove `--env=jsdom`, and your tests will run faster:

```diff
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
-   "test": "react-scripts test --env=jsdom"
+   "test": "react-scripts test"
```

To help you make up your mind, here is a list of APIs that **need jsdom**:

* Any browser globals like `window` and `document`
* [`ReactDOM.render()`](https://facebook.github.io/react/docs/top-level-api.html#reactdom.render)
* [`TestUtils.renderIntoDocument()`](https://facebook.github.io/react/docs/test-utils.html#renderintodocument) ([a shortcut](https://github.com/facebook/react/blob/34761cf9a252964abfaab6faf74d473ad95d1f21/src/test/ReactTestUtils.js#L83-L91) for the above)
* [`mount()`](http://airbnb.io/enzyme/docs/api/mount.html) in [Enzyme](http://airbnb.io/enzyme/index.html)

In contrast, **jsdom is not needed** for the following APIs:

* [`TestUtils.createRenderer()`](https://facebook.github.io/react/docs/test-utils.html#shallow-rendering) (shallow rendering)
* [`shallow()`](http://airbnb.io/enzyme/docs/api/shallow.html) in [Enzyme](http://airbnb.io/enzyme/index.html)

Finally, jsdom is also not needed for [snapshot testing](http://facebook.github.io/jest/blog/2016/07/27/jest-14.html).

### 快照测试

Snapshot testing is a feature of Jest that automatically generates text snapshots of your components and saves them on the disk so if the UI output changes, you get notified without manually writing any assertions on the component output. [Read more about snapshot testing.](http://facebook.github.io/jest/blog/2016/07/27/jest-14.html)

### 编辑器集成

If you use [Visual Studio Code](https://code.visualstudio.com), there is a [Jest extension](https://github.com/orta/vscode-jest) which works with Create React App out of the box. This provides a lot of IDE-like features while using a text editor: showing the status of a test run with potential fail messages inline, starting and stopping the watcher automatically, and offering one-click snapshot updates.

![VS Code Jest Preview](https://cloud.githubusercontent.com/assets/49038/20795349/a032308a-b7c8-11e6-9b34-7eeac781003f.png)

## 调试测试 TEST

There are various ways to setup a debugger for your Jest tests. We cover debugging in Chrome and [Visual Studio Code](https://code.visualstudio.com/).

>Note: debugging tests requires Node 8 or higher.

### 在 Chrome 中调试测试

Add the following to the `scripts` section in your project's `package.json`
```json
"scripts": {
    "test:debug": "react-scripts --inspect-brk test --runInBand --env=jsdom"
  }
```
Place `debugger;` statements in any test and run:
```bash
$ npm run test:debug
```

This will start running your Jest tests, but pause before executing to allow a debugger to attach to the process.

Open the following in Chrome
```
about:inspect
```

After opening that link, the Chrome Developer Tools will be displayed. Select `inspect` on your process and a breakpoint will be set at the first line of the react script (this is done simply to give you time to open the developer tools and to prevent Jest from executing before you have time to do so). Click the button that looks like a "play" button in the upper right hand side of the screen to continue execution. When Jest executes the test that contains the debugger statement, execution will pause and you can examine the current scope and call stack.

>Note: the --runInBand cli option makes sure Jest runs test in the same process rather than spawning processes for individual tests. Normally Jest parallelizes test runs across processes but it is hard to debug many processes at the same time.

### 在 Visual Studio Code 中调试测试

Debugging Jest tests is supported out of the box for [Visual Studio Code](https://code.visualstudio.com).

Use the following [`launch.json`](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) configuration file:
```
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug CRA Tests",
      "type": "node",
      "request": "launch",
      "runtimeExecutable": "${workspaceRoot}/node_modules/.bin/react-scripts",      
      "args": [
        "test",
        "--runInBand",
        "--no-cache",
        "--env=jsdom"
      ],
      "cwd": "${workspaceRoot}",
      "protocol": "inspector",
      "console": "integratedTerminal",
      "internalConsoleOptions": "neverOpen"
    }
  ]
}
```

## 开发独立组件 Components

Usually, in an app, you have a lot of UI components, and each of them has many different states.
For an example, a simple button component could have following states:

* In a regular state, with a text label.
* In the disabled mode.
* In a loading state.

Usually, it’s hard to see these states without running a sample app or some examples.

Create React App doesn’t include any tools for this by default, but you can easily add [Storybook for React](https://storybook.js.org) ([source](https://github.com/storybooks/storybook)) or [React Styleguidist](https://react-styleguidist.js.org/) ([source](https://github.com/styleguidist/react-styleguidist)) to your project. **These are third-party tools that let you develop components and see all their states in isolation from your app**.

![Storybook for React Demo](http://i.imgur.com/7CIAWpB.gif)

You can also deploy your Storybook or style guide as a static app. This way, everyone in your team can view and review different states of UI components without starting a backend server or creating an account in your app.

### Storybook 入门

Storybook is a development environment for React UI components. It allows you to browse a component library, view the different states of each component, and interactively develop and test components.

First, install the following npm package globally:

```sh
npm install -g @storybook/cli
```

Then, run the following command inside your app’s directory:

```sh
getstorybook
```

After that, follow the instructions on the screen.

Learn more about React Storybook:

* Screencast: [Getting Started with React Storybook](https://egghead.io/lessons/react-getting-started-with-react-storybook)
* [GitHub Repo](https://github.com/storybooks/storybook)
* [Documentation](https://storybook.js.org/basics/introduction/)
* [Snapshot Testing UI](https://github.com/storybooks/storybook/tree/master/addons/storyshots) with Storybook + addon/storyshot

### Styleguidist 入门

Styleguidist combines a style guide, where all your components are presented on a single page with their props documentation and usage examples, with an environment for developing components in isolation, similar to Storybook. In Styleguidist you write examples in Markdown, where each code snippet is rendered as a live editable playground.

First, install Styleguidist:

```sh
npm install --save react-styleguidist
```

Alternatively you may use `yarn`:

```sh
yarn add react-styleguidist
```

Then, add these scripts to your `package.json`:

```diff
   "scripts": {
+    "styleguide": "styleguidist server",
+    "styleguide:build": "styleguidist build",
     "start": "react-scripts start",
```

Then, run the following command inside your app’s directory:

```sh
npm run styleguide
```

After that, follow the instructions on the screen.

Learn more about React Styleguidist:

* [GitHub Repo](https://github.com/styleguidist/react-styleguidist)
* [Documentation](https://react-styleguidist.js.org/docs/getting-started.html)

## 发布组件 Components 到 npm

Create React App doesn't provide any built-in functionality to publish a component to npm. If you're ready to extract a component from your project so other people can use it, we recommend moving it to a separate directory outside of your project and then using a tool like [nwb](https://github.com/insin/nwb#react-components-and-libraries) to prepare it for publishing.

## 开发渐进式网页应用 (PWA,即 Progressive Web App)

By default, the production build is a fully functional, offline-first
[Progressive Web App](https://developers.google.com/web/progressive-web-apps/).

Progressive Web Apps are faster and more reliable than traditional web pages, and provide an engaging mobile experience:

 * All static site assets are cached so that your page loads fast on subsequent visits, regardless of network connectivity (such as 2G or 3G). Updates are downloaded in the background.
 * Your app will work regardless of network state, even if offline. This means your users will be able to use your app at 10,000 feet and on the subway.
 * On mobile devices, your app can be added directly to the user's home screen, app icon and all. You can also re-engage users using web **push notifications**. This eliminates the need for the app store.

The [`sw-precache-webpack-plugin`](https://github.com/goldhand/sw-precache-webpack-plugin)
is integrated into production configuration,
and it will take care of generating a service worker file that will automatically
precache all of your local assets and keep them up to date as you deploy updates.
The service worker will use a [cache-first strategy](https://developers.google.com/web/fundamentals/instant-and-offline/offline-cookbook/#cache-falling-back-to-network)
for handling all requests for local assets, including the initial HTML, ensuring
that your web app is reliably fast, even on a slow or unreliable network.

### Opting Out of Caching

If you would prefer not to enable service workers prior to your initial
production deployment, then remove the call to `registerServiceWorker()`
from [`src/index.js`](src/index.js).

If you had previously enabled service workers in your production deployment and
have decided that you would like to disable them for all your existing users,
you can swap out the call to `registerServiceWorker()` in
[`src/index.js`](src/index.js) first by modifying the service worker import:
```javascript
import { unregister } from './registerServiceWorker';
```
and then call `unregister()` instead.
After the user visits a page that has `unregister()`,
the service worker will be uninstalled. Note that depending on how `/service-worker.js` is served,
it may take up to 24 hours for the cache to be invalidated.

### 优先考虑离线

1. Service workers [require HTTPS](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers#you_need_https),
although to facilitate local testing, that policy
[does not apply to `localhost`](http://stackoverflow.com/questions/34160509/options-for-testing-service-workers-via-http/34161385#34161385).
If your production web server does not support HTTPS, then the service worker
registration will fail, but the rest of your web app will remain functional.

1. Service workers are [not currently supported](https://jakearchibald.github.io/isserviceworkerready/)
in all web browsers. Service worker registration [won't be attempted](src/registerServiceWorker.js)
on browsers that lack support.

1. The service worker is only enabled in the [production environment](#deployment),
e.g. the output of `npm run build`. It's recommended that you do not enable an
offline-first service worker in a development environment, as it can lead to
frustration when previously cached assets are used and do not include the latest
changes you've made locally.

1. If you *need* to test your offline-first service worker locally, build
the application (using `npm run build`) and run a simple http server from your
build directory. After running the build script, `create-react-app` will give
instructions for one way to test your production build locally and the [deployment instructions](#deployment) have
instructions for using other methods. *Be sure to always use an
incognito window to avoid complications with your browser cache.*

1. If possible, configure your production environment to serve the generated
`service-worker.js` [with HTTP caching disabled](http://stackoverflow.com/questions/38843970/service-worker-javascript-update-frequency-every-24-hours).
If that's not possible—[GitHub Pages](#github-pages), for instance, does not
allow you to change the default 10 minute HTTP cache lifetime—then be aware
that if you visit your production site, and then revisit again before
`service-worker.js` has expired from your HTTP cache, you'll continue to get
the previously cached assets from the service worker. If you have an immediate
need to view your updated production deployment, performing a shift-refresh
will temporarily disable the service worker and retrieve all assets from the
network.

1. Users aren't always familiar with offline-first web apps. It can be useful to
[let the user know](https://developers.google.com/web/fundamentals/instant-and-offline/offline-ux#inform_the_user_when_the_app_is_ready_for_offline_consumption)
when the service worker has finished populating your caches (showing a "This web
app works offline!" message) and also let them know when the service worker has
fetched the latest updates that will be available the next time they load the
page (showing a "New content is available; please refresh." message). Showing
this messages is currently left as an exercise to the developer, but as a
starting point, you can make use of the logic included in [`src/registerServiceWorker.js`](src/registerServiceWorker.js), which
demonstrates which service worker lifecycle events to listen for to detect each
scenario, and which as a default, just logs appropriate messages to the
JavaScript console.

1. By default, the generated service worker file will not intercept or cache any
cross-origin traffic, like HTTP [API requests](#integrating-with-an-api-backend),
images, or embeds loaded from a different domain. If you would like to use a
runtime caching strategy for those requests, you can [`eject`](#npm-run-eject)
and then configure the
[`runtimeCaching`](https://github.com/GoogleChrome/sw-precache#runtimecaching-arrayobject)
option in the `SWPrecacheWebpackPlugin` section of
[`webpack.config.prod.js`](../config/webpack.config.prod.js).

### PWA(Progressive Web App) 元数据

The default configuration includes a web app manifest located at
[`public/manifest.json`](public/manifest.json), that you can customize with
details specific to your web application.

When a user adds a web app to their homescreen using Chrome or Firefox on
Android, the metadata in [`manifest.json`](public/manifest.json) determines what
icons, names, and branding colors to use when the web app is displayed.
[The Web App Manifest guide](https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/)
provides more context about what each field means, and how your customizations
will affect your users' experience.

## 对打包文件大小的分析

[Source map explorer](https://www.npmjs.com/package/source-map-explorer) analyzes
JavaScript bundles using the source maps. This helps you understand where code
bloat is coming from.

To add Source map explorer to a Create React App project, follow these steps:

```sh
npm install --save source-map-explorer
```

Alternatively you may use `yarn`:

```sh
yarn add source-map-explorer
```

Then in `package.json`, add the following line to `scripts`:

```diff
   "scripts": {
+    "analyze": "source-map-explorer build/static/js/main.*",
     "start": "react-scripts start",
     "build": "react-scripts build",
     "test": "react-scripts test --env=jsdom",
```

Then to analyze the bundle run the production build then run the analyze
script.

```
npm run build
npm run analyze
```

## 部署

`npm run build` creates a `build` directory with a production build of your app. Set up your favorite HTTP server so that a visitor to your site is served `index.html`, and requests to static paths like `/static/js/main.<hash>.js` are served with the contents of the `/static/js/main.<hash>.js` file.

### 静态服务器

For environments using [Node](https://nodejs.org/), the easiest way to handle this would be to install [serve](https://github.com/zeit/serve) and let it handle the rest:

```sh
npm install -g serve
serve -s build
```

The last command shown above will serve your static site on the port **5000**. Like many of [serve](https://github.com/zeit/serve)’s internal settings, the port can be adjusted using the `-p` or `--port` flags.

Run this command to get a full list of the options available:

```sh
serve -h
```

### 其他方案

You don’t necessarily need a static server in order to run a Create React App project in production. It works just as fine integrated into an existing dynamic one.

Here’s a programmatic example using [Node](https://nodejs.org/) and [Express](http://expressjs.com/):

```javascript
const express = require('express');
const path = require('path');
const app = express();

app.use(express.static(path.join(__dirname, 'build')));

app.get('/', function (req, res) {
  res.sendFile(path.join(__dirname, 'build', 'index.html'));
});

app.listen(9000);
```

The choice of your server software isn’t important either. Since Create React App is completely platform-agnostic, there’s no need to explicitly use Node.

The `build` folder with static assets is the only output produced by Create React App.

However this is not quite enough if you use client-side routing. Read the next section if you want to support URLs like `/todos/42` in your single-page app.

### 使用客户端路由的服务端配置

If you use routers that use the HTML5 [`pushState` history API](https://developer.mozilla.org/en-US/docs/Web/API/History_API#Adding_and_modifying_history_entries) under the hood (for example, [React Router](https://github.com/ReactTraining/react-router) with `browserHistory`), many static file servers will fail. For example, if you used React Router with a route for `/todos/42`, the development server will respond to `localhost:3000/todos/42` properly, but an Express serving a production build as above will not.

This is because when there is a fresh page load for a `/todos/42`, the server looks for the file `build/todos/42` and does not find it. The server needs to be configured to respond to a request to `/todos/42` by serving `index.html`. For example, we can amend our Express example above to serve `index.html` for any unknown paths:

```diff
 app.use(express.static(path.join(__dirname, 'build')));

-app.get('/', function (req, res) {
+app.get('/*', function (req, res) {
   res.sendFile(path.join(__dirname, 'build', 'index.html'));
 });
```

If you’re using [Apache HTTP Server](https://httpd.apache.org/), you need to create a `.htaccess` file in the `public` folder that looks like this:

```
    Options -MultiViews
    RewriteEngine On
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteRule ^ index.html [QSA,L]
```

It will get copied to the `build` folder when you run `npm run build`. 

If you’re using [Apache Tomcat](http://tomcat.apache.org/), you need to follow [this Stack Overflow answer](https://stackoverflow.com/a/41249464/4878474).

Now requests to `/todos/42` will be handled correctly both in development and in production.

On a production build, and in a browser that supports [service workers](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers),
the service worker will automatically handle all navigation requests, like for
`/todos/42`, by serving the cached copy of your `index.html`. This
service worker navigation routing can be configured or disabled by
[`eject`ing](#npm-run-eject) and then modifying the
[`navigateFallback`](https://github.com/GoogleChrome/sw-precache#navigatefallback-string)
and [`navigateFallbackWhitelist`](https://github.com/GoogleChrome/sw-precache#navigatefallbackwhitelist-arrayregexp)
options of the `SWPreachePlugin` [configuration](../config/webpack.config.prod.js).

When users install your app to the homescreen of their device the default configuration will make a shortcut to `/index.html`. This may not work for client-side routers which expect the app to be served from `/`. Edit the web app manifest at [`public/manifest.json`](public/manifest.json) and change `start_url` to match the required URL scheme, for example:

```js
  "start_url": ".",
```

### 在构建打包时相对路径的设置

By default, Create React App produces a build assuming your app is hosted at the server root.<br>
To override this, specify the `homepage` in your `package.json`, for example:

```js
  "homepage": "http://mywebsite.com/relativepath",
```

This will let Create React App correctly infer the root path to use in the generated HTML file.

**Note**: If you are using `react-router@^4`, you can root `<Link>`s using the `basename` prop on any `<Router>`.<br>
More information [here](https://reacttraining.com/react-router/web/api/BrowserRouter/basename-string).<br>
<br>
For example:
```js
<BrowserRouter basename="/calendar"/>
<Link to="/today"/> // renders <a href="/calendar/today">
```

#### Serving the Same Build from Different Paths

>Note: this feature is available with `react-scripts@0.9.0` and higher.

If you are not using the HTML5 `pushState` history API or not using client-side routing at all, it is unnecessary to specify the URL from which your app will be served. Instead, you can put this in your `package.json`:

```js
  "homepage": ".",
```

This will make sure that all the asset paths are relative to `index.html`. You will then be able to move your app from `http://mywebsite.com` to `http://mywebsite.com/relativepath` or even `http://mywebsite.com/relative/path` without having to rebuild it.

### [Azure](https://azure.microsoft.com/)

See [this](https://medium.com/@to_pe/deploying-create-react-app-on-microsoft-azure-c0f6686a4321) blog post on how to deploy your React app to Microsoft Azure.

See [this](https://medium.com/@strid/host-create-react-app-on-azure-986bc40d5bf2#.pycfnafbg) blog post or [this](https://github.com/ulrikaugustsson/azure-appservice-static) repo for a way to use automatic deployment to Azure App Service.

### [Firebase](https://firebase.google.com/)

Install the Firebase CLI if you haven’t already by running `npm install -g firebase-tools`. Sign up for a [Firebase account](https://console.firebase.google.com/) and create a new project. Run `firebase login` and login with your previous created Firebase account.

Then run the `firebase init` command from your project’s root. You need to choose the **Hosting: Configure and deploy Firebase Hosting sites** and choose the Firebase project you created in the previous step. You will need to agree with `database.rules.json` being created, choose `build` as the public directory, and also agree to **Configure as a single-page app** by replying with `y`.

```sh
    === Project Setup

    First, let's associate this project directory with a Firebase project.
    You can create multiple project aliases by running firebase use --add,
    but for now we'll just set up a default project.

    ? What Firebase project do you want to associate as default? Example app (example-app-fd690)

    === Database Setup

    Firebase Realtime Database Rules allow you to define how your data should be
    structured and when your data can be read from and written to.

    ? What file should be used for Database Rules? database.rules.json
    ✔  Database Rules for example-app-fd690 have been downloaded to database.rules.json.
    Future modifications to database.rules.json will update Database Rules when you run
    firebase deploy.

    === Hosting Setup

    Your public directory is the folder (relative to your project directory) that
    will contain Hosting assets to uploaded with firebase deploy. If you
    have a build process for your assets, use your build's output directory.

    ? What do you want to use as your public directory? build
    ? Configure as a single-page app (rewrite all urls to /index.html)? Yes
    ✔  Wrote build/index.html

    i  Writing configuration info to firebase.json...
    i  Writing project information to .firebaserc...

    ✔  Firebase initialization complete!
```

IMPORTANT: you need to set proper HTTP caching headers for `service-worker.js` file in `firebase.json` file or you will not be able to see changes after first deployment ([issue #2440](https://github.com/facebookincubator/create-react-app/issues/2440)). It should be added inside `"hosting"` key like next:

```
{
  "hosting": {
    ...
    "headers": [
      {"source": "/service-worker.js", "headers": [{"key": "Cache-Control", "value": "no-cache"}]}
    ]
    ...
```

Now, after you create a production build with `npm run build`, you can deploy it by running `firebase deploy`.

```sh
    === Deploying to 'example-app-fd690'...

    i  deploying database, hosting
    ✔  database: rules ready to deploy.
    i  hosting: preparing build directory for upload...
    Uploading: [==============================          ] 75%✔  hosting: build folder uploaded successfully
    ✔  hosting: 8 files uploaded successfully
    i  starting release process (may take several minutes)...

    ✔  Deploy complete!

    Project Console: https://console.firebase.google.com/project/example-app-fd690/overview
    Hosting URL: https://example-app-fd690.firebaseapp.com
```

For more information see [Add Firebase to your JavaScript Project](https://firebase.google.com/docs/web/setup).

### [GitHub 页面](https://pages.github.com/)

>Note: this feature is available with `react-scripts@0.2.0` and higher.

#### Step 1: Add `homepage` to `package.json`

**The step below is important!**<br>
**If you skip it, your app will not deploy correctly.**

Open your `package.json` and add a `homepage` field for your project:

```json
  "homepage": "https://myusername.github.io/my-app",
```

or for a GitHub user page:

```json
  "homepage": "https://myusername.github.io",
```

Create React App uses the `homepage` field to determine the root URL in the built HTML file.

#### Step 2: Install `gh-pages` and add `deploy` to `scripts` in `package.json`

Now, whenever you run `npm run build`, you will see a cheat sheet with instructions on how to deploy to GitHub Pages.

To publish it at [https://myusername.github.io/my-app](https://myusername.github.io/my-app), run:

```sh
npm install --save gh-pages
```

Alternatively you may use `yarn`:

```sh
yarn add gh-pages
```

Add the following scripts in your `package.json`:

```diff
  "scripts": {
+   "predeploy": "npm run build",
+   "deploy": "gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build",
```

The `predeploy` script will run automatically before `deploy` is run.

If you are deploying to a GitHub user page instead of a project page you'll need to make two
additional modifications:

1. First, change your repository's source branch to be any branch other than **master**.
1. Additionally, tweak your `package.json` scripts to push deployments to **master**:
```diff
  "scripts": {
    "predeploy": "npm run build",
-   "deploy": "gh-pages -d build",
+   "deploy": "gh-pages -b master -d build",
```

#### Step 3: Deploy the site by running `npm run deploy`

Then run:

```sh
npm run deploy
```

#### Step 4: Ensure your project’s settings use `gh-pages`

Finally, make sure **GitHub Pages** option in your GitHub project settings is set to use the `gh-pages` branch:

<img src="http://i.imgur.com/HUjEr9l.png" width="500" alt="gh-pages branch setting">

#### Step 5: Optionally, configure the domain

You can configure a custom domain with GitHub Pages by adding a `CNAME` file to the `public/` folder.

#### Notes on client-side routing

GitHub Pages doesn’t support routers that use the HTML5 `pushState` history API under the hood (for example, React Router using `browserHistory`). This is because when there is a fresh page load for a url like `http://user.github.io/todomvc/todos/42`, where `/todos/42` is a frontend route, the GitHub Pages server returns 404 because it knows nothing of `/todos/42`. If you want to add a router to a project hosted on GitHub Pages, here are a couple of solutions:

* You could switch from using HTML5 history API to routing with hashes. If you use React Router, you can switch to `hashHistory` for this effect, but the URL will be longer and more verbose (for example, `http://user.github.io/todomvc/#/todos/42?_k=yknaj`). [Read more](https://reacttraining.com/react-router/web/api/Router) about different history implementations in React Router.
* Alternatively, you can use a trick to teach GitHub Pages to handle 404 by redirecting to your `index.html` page with a special redirect parameter. You would need to add a `404.html` file with the redirection code to the `build` folder before deploying your project, and you’ll need to add code handling the redirect parameter to `index.html`. You can find a detailed explanation of this technique [in this guide](https://github.com/rafrex/spa-github-pages).

#### Troubleshooting

##### "/dev/tty: No such a device or address"

If, when deploying, you get `/dev/tty: No such a device or address` or a similar error, try the follwing:

1. Create a new [Personal Access Token](https://github.com/settings/tokens)
2. `git remote set-url origin https://<user>:<token>@github.com/<user>/<repo>` .
3. Try `npm run deploy again`

### [Heroku](https://www.heroku.com/)

Use the [Heroku Buildpack for Create React App](https://github.com/mars/create-react-app-buildpack).<br>
You can find instructions in [Deploying React with Zero Configuration](https://blog.heroku.com/deploying-react-with-zero-configuration).

#### Resolving Heroku Deployment Errors

Sometimes `npm run build` works locally but fails during deploy via Heroku. Following are the most common cases.

##### "Module not found: Error: Cannot resolve 'file' or 'directory'"

If you get something like this:

```
remote: Failed to create a production build. Reason:
remote: Module not found: Error: Cannot resolve 'file' or 'directory'
MyDirectory in /tmp/build_1234/src
```

It means you need to ensure that the lettercase of the file or directory you `import` matches the one you see on your filesystem or on GitHub.

This is important because Linux (the operating system used by Heroku) is case sensitive. So `MyDirectory` and `mydirectory` are two distinct directories and thus, even though the project builds locally, the difference in case breaks the `import` statements on Heroku remotes.

##### "Could not find a required file."

If you exclude or ignore necessary files from the package you will see a error similar this one:

```
remote: Could not find a required file.
remote:   Name: `index.html`
remote:   Searched in: /tmp/build_a2875fc163b209225122d68916f1d4df/public
remote:
remote: npm ERR! Linux 3.13.0-105-generic
remote: npm ERR! argv "/tmp/build_a2875fc163b209225122d68916f1d4df/.heroku/node/bin/node" "/tmp/build_a2875fc163b209225122d68916f1d4df/.heroku/node/bin/npm" "run" "build"
```

In this case, ensure that the file is there with the proper lettercase and that’s not ignored on your local `.gitignore` or `~/.gitignore_global`.

### [Netlify](https://www.netlify.com/)

**To do a manual deploy to Netlify’s CDN:**

```sh
npm install netlify-cli -g
netlify deploy
```

Choose `build` as the path to deploy.

**To setup continuous delivery:**

With this setup Netlify will build and deploy when you push to git or open a pull request:

1. [Start a new netlify project](https://app.netlify.com/signup)
2. Pick your Git hosting service and select your repository
3. Set `yarn build` as the build command and `build` as the publish directory
4. Click `Deploy site`

**Support for client-side routing:**

To support `pushState`, make sure to create a `public/_redirects` file with the following rewrite rules:

```
/*  /index.html  200
```

When you build the project, Create React App will place the `public` folder contents into the build output.

### [Now](https://zeit.co/now)

Now offers a zero-configuration single-command deployment. You can use `now` to deploy your app for free.

1. Install the `now` command-line tool either via the recommended [desktop tool](https://zeit.co/download) or via node with `npm install -g now`.

2. Build your app by running `npm run build`.

3. Move into the build directory by running `cd build`.

4. Run `now --name your-project-name` from within the build directory. You will see a **now.sh** URL in your output like this:

    ```
    > Ready! https://your-project-name-tpspyhtdtk.now.sh (copied to clipboard)
    ```

    Paste that URL into your browser when the build is complete, and you will see your deployed app.

Details are available in [this article.](https://zeit.co/blog/unlimited-static)

### [S3](https://aws.amazon.com/s3) 和 [CloudFront](https://aws.amazon.com/cloudfront/)

See this [blog post](https://medium.com/@omgwtfmarc/deploying-create-react-app-to-s3-or-cloudfront-48dae4ce0af) on how to deploy your React app to Amazon Web Services S3 and CloudFront.

### [Surge](https://surge.sh/)

Install the Surge CLI if you haven’t already by running `npm install -g surge`. Run the `surge` command and log in you or create a new account.

When asked about the project path, make sure to specify the `build` folder, for example:

```sh
       project path: /path/to/project/build
```

Note that in order to support routers that use HTML5 `pushState` API, you may want to rename the `index.html` in your build folder to `200.html` before deploying to Surge. This [ensures that every URL falls back to that file](https://surge.sh/help/adding-a-200-page-for-client-side-routing).

## 高级配置

You can adjust various development and production settings by setting environment variables in your shell or with [.env](#adding-development-environment-variables-in-env).

Variable | Development | Production | Usage
:--- | :---: | :---: | :---
BROWSER | :white_check_mark: | :x: | By default, Create React App will open the default system browser, favoring Chrome on macOS. Specify a [browser](https://github.com/sindresorhus/opn#app) to override this behavior, or set it to `none` to disable it completely. If you need to customize the way the browser is launched, you can specify a node script instead. Any arguments passed to `npm start` will also be passed to this script, and the url where your app is served will be the last argument. Your script's file name must have the `.js` extension.
HOST | :white_check_mark: | :x: | By default, the development web server binds to `localhost`. You may use this variable to specify a different host.
PORT | :white_check_mark: | :x: | By default, the development web server will attempt to listen on port 3000 or prompt you to attempt the next available port. You may use this variable to specify a different port.
HTTPS | :white_check_mark: | :x: | When set to `true`, Create React App will run the development server in `https` mode.
PUBLIC_URL | :x: | :white_check_mark: | Create React App assumes your application is hosted at the serving web server's root or a subpath as specified in [`package.json` (`homepage`)](#building-for-relative-paths). Normally, Create React App ignores the hostname. You may use this variable to force assets to be referenced verbatim to the url you provide (hostname included). This may be particularly useful when using a CDN to host your application.
CI | :large_orange_diamond: | :white_check_mark: | When set to `true`, Create React App treats warnings as failures in the build. It also makes the test runner non-watching. Most CIs set this flag by default.
REACT_EDITOR | :white_check_mark: | :x: | When an app crashes in development, you will see an error overlay with clickable stack trace. When you click on it, Create React App will try to determine the editor you are using based on currently running processes, and open the relevant source file. You can [send a pull request to detect your editor of choice](https://github.com/facebookincubator/create-react-app/issues/2636). Setting this environment variable overrides the automatic detection. If you do it, make sure your systems [PATH](https://en.wikipedia.org/wiki/PATH_(variable)) environment variable points to your editor’s bin folder. You can also set it to `none` to disable it completely.
CHOKIDAR_USEPOLLING | :white_check_mark: | :x: | When set to `true`, the watcher runs in polling mode, as necessary inside a VM. Use this option if `npm start` isn't detecting changes.
GENERATE_SOURCEMAP | :x: | :white_check_mark: | When set to `false`, source maps are not generated for a production build. This solves OOM issues on some smaller machines.
NODE_PATH | :white_check_mark: |  :white_check_mark: | Same as [`NODE_PATH` in Node.js](https://nodejs.org/api/modules.html#modules_loading_from_the_global_folders), but only relative folders are allowed. Can be handy for emulating a monorepo setup by setting `NODE_PATH=src`.

## 问题排查

### `npm start` 后检测不到变化

When you save a file while `npm start` is running, the browser should refresh with the updated code.<br>
If this doesn’t happen, try one of the following workarounds:

* If your project is in a Dropbox folder, try moving it out.
* If the watcher doesn’t see a file called `index.js` and you’re referencing it by the folder name, you [need to restart the watcher](https://github.com/facebookincubator/create-react-app/issues/1164) due to a Webpack bug.
* Some editors like Vim and IntelliJ have a “safe write” feature that currently breaks the watcher. You will need to disable it. Follow the instructions in [“Adjusting Your Text Editor”](https://webpack.js.org/guides/development/#adjusting-your-text-editor).
* If your project path contains parentheses, try moving the project to a path without them. This is caused by a [Webpack watcher bug](https://github.com/webpack/watchpack/issues/42).
* On Linux and macOS, you might need to [tweak system settings](https://github.com/webpack/docs/wiki/troubleshooting#not-enough-watchers) to allow more watchers.
* If the project runs inside a virtual machine such as (a Vagrant provisioned) VirtualBox, create an `.env` file in your project directory if it doesn’t exist, and add `CHOKIDAR_USEPOLLING=true` to it. This ensures that the next time you run `npm start`, the watcher uses the polling mode, as necessary inside a VM.

If none of these solutions help please leave a comment [in this thread](https://github.com/facebookincubator/create-react-app/issues/659).

### `npm test` 在 macOS Sierra 运行被挂起

If you run `npm test` and the console gets stuck after printing `react-scripts test --env=jsdom` to the console there might be a problem with your [Watchman](https://facebook.github.io/watchman/) installation as described in [facebookincubator/create-react-app#713](https://github.com/facebookincubator/create-react-app/issues/713).

We recommend deleting `node_modules` in your project and running `npm install` (or `yarn` if you use it) first. If it doesn't help, you can try one of the numerous workarounds mentioned in these issues:

* [facebook/jest#1767](https://github.com/facebook/jest/issues/1767)
* [facebook/watchman#358](https://github.com/facebook/watchman/issues/358)
* [ember-cli/ember-cli#6259](https://github.com/ember-cli/ember-cli/issues/6259)

It is reported that installing Watchman 4.7.0 or newer fixes the issue. If you use [Homebrew](http://brew.sh/), you can run these commands to update it:

```
watchman shutdown-server
brew update
brew reinstall watchman
```

You can find [other installation methods](https://facebook.github.io/watchman/docs/install.html#build-install) on the Watchman documentation page.

If this still doesn’t help, try running `launchctl unload -F ~/Library/LaunchAgents/com.github.facebook.watchman.plist`.

There are also reports that *uninstalling* Watchman fixes the issue. So if nothing else helps, remove it from your system and try again.

### `npm run build` 提前退出

It is reported that `npm run build` can fail on machines with limited memory and no swap space, which is common in cloud environments. Even with small projects this command can increase RAM usage in your system by hundreds of megabytes, so if you have less than 1 GB of available memory your build is likely to fail with the following message:

>  The build failed because the process exited too early. This probably means the system ran out of memory or someone called `kill -9` on the process.

If you are completely sure that you didn't terminate the process, consider [adding some swap space](https://www.digitalocean.com/community/tutorials/how-to-add-swap-on-ubuntu-14-04) to the machine you’re building on, or build the project locally.

### `npm run build` 在 Heroku 执行失败

This may be a problem with case sensitive filenames.
Please refer to [this section](#resolving-heroku-deployment-errors).

### Moment.js 缺少语言支持

If you use a [Moment.js](https://momentjs.com/), you might notice that only the English locale is available by default. This is because the locale files are large, and you probably only need a subset of [all the locales provided by Moment.js](https://momentjs.com/#multiple-locale-support).

To add a specific Moment.js locale to your bundle, you need to import it explicitly.<br>
For example:

```js
import moment from 'moment';
import 'moment/locale/fr';
```

If import multiple locales this way, you can later switch between them by calling `moment.locale()` with the locale name:

```js
import moment from 'moment';
import 'moment/locale/fr';
import 'moment/locale/es';

// ...

moment.locale('fr');
```

This will only work for locales that have been explicitly imported before.

### `npm run build` fails to minify

Some third-party packages don't compile their code to ES5 before publishing to npm. This often causes problems in the ecosystem because neither browsers (except for most modern versions) nor some tools currently support all ES6 features. We recommend to publish code on npm as ES5 at least for a few more years.

<br>
To resolve this:

1. Open an issue on the dependency's issue tracker and ask that the package be published pre-compiled.
  * Note: Create React App can consume both CommonJS and ES modules. For Node.js compatibility, it is recommended that the main entry point is CommonJS. However, they can optionally provide an ES module entry point with the `module` field in `package.json`. Note that **even if a library provides an ES Modules version, it should still precompile other ES6 features to ES5 if it intends to support older browsers**.

2. Fork the package and publish a corrected version yourself. 

3. If the dependency is small enough, copy it to your `src/` folder and treat it as application code.

In the future, we might start automatically compiling incompatible third-party modules, but it is not currently supported. This approach would also slow down the production builds.

## Eject 替代方案

[Ejecting](#npm-run-eject) lets you customize anything, but from that point on you have to maintain the configuration and scripts yourself. This can be daunting if you have many similar projects. In such cases instead of ejecting we recommend to *fork* `react-scripts` and any other packages you need. [This article](https://auth0.com/blog/how-to-configure-create-react-app/) dives into how to do it in depth. You can find more discussion in [this issue](https://github.com/facebookincubator/create-react-app/issues/682).

## 您觉得不足之处

If you have ideas for more “How To” recipes that should be on this page, [let us know](https://github.com/facebookincubator/create-react-app/issues) or [contribute some!](https://github.com/facebookincubator/create-react-app/edit/master/packages/react-scripts/template/README.md)
