# 隐身提示

合格名称：`manim.mobject.geometry.tips.StealthTip`


```py
class StealthTip(fill_opacity=1, stroke_width=3, length=0.175, start_angle=3.141592653589793, **kwargs)
```

Bases: `ArrowTip`

“隐形”战斗机/风筝箭形状。

命名灵感来自于对应的 [TikZ 箭头形状](https://tikz.dev/tikz-arrows#sec-16.3)。

方法



属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`base`|箭头尖端的基点。
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
[`length`]()|箭头尖端的长度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`tip_angle`|箭头尖端的角度。
`tip_point`|箭头尖端的尖端点。
`vector`|从基点指向端点的矢量。
`width`|mobject 的宽度。


_属性_ `length`

箭头尖端的长度。

在这种情况下，长度计算为包围隐形尖端的三角形的高度（否则，尖端缩放得太大）。
