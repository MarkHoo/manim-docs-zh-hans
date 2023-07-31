# 圆角矩形[#](#roundedrectangle "此标题的固定链接")

合格名称：`manim.mobject.geometry.polygram.RoundedRectangle`

_类_ RoundedRectangle (_角半径= 0.5_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/polygram.html#RoundedRectangle)[#](#manim.mobject.geometry.polygram.RoundedRectangle "此定义的固定链接")

基地：[`Rectangle`](manim.mobject.geometry.polygram.Rectangle.html#manim.mobject.geometry.polygram.Rectangle "manim.mobject.geometry.polygram.矩形")

带圆角的矩形。

参数

- **corner_radius** ( _float_ _|_ _list_ _\[_ _float_ _\]_ ) – 矩形角的曲率。
- **kwargs** – 要传递给的附加参数[`Rectangle`](manim.mobject.geometry.polygram.Rectangle.html#manim.mobject.geometry.polygram.Rectangle "manim.mobject.geometry.polygram.矩形")

例子

示例：圆角矩形示例[¶](#roundedrectangleexample)

![../_images/RoundedRectangleExample-1.png](../_images/RoundedRectangleExample-1.png)

from manim import \*

class RoundedRectangleExample(Scene):
def construct(self):
rect_1 = RoundedRectangle(corner_radius=0.5)
rect_2 = RoundedRectangle(corner_radius=1.5, height=4.0, width=4.0)

        rect_group = Group(rect_1, rect_2).arrange(buff=1)
        self.add(rect_group)

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
