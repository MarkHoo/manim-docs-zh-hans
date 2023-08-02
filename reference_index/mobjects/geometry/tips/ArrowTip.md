# 箭头提示

合格名称：`manim.mobject.geometry.tips.ArrowTip`


```py
class ArrowTip(*args, **kwargs)
```

Bases: `VMobject`

箭头提示的基类。

> 也可以看看

> [`ArrowTriangleTip`]() [`ArrowTriangleFilledTip`]() [`ArrowCircleTip`]() [`ArrowCircleFilledTip`]() [`ArrowSquareTip`]() [`ArrowSquareFilledTip`]() [`StealthTip`]()

例子

不能直接使用，仅用于继承：


```sh
>>> tip = ArrowTip()
Traceback (most recent call last):
...
NotImplementedError: Has to be implemented in inheriting subclasses.
```


相反，使用预定义的之一，或制作一个自定义的，如下所示：

示例：自定义提示示例


```sh
from manim import *

>>> from manim import RegularPolygon, Arrow
>>> class MyCustomArrowTip(ArrowTip, RegularPolygon):
...     def __init__(self, length=0.35, **kwargs):
...         RegularPolygon.__init__(self, n=5, **kwargs)
...         self.width = length
...         self.stretch_to_fit_height(length)
>>> arr = Arrow(np.array([-2, -2, 0]), np.array([2, 2, 0]),
...             tip_shape=MyCustomArrowTip)
>>> isinstance(arr.tip, RegularPolygon)
True
>>> from manim import Scene, Create
>>> class CustomTipExample(Scene):
...     def construct(self):
...         self.play(Create(arr))
```


使用继承自的类来[`ArrowTip`]()获取未填充的提示是手动指定箭头提示样式的简写，如下所示：


```sh
>>> arrow = Arrow(np.array([0, 0, 0]), np.array([1, 1, 0]),
              tip_style={'fill_opacity': 0, 'stroke_width': 3})
```


以下示例说明了所有预定义箭头提示的用法。

示例：ArrowTipsShowcase 

![ArrowTipsShowcase-1.png](../static/ArrowTipsShowcase-1.png)


```py
from manim import *

from manim.mobject.geometry.tips import ArrowTriangleTip,\
                                        ArrowSquareTip, ArrowSquareFilledTip,\
                                        ArrowCircleTip, ArrowCircleFilledTip
class ArrowTipsShowcase(Scene):
    def construct(self):
        a00 = Arrow(start=[-2, 3, 0], end=[2, 3, 0], color=YELLOW)
        a11 = Arrow(start=[-2, 2, 0], end=[2, 2, 0], tip_shape=ArrowTriangleTip)
        a12 = Arrow(start=[-2, 1, 0], end=[2, 1, 0])
        a21 = Arrow(start=[-2, 0, 0], end=[2, 0, 0], tip_shape=ArrowSquareTip)
        a22 = Arrow([-2, -1, 0], [2, -1, 0], tip_shape=ArrowSquareFilledTip)
        a31 = Arrow([-2, -2, 0], [2, -2, 0], tip_shape=ArrowCircleTip)
        a32 = Arrow([-2, -3, 0], [2, -3, 0], tip_shape=ArrowCircleFilledTip)
        b11 = a11.copy().scale(0.5, scale_tips=True).next_to(a11, RIGHT)
        b12 = a12.copy().scale(0.5, scale_tips=True).next_to(a12, RIGHT)
        b21 = a21.copy().scale(0.5, scale_tips=True).next_to(a21, RIGHT)
        self.add(a00, a11, a12, a21, a22, a31, a32, b11, b12, b21)
```


方法



属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
[`base`]()|箭头尖端的基点。
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
[`length`]()|箭头尖端的长度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
[`tip_angle`]()|箭头尖端的角度。
[`tip_point`]()|箭头尖端的尖端点。
[`vector`]()|从基点指向端点的矢量。
`width`|mobject 的宽度。


_属性_ `base`

箭头尖端的基点。

这是连接到箭头线的点。

例子

```sh
>>> from manim import Arrow
>>> arrow = Arrow(np.array([0, 0, 0]), np.array([2, 0, 0]), buff=0)
>>> arrow.tip.base.round(2) + 0.  # add 0. to avoid negative 0 in output
array([1.65, 0.  , 0.  ])
```

_属性_ `length`

箭头尖端的长度。

例子

```sh
>>> from manim import Arrow
>>> arrow = Arrow(np.array([0, 0, 0]), np.array([1, 2, 0]))
>>> round(arrow.tip.length, 3)
0.35
```


_属性_ `tip_angle`

箭头尖端的角度。

例子

```sh
>>> from manim import Arrow
>>> arrow = Arrow(np.array([0, 0, 0]), np.array([1, 1, 0]), buff=0)
>>> round(arrow.tip.tip_angle, 5) == round(PI/4, 5)
True
```


_属性_ `tip_point`

箭头尖端的尖端点。

例子

```sh
>>> from manim import Arrow
>>> arrow = Arrow(np.array([0, 0, 0]), np.array([2, 0, 0]), buff=0)
>>> arrow.tip.tip_point.round(2) + 0.
array([2., 0., 0.])
```


_属性_ `vector`

从基点指向端点的矢量。

例子


```sh
>>> from manim import Arrow
>>> arrow = Arrow(np.array([0, 0, 0]), np.array([2, 2, 0]), buff=0)
>>> arrow.tip.vector.round(2) + 0.
array([0.25, 0.25, 0.  ])
```

