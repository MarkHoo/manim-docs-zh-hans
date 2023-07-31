# 圈[#](#circle "此标题的固定链接")

合格名称：`manim.mobject.geometry.arc.Circle`

圆*类*（_半径=无_，_颜色= '#FC6255'_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Circle)[#](#manim.mobject.geometry.arc.Circle "此定义的固定链接")

基地：[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc")

一个圆圈。

参数

- **color** ( _Color_ _|_ _str_ ) – 形状的颜色。
- **kwargs** – 要传递给的附加参数[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc")
- **半径**（_浮点数**|**无_）–

例子

示例：圆形示例[¶](#circleexample)

![../_images/CircleExample-1.png](../_images/CircleExample-1.png)

from manim import \*

class CircleExample(Scene):
def construct(self):
circle_1 = Circle(radius=1.0)
circle_2 = Circle(radius=1.5, color=GREEN)
circle_3 = Circle(radius=1.0, color=BLUE_B, fill_opacity=1)

        circle_group = Group(circle_1, circle_2, circle_3).arrange(buff=1)
        self.add(circle_group)

Copy to clipboard

方法

[`from_three_points`](#manim.mobject.geometry.arc.Circle.from_three_points "manim.mobject.geometry.arc.Circle.from_ Three_points")

返回经过指定三个点的圆。

[`point_at_angle`](#manim.mobject.geometry.arc.Circle.point_at_angle "manim.mobject.geometry.arc.Circle.point_at_angle")

返回圆上点的位置。

[`surround`](#manim.mobject.geometry.arc.Circle.surround "manim.mobject.geometry.arc.Circle.surround")

修改一个圆，使其包围给定的对象。

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

_静态_ from*two_points ( \_p1* , _p2_ , _p3_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Circle.from_three_points)[#](#manim.mobject.geometry.arc.Circle.from_three_points "此定义的固定链接")

返回经过指定三个点的圆。

例子

示例：CircleFromPointsExample [¶](#circlefrompointsexample)

![../_images/CircleFromPointsExample-1.png](../_images/CircleFromPointsExample-1.png)

from manim import \*

class CircleFromPointsExample(Scene):
def construct(self):
circle = Circle.from*three_points(LEFT, LEFT + UP, UP * 2, color=RED)
dots = VGroup(
Dot(LEFT),
Dot(LEFT + UP),
Dot(UP \_ 2),
)
self.add(NumberPlane(), circle, dots)

Copy to clipboard

参数

- **p1** (_序列\_\_\[_ _float_ _\]_ ) –
- **p2** (_序列\_\_\[_ _float_ _\]_ ) –
- **p3** (_序列\_\_\[_ _float_ _\]_ ) –

角度点（_角度_）[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Circle.point_at_angle)[#](#manim.mobject.geometry.arc.Circle.point_at_angle "此定义的固定链接")

返回圆上点的位置。

参数

**angle** ( _float_ ) – 点沿圆的角度（以弧度表示）。

退货

点沿圆圆周的位置。

返回类型

`numpy.ndarray`

例子

示例：PointAtAngleExample [¶](#pointatangleexample)

![../_images/PointAtAngleExample-1.png](../_images/PointAtAngleExample-1.png)

from manim import \*

class PointAtAngleExample(Scene):
def construct(self):
circle = Circle(radius=2.0)
p1 = circle.point_at_angle(PI/2)
p2 = circle.point_at_angle(270\*DEGREES)

        s1 = Square(side_length=0.25).move_to(p1)
        s2 = Square(side_length=0.25).move_to(p2)
        self.add(circle, s1, s2)

Copy to clipboard

环绕（_mobject_， _dim_to_match = 0_， _stretch = False_， _buffer_factor = 1.2_）[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Circle.surround)[#](#manim.mobject.geometry.arc.Circle.surround "此定义的固定链接")

修改一个圆，使其包围给定的对象。

参数

- **mobject** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 圆将围绕的 mobject。
- **dim_to_match** ( _int_ ) –
- **buffer_factor** ( _float_ ) – 相对于 mobject 缩放圆。buffer_factor < 1 使圆小于 mobject。
- **stretch** ( _bool_ ) – 拉伸圆以更紧密地围绕对象。注意：不适用于`Line`

例子

示例：圆形环绕[¶](#circlesurround)

![../_images/CircleSurround-1.png](../_images/CircleSurround-1.png)

from manim import \*

class CircleSurround(Scene):
def construct(self):
triangle1 = Triangle()
circle1 = Circle().surround(triangle1)
group1 = Group(triangle1,circle1) \# treat the two mobjects as one

        line2 = Line()
        circle2 = Circle().surround(line2, buffer_factor=2.0)
        group2 = Group(line2,circle2)

        \# buffer_factor < 1, so the circle is smaller than the square
        square3 = Square()
        circle3 = Circle().surround(square3, buffer_factor=0.5)
        group3 = Group(square3, circle3)

        group = Group(group1, group2, group3).arrange(buff=1)
        self.add(group)

Copy to clipboard
