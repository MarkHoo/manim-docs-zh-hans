# 箭头提示

合格名称：`manim.mobject.geometry.tips.ArrowTip`

_类_ ArrowTip ( _\* args_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/tips.html#ArrowTip)[#](#manim.mobject.geometry.tips.ArrowTip "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

箭头提示的基类。

也可以看看

[`ArrowTriangleTip`](manim.mobject.geometry.tips.ArrowTriangleTip.html#manim.mobject.geometry.tips.ArrowTriangleTip "manim.mobject.geometry.tips.ArrowTriangleTip") [`ArrowTriangleFilledTip`](manim.mobject.geometry.tips.ArrowTriangleFilledTip.html#manim.mobject.geometry.tips.ArrowTriangleFilledTip "manim.mobject.geometry.tips.ArrowTriangleFilledTip") [`ArrowCircleTip`](manim.mobject.geometry.tips.ArrowCircleTip.html#manim.mobject.geometry.tips.ArrowCircleTip "manim.mobject.geometry.tips.ArrowCircleTip") [`ArrowCircleFilledTip`](manim.mobject.geometry.tips.ArrowCircleFilledTip.html#manim.mobject.geometry.tips.ArrowCircleFilledTip "manim.mobject.geometry.tips.ArrowCircleFilledTip") [`ArrowSquareTip`](manim.mobject.geometry.tips.ArrowSquareTip.html#manim.mobject.geometry.tips.ArrowSquareTip "manim.mobject.geometry.tips.ArrowSquareTip") [`ArrowSquareFilledTip`](manim.mobject.geometry.tips.ArrowSquareFilledTip.html#manim.mobject.geometry.tips.ArrowSquareFilledTip "manim.mobject.geometry.tips.ArrowSquareFilledTip") [`StealthTip`](manim.mobject.geometry.tips.StealthTip.html#manim.mobject.geometry.tips.StealthTip "manim.mobject.geometry.tips.StealthTip")

例子

不能直接使用，仅用于继承：

> > \> tip = ArrowTip()
> > Traceback (most recent call last):
> > ...
> > NotImplementedError: Has to be implemented in inheriting subclasses.

Copy to clipboard

相反，使用预定义的之一，或制作一个自定义的，如下所示：

示例：自定义提示示例[¶](#customtipexample)

from manim import \*

> > > from manim import RegularPolygon, Arrow
> > > class MyCustomArrowTip(ArrowTip, RegularPolygon):
> > > ... def \_\_init\_\_(self, length=0.35, **kwargs):
> > > ... RegularPolygon.\_\_init\_\_(self, n=5, **kwargs)
> > > ... self.width = length
> > > ... self.stretch_to_fit_height(length)
> > > arr = Arrow(np.array(\[-2, -2, 0\]), np.array(\[2, 2, 0\]),
> > > ... tip_shape=MyCustomArrowTip)
> > > isinstance(arr.tip, RegularPolygon)
> > > True
> > > from manim import Scene, Create
> > > class CustomTipExample(Scene):
> > > ... def construct(self):
> > > ... self.play(Create(arr))

Copy to clipboard

使用继承自的类来[`ArrowTip`](#manim.mobject.geometry.tips.ArrowTip "manim.mobject.geometry.tips.ArrowTip")获取未填充的提示是手动指定箭头提示样式的简写，如下所示：

> > \> arrow = Arrow(np.array(\[0, 0, 0\]), np.array(\[1, 1, 0\]),
> > ... tip_style={'fill_opacity': 0, 'stroke_width': 3})

Copy to clipboard

以下示例说明了所有预定义箭头提示的用法。

示例：ArrowTipsShowcase [¶](#arrowtipsshowcase)

![../_images/ArrowTipsShowcase-1.png](../_images/ArrowTipsShowcase-1.png)

from manim import \*

from manim.mobject.geometry.tips import ArrowTriangleTip,\
 ArrowSquareTip, ArrowSquareFilledTip,\
 ArrowCircleTip, ArrowCircleFilledTip
class ArrowTipsShowcase(Scene):
def construct(self):
a00 = Arrow(start=\[-2, 3, 0\], end=\[2, 3, 0\], color=YELLOW)
a11 = Arrow(start=\[-2, 2, 0\], end=\[2, 2, 0\], tip_shape=ArrowTriangleTip)
a12 = Arrow(start=\[-2, 1, 0\], end=\[2, 1, 0\])
a21 = Arrow(start=\[-2, 0, 0\], end=\[2, 0, 0\], tip_shape=ArrowSquareTip)
a22 = Arrow(\[-2, -1, 0\], \[2, -1, 0\], tip_shape=ArrowSquareFilledTip)
a31 = Arrow(\[-2, -2, 0\], \[2, -2, 0\], tip_shape=ArrowCircleTip)
a32 = Arrow(\[-2, -3, 0\], \[2, -3, 0\], tip_shape=ArrowCircleFilledTip)
b11 = a11.copy().scale(0.5, scale_tips=True).next_to(a11, RIGHT)
b12 = a12.copy().scale(0.5, scale_tips=True).next_to(a12, RIGHT)
b21 = a21.copy().scale(0.5, scale_tips=True).next_to(a21, RIGHT)
self.add(a00, a11, a12, a21, a22, a31, a32, b11, b12, b21)

Copy to clipboard

方法

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

[`base`](#manim.mobject.geometry.tips.ArrowTip.base "manim.mobject.geometry.tips.ArrowTip.base")

箭头尖端的基点。

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

[`length`](#manim.mobject.geometry.tips.ArrowTip.length "manim.mobject.geometry.tips.ArrowTip.length")

箭头尖端的长度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

[`tip_angle`](#manim.mobject.geometry.tips.ArrowTip.tip_angle "manim.mobject.geometry.tips.ArrowTip.tip_angle")

箭头尖端的角度。

[`tip_point`](#manim.mobject.geometry.tips.ArrowTip.tip_point "manim.mobject.geometry.tips.ArrowTip.tip_point")

箭头尖端的尖端点。

[`vector`](#manim.mobject.geometry.tips.ArrowTip.vector "manim.mobject.geometry.tips.ArrowTip.vector")

从基点指向端点的矢量。

`width`

mobject 的宽度。

_财产_ 基础[#](#manim.mobject.geometry.tips.ArrowTip.base "此定义的固定链接")

箭头尖端的基点。

这是连接到箭头线的点。

例子

> > \> from manim import Arrow
> > \> arrow = Arrow(np.array(\[0, 0, 0\]), np.array(\[2, 0, 0\]), buff=0)
> > \> arrow.tip.base.round(2) + 0. \# add 0. to avoid negative 0 in output
> > array(\[1.65, 0. , 0. \])

Copy to clipboard

_属性_ 长度[#](#manim.mobject.geometry.tips.ArrowTip.length "此定义的固定链接")

箭头尖端的长度。

例子

> > \> from manim import Arrow
> > \> arrow = Arrow(np.array(\[0, 0, 0\]), np.array(\[1, 2, 0\]))
> > \> round(arrow.tip.length, 3)
> > 0.35

Copy to clipboard

_属性_ tip_angle [#](#manim.mobject.geometry.tips.ArrowTip.tip_angle "此定义的固定链接")

箭头尖端的角度。

例子

> > \> from manim import Arrow
> > \> arrow = Arrow(np.array(\[0, 0, 0\]), np.array(\[1, 1, 0\]), buff=0)
> > \> round(arrow.tip.tip_angle, 5) == round(PI/4, 5)
> > True

Copy to clipboard

_属性_ 提示点[#](#manim.mobject.geometry.tips.ArrowTip.tip_point "此定义的固定链接")

箭头尖端的尖端点。

例子

> > \> from manim import Arrow
> > \> arrow = Arrow(np.array(\[0, 0, 0\]), np.array(\[2, 0, 0\]), buff=0)
> > \> arrow.tip.tip_point.round(2) + 0.
> > array(\[2., 0., 0.\])

Copy to clipboard

_属性_ 向量[#](#manim.mobject.geometry.tips.ArrowTip.vector "此定义的固定链接")

从基点指向端点的矢量。

例子

> > \> from manim import Arrow
> > \> arrow = Arrow(np.array(\[0, 0, 0\]), np.array(\[2, 2, 0\]), buff=0)
> > \> arrow.tip.vector.round(2) + 0.
> > array(\[0.25, 0.25, 0. \])

Copy to clipboard
