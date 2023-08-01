# 联盟

合格名称：`manim.mobject.geometry.boolean\_ops.Union`

_类_ Union ( _\* vmobjects_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/boolean_ops.html#Union)[#](#manim.mobject.geometry.boolean_ops.Union "此定义的固定链接")

基地：`_BooleanOps`

两个或多个[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")s 的并集。这将返回 s 的公共区域`VMobject`。

参数

**vmobjects** ( [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) –[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")要查找并集的 s。

提高

**ValueError**[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") – 如果经过的时间少于 2 秒。

例子

示例：UnionExample [¶](#unionexample)

![../_images/UnionExample-1.png](../_images/UnionExample-1.png)

from manim import \*

class UnionExample(Scene):
def construct(self):
sq = Square(color=RED, fill_opacity=1)
sq.move_to(\[-2, 0, 0\])
cr = Circle(color=BLUE, fill_opacity=1)
cr.move_to(\[-1.3, 0.7, 0\])
un = Union(sq, cr, color=GREEN, fill_opacity=1)
un.move_to(\[1.5, 0.3, 0\])
self.add(sq, cr, un)

Copy to clipboard

方法

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
