# VGroup

合格名称：`manim.mobject.types.vectorized\_mobject.VGroup`


```py

```

一组矢量化的对象。

这可用于将多个[`VMobject`]()实例分组在一起，以便缩放、移动……它们在一起。

笔记

当多次添加相同的 mobject 时，重复的内容将被忽略。用于[`Mobject.copy()`]()创建一个单独的副本，然后可以将其添加到组中。

例子

要添加`VGroup`，您可以使用 [`add()`]()方法，或使用+和+=运算符。`remove()`同样，您可以通过方法或 -和-=运算符减去 VGroup 的元素：

```py

```


示例：ArcShapeIris 

![ArcShapeIris-1.png](../../static/ArcShapeIris-1.png)

```py

```


方法

|||
|-|-|
[`add`]()|检查所有传递的元素是否是 VMobject 的实例，然后将它们添加到 submobjects


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


添加（_\* vmobjects_）

检查所有传递的元素是否是 VMobject 的实例，然后将它们添加到 submobjects

参数

**vmobjects** ( [_VMobject_]() ) – 要添加的 VMobject 列表

返回类型

[`VGroup`]()

提高

**TypeError** – 如果列表的一个元素不是 VMobject 的实例

例子

示例：添加到 VGroup 

```py

```
