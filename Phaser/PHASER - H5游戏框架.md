Phaser 是一个快速，免费且有趣的开源 HTML5 游戏框架，可在桌面和移动Web浏览器中提供 WebGL 和 Canvas 渲染。游戏可以使用第三方工具编译成为 iOS、安卓和桌面应用程序。您可以使用JavaScript或TypeScript进行开发。

除了出色的开源社区外，Phaser还由[Photon Storm](http://www.photonstorm.com)积极开发和维护。由于快速的支持和开发人员友好的API，Phaser目前是GitHub上[最受关注](https://github.com/collections/javascript-game-engines)的游戏框架之一。

成千上万独立或跨国数字机构以及全球许多大学的开发人员使用Phaser。你可以看看他们开发的出色的[游戏](https://phaser.io/games/)。

**访问：** [Phaser 的主页](https://phaser.io) 并关注 [Phaser 的 Twitter](https://twitter.com/phaser_) **游玩**一些令人惊讶的游戏[#madewithphaser](https://twitter.com/search?q=%23madewithphaser&src=typed_query&f=live)  
**学习：** [API 文档](https://photonstorm.github.io/phaser3-docs/index.html), [帮助论坛](https://phaser.discourse.group/) 和 [StackOverflow](https://stackoverflow.com/questions/tagged/phaser-framework)  
**代码：** 1770余[例](https://phaser.io/examples) ([源码](https://github.com/photonstorm/phaser3-examples)在这里)  
**Discord:** 在 [Discord](https://phaser.io/community/discord) 中加入我们 
**扩展：** [Phaser 插件](https://phaser.io/shop/plugins) 
**捐助：** [支持](https://phaser.io/community/donate) Phaser 的未来

下载源码然后一起玩吧！

## What's New？

这块就不翻了。

## 帮助 Phaser 变得更好

因为Phaser是一个开源项目，我们不能像传统零售软件那样收费。更重要的是，我们从来都不想这样做。毕竟，它是建立在开放网络标准之上的，并且是从开放网络标准中诞生的。这是我们宣言的一部分，核心框架将永远是免费的，即使你像你们中的许多人一样在商业上使用它。 
**你可能没有意识到，但正因为如此，我们100%依靠社区支持来资助发展。**
这些资金使Phaser得以改善，当它改善时，所有相关人员都会受益。您的支持有助于确保不断更新、修复、新功能和规划未来。

我们使用 [Patreon](https://www.patreon.com/photonstorm) 来管理资金，您可以从每月1美元起[为 Phaser 提供支持](https://www.patreon.com/join/photonstorm?)。你承诺的金额完全由你决定，可以随时更改。Patreon每月更新一次，就像Netflix一样。当然，你可以随时取消。眼泪会为此而流，但这不是你关心的。

## 下载 Phaser
Phaser 3可通过 GitHub、npm 和 CDN 获得：
-  通过 [https](https://github.com/photonstorm/phaser.git), [ssh](https://photonstorm.github.io/phaser3-docs/git@github.com:photonstorm/phaser.git) 或者 [Windows](github-windows://openRepo/https://github.com/photonstorm/phaser) 和 [Mac](github-mac://openRepo/https://github.com/photonstorm/phaser) 客户端克隆Git仓库
-   以[压缩文件](https://github.com/photonstorm/phaser/archive/master.zip) 下载
-   下载完成编译的 [phaser.js](https://github.com/photonstorm/phaser/releases/download/v3.51.0/phaser.js) 和 [phaser.min.js](https://github.com/photonstorm/phaser/releases/download/v3.51.0/phaser.min.js)

### NPM
通过 [npm](https://www.npmjs.com) 下载
```bash
npm install phaser
```
### CDN
[Phaser 在 jsDelivr 上](https://www.jsdelivr.com/projects/phaser)，这是一个 "面向开发者的超快 CDN"。在 html 代码中添加以下内容：
```html
<script src="//cdn.jsdelivr.net/npm/phaser@3.51.0/dist/phaser.js"></script>
```
或最小化版本。
```html
<script src="//cdn.jsdelivr.net/npm/phaser@3.51.0/dist/phaser.min.js"></script>
```

### API 文档

进入(https://photonstorm.github.io/phaser3-docs/index.html)，在线阅读文档。使用顶部的下拉菜单来浏览命名空间、类和游戏对象列表。

或者，如果你想在本地运行文档，你可以签出[phaser3-docs库](https://github.com/photonstorm/phaser3-docs)，然后将浏览器指向docs/文件夹来阅读文档。

Phaser 3的文档是一个持续的项目。请帮助我们改进文档和例子。

### TypeScript定义

[TypeScript的定义](https://github.com/photonstorm/phaser/tree/master/types)可以在`types`文件夹中找到。他们也在`package.json`的`types`条目中被引用。

根据你的项目，你可能需要添加以下内容到你的`tsconfig.json`文件。
```JSON
"typeRoots": [
    "./node_modules/phaser/types"
],
"types": [
    "Phaser"
]
```
我们最近发布了一个新的[Phaser 3 TypeScript项目模板](https://github.com/photonstorm/phaser3-typescript-project-template)，如果你喜欢，可以用它来入门。

TS defs是由Phaser源代码中的JSDoc注释自动生成的。如果你想帮助完善它们，那么你必须直接编辑Phaser JSDoc块，而不是defs文件。你可以在`scripts/tsgen`文件夹中找到更多关于我们构建的解析器的细节。

### Webpack

我们使用Webpack来构建Phaser，并利用其条件性构建标志功能来处理渲染器的交换。如果你想在Phaser中使用Webpack，请使用我们的[Phaser 3项目模板](https://github.com/photonstorm/phaser3-project-template)，因为它已经设置好了Phaser所需的构建条件。最近我们对构建步骤进行了修改，这意味着你现在可以使用任何其他的打包器，比如Parcel，而不需要修改任何配置。

### 许可证

Phaser是在[MIT许可](https://opensource.org/licenses/MIT)下发布的。

## 开始

关于Phaser 3开发的教程和指南每周都在发布。
- [Phaser 3 入门](https://phaser.io/tutorials/getting-started-phaser3)（如果您完全不熟悉 Phaser，则很有用）
- [制作您的第一个 Phaser 3 游戏](https://phaser.io/tutorials/making-your-first-phaser-3-game)
- 完整的 [Phaser 3 游戏开发课程](https://academy.zenva.com/product/html5-game-phaser-mini-degree/?a=13)包含超过 15 小时的视频，涵盖各种重要主题。
- 此外，官方网站上列出了[ 700 多个 Phaser 教程](http://phaser.io/learn)。

我们有 3 个专门与使用 Phaser 创建 Facebook Instant Games 相关的教程：
- [Facebook Instant Games 入门](http://phaser.io/news/2018/10/facebook-instant-games-phaser-tutorial)
- [Facebook Instant Games 排行榜教程](http://phaser.io/news/2018/11/facebook-instant-games-leaderboards-tutorial)
- [在您的小游戏中展示广告](http://phaser.io/news/2018/12/facebook-instant-games-ads-tutorial)

### 源代码示例

在 Phaser 3 的开发过程中，我们创建了数百个示例，其中包含完整的源代码和可用资产。 这些示例现已完全集成到 [Phaser 网站](https://phaser.io/examples)。 您还可以通过更高级的界面在 [Phaser 3 Labs](https://labs.phaser.io) 上浏览它们，或克隆 [示例仓库](https://github.com/photonstorm/phaser3-examples) 。我们不断添加和完善这些示例。

### 庞大的 Phaser 3 插件列表

社区超级成员 RexRainbow 多年来一直在发布 Phaser 3 的内容，在那段时间建立了一个令人印象深刻的目录。 您会发现[大量插件](https://rexrainbow.github.io/phaser3-rex-notes/docs/site/index.html#list-of-my-plugins) ，从文本输入框等 UI 控件到 Firebase 支持、有限状态机等等。除了插件之外，还有一套关于 Phaser 3 的综合“注释”，详细介绍了各种系统的工作原理。 这是一个非常宝贵的资源，非常值得在 [https://rexrainbow.github.io](https://rexrainbow.github.io/phaser3-rex-notes/docs/site/index.html) 查看。

### 创建您的第一个 Phaser 3 示例

在本地创建一个 `index.html` 页面并将以下代码粘贴到其中：
```html
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.jsdelivr.net/npm/phaser@3.51.0/dist/phaser-arcade-physics.min.js"></script> 
</head>
<body>

    <script></script>

</body>
</html>
```

这是一个标准的空网页。 你会注意到有一个脚本标签正在拉入 Phaser 3 的构建，但除此之外，这个网页还没有做任何事情。 现在让我们设置游戏配置。 在 `<script></script> `标记之间粘贴以下内容：
```js
var config = {
    type: Phaser.AUTO,
    width: 800,
    height: 600,
    physics: {
        default: 'arcade',
        arcade: {
            gravity: { y: 200 }
        }
    },
    scene: {
        preload: preload,
        create: create
    }
};
```

`config`是一个非常标准的 Phaser 3 游戏配置对象。我们告诉 `config` 使用 WebGL 渲染器（如果可以的话），并将画布设置为 800x600 像素的大小，启用 Arcade 物理效果，最后调用 `preload` 和 `create` 函数。 `preload` 和 `create` 还没有实现，所以如果你运行这段 JavaScript 代码，你会遇到错误。 在`config`后添加以下内容：
```js
var game = new Phaser.Game(config);

function preload ()
{
    this.load.setBaseURL('https://labs.phaser.io');

    this.load.image('sky', 'assets/skies/space3.png');
    this.load.image('logo', 'assets/sprites/phaser3-logo.png');
    this.load.image('red', 'assets/particles/red.png');
}

function create ()
{
}
```
`game` 是一个 Phaser 游戏实例，它使用我们的配置对象 `config`。 我们还为 `preload` 和 `create` 添加了函数定义。 预加载功能可帮助您轻松地将资产加载到游戏中。 在预加载中，我们将 Base URL 设置为 Phaser 服务器并加载 3 个 PNG 文件。 

目前 `create` 函数还是空的，所以是时候填充它了：
```js
function create ()
{
    this.add.image(400, 300, 'sky');

    var particles = this.add.particles('red');

    var emitter = particles.createEmitter({
        speed: 100,
        scale: { start: 1, end: 0 },
        blendMode: 'ADD'
    });

    var logo = this.physics.add.image(400, 100, 'logo');

    logo.setVelocity(100, 200);
    logo.setBounce(1, 1);
    logo.setCollideWorldBounds(true);

    emitter.startFollow(logo);
}
```
在这里，我们将天空图像添加到游戏中并创建粒子发射器。 `scale`意味着粒子最初会很大，随着寿命的延长会缩小到零。 
创建发射器(`emitter`)后，我们添加一个名为 `logo` 的LOGO图像。 因为 `logo` 是一个物理图像，所以 `logo` 默认是一个物理体。 我们为 `logo` 设置了一些属性：速度、反弹（或恢复）和与世界边界的碰撞。 这些属性将使我们的标志在屏幕上反弹。 最后，我们告诉粒子发射器跟随 LOGO —— 所以当 LOGO 移动时，粒子将从它流出。
在浏览器中运行它，您将看到以下内容：
![img](imgs/phaser/sample1.png)
（有问题？这里是[完整代码](https://gist.github.com/photonstorm/46cb8fb4b19fc7717dcad514cdcec064)）

这是一个很小的示例，还有数百个示例供您探索，但希望它展示了 Phaser 的使用速度和表现力。 只需几行易于阅读的代码，我们就可以在屏幕上展示一些令人印象深刻的东西！

Ourcade 已经出版了两本很棒的 [Phaser 3 书籍](https://blog.ourcade.co/)。 他们会带你从设置到使用 JavaScript 或 TypeScript 完成你的第一款游戏，而且它们都是完全免费的！ 他们还发布了大量高质量的教程和视频，因此请务必每周查看他们的网站。

使用 Phaser 3.50 了解 HTML5 游戏开发的秘密，同时构建跨平台的无尽奔跑游戏。 该课程专为初学者和熟练的程序员设计，引导您从一个空文件夹介绍 JavaScript 的基本原理到高级 Phaser 3 功能。 了解有关[使用 Phaser 的 HTML5 跨平台游戏开发](https://gumroad.com/a/244184179)的更多详细信息。

## 构建 Phaser

在存储库的 `dist` 文件夹中有 Phaser 的普通和缩小编译版本。普通版用于开发期间使用，缩小版用于生产使用。您理应可以创建自己的构建。

### 自定义构建

Phaser 3 是使用 Webpack 构建的，我们利用 Webpack definePlugin 功能来允许有条件地构建 Canvas 和 WebGL 渲染器以及额外的插件。您可以自定义构建过程以仅包含您需要的功能。这样做可以将主构建文件的大小减少到仅 70KB。 
阅读我们关于创建 Phaser 3 的自定义构建的[综合指南](https://github.com/photonstorm/phaser3-custom-build#creating-custom-phaser-3-builds)以获取完整的详细信息。

### 从源码构建

如果您希望从源代码构建 Phaser 3，请通过克隆存储库然后在源目录上运行 `npm install` 来确保您拥有所需的包。
然后，您可以运行 `webpack` 在 `build` 文件夹中创建一个开发构建，其中包含用于本地测试的源映射。您还可以` npm run dist` 在 `dist` 文件夹中创建一个缩小的打包构建。有关所有可用命令的列表，请使用 `npm run help`。

## 更新日志

### 更新日志

传统意义上，我们总是在本 README 中包含最新的变更日志。 对于访问者来说，这是一种快速浏览最新版本中新增内容的好方法。 但是，对于 3.50.0 版本，我们不能这样做，因为更改日志本身有 1300 行长，大小超过 160KB。
这对于 Phaser 来说是前所未有的，但 3.50 是一个真正的大规模发布！
您可以在此处阅读完整的 [3.51 版本的更新日志](https://github.com/photonstorm/phaser/blob/master/CHANGELOG-v3.50.md)。
我们已将变更日志组织成共同主题的部分，以使其更易于理解，但我们很欣赏其中有很多内容。 请不要感到不知所措！ 如果您需要搞清楚某些事情，请加入我们的 Phaser Discord 并随时提问。
对于 3.50 之前的版本，您也可以阅读之前的[更新日志](https://github.com/photonstorm/phaser/blob/master/CHANGELOG.md)。

## 贡献指南

[贡献者指南](https://github.com/photonstorm/phaser/blob/master/.github/CONTRIBUTING.md)包含有关如何帮助 Phaser 开发的完整详细信息。 要点是：

- 发现错误？ 在 [GitHub Issues](https://github.com/photonstorm/phaser/issues)上报告并包含代码示例。 请说明您使用的是哪个版本的 Phaser！ 这是至关重要的。
- 在提交 Pull Request 之前，使用我们的[配置文件](https://github.com/photonstorm/phaser/blob/master/.eslintrc.json)通过 [ES Lint](https://eslint.org/) 运行您的代码并尊重我们的[编辑器配置](https://github.com/photonstorm/phaser/blob/master/.editorconfig)。
- 在贡献之前阅读[行为准则](https://github.com/photonstorm/phaser/blob/master/.github/CODE_OF_CONDUCT.md)。

在 Phaser 中写了一些很酷的东西？ 请在[论坛](https://phaser.discourse.group/)中告诉我们，或发送电子邮件至 support@phaser.io

Phaser 是 Photon Storm 的作品。
![img](imgs/phaser/photonstorm-x2.png)
由Richard Davey创建。 由咖啡、动漫、像素和爱提供支持。
Phaser 徽标和字符版权归 © 2020 Photon Storm Limited 所有。

> “最重要的是，电子游戏只是为了一件事：有趣。每个人都有趣。” ——岩田聪

