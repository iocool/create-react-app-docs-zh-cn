# 写在前面的话

``最近在看 react 但是发现 create-react-app 文档是英文的,于是想着在学习的过程中顺便翻译一下文档,文档与原版项目的目录内容保持一致,由于本人英语水平有限,翻译过程中难免会有错误,还请各位大佬指出,谢谢!``

英文原版 [Create React App](https://github.com/facebook/create-react-app)

# Create React App 中文文档

创建无需构建配置的 React 应用.

* [创建应用](#创建应用) – 如何创建一个新的应用.
* [用户指南](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md)   – 如何使用 Create React App 引导开发应用.

Create React App 适用于 MacOs Windows 和 Linux.<br>
如果在使用过程中出现任何问题,请提交 [issue](https://github.com/facebookincubator/create-react-app/issues/new).

## 快速开始

```sh
npx create-react-app my-app
cd my-app
npm start
```

*([npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) 命令在 npm 5.2及以上版本可以使用,详情参见 [历史 npm 版本说明](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f))*

执行完上述命令后,浏览器默认会通过 [http://localhost:3000/](http://localhost:3000/) 打开你的项目. <br>
当准备部署到生产环境的时候, 使用 `npm run build` 命令可构建一个压缩版的项目.

<p align='center'>
<img src='https://cdn.rawgit.com/facebookincubator/create-react-app/6ab67e6b96457720d843aa3c557ff951a41bafc2/screencast.svg' width='600' alt=''>
</p>

### 立即开始

**不需要** 安装或配置类似 webpack 或者 Babel 类的工具. <br>
大部分配置都是预先配置好的,项目中是看不到这些配置的,这样的话我们就可以专注于代码的书写而不用过多的在意项目该如何配置.

只需要创建一个项目,所有的一切就都搞定了.

## 创建应用

**注意:本地开发机环境的 node 版本要求 6及以上版本**(在服务器上不需要).可以使用 node 版本管理工具 [nvm](https://github.com/creationix/nvm#installation) (在 macOS/Linux 上) 或者 [nvm-windows](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows) (在 Windows 上),方便切换不同的 node 版本.

要创建应用,使用以下任意一条命令即可:

### npx

```sh
npx create-react-app my-app
```

*([npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) 命令在 npm 5.2及以上版本可以使用,详情参见 [历史 npm 版本说明](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f))*

### npm

```sh
npm init react-app my-app
```
*`npm init <initializer>` 在 npm 6 版本及以上可用*

### Yarn

```sh
yarn create react-app my-app
```
*`yarn create` 在 Yarn 0.25 及以上版本可用*

以上命令将会在当前文件夹创建一个名为 `my-app` 的目录. <br>
在新建的目录中,会生成初始的项目结构,并安装相应的依赖项:

```
my-app
├── README.md
├── node_modules
├── package.json
├── .gitignore
├── public
│   ├── favicon.ico
│   ├── index.html
│   └── manifest.json
└── src
    ├── App.css
    ├── App.js
    ├── App.test.js
    ├── index.css
    ├── index.js
    ├── logo.svg
    └── registerServiceWorker.js
```

不会产生多余的配置文件或复杂的文件结构,只有构建应用所需的文件.<br>
安装完成后,打开项目文件夹:

```sh
cd my-app
```

在新创建的项目中,就可以运行一些内置的命令:

### `npm start` 或 `yarn start`

在开发模式 (development mode) 下运行应用.<br>
在浏览器中访问 [http://localhost:3000](http://localhost:3000) ,可以查看页面.

如果代码有修改,将自动重新加载页面.<br>
构建过程中,出现的错误信息和 lint 警告信息会显示在控制台中.

<p align='center'>
<img src='https://cdn.rawgit.com/marionebl/create-react-app/9f62826/screencast-error.svg' width='600' alt='Build errors'>
</p>

### `npm test` 或 `yarn test`

在交互模式下运行测试监测 (test wathcer) .<br>
默认会测试最近提交修改后的文件.<br>
(注: 原文: By default, runs tests related to files changed since the last commit. 此处翻译或许有问题,后续修改)

[详细了解测试](https://github.com/iocool/create-react-app-docs-zh-cn/tree/master/guide#%E8%BF%90%E8%A1%8C%E6%B5%8B%E8%AF%95-test)

### `npm run build` 或 `yarn build`

在构建 (build) 模式下,会在 `build` 文件目录中生成用以生产环境的应用.<br>
build 模式将会合理的将 react 项目打包,并进行足够的优化,以保证在生产环境中获得最佳的性能.

build 模式会尽可能的压缩打包文件,并在打包的文件名中加入文件内容的 hash.<br>
通常情况下,还包括一个 [service worker](https://github.com/iocool/create-react-app-docs-zh-cn/tree/master/guide#%E5%BC%80%E5%8F%91%E6%B8%90%E8%BF%9B%E5%BC%8F%E7%BD%91%E9%A1%B5%E5%BA%94%E7%94%A8-pwa%E5%8D%B3-progressive-web-app) ,以便于后续访问应用的时候直接从本地缓存中加载. <br>
到这里,应用程序已经可以进行部署了.

## 用户指南

[用户指南](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md) 包括不同的主题,详情参见下面列表:

- [更新到最新版](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%9B%B4%E6%96%B0%E5%88%B0%E6%9C%80%E6%96%B0%E7%89%88)
- [文件结构](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%96%87%E4%BB%B6%E7%BB%93%E6%9E%84)
- [script配置信息](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#script%E9%85%8D%E7%BD%AE%E4%BF%A1%E6%81%AF)
- [浏览器支持](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%B5%8F%E8%A7%88%E5%99%A8%E6%94%AF%E6%8C%81)
- [支持的语法特点及 Polyfill](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%94%AF%E6%8C%81%E7%9A%84%E8%AF%AD%E6%B3%95%E7%89%B9%E7%82%B9%E5%8F%8A-polyfill)
- [编辑器中的语法高亮](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E7%BC%96%E8%BE%91%E5%99%A8%E4%B8%AD%E7%9A%84%E8%AF%AD%E6%B3%95%E9%AB%98%E4%BA%AE)
- [编辑器中 Lint 信息显示](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E7%BC%96%E8%BE%91%E5%99%A8%E4%B8%AD-lint-%E4%BF%A1%E6%81%AF%E6%98%BE%E7%A4%BA)
- [代码自动格式化](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E4%BB%A3%E7%A0%81%E8%87%AA%E5%8A%A8%E6%A0%BC%E5%BC%8F%E5%8C%96)
- [编辑器中进行调试](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E7%BC%96%E8%BE%91%E5%99%A8%E4%B8%AD%E8%BF%9B%E8%A1%8C%E8%B0%83%E8%AF%95)
- [修改页面标题 `<title>`](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E4%BF%AE%E6%94%B9%E9%A1%B5%E9%9D%A2%E6%A0%87%E9%A2%98)
- [安装依赖项](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%AE%89%E8%A3%85%E4%BE%9D%E8%B5%96%E9%A1%B9)
- [组件引入](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E7%BB%84%E4%BB%B6%E5%BC%95%E5%85%A5)
- [代码拆分](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E4%BB%A3%E7%A0%81%E6%8B%86%E5%88%86)
- [样式添加](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%A0%B7%E5%BC%8F%E6%B7%BB%E5%8A%A0)
- [CSS 处理](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#css%E5%A4%84%E7%90%86)
- [添加CSS 预处理器 (如Sass, Less 等.)](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%B7%BB%E5%8A%A0-css-%E9%A2%84%E5%A4%84%E7%90%86%E5%99%A8%E5%A6%82-sass-less-%E7%AD%89)
- [图像, 字体和文件的添加](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%9B%BE%E5%83%8F%E5%AD%97%E4%BD%93%E5%92%8C%E6%96%87%E4%BB%B6%E7%9A%84%E6%B7%BB%E5%8A%A0)
- [`public` 文件夹的使用](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#public-%E6%96%87%E4%BB%B6%E5%A4%B9%E7%9A%84%E4%BD%BF%E7%94%A8)
- [全局变量的使用](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%85%A8%E5%B1%80%E5%8F%98%E9%87%8F%E7%9A%84%E4%BD%BF%E7%94%A8)
- [添加 Bootstrap](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%B7%BB%E5%8A%A0-bootstrap)
- [添加 Flow](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%B7%BB%E5%8A%A0-flow)
- [添加路由 Router](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%B7%BB%E5%8A%A0%E8%B7%AF%E7%94%B1-router)
- [添加自定义环境变量](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%B7%BB%E5%8A%A0%E8%87%AA%E5%AE%9A%E4%B9%89%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F)
- [能否使用修饰器](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E8%83%BD%E5%90%A6%E4%BD%BF%E7%94%A8%E4%BF%AE%E9%A5%B0%E5%99%A8)
- [使用 AJAX 请求数据](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E4%BD%BF%E7%94%A8-ajax-%E8%AF%B7%E6%B1%82%E6%95%B0%E6%8D%AE)
- [与后端的 API 集成](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E4%B8%8E%E5%90%8E%E7%AB%AF%E7%9A%84-api-%E9%9B%86%E6%88%90)
- [在开发中使用代理 API 请求](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%9C%A8%E5%BC%80%E5%8F%91%E4%B8%AD%E4%BD%BF%E7%94%A8%E4%BB%A3%E7%90%86-api-%E8%AF%B7%E6%B1%82)
- [在开发中使用 HTTPS](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%9C%A8%E5%BC%80%E5%8F%91%E4%B8%AD%E4%BD%BF%E7%94%A8-https)
- [在服务器上生成动态 `<meta>` 标签](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%9C%A8%E6%9C%8D%E5%8A%A1%E5%99%A8%E4%B8%8A%E7%94%9F%E6%88%90%E5%8A%A8%E6%80%81-meta-%E6%A0%87%E7%AD%BE)
- [预加载静态 HTML 文件](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E9%A2%84%E5%8A%A0%E8%BD%BD%E9%9D%99%E6%80%81-html-%E6%96%87%E4%BB%B6)
- [运行测试 TEST](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E8%BF%90%E8%A1%8C%E6%B5%8B%E8%AF%95-test)
- [调试测试 TEST](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E8%B0%83%E8%AF%95%E6%B5%8B%E8%AF%95-test)
- [开发独立组件 Components ](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%BC%80%E5%8F%91%E7%8B%AC%E7%AB%8B%E7%BB%84%E4%BB%B6-components)
- [发布组件 Components 到 npm](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%8F%91%E5%B8%83%E7%BB%84%E4%BB%B6-components-%E5%88%B0-npm)
- [开发渐进式网页应用 (PWA,即 Progressive Web App)](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%BC%80%E5%8F%91%E6%B8%90%E8%BF%9B%E5%BC%8F%E7%BD%91%E9%A1%B5%E5%BA%94%E7%94%A8-pwa%E5%8D%B3-progressive-web-app)
- [对打包文件大小的分析](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%AF%B9%E6%89%93%E5%8C%85%E6%96%87%E4%BB%B6%E5%A4%A7%E5%B0%8F%E7%9A%84%E5%88%86%E6%9E%90)
- [部署](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E9%83%A8%E7%BD%B2)
- [高级配置](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E9%AB%98%E7%BA%A7%E9%85%8D%E7%BD%AE)
- [问题排查](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E9%97%AE%E9%A2%98%E6%8E%92%E6%9F%A5)

在你的项目文件夹中会创建以户指南的副本为内容的 `README.md` 文件

## 如何更新到最新版本?

有关此信息,请参阅 [用户指南](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E6%9B%B4%E6%96%B0%E5%88%B0%E6%9C%80%E6%96%B0%E7%89%88)

## 设计思想(Philosophy)

* **一个依赖:** 只需一个构建依赖. 其中用到了 Webpack, Babel, ESLint, 以及其他的一些相当出色的项目, 将这些资源进行统一合理的整合,以提供一种更加出色的开发体验.

* **无需配置:** 无需进行任何配置.针对开发环境和生产环境下会分别提供相应的合理配置信息,以便于我们可以更专注于代码的编写. 

* **无锁定:** 可以随时使用 `eject`功能,使用户自己接管所有配置项,运行这一命令后,所有的配置和构建依赖都会移动到项目中,因此可以从上次停止的地方继续操作.

## 包含内容

项目环境中会涵盖构建单页 REACT 应用所需的一切:

* React, JSX, ES6, 及 Flow 语法支持.
* 超出 ES6 语言附加功能, 如对象扩展运算符等.
* CSS 前缀自动补全 (Autoprefixed CSS) , 不再需要 如 `-webkit-` 或其他前缀.
* 快速交互单元测试运行工具, 可输出相应的测试报告.
* 启动即时开发服务器, 可实时显示常见的警告及错误.
* 针对生产环境的构建配置脚本,用以对 JS, CSS 及图片资源打包, 并包含相应的文件 hash 值和资源映射等.
* 优先加载离线资源 [service worker](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers) 和 [web app manifest](https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/), 满足 [PWA 标准 (Progressive Web App)](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#%E5%BC%80%E5%8F%91%E6%B8%90%E8%BF%9B%E5%BC%8F%E7%BD%91%E9%A1%B5%E5%BA%94%E7%94%A8-pwa%E5%8D%B3-progressive-web-app).
* 仅使用单个的依赖项即可对上述工具进行更新.

查看[指南](https://github.com/nitishdayal/cra_closer_look)中概述信息,了解上述工具如何组合使用.

在一些特殊情况下,以上工具都会被 **预先配置好**,这也是一个折中的方案.如果希望更多的配置,或自定义配置,可以使用 [eject](https://github.com/iocool/create-react-app-docs-zh-cn/blob/master/guide/README.md#npm-run-eject) 命令来自定义,当然后续的配置都得由我们自己来进行维护.

## 其他热门的方案

Create React App 适用于这些场景:

* 相对功能丰富,开发便捷的开发环境下 **学习 React** .
* **新的 React 单页应用.**
* 使用 React 为库和组件**创建实例**.

以下是一些常见的问题以及问题处理办法:

* 如果需要使用没有依赖项以及一些构建工具项的 React ,可以使用 [单个HTML文件或在线沙箱](https://reactjs.org/docs/try-react.html)

* 如果需要将 React 与服务器端模板框架（如 Rails 或 Django ）集成，或者不构建单页应用程序，请考虑使用更灵活的[nwb](https://github.com/insin/nwb) 或 [Neutrino](https://neutrino.js.org/). 特别是 Rails，可以使用 [Rails Webpacker](https://github.com/rails/webpacker).

* 如果需要发布 **React 组件** ,[nwb](https://github.com/insin/nwb) [也可以执行该操作](https://github.com/insin/nwb#react-components-and-libraries),当然使用 [Neutrino's react-components preset](https://neutrino.js.org/packages/react-components/)也可以.

* 如果想使用  React 和 Node.js 进行 **服务端渲染**, 可以查看 [Next.js](https://github.com/zeit/next.js/) 或 [Razzle](https://github.com/jaredpalmer/razzle). 创建 React App 与后端无关，这些工具只会生成静态的 HTML / JS / CSS 包.

* 如果网站以**静态**为主(如公司机构或博客),可使用 [Gatsby](https://www.gatsbyjs.org/) .与Create React App 不同,在构建时只会以 HTML 形式展现.

* 如果要使用 **TypeScript**, 请参照 [create-react-app-typescript](https://github.com/wmonk/create-react-app-typescript).

* 如果是使用 **Parcel** 替代 **Webpack** 作为打包工具, 请使用 [create-react-app-parcel](https://github.com/sw-yx/create-react-app-parcel).

* 最后,如果需要 **更多的定制**, 请参照 [Neutrino](https://neutrino.js.org/) 以及 [React preset](https://neutrino.js.org/packages/react/).

以上所有工具都可以在少量配置甚至没有配置的情况下正常工作.

如果更多倾向于自己配置以及构建项目,请参照 [指南](https://reactjs.org/docs/add-react-to-an-existing-app.html) 进行配置操作.

## 贡献

我们很乐意在 `create-react-app` 这个项目上提供帮助! 有关目前我们在探索的以及一些如何入门的更多信息,请参阅 [CONTRIBUTING.md](https://github.com/facebook/create-react-app/blob/next/CONTRIBUTING.md)

## React Native

在 React Native 中遇到类似的问题,可参阅 [Create React Native App](https://github.com/react-community/create-react-native-app/).

## 致谢

我们感谢相关项目的作者通力的合作,以及他们付出的精力

* [@eanplatter](https://github.com/eanplatter)
* [@insin](https://github.com/insin)
* [@mxstbr](https://github.com/mxstbr)

## 许可证

Create React App 遵循 [MIT 许可证](https://github.com/facebook/create-react-app/blob/master/LICENSE). 
