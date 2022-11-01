## [Phaser](命名空间：Phaser.md). Actions

Source: [src/actions/index.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/index.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/index.js#L7))

### 方法

---
#### AlignTo

\<static\> AlignTo(items, position \[, offsetX\] \[, offsetY\])

获取一组游戏对象，或任何具有公共 `x` 和 `y` 属性的对象，并将它们彼此相邻对齐。
第一项不会移动。 第二项与第一项对齐，然后第三项与第二项相邻，依此类推。

##### 参数：
| 名称       | 类型                                                                  | 声明     | 默认值 | 描述                                                                          |
| ---------- | --------------------------------------------------------------------- | -------- | ------ | ----------------------------------------------------------------------------- |
| `items`    | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |          |        | 此操作要更新的项目（item）数组。                                              |
| `position` | number                                                                |          |        | 对齐项目的位置。 这是一个对齐常量，例如 `Phaser.Display.Align.LEFT_CENTER` 。 |
| `offsetX`  | number                                                                | \<可选\> | 0      | 可选,与目标位置水平偏移。                                                    |
| `offsetY`  | number                                                                | \<可选\> | 0      | 可选,与目标位置垂直偏移。                                                    |

Since: 3.22.0

Source: [src/actions/AlignTo.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/AlignTo.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/AlignTo.js#L9))

##### Returns:

The array of objects that were passed to this Action.

Type

array | Array.\<[Phaser.GameObjects.GameObject](file:///home/github/gitfloder/phaser3-docs/docs/Phaser.GameObjects.GameObject.html)\>


