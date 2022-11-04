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

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时：`Angle(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                                                    | 声明     | 默认值 | 描述                                         |
| --------- | ----------------------------------------------------------------------- | -------- | ------ | -------------------------------------------- |
| items     | array \| Array.<[Phaser.GameObjects.GameObject](类：GameObject.md)> |          |        | 此操作要更新的项目数组。                     |
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
| callback | [Phaser.Types.Actions.CallCallback](Phaser/01-Namespace/Types/命名空间：Actions.md#CallCallback)                | 要调用的回调函数。它只传递一个参数：数组中的项目。 |
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

要将其与组一起使用时：`GetFirst(group.getChildren(), compare, index)`

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

要将其与组一起使用时：`GetLast(group.getChildren(), compare, index)`

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
| options | [Phaser.Types.Actions.GridAlignConfig](Phaser/01-Namespace/Types/命名空间：Actions.md#GridAlignConfig) | GridAlign 配置对象。     |

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

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时：`IncAlpha(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                                                 | 声明    | 默认值 | 描述                                         |
| --------- | -------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)> |         |        | 此操作要更新的项目数组。                     |
| value     | number                                                               |         |        | 要添加到`alpha`属性上的量。                   |
| step      | number                                                               | \<可选> | 0      | 步长，这个值将会持续加在 `value` 上          |
| index     | number                                                               | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                               | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 | 

开始支持的版本：3.0.0

源代码：[src/actions/IncAlpha.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncAlpha.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncAlpha.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---
#### IncX

\<static> IncX(items, value \[, step] \[, index] \[, direction])

获取一个游戏对象数组，或任何具有公共 `x` 属性的对象，然后将给定值添加到它们的每个 `x` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时：`IncX(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                            | 声明        | 默认值 | 描述                                                                                       |
| --------- | ----------------------------------------------- | ----------- | ------ | ------------------------------------------------------------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |        | 此操作要更新的项目数组。                                                  |
| value     | number                                          |             |        | 要添加到`x`属性上的量。                                                       |
| step      | number                                          | \<可选> | 0      | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                          | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                          | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/IncX.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncX.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncX.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---
#### IncXY

\<static> IncXY(items, x \[, y] \[, stepX] \[, stepY] \[, index] \[, direction])

获取一个游戏对象数组，或任何具有公共 `x` 和 `y` 属性的对象，然后将给定值添加到它们的每个 `x` 和 `y` 属性。

可选的 `stepX` 和 `stepY` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时：`IncXY(group.getChildren(), x, y, stepX, stepY)`

##### 参数：

| 名称      | 类型                                                                  | 声明        | 默认值 | 描述                                                                             |
| --------- | --------------------------------------------------------------------- | ----------- | ------ | -------------------------------------------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |        | 此操作要更新的项目数组。                                                         |
| x         | number                                                                |             |        | 要添加到`x`属性上的量。                                                          |
| y         | number                                                                | \<可选> | x      | 要添加到`y`属性上的量。 如果值为 `undefined` 或为 `null` 则将 `x` 的值赋予给 `y` | 
| stepX     | number                                                                | \<可选> | 0      | `x` 的步长，这个值将会持续加在 `x` 上。              |
| stepY     | number                                                                | \<可选> | 0      | `y` 的步长，这个值将会持续加在 `y` 上。             |
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。                                          |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。                                     |

开始支持的版本：3.0.0

源代码： [src/actions/IncXY.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncXY.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncXY.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---
#### IncY

\<static> IncY(items, value \[, step] \[, index] \[, direction])

获取一个游戏对象数组，或任何具有公共 `y` 属性的对象，然后将给定值添加到它们的每个 `y` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时：`IncY(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                           | 声明    | 默认值 | 描述                                                                                       |
|-----------|------------------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------|
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                  |
| value     | number                                         |             |         | 要添加到`y`属性上的量。                                                         |
| step      | number                                         | \<可选> | 0       | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/IncY.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncY.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/IncY.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---
#### PlaceOnCircle

\<static> PlaceOnCircle(items, circle \[, startAngle] \[, endAngle])

获取游戏对象的数组，并将它们放置在圆周周围均匀分布的点上。

如果您希望将 `Phaser.GameObjects.Circle` 形状传递给此函数，则应传递其 `geom` 属性。

##### 参数：
| 名称       | 类型                                                                  | 声明    | 默认值 | 描述                                       |
| ---------- | --------------------------------------------------------------------- | ------- | ------ | ------------------------------------------ |
| items      | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 游戏对象的数组。此操作将更新此数组的内容。 |
| circle     | [Phaser.Geom.Circle](类：Circle.md)                                   |         |        | 用于放置游戏对象的圆圈。                   |
| startAngle | number                                                                | \<可选> | 0      | 可选，起始位置的角度，以弧度为单位。       |
| endAngle   | number                                                                | \<可选> | 6.28   | 可选，终止位置的角度，以弧度为单位。       | 

开始支持的版本：3.0.0

源代码： [src/actions/PlaceOnCircle.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnCircle.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnCircle.js#L7))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---
#### PlaceOnEllipse

\<static> PlaceOnEllipse(items, ellipse \[, startAngle] \[, endAngle])

获取游戏对象的数组，并将它们放置在椭圆周边均匀分布的点上。

如果您希望将 `Phaser.GameObjects.Ellipse` 形状传递给此函数，则应传递其 `geom` 属性。

##### 参数：
| 名称       | 类型                                                                  | 声明    | 默认值 | 描述                                       |
| ---------- | --------------------------------------------------------------------- | ------- | ------ | ------------------------------------------ |
| items      | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 游戏对象的数组。此操作将更新此数组的内容。 |
| ellipse    | [Phaser.Geom.Ellipse](类：Ellipse.md)                                                   |         |        | 用于放置游戏对象的椭圆。                   |
| startAngle | number                                                                | \<可选> | 0      | 可选，起始位置的角度，以弧度为单位。       |
| endAngle   | number                                                                | \<可选> | 6.28   | 可选，终止位置的角度，以弧度为单位。       |

开始支持的版本：3.0.0

源代码： [src/actions/PlaceOnEllipse.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnEllipse.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnEllipse.js#L7))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---
#### PlaceOnLine

\<static> PlaceOnLine(items, line)

将游戏对象数组放置在线条的上均匀分布点上。

##### 参数：
| 名称  | 类型                                                                  | 描述                                       |
| ----- | --------------------------------------------------------------------- | ------------------------------------------ |
| items | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。 | 
| line  | [Phaser.Geom.Line](类：Line.md)                                       | 用于放置游戏对象的线。                     |

开始支持的版本：3.0.0

源代码： [src/actions/PlaceOnLine.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnLine.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnLine.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---
#### PlaceOnRectangle

\<static> PlaceOnRectangle(items, rect \[, shift])

获取游戏对象的数组，并将它们放置在矩形周边均匀分布的点上。

放置从矩形的左上角开始，沿顺时针方向进行。如果给定了 `shift` 参数，则可以偏移开始放置的位置。

##### 参数：
| 名称  | 类型                                                                  | 声明    | 默认值 | 描述                                       |
| ----- | --------------------------------------------------------------------- | ------- | ------ | ------------------------------------------ |
| items | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 游戏对象的数组。此操作将更新此数组的内容。 |
| rect  | [Phaser.Geom.Rectangle](类：Rectangle.md)                                                 |         |        | 用于放置游戏对象的矩形。                   |
| shift | number                                                                | \<可选> | 1      | 可选，位置偏移。                           | 

开始支持的版本：3.0.0

源代码： [src/actions/PlaceOnRectangle.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnRectangle.js) ([Line 11](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnRectangle.js#L11))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### PlaceOnTriangle

\<static> PlaceOnTriangle(items, triangle \[, stepRate])

获取游戏对象的数组，并将它们放置在三角形边缘周围均匀分布的点上。

如果您希望将 `Phaser.GameObjects.Triangle` 形状传递给此函数，则应传递其 `geom` 属性。

##### 参数：
| 名称     | 类型                                                                  | 声明    | 默认值 | 描述                                                                                         |
| -------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------------------------------------------------------- |
| items    | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 游戏对象的数组。此操作将更新此数组的内容。                                                   |
| triangle | [Phaser.Geom.Triangle](类：Triangle.md)                                                  |         |        | 用于放置游戏对象的三角形。                                                                   |
| stepRate | number                                                                | \<可选> | 1      | An optional step rate, to increase or decrease the packing of the Game Objects on the lines. |

开始支持的版本：3.0.0

源代码： [src/actions/PlaceOnTriangle.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnTriangle.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlaceOnTriangle.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### PlayAnimation
\<static> PlayAnimation(items, key \[, startFrame])

在项目中的所有游戏对象上使用给定的键值播放动画，可以从给定的开始帧开始。

##### 参数：
| 名称       | 类型                                                                  | 声明    | 描述                                       |
| ---------- | --------------------------------------------------------------------- | ------- | ------------------------------------------ |
| items      | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         | 游戏对象的数组。此操作将更新此数组的内容。 |
| key        | string                                                                |         | 要播放的动画的名称。                       | 
| startFrame | string \| number                                                      | \<可选> | 从给定关键帧作为动画的起始帧。             |

开始支持的版本：3.0.0

源代码： [src/actions/PlayAnimation.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlayAnimation.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PlayAnimation.js#L7))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### PropertyValueInc

\<static> PropertyValueInc(items, key, value \[, step] \[, index] \[, direction])

获取游戏对象的数组，或具有 `key` 中定义的公共属性的任何对象，然后将给定值添加到其中。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `PropertyValueInc(group.getChildren(), key, value, step)`

##### 参数：
| 名称      | 类型                                           | 声明    | 默认值 | 描述                                                                                       |
|-----------|------------------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------|
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                  |
| key       | string                                         |             |         | 要更新的属性。                                                                      |
| value     | number                                         |             |         | 要添加到属性的值。                                                          |
| step      | number                                         | \<可选> | 0       | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.3.0

源代码： [src/actions/PropertyValueInc.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PropertyValueInc.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PropertyValueInc.js#L7))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### PropertyValueSet

\<static> PropertyValueSet(items, key, value \[, step] \[, index] \[, direction])

获取游戏对象的数组，或具有 `key` 中定义的公共属性的任何对象，然后将其设置为给定值。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `PropertyValueSet(group.getChildren(), key, value, step)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                         |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                     |
| key       | string                                                                |         |        | 要更新的属性。                               | 
| value     | number                                                                |         |        | 要添加到属性的值。                           |
| step      | number                                                                | \<可选> | 0      | 步长，这个值将会持续加在 `value` 上。        |
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.3.0

源代码： [src/actions/PropertyValueSet.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PropertyValueSet.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/PropertyValueSet.js#L7))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### RandomCircle

\<static> RandomCircle(items, circle)

获取游戏对象的数组，并将它们放置在圆圈内的随机位置。

如果您希望将 `Phaser.GameObjects.Circle` 形状传递给此函数，则应传递其 `geom` 属性。

##### 参数：
| 名称   | 类型                                                                  | 描述                                       |
| ------ | --------------------------------------------------------------------- | ------------------------------------------ |
| items  | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。 |
| circle | [Phaser.Geom.Circle](类：Circle.md)                                                   | 用于在其中放置游戏对象的圆圈。             | 

开始支持的版本：3.0.0

源代码： [src/actions/RandomCircle.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomCircle.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomCircle.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### RandomEllipse
\<static> RandomEllipse(items, ellipse)

获取游戏对象的数组，并将它们放置在椭圆内的随机位置。

如果您希望将 `Phaser.GameObjects.Ellipse` 形状传递给此函数，则应传递其 `geom` 属性。

##### 参数：
| 名称    | 类型                                                                  | 描述                                       |
| ------- | --------------------------------------------------------------------- | ------------------------------------------ |
| items   | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。 |
| ellipse | [Phaser.Geom.Ellipse](类：Ellipse.md)                                 | 用于在其中定位游戏对象的椭圆。             |

开始支持的版本：3.0.0

源代码： [src/actions/RandomEllipse.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomEllipse.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomEllipse.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### RandomLine
\<static> RandomLine(items, line)

获取游戏对象的数组，并将它们放置在线上的随机位置。

如果您希望将  `Phaser.GameObjects.Line` 形状传递给此函数，则应传递其 `geom` 属性。

##### 参数：
| 名称  | 类型                                                                  | 描述                                       |
| ----- | --------------------------------------------------------------------- | ------------------------------------------ |
| items | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。 |
| line  | [Phaser.Geom.Line](类：Line.md)                                       | 用于随机放置游戏对象的线。                 |

开始支持的版本：3.0.0

源代码： [src/actions/RandomLine.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomLine.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomLine.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### RandomRectangle
\<static> RandomRectangle(items, rect)

获取游戏对象的数组，并将它们放置在矩形内的随机位置。

##### 参数：
| 名称  | 类型                                                                  | 描述                                       |
| ----- | --------------------------------------------------------------------- | ------------------------------------------ |
| items | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。 |
| rect  | [Phaser.Geom.Rectangle](类：Rectangle.md)                             | 用于在其中放置游戏对象的矩形。             |

开始支持的版本：3.0.0

源代码： [src/actions/RandomRectangle.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomRectangle.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomRectangle.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### RandomTriangle
\<static> RandomTriangle(items, triangle)

获取游戏对象数组并将它们放置在三角形内的随机位置。

如果您希望将 `Phaser.GameObjects.Triangle` 形状传递给此函数，则应传递其 `geom` 属性。

##### 参数：
| 名称     | 类型                                                                  | 描述                                       |
| -------- | --------------------------------------------------------------------- | ------------------------------------------ |
| items    | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。 |
| triangle | [Phaser.Geom.Triangle](类：Triangle.md)                               | 用于在其中放置游戏对象的三角形。           |

开始支持的版本：3.0.0

源代码： [src/actions/RandomTriangle.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomTriangle.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RandomTriangle.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### Rotate
\<static> Rotate(items, value \[, step] \[, index] \[, direction])

获取游戏对象的数组或具有公共旋转（ `rotation`  ）属性的任何对象，然后将给定值添加到其每个 `rotation` 属性中。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `Rotate(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                         |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                     |
| value     | number                                                                |         |        | 要添加到旋转属性的量（以弧度为单位）。       |
| step      | number                                                                | \<可选> | 0      | 步长，这个值将会持续加在 `value` 上。        |
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/Rotate.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Rotate.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Rotate.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### RotateAround

\<static> RotateAround(items, point, angle)

按给定角度围绕给定点旋转每个项目。

##### 参数：
| 名称  | 类型                                                                  | 描述                                       |
| ----- | --------------------------------------------------------------------- | ------------------------------------------ |
| items | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。 |
| point | object                                                                | 具有公共 `x` 和 `y` 属性的任何对象。       |
| angle | number                                                                | 要旋转的角度，以弧度为单位。               |

开始支持的版本：3.0.0

源代码： [src/actions/RotateAround.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RotateAround.js) ([Line 10](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RotateAround.js#L10))

See:

-   [Phaser.Math.RotateAroundDistance](命名空间：Math.md#RotateAroundDistance)

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### RotateAroundDistance

\<static> RotateAroundDistance(items, point, angle, distance)

围绕一个点旋转游戏对象数组，按给定的角度和距离旋转。

##### 参数：
| 名称     | 类型                                                                  | 描述                                               |
| -------- | --------------------------------------------------------------------- | -------------------------------------------------- |
| items    | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。         |
| point    | object                                                                | 具有公共 `x` 和 `y` 属性的任何对象。               |
| angle    | number                                                                | 要旋转的角度，以弧度为单位。                       | 
| distance | number                                                                | 与旋转点的距离（以像素为单位）。 |

开始支持的版本：3.0.0

源代码： [src/actions/RotateAroundDistance.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RotateAroundDistance.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/RotateAroundDistance.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### ScaleX
\<static> ScaleX(items, value \[, step] \[, index] \[, direction])

获取游戏对象的数组，或任何具有公共 `scaleX` 属性的对象，然后将给定值添加到其每个 `scaleX` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `ScaleX(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                         |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                     |
| value     | number                                                                |         |        | 要添加到 `scaleX` 属性的量。                 | 
| step      | number                                                                | \<可选> | 0      | 步长，这个值将会持续加在 `value` 上。        |
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/ScaleX.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ScaleX.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ScaleX.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### ScaleXY

\<static> ScaleXY(items, scaleX \[, scaleY] \[, stepX] \[, stepY] \[, index] \[, direction])

获取游戏对象数组或具有公共 `scaleX` 和 `scaleY` 属性的任何对象，然后将给定值添加到每个对象。

可选的 `stepX` 和 `stepY` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `ScaleXY(group.getChildren(), scaleX, scaleY, stepX, stepY)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                                                                          |
| --------- | --------------------------------------------------------------------- | ------- | ------ | --------------------------------------------------------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                                                                      |
| scaleX    | number                                                                |         |        | 要添加到 `scaleX` 属性的量。                                                                    | 
| scaleY    | number                                                                | \<可选> |        | 要添加到 `scaleY` 属性的量。 如果值为 `undefined` 或为 `null` 则将 `scaleX` 的值赋予给 `scaleY` |
| stepX     | number                                                                | \<可选> | 0      | `scaleX` 的步长，这个值将会持续加在 `scaleX` 上。                     |
| stepY     | number                                                                | \<可选> | 0      | `scaleY` 的步长，这个值将会持续加在 `scaleY` 上。                     |
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。                                                       |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。                                                  |

开始支持的版本：3.0.0

源代码： [src/actions/ScaleXY.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ScaleXY.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ScaleXY.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### ScaleY

\<static> ScaleY(items, value \[, step] \[, index] \[, direction])

获取游戏对象的数组，或任何具有公共 `scaleY` 属性的对象，然后将给定值添加到其每个 `scaleY` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `ScaleY(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                         |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                     |
| value     | number                                                                |         |        | 要添加到 `scaleY` 属性的量。                 | 
| step      | number                                                                | \<可选> | 0      | 步长，这个值将会持续加在 `value` 上。        |
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/ScaleY.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ScaleY.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ScaleY.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetAlpha

\<static> SetAlpha(items, value \[, step] \[, index] \[, direction])

获取游戏对象数组或具有公共属性 `alpha` 的任何对象，然后将其设置为给定值。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetAlpha(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                         |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                     |
| value     | number                                                                |         |        | 要添加到`alpha`属性上的量。                  | 
| step      | number                                                                | \<可选> | 0      | 步长，这个值将会持续加在 `value` 上。        |
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/SetAlpha.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetAlpha.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetAlpha.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetBlendMode

\<static> SetBlendMode(items, value \[, index] \[, direction])

获取游戏对象数组或具有公共属性 `blendMode` （混合模式）的任何对象，然后将其设置为给定值。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetBlendMode(group.getChildren(), value)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                         |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                     |
| value     | number                                                                |         |        | 要将属性设置为的数值。                       | 
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/SetBlendMode.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetBlendMode.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetBlendMode.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetDepth

\<static> SetDepth(items, value \[, step] \[, index] \[, direction])

获取游戏对象数组或具有公共属性 `depth` 的任何对象，然后将其设置为给定值。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetDepth(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                         |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                     |
| value     | number                                                                |         |        | 要将属性设置为的数值。                       | 
| step      | number                                                                | \<可选> | 0      | 步长，这个值将会持续加在 `value` 上。        |
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/SetDepth.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetDepth.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetDepth.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetHitArea

\<static> SetHitArea(items, hitArea, hitAreaCallback)

将所有提供的游戏对象传递给输入管理器，以使它们能够输入具有相同区域和回调的内容。

##### 参数：
| 名称            | 类型                                                                  | 描述                                                                   |
| --------------- | --------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| items           | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。                             |
| hitArea         | *                                                                     | 输入配置对象或定义游戏对象命中区域的几何形状。如果未指定，将使用矩形。 | 
| hitAreaCallback | [Phaser.Types.Input.HitAreaCallback](Phaser/01-Namespace/Types/命名空间：Input.md#HitAreaCallback)                                    | 与游戏对象交互时要调用的回调。如果提供形状，还必须提供回调。           |

开始支持的版本：3.0.0

源代码： [src/actions/SetHitArea.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetHitArea.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetHitArea.js#L7))

See:

-   [Phaser.GameObjects.GameObject#setInteractive](类：GameObject.md#setInteractive)

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetOrigin

\<static> SetOrigin(items, originX \[, originY] \[, stepX] \[, stepY] \[, index] \[, direction])

获取游戏对象的数组，或具有公共属性 `originX` 和 `originY` 的任何对象，然后将它们设置为给定值。

可选的 `stepX` 和 `stepY` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetOrigin(group.getChildren(), originX, originY, stepX, stepY)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                                                                               |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------------------------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                                                                           |
| originX   | number                                                                |         |        | 要添加到 `originX` 属性上的量。                                                                    |
| originY   | number                                                                | \<可选> |        | 要添加到`originY`属性上的量。 如果值为 `undefined` 或为 `null` 则将 `originX` 的值赋予给 `originY` |
| stepX     | number                                                                | \<可选> | 0      | `originX` 的步长，这个值将会持续加在 `originX` 上。                                                |
| stepY     | number                                                                | \<可选> | 0      | `originY` 的步长，这个值将会持续加在 `originY` 上。                                                | 
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。                                                            |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。                                                       |

开始支持的版本：3.0.0

源代码： [src/actions/SetOrigin.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetOrigin.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetOrigin.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetRotation

\<static> SetRotation(items, value \[, step] \[, index] \[, direction])

获取游戏对象数组或具有公共属性 `rotation` （“旋转”）的任何对象，然后将其设置为给定值。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetRotation(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                           | 声明    | 默认值 | 描述                                                                                       |
|-----------|------------------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------|
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                  |
| value     | number                                         |             |         | 要将属性设置为的数值。                                                                |
| step      | number                                         | \<可选> | 0       | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/SetRotation.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetRotation.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetRotation.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetScale

\<static> SetScale(items, scaleX \[, scaleY] \[, stepX] \[, stepY] \[, index] \[, direction])

获取游戏对象的数组，或具有公共属性 `scaleX` 和 `scaleY` 的任何对象，然后将它们设置为给定值。

可选的 `stepX` 和 `stepY` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetScale(group.getChildren(), scaleX, scaleY, stepX, stepY)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                                                                            |
| --------- | --------------------------------------------------------------------- | ------- | ------ | ----------------------------------------------------------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                                                                        |
| scaleX    | number                                                                |         |        | 要添加到 `scaleX` 属性的量。                                                                    |
| scaleY    | number                                                                | \<可选> |        | 要添加到 `scaleY` 属性的量。 如果值为 `undefined` 或为 `null` 则将 `scaleX` 的值赋予给 `scaleY` | 
| stepX     | number                                                                | \<可选> | 0      | `scaleX` 的步长，这个值将会持续加在 `scaleX` 上。                                               |
| stepY     | number                                                                | \<可选> | 0      | `scaleY` 的步长，这个值将会持续加在 `scaleY` 上。                                               |
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。                                                         |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。                                                    |

开始支持的版本：3.0.0

源代码： [src/actions/SetScale.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScale.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScale.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetScaleX
\<static> SetScaleX(items, value \[, step] \[, index] \[, direction])

获取游戏对象的数组，或任何具有公共 `scaleX` 属性的对象，然后将给定值添加到其每个 `scaleX` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetScaleX(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                           | 声明    | 默认值 | 描述                                                                                       |
|-----------|------------------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------|
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                  |
| value     | number                                         |             |         | 要将属性设置为的数值。                                                                |
| step      | number                                         | \<可选> | 0       | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/SetScaleX.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScaleX.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScaleX.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetScaleY
\<static> SetScaleY(items, value \[, step] \[, index] \[, direction])

获取游戏对象的数组，或任何具有公共 `scaleY` 属性的对象，然后将给定值添加到其每个 `scaleY` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetScaleY(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                           | 声明    | 默认值 | 描述                                                                                       |
|-----------|------------------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------|
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                  |
| value     | number                                         |             |         | 要将属性设置为的数值。                                                                |
| step      | number                                         | \<可选> | 0       | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/SetScaleY.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScaleY.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScaleY.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetScrollFactor

\<static> SetScrollFactor(items, scrollFactorX \[, scrollFactorY] \[, stepX] \[, stepY] \[, index] \[, direction])

获取游戏对象的数组，或具有公共属性 `scrollFactorX` （X滚动元素）和 `scrollFactorY` （Y滚动元素）的任何对象，然后将它们设置为给定值。

可选的 `stepX` 和 `stepY` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetScrollFactor(group.getChildren(), scrollFactorX, scrollFactorY, stepX, stepY)`

##### 参数：
| 名称          | 类型                                           | 声明    | 默认值 | 描述                                                                                            |
|---------------|------------------------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------|
| items         | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                       |
| scrollFactorX | number                                         |             |         | 要添加到 `scrollFactorX` 属性的量。                                                       |
| scrollFactorY | number                                         | \<可选> |         | 要添加到 scrollFactorY 属性的量。 如果值为 `undefined` 或为 `null` 则将 `scrollFactorX` 的值赋予给 `scrollFactorY` |
| stepX         | number                                         | \<可选> | 0       | `scrollFactorX` 的步长，这个值将会持续加在 `scrollFactorX` 上。                       |
| stepY         | number                                         | \<可选> | 0       | `scrollFactorY` 的步长，这个值将会持续加在 `scrollFactorY` 上。                        |
| index         | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                     |
| direction     | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。      |

开始支持的版本：3.21.0

源代码： [src/actions/SetScrollFactor.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScrollFactor.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScrollFactor.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetScrollFactorX

\<static> SetScrollFactorX(items, value \[, step] \[, index] \[, direction])

获取游戏对象的数组，或具有公共属性 `scrollFactorX` （X滚动元素）的任何对象，然后将它们设置为给定值。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetScrollFactorX(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                           | 声明    | 默认值 | 描述                                                                                       |
|-----------|------------------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------|
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                  |
| value     | number                                         |             |         | 要将属性设置为的数值。                                                                |
| step      | number                                         | \<可选> | 0       | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.21.0

源代码： [src/actions/SetScrollFactorX.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScrollFactorX.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScrollFactorX.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetScrollFactorY

\<static> SetScrollFactorY(items, value \[, step] \[, index] \[, direction])

获取游戏对象的数组，或具有公共属性 `scrollFactorY` （Y滚动元素）的任何对象，然后将它们设置为给定值。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetScrollFactorY(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                           | 声明    | 默认值 | 描述                                                                                       |
|-----------|------------------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------|
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                  |
| value     | number                                         |             |         | 要将属性设置为的数值。                                                                |
| step      | number                                         | \<可选> | 0       | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.21.0

源代码： [src/actions/SetScrollFactorY.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScrollFactorY.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetScrollFactorY.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetTint

\<static> SetTint(items, topLeft \[, topRight] \[, bottomLeft] \[, bottomRight])

获取游戏对象的数组，或任何具有公共方法 `setTint()` 的对象，然后将其更新为给定值。您可以为每个角指定色调颜色，也可以只为 `topLeft` 参数提供一个颜色值，在这种情况下，整个项目将使用该颜色着色。

##### 参数：
| 名称        | 类型                                                                  | 声明    | 描述                                                                       |
| ----------- | --------------------------------------------------------------------- | ------- | -------------------------------------------------------------------------- |
| items       | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         | 游戏对象的数组。此操作将更新此数组的内容。                                 |
| topLeft     | number                                                                |         | 应用于项目左上角的色调。如果没有赋予其他参数值，则此色调将应用于整个项目。 | 
| topRight    | number                                                                | \<可选> | 可选，应用于项目右上角的色调。                       |
| bottomLeft  | number                                                                | \<可选> | 可选，应用于项目左下角的色调。                  |
| bottomRight | number                                                                | \<可选> | 可选，应用于项目右下角的色调。                |

开始支持的版本：3.0.0

源代码： [src/actions/SetTint.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetTint.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetTint.js#L7))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetVisible

\<static> SetVisible(items, value \[, index] \[, direction])

获取游戏对象数组或具有公共属性 `visible` （“可见”）的任何对象，然后将其设置为给定值。

要将其与组一起使用时： `SetVisible(group.getChildren(), value)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                         |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                     |
| value     | boolean                                                               |         |        | 要将属性设置为的值。                       | 
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。      |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/SetVisible.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetVisible.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetVisible.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetX

\<static> SetX(items, value \[, step] \[, index] \[, direction])

获取一个游戏对象数组，或任何具有公共 `x` 属性的对象，然后将给定值添加到它们的每个 `x` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetX(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                           | 声明    | 默认值 | 描述                                                                                       |
|-----------|------------------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------|
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                  |
| value     | number                                         |             |         | 要将属性设置为的数值。                                                                |
| step      | number                                         | \<可选> | 0       | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/SetX.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetX.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetX.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetXY

\<static> SetXY(items, x \[, y] \[, stepX] \[, stepY] \[, index] \[, direction])

获取一个游戏对象数组，或任何具有公共 `x` 和 `y` 属性的对象，然后将给定值添加到它们的每个 `x` 和 `y` 属性。

可选的 `stepX` 和 `stepY` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetXY(group.getChildren(), x, y, stepX, stepY)`

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                                                             |
| --------- | --------------------------------------------------------------------- | ------- | ------ | -------------------------------------------------------------------------------- |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 此操作要更新的项目数组。                                                         |
| x         | number                                                                |         |        | 要添加到`x`属性上的量。                                                          |
| y         | number                                                                | \<可选> | x      | 要添加到`y`属性上的量。 如果值为 `undefined` 或为 `null` 则将 `x` 的值赋予给 `y` |
| stepX     | number                                                                | \<可选> | 0      | `x` 的步长，这个值将会持续加在 `x` 上。                                          |
| stepY     | number                                                                | \<可选> | 0      | `y` 的步长，这个值将会持续加在 `y` 上。                                          | 
| index     | number                                                                | \<可选> | 0      | 可选，从 items 数组中开始搜索的偏移量。                                          |
| direction | number                                                                | \<可选> | 1      | 遍历数组的方向。 1是从头到尾，-1是从尾到头。                                     |

开始支持的版本：3.0.0

源代码： [src/actions/SetXY.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetXY.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetXY.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SetY

\<static> SetY(items, value \[, step] \[, index] \[, direction])

获取一个游戏对象数组，或任何具有公共 `y` 属性的对象，然后将给定值添加到它们的每个 `y` 属性。

可选的 `step` 属性以递增方式应用，乘以数组中的每个项目的索引值。

要将其与组一起使用时： `SetY(group.getChildren(), value, step)`

##### 参数：
| 名称      | 类型                                           | 声明    | 默认值 | 描述                                                                                       |
|-----------|------------------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------|
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 此操作要更新的项目数组。                                                  |
| value     | number                                         |             |         | 要将属性设置为的数值。                                                                |
| step      | number                                         | \<可选> | 0       | 步长，这个值将会持续加在 `value` 上。                           |
| index     | number                                         | \<可选> | 0       | 可选，从 items 数组中开始搜索的偏移量。                                |
| direction | number                                         | \<可选> | 1       | 遍历数组的方向。 1是从头到尾，-1是从尾到头。 |

开始支持的版本：3.0.0

源代码： [src/actions/SetY.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetY.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SetY.js#L9))

##### 返回值：

传递给此方法的对象数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### ShiftPosition

\<static> ShiftPosition(items, x, y \[, direction] \[, output])

遍历 items 数组，将每个元素的位置更改为数组中它前面的元素的位置（如果方向 = 1，则更改为它之后的元素的位置）

第一个项目位置设置为 x/y 坐标。

返回最终的 x/y 坐标

##### 参数：
| 名称      | 类型                                                                  | 声明    | 默认值 | 描述                                                   |
| --------- | --------------------------------------------------------------------- | ------- | ------ | ------------------------------------------------------ |
| items     | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 游戏对象的数组。此操作将更新此数组的内容。             |
| x         | number                                                                |         |        | 用于放置数组中第一项的 x 坐标。                        |
| y         | number                                                                |         |        | 用于放置数组中第一项的 y 坐标。                        |
| direction | number                                                                | \<可选> | 0      | 迭代方向。0 = 第一个到最后一个，1 = 最后一个到第一个。 |
| output    | [Phaser.Math.Vector2](类：Vector2.md) \| object                       | \<可选> |        | 一个可选的对象，用于存储最终对象的位置。               |

开始支持的版本：3.0.0

源代码： [src/actions/ShiftPosition.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ShiftPosition.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ShiftPosition.js#L9))

##### 返回值：

output对象（vector类型）

Type

[Phaser.Math.Vector2](类：Vector2.md)

---

#### Shuffle

\<static> Shuffle(items)

将数组随机排列。原数组既被修改又被返回。

##### 参数：
| 名称  | 类型                                           | 描述                                                                      |
|-------|------------------------------------------------|----------------------------------------------------------------------------------|
| items | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。 |

开始支持的版本：3.0.0

源代码： [src/actions/Shuffle.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Shuffle.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Shuffle.js#L9))

See:

-   [Phaser.Utils.Array.Shuffle](命名空间：Array.md#Shuffle)

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SmootherStep

\<static> SmootherStep(items, property, min, max \[, inc])

Smootherstep is a sigmoid-like interpolation and clamping function.

The function depends on three parameters, the input x, the "left edge" and the "right edge", with the left edge being assumed smaller than the right edge. The function receives a real number x as an argument and returns 0 if x is less than or equal to the left edge, 1 if x is greater than or equal to the right edge, and smoothly interpolates, using a Hermite polynomial, between 0 and 1 otherwise. The slope of the smoothstep function is zero at both edges. This is convenient for creating a sequence of transitions using smoothstep to interpolate each segment as an alternative to using more sophisticated or expensive interpolation techniques.

##### 参数：
| 名称     | 类型                                           | 声明    | 默认值 | 描述                                                                      |
|----------|------------------------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| items    | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 游戏对象的数组。此操作将更新此数组的内容。 |
| property | string                                         |             |         | The property of the Game Object to interpolate.                                  |
| min      | number                                         |             |         | The minimum interpolation value.                                                 |
| max      | number                                         |             |         | The maximum interpolation value.                                                 |
| inc      | boolean                                        | \<可选> | FALSE   | Should the values be incremented? true or set (false)                            |

开始支持的版本：3.0.0

源代码： [src/actions/SmootherStep.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SmootherStep.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SmootherStep.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### SmoothStep(这个和上方一样)

\<static> SmoothStep(items, property, min, max \[, inc])

Smoothstep is a sigmoid-like interpolation and clamping function.

The function depends on three parameters, the input x, the "left edge" and the "right edge", with the left edge being assumed smaller than the right edge. The function receives a real number x as an argument and returns 0 if x is less than or equal to the left edge, 1 if x is greater than or equal to the right edge, and smoothly interpolates, using a Hermite polynomial, between 0 and 1 otherwise. The slope of the smoothstep function is zero at both edges. This is convenient for creating a sequence of transitions using smoothstep to interpolate each segment as an alternative to using more sophisticated or expensive interpolation techniques.

##### 参数：
| 名称     | 类型                                           | 声明    | 默认值 | 描述                                                                      |
|----------|------------------------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| items    | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 游戏对象的数组。此操作将更新此数组的内容。 |
| property | string                                         |             |         | The property of the Game Object to interpolate.                                  |
| min      | number                                         |             |         | The minimum interpolation value.                                                 |
| max      | number                                         |             |         | The maximum interpolation value.                                                 |
| inc      | boolean                                        | \<可选> | FALSE   | Should the values be incremented? true or set (false)                            |

开始支持的版本：3.0.0

源代码： [src/actions/SmoothStep.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SmoothStep.js) ([Line 9](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/SmoothStep.js#L9))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### Spread

\<static> Spread(items, property, min, max \[, inc])

获取游戏对象的数组，然后修改其 `property` （“属性”），使值等于或递增计算出的分散值。

分散值源自给定的 `min` 和 `max` 值以及数组中的项目总数。

例如，要使精灵数组的 alpha 从 0 变为 1，您可以调用：

```
Phaser.Actions.Spread(itemsArray, 'alpha', 0, 1);
```

##### 参数：
| 名称     | 类型                                                                  | 声明    | 默认值 | 描述                                       |
| -------- | --------------------------------------------------------------------- | ------- | ------ | ------------------------------------------ |
| items    | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |         |        | 游戏对象的数组。此操作将更新此数组的内容。 |
| property | string                                                                |         |        | 要设置分散的游戏对象的属性。               |
| min      | number                                                                |         |        | 最小值                                     |
| max      | number                                                                |         |        | 最大值                                     |
| inc      | boolean                                                               | \<可选> | FALSE  | 值是否应该递增？`true`或设置（`false`）    |

开始支持的版本：3.0.0

源代码： [src/actions/Spread.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Spread.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/Spread.js#L7))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### ToggleVisible

\<static> ToggleVisible(items)

获取游戏对象的数组并切换每个对象的可见性。那些以前 `可见=假` 将变为 `可见=真` ，反之亦然。

##### 参数：
| 名称  | 类型                                           | 描述                                                                      |
|-------|------------------------------------------------|----------------------------------------------------------------------------------|
| items | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> | 游戏对象的数组。此操作将更新此数组的内容。 |

开始支持的版本：3.0.0

源代码： [src/actions/ToggleVisible.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ToggleVisible.js) ([Line 7](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/ToggleVisible.js#L7))

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>

---

#### WrapInRectangle
\<static> WrapInRectangle(items, rect \[, padding])

将每个项目的坐标包装在矩形的区域内。

##### 参数：
| 名称    | 类型                                           | 声明    | 默认值 | 描述                                                                      |
|---------|------------------------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| items   | array \| Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)\> |             |         | 游戏对象的数组。此操作将更新此数组的内容。 |
| rect    | [Phaser.Geom.Rectangle](类：Rectangle.md)                           |             |         | 矩形区域                                                                  |
| padding | number                                         | \<可选> | 0       | 在操作过程中添加到矩形每边的量。              |

开始支持的版本：3.0.0

源代码： [src/actions/WrapInRectangle.js](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/WrapInRectangle.js) ([Line 10](https://github.com/photonstorm/phaser/tree/v3.51.0/src/actions/WrapInRectangle.js#L10))

See:

-   [Phaser.Math.Wrap](命名空间：Math.md#Wrap)

##### 返回值：

传递给此操作的游戏对象的数组。

Type

array | Array.\<[Phaser.GameObjects.GameObject](类：GameObject.md)>