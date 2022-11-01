## [Phaser](命名空间：Phaser.md). Actions

源代码： [src/actions/index.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/index.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/index.js#L7))

### 方法

---
#### AlignTo

\<static\> AlignTo(items, position \[, offsetX\] \[, offsetY\])

获取一组游戏对象，或任何具有公共 `x` 和 `y` 属性的对象，并将它们彼此相邻对齐。
第一项不会移动。 第二项与第一项对齐，然后第三项与第二项相邻，依此类推。

##### 参数：
| 名称       | 类型                                                                  | 声明     | 默认值 | 描述                                                                          |
| ---------- | --------------------------------------------------------------------- | -------- | ------ | ----------------------------------------------------------------------------- |
| items    | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |          |        | 此操作要更新的项目（item）数组。                                              |
| position | number                                                                |          |        | 对齐项目的位置。 这是一个对齐常量，例如 `Phaser.Display.Align.LEFT_CENTER` 。 |
| offsetX  | number                                                                | \<可选\> | 0      | 可选,与目标位置水平偏移。                                                    |
| offsetY  | number                                                                | \<可选\> | 0      | 可选,与目标位置垂直偏移。                                                    |

开始支持的版本：3.22.0

源代码： [src/actions/AlignTo.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/AlignTo.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/AlignTo.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\>

---

#### Angle

\<static\> Angle(items, value \[, step\] \[, index\] \[, direction\])

获取一个游戏对象数组，或任何具有公共 `angle` 属性的对象，然后将给定值添加到它们的每个 `angle` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目。

要将其与组一起使用时：：`Angle(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                                                    | 声明     | 默认值 | 描述                                         |
| --------- | ----------------------------------------------------------------------- | -------- | ------ | -------------------------------------------- |
| items     | array \| Array.<**[Phaser.GameObjects.GameObject](类：GameObject.md)**> |          |        | 此操作要更新的项目数组。                     |
| value     | number                                                                  |          |        | 要添加到角度属性的量。                       |
| step      | number                                                                  | \<可选\> | 0      | 步长，这个值将会持续加在 `value` 上          |
| index     | number                                                                  | \<可选\> | 0      | 可选，从 items 数组中开始搜索的偏移量。      | 
| direction | number                                                                  | \<可选\> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/Angle.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Angle.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Angle.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\>

---

#### Call
\<static\> Call(items, callback, context)

获取一个对象数组并将它们中的每一个对象传递给给定的回调函数。

##### 参数：
| 名称     | 类型                                             | 描述                                                                               |
|----------|--------------------------------------------------|-------------------------------------------------------------------------------------------|
| items    | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\>  | 此操作要更新的项目数组。                                        |
| callback | [Phaser.Types.Actions.CallCallback](../Types/Actions.md#CallCallback)                | 要调用的回调函数。它只传递一个参数：数组中的项目。 |
| context  | *                                                | The scope in which the callback will be invoked.                                          |

开始支持的版本：3.0.0

源代码： [src/actions/Call.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Call.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Call.js#L7))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\>

---

#### GetFirst
\<static\> GetFirst(items, compare \[, index\])

获取一个对象数组并返回数组中的第一个元素，该元素的属性与 `compare` 对象中指定的所有属性相匹配。 例如，如果比较对象是：`{ scaleX: 0.5, alpha: 1 }`，那么它将返回第一个将属性 `scaleX` 设置为 0.5 和 `alpha` 设置为 1 的项目。

要将其与组一起使用时：：`GetFirst(group.getChildren(), compare, index)`

##### 参数：
| 名称    | 类型                                                                  | 声明     | 默认值 | 描述                                                    |
| ------- | --------------------------------------------------------------------- | -------- | ------ | ------------------------------------------------------- |
| items   | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |          |        | 此操作要搜索的项目数组。                                |
| compare | object                                                                |          |        | 比较对象。 该对象中的每个属性都将根据数组的项进行检查。 | 
| index   | number                                                                | \<可选\> | 0      | 可选，从 items 数组中开始搜索的偏移量。                 |

开始支持的版本：3.0.0

源代码： [src/actions/GetFirst.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/GetFirst.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/GetFirst.js#L7))

##### 返回值：

数组中与比较对象匹配的第一个对象，如果未找到匹配项，则为 `null` 。

Type

object | [Phaser.GameObjects.GameObject](类：GameObject.md)

---

#### GetLast

\<static\> GetLast(items, compare \[, index\])

获取一个对象数组并返回数组中的最后一个元素，该元素的属性与 `compare` 对象中指定的所有属性相匹配。 例如，如果比较对象是：`{ scaleX: 0.5, alpha: 1 }`，那么它将返回属性`scaleX`设置为 0.5 且`alpha`设置为 1 的最后一项。

要将其与组一起使用时：：`GetLast(group.getChildren(), compare, index)`

##### 参数：
| 名称    | 类型                                                                  | 声明     | 默认值 | 描述                                                    |
| ------- | --------------------------------------------------------------------- | -------- | ------ | ------------------------------------------------------- |
| items   | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |          |        | 此操作要搜索的项目数组。                                |
| compare | object                                                                |          |        | 比较对象。 该对象中的每个属性都将根据数组的项进行检查。 | 
| index   | number                                                                | \<可选\> | 0      | 可选，从 items 数组中开始搜索的偏移量。                 |

开始支持的版本：3.3.0

源代码： [src/actions/GetLast.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/GetLast.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/GetLast.js#L7))

##### 返回值：

数组中与比较对象匹配的最后一个对象，如果未找到匹配项，则为 `null` 。

Type

object | [Phaser.GameObjects.GameObject](类：GameObject.md)

---

#### GridAlign

\<static> GridAlign(items, options)

获取一组游戏对象，或任何具有公共 `x` 和 `y` 属性的对象，然后根据给定此操作的网格配置对齐它们。

##### 参数：
| 名称    | 类型                                                                        | 描述                     |
| ------- | --------------------------------------------------------------------------- | ------------------------ |
| items   | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>        | 此操作要更新的项目数组。 | 
| options | [Phaser.Types.Actions.GridAlignConfig](../Types/Actions.md#GridAlignConfig) | GridAlign 配置对象。     |

开始支持的版本：3.0.0

源代码： [src/actions/GridAlign.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/GridAlign.js) ([Line 15](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/GridAlign.js#L15))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### IncAlpha

\<static> IncAlpha(items, value \[, step] \[, index] \[, direction])

获取一个游戏对象数组，或任何具有公共 `alpha` 属性的对象，然后将给定值添加到它们的每个 `alpha` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目。

要将其与组一起使用时：：`IncAlpha(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                                                 | 声明    | 默认值 | 描述                                         |
| --------- | -------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)> |         |        | 此操作要更新的项目数组。                     |
| value     | number                                                               |         |        | 要添加到透明度属性上的量。                   |
| step      | number                                                               | \<可选> | 0      | 步长，这个值将会持续加在 `value` 上          |
| index     | number                                                               | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                               | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 | 

开始支持的版本：3.0.0

源代码：[src/actions/IncAlpha.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncAlpha.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncAlpha.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>