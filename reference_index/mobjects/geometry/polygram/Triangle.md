# 三角形

合格名称：`manim.mobject.geometry.polygram.Triangle`

三角形*类*( _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/polygram.html#Triangle)[#](#manim.mobject.geometry.polygram.Triangle "此定义的固定链接")

基地：[`RegularPolygon`](manim.mobject.geometry.polygram.RegularPolygon.html#manim.mobject.geometry.polygram.RegularPolygon "manim.mobject.geometry.polygram.RegularPolygon")

一个等边三角形。

参数

**kwargs** – 要传递给的附加参数[`RegularPolygon`](manim.mobject.geometry.polygram.RegularPolygon.html#manim.mobject.geometry.polygram.RegularPolygon "manim.mobject.geometry.polygram.RegularPolygon")

例子

示例：三角形示例[¶](#triangleexample)

![../_images/TriangleExample-1.png](../_images/TriangleExample-1.png)

from manim import \*

class TriangleExample(Scene):
def construct(self):
triangle_1 = Triangle()
triangle_2 = Triangle().scale(2).rotate(60\*DEGREES)
tri_group = Group(triangle_1, triangle_2).arrange(buff=1)
self.add(tri_group)

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
