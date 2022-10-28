## Phaser

源码： [src/phaser.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/phaser.js) ([第12行](https://github.com/photonstorm/phaser/tree/v3.51.0/src/phaser.js#L12))

## 类

[FacebookInstantGamesLeaderboard](FacebookInstantGamesLeaderboard.md)
[FacebookInstantGamesPlugin](FacebookInstantGamesPlugin.md)
[Game](Game.md)
[Scene](Scene.md)

## 命名空间

[Actions](Phaser/01-Namespace/Phaser/Actions.md)
[Animations](Animations.md)
[BlendModes](BlendModes.md)
[Cache](Cache.md)
[Cameras](Cameras.md)
[Core](Core.md)
[Create](Create.md)
[Curves](Curves.md)
[Data](Data.md)
[Device](Device.md)
[Display](Display.md)
[DOM](DOM.md)
[Events](Events.md)
[GameObjects](GameObjects.md)
[Geom](Geom.md)
[Input](Input.md)
[Loader](Loader.md)
[Math](Math.md)
[Physics](Physics.md)
[Plugins](Plugins.md)
[Renderer](Renderer.md)
[Scale](Scale.md)
[ScaleModes](ScaleModes.md)
[Scenes](Scenes.md)
[Sound](Sound.md)
[Structs](Structs.md)
[Textures](Textures.md)
[Tilemaps](Tilemaps.md)
[Time](Time.md)
[Tweens](Tweens.md)
[Types](Types.md)
[Utils](Utils.md)

## 成员变量

#### <静态， 常量> AUTO :number
此设置将自动检测浏览器是否能够支持 WebGL。 如果是，它将使用 WebGL 渲染器。 如果没有，它将回退到 Canvas 渲染器。
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 29](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L29))

---
#### <静态， 常量> CANVAS :number
强制 Phaser 仅使用 Canvas Renderer，无论浏览器是否支持 WebGL。
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 40](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L40))

---
#### <静态， 常量> DOWN :number
方向常数（Direction constant.）
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 106](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L106))

---
#### <静态， 常量> FOREVER :number
在 Phaser 中，值 -1 在很多情况下意味着“永远”，这个常量允许您使用它来帮助您记住值在代码中的作用。
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 75](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L75))

---
#### <静态， 常量> HEADLESS :number
Headless渲染器不会创建 Canvas 或 WebGL 渲染器。 但是，它仍然绝对依赖于存在和可用的 DOM 上。 此模式用于单元测试，而不是用于在服务器上运行 Phaser，这是您真正不应该做的事情。
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 63](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L63))

---
#### <静态， 常量> LEFT :number
方向常数（Direction constant.）
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 116](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L116))

---
#### <静态， 常量> NONE :number
方向常数（Direction constant.）
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 86](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L86))

---
#### <静态， 常量> RIGHT :number
方向常数（Direction constant.）
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 126](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L126))

---
#### <静态， 常量> UP :number
方向常数（Direction constant.）
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 96](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L96))

---
#### <静态， 常量> VERSION :string
Phaser 的发布版本
##### 类型：
-   string
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 15](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L15))

---
#### <静态， 常量> WEBGL :number
强制 Phaser 使用 WebGL 渲染器。 如果浏览器不支持它，则使用此设置不会回退到 Canvas，因此您应该捕获报错并向用户显示合适的消息。
##### 类型：
-   数值（number）
加入版本：3.0.0
源码：[src/const.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js) ([Line 51](https://github.com/photonstorm/phaser/tree/v3.51.0/src/const.js#L51))


### 类型定义

---
#### 设备配置（DeviceConf）
##### 类型：
-   对象（object）
##### 属性：
| 名称           | 类型                                                             | 描述               |
| -------------- | ---------------------------------------------------------------- | ------------------ |
| os             | [Phaser.Device.OS](Phaser/Device.md#.OS)                         | 设备操作系统方法。 |
| browser        | [Phaser.Device.Browser](Phaser/Device.md#.Browser)               | 设备浏览器方法。   |
| features       | [Phaser.Device.Features](Phaser/Device.md#.Features)             | 设备功能方法。 |
| input          | [Phaser.Device.Input](Phaser/Device.md#.Input)                   | 设备输入方法。     |
| audio          | [Phaser.Device.Audio](Phaser/Device.md#.Audio)                   | 设备音频方法。     |
| video          | [Phaser.Device.Video](Phaser/Device.md#.Video)                   | 设备视频方法。     |
| fullscreen     | [Phaser.Device.Fullscreen](Phaser/Device.md#.Fullscreen)         | 设备全屏方法。     |
| canvasFeatures | [Phaser.Device.CanvasFeatures](Phaser/Device.md#.CanvasFeatures) | 设备画布方法。     |
源码：[src/device/index.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/device/index.js) ([Line 17](https://github.com/photonstorm/phaser/tree/v3.51.0/src/device/index.js#L17))