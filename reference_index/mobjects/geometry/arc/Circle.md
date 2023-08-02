# 圈

合格名称：`manim.mobject.geometry.arc.Circle`

```py
class Circle(radius=None, color='#FC6255', **kwargs)
```

Bases: `Arc`

一个圆圈。

参数

- **color** ( _Color_ _|_ _str_ ) – 形状的颜色。
- **kwargs** – 要传递给的附加参数[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc")
- **radius**（_浮点数**|**无_）–

例子

示例：圆形示例

![CircleExample-1.png](../static/CircleExample-1.png)

```py
from manim import *

class CircleExample(Scene):
    def construct(self):
        circle_1 = Circle(radius=1.0)
        circle_2 = Circle(radius=1.5, color=GREEN)
        circle_3 = Circle(radius=1.0, color=BLUE_B, fill_opacity=1)

        circle_group = Group(circle_1, circle_2, circle_3).arrange(buff=1)
        self.add(circle_group)
```

方法

|||
|-|-|
[`from_three_points`]()|返回经过指定三个点的圆。
[`point_at_angle`]()|返回圆上点的位置。
[`surround`]()|修改一个圆，使其包围给定的对象。


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


`static from_three_points(p1, p2, p3, **kwargs)`

返回经过指定三个点的圆。

例子

示例：CircleFromPointsExample

![CircleFromPointsExample-1.png](../static/CircleFromPointsExample-1.png)

```py
from manim import *

class CircleFromPointsExample(Scene):
    def construct(self):
        circle = Circle.from_three_points(LEFT, LEFT + UP, UP * 2, color=RED)
        dots = VGroup(
            Dot(LEFT),
            Dot(LEFT + UP),
            Dot(UP * 2),
        )
        self.add(NumberPlane(), circle, dots)
```

参数

- **p1** (_Sequence\_\_\[_ _float_ _\]_ ) –
- **p2** (_Sequence\_\_\[_ _float_ _\]_ ) –
- **p3** (_Sequence\_\_\[_ _float_ _\]_ ) –

`point_at_angle(angle)`

返回圆上点的位置。

参数

**angle** ( _float_ ) – 点沿圆的角度（以弧度表示）。

返回

点沿圆圆周的位置。

返回类型

`numpy.ndarray`

例子

示例：PointAtAngleExample

![PointAtAngleExample-1.png](../static/PointAtAngleExample-1.png)

```py
from manim import *

class PointAtAngleExample(Scene):
    def construct(self):
        circle = Circle(radius=2.0)
        p1 = circle.point_at_angle(PI/2)
        p2 = circle.point_at_angle(270*DEGREES)

        s1 = Square(side_length=0.25).move_to(p1)
        s2 = Square(side_length=0.25).move_to(p2)
        self.add(circle, s1, s2)
```

`surround(mobject, dim_to_match=0, stretch=False, buffer_factor=1.2)`

修改一个圆，使其包围给定的对象。

参数

- **mobject** ( [_Mobject_]() ) – 圆将围绕的 mobject。
- **dim_to_match** ( _int_ ) –
- **buffer_factor** ( _float_ ) – 相对于 mobject 缩放圆。buffer_factor < 1 使圆小于 mobject。
- **stretch** ( _bool_ ) – 拉伸圆以更紧密地围绕对象。注意：不适用于`Line`

例子

示例：圆形环绕

![CircleSurround-1.png](../static/CircleSurround-1.png)

```py
from manim import *

class CircleSurround(Scene):
    def construct(self):
        triangle1 = Triangle()
        circle1 = Circle().surround(triangle1)
        group1 = Group(triangle1,circle1) # treat the two mobjects as one

        line2 = Line()
        circle2 = Circle().surround(line2, buffer_factor=2.0)
        group2 = Group(line2,circle2)

        # buffer_factor < 1, so the circle is smaller than the square
        square3 = Square()
        circle3 = Circle().surround(square3, buffer_factor=0.5)
        group3 = Group(square3, circle3)

        group = Group(group1, group2, group3).arrange(buff=1)
        self.add(group)
```
