# 隐身提示[#](#stealthtip "此标题的固定链接")

合格名称：`manim.mobject.geometry.tips.StealthTip`

_类_ StealthTip ( _fill_opacity = 1_ , _stroke_width = 3_ , _length = 0.175_ , _start_angle = 3.141592653589793_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/tips.html#StealthTip)[#](#manim.mobject.geometry.tips.StealthTip "此定义的固定链接")

基地：[`ArrowTip`](manim.mobject.geometry.tips.ArrowTip.html#manim.mobject.geometry.tips.ArrowTip "manim.mobject.geometry.tips.ArrowTip")

“隐形”战斗机/风筝箭形状。

命名灵感来自于对应的 [TikZ 箭头形状](https://tikz.dev/tikz-arrows#sec-16.3)。

方法

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`base`

箭头尖端的基点。

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

[`length`](#manim.mobject.geometry.tips.StealthTip.length "manim.mobject.geometry.tips.StealthTip.length")

箭头尖端的长度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`tip_angle`

箭头尖端的角度。

`tip_point`

箭头尖端的尖端点。

`vector`

从基点指向端点的矢量。

`width`

mobject 的宽度。

_属性_ 长度[#](#manim.mobject.geometry.tips.StealthTip.length "此定义的固定链接")

箭头尖端的长度。

在这种情况下，长度计算为包围隐形尖端的三角形的高度（否则，尖端缩放得太大）。