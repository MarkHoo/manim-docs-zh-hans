# 正多边形[#](#regularpolygon "此标题的固定链接")

合格名称：`manim.mobject.geometry.polygram.RegularPolygon`

_类_ RegularPolygon ( _n = 6_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/polygram.html#RegularPolygon)[#](#manim.mobject.geometry.polygram.RegularPolygon "此定义的固定链接")

基地：[`RegularPolygram`](manim.mobject.geometry.polygram.RegularPolygram.html#manim.mobject.geometry.polygram.RegularPolygram "manim.mobject.geometry.polygram.RegularPolygram")

n 边正则[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon").

参数

- **n** ( _int_ ) – 的边数[`RegularPolygon`](#manim.mobject.geometry.polygram.RegularPolygon "manim.mobject.geometry.polygram.RegularPolygon")。
- **kwargs** – 转发到父构造函数。

例子

示例：正则多边形示例[¶](#regularpolygonexample)

![../_images/RegularPolygonExample-1.png](../_images/RegularPolygonExample-1.png)

from manim import \*

class RegularPolygonExample(Scene):
def construct(self):
poly_1 = RegularPolygon(n=6)
poly_2 = RegularPolygon(n=6, start_angle=30\*DEGREES, color=GREEN)
poly_3 = RegularPolygon(n=10, color=RED)

        poly_group = Group(poly_1, poly_2, poly_3).scale(1.5).arrange(buff=1)
        self.add(poly_group)

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
