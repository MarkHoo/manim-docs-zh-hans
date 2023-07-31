# 宝丽码[#](#polygram "此标题的固定链接")

合格名称：`manim.mobject.geometry.polygram.Polygram`

_类_ Polygram ( _\* vertex_groups_ , _color = '#58C4DD'_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/polygram.html#Polygram)[#](#manim.mobject.geometry.polygram.Polygram "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

广义的[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon")，允许断开连接的边集。

参数

- **vertex_groups** (_可迭代**\[**序列\_\_\[_ _float_ _\]_ _\]_ ) –

  组成 的顶点组[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。

  重复每组中的第一个顶点以闭合形状。每个点必须是 3 维的：`[x,y,z]`

- **颜色**– 的颜色[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。
- **kwargs** – 转发到父构造函数。

例子

示例：Polygram 示例[¶](#polygramexample)

from manim import \*

import numpy as np

class PolygramExample(Scene):
def construct(self):
hexagram = Polygram(
\[\[0, 2, 0\], \[-np.sqrt(3), -1, 0\], \[np.sqrt(3), -1, 0\]\],
\[\[-np.sqrt(3), 1, 0\], \[0, -2, 0\], \[np.sqrt(3), 1, 0\]\],
)
self.add(hexagram)

        dot = Dot()
        self.play(MoveAlongPath(dot, hexagram), run_time=5, rate_func=linear)
        self.remove(dot)
        self.wait()

Copy to clipboard

方法

[`get_vertex_groups`](#manim.mobject.geometry.polygram.Polygram.get_vertex_groups "manim.mobject.geometry.polygram.Polygram.get_vertex_groups")

获取 的顶点组[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。

[`get_vertices`](#manim.mobject.geometry.polygram.Polygram.get_vertices "manim.mobject.geometry.polygram.Polygram.get_vertices")

获取 的顶点[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。

[`round_corners`](#manim.mobject.geometry.polygram.Polygram.round_corners "manim.mobject.geometry.polygram.Polygram.round_corners")

将 的角磨圆[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。

获取顶点组( )[\[来源\]](../_modules/manim/mobject/geometry/polygram.html#Polygram.get_vertex_groups)[#](#manim.mobject.geometry.polygram.Polygram.get_vertex_groups "此定义的固定链接")

获取 的顶点组[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。

退货

的顶点组[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。

返回类型

`numpy.ndarray`

例子

> > \> poly = Polygram(\[ORIGIN, RIGHT, UP\], \[LEFT, LEFT + UP, 2 \* LEFT\])
> > \> poly.get_vertex_groups()
> > array(\[\[\[ 0., 0., 0.\],
> > \[ 1., 0., 0.\],
> > \[ 0., 1., 0.\]\],

\[\[-1., 0., 0.\],
\[-1., 1., 0.\],
\[-2., 0., 0.\]\]\])

Copy to clipboard

获取顶点( )[\[来源\]](../_modules/manim/mobject/geometry/polygram.html#Polygram.get_vertices)[#](#manim.mobject.geometry.polygram.Polygram.get_vertices "此定义的固定链接")

获取 的顶点[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。

退货

的顶点[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。

返回类型

`numpy.ndarray`

例子

> > \> sq = Square()
> > \> sq.get_vertices()
> > array(\[\[ 1., 1., 0.\],
> > \[-1., 1., 0.\],
> > \[-1., -1., 0.\],
> > \[ 1., -1., 0.\]\])

Copy to clipboard

圆角（_半径= 0.5_，_均匀分配锚点=假_，_组件每个圆角= 2_）[\[来源\]](../_modules/manim/mobject/geometry/polygram.html#Polygram.round_corners)[#](#manim.mobject.geometry.polygram.Polygram.round_corners "此定义的固定链接")

将 的角磨圆[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。

参数

- **radius** ( _float_ _|_ _list_ _\[_ _float_ _\]_ ) – 角点的曲率[`Polygram`](#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")。
- **Evenly_distribute_anchors** ( _bool_ ) – 将长线段分成按比例大小的线段。
- **Components_per_rounded_corner** ( _int_ ) – 用于表示圆角曲线的点数。

也可以看看

`RoundedRectangle`

笔记

如果半径作为单个值提供，则相同的半径将应用于所有角。如果 radius 是一个列表，则将按顺序应用各个值，第一个角接收 radius\[0\]，第二个角接收 radius\[1\]等。半径列表将根据需要重复。

提供 components_per_rounded_corner 值以便可以根据需要微调圆角的保真度。2 对于大多数形状来说都是合适的值，但是如果圆角特别大，则可能需要更大的值。2 是允许的最小数字，代表曲线的起点和终点。3 将产生起点、中间点和终点，这意味着将生成 2 条曲线。

提供了 evenly_distribute_anchors 选项，以便可以将线段（圆角后剩余的每条线的部分）细分为与圆角平均密度相似的密度。在需要在稍后的变换动画中使用均匀分布的曲线的情况下，这可能是理想的。但请注意，启用此选项可能会导致对象包含比原始对象多得多的点，尤其是当圆角曲线较小时。

例子

示例：PolygramRoundCorners [¶](#polygramroundcorners)

![../_images/PolygramRoundCorners-1.png](../_images/PolygramRoundCorners-1.png)

from manim import \*

class PolygramRoundCorners(Scene):
def construct(self):
star = Star(outer_radius=2)

        shapes = VGroup(star)
        shapes.add(star.copy().round_corners(radius=0.1))
        shapes.add(star.copy().round_corners(radius=0.25))

        shapes.arrange(RIGHT)
        self.add(shapes)

Copy to clipboard
