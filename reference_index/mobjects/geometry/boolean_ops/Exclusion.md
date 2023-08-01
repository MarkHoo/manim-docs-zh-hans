# 排除

合格名称：`manim.mobject.geometry.boolean\_ops.Exclusion`

排除*类*（_主题_、_剪辑_、 _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/boolean_ops.html#Exclusion)[#](#manim.mobject.geometry.boolean_ops.Exclusion "此定义的固定链接")

基地：`_BooleanOps`

求两个 之间的异或[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。这将创建一个新的[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")区域，该区域由其中一个区域所覆盖。

参数

- **主题**——第一[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。
- **剪辑**– 第二个[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

例子

示例：Intersection 示例[¶](#intersectionexample)

![../_images/IntersectionExample-1.png](../_images/IntersectionExample-1.png)

from manim import \*

class IntersectionExample(Scene):
def construct(self):
sq = Square(color=RED, fill_opacity=1)
sq.move_to(\[-2, 0, 0\])
cr = Circle(color=BLUE, fill_opacity=1)
cr.move_to(\[-1.3, 0.7, 0\])
un = Exclusion(sq, cr, color=GREEN, fill_opacity=1)
un.move_to(\[1.5, 0.4, 0\])
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
