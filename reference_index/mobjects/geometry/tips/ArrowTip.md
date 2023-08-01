# 箭头提示

合格名称：`manim.mobject.geometry.tips.ArrowTip`

_类_ ArrowTip ( _\* args_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/tips.html#ArrowTip)[#](#manim.mobject.geometry.tips.ArrowTip "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

箭头提示的基类。

也可以看看

[`ArrowTriangleTip`]() [`ArrowTriangleFilledTip`]() [`ArrowCircleTip`]() [`ArrowCircleFilledTip`]() [`ArrowSquareTip`]() [`ArrowSquareFilledTip`]() [`StealthTip`]()

例子

不能直接使用，仅用于继承：


```py

```


相反，使用预定义的之一，或制作一个自定义的，如下所示：

示例：自定义提示示例


```py

```


使用继承自的类来[`ArrowTip`]()获取未填充的提示是手动指定箭头提示样式的简写，如下所示：


```py

```


以下示例说明了所有预定义箭头提示的用法。

示例：ArrowTipsShowcase 

![ArrowTipsShowcase-1.png](../static/ArrowTipsShowcase-1.png)


```py

```


方法



属性


`animate`
用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`
[`base`]()
箭头尖端的基点。
`color`
`depth`
对象的深度。
`fill_color`
如果有多种颜色（对于渐变），则返回第一个颜色
`height`
mobject 的高度。
[`length`]()
箭头尖端的长度。
`n_points_per_curve`
`sheen_factor`
`stroke_color`
[`tip_angle`]()
箭头尖端的角度。
[`tip_point`]()
箭头尖端的尖端点。
[`vector`]()
从基点指向端点的矢量。
`width`
mobject 的宽度。


_财产_ 基础

箭头尖端的基点。

这是连接到箭头线的点。

例子


```py

```


_属性_ 长度

箭头尖端的长度。

例子


```py

```


_属性_ tip_angle 

箭头尖端的角度。

例子


```py

```


_属性_ 提示点

箭头尖端的尖端点。

例子


```py

```


_属性_ 向量

从基点指向端点的矢量。

例子


```py

```

