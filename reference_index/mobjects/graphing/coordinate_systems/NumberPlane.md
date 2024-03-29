# 数字平面

合格名称：`manim.mobject.graphing.coordinate\_systems.NumberPlane`


```py
class NumberPlane(x_range=(- 7.111111111111111, 7.111111111111111, 1), y_range=(- 4.0, 4.0, 1), x_length=None, y_length=None, background_line_style=None, faded_line_style=None, faded_line_ratio=1, make_smooth_after_applying_functions=True, **kwargs)
```

Bases: `Axes`

创建带有背景线的笛卡尔平面。

参数

- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) –水平方向平面的值。`[x_min, x_max, x_step]`
- **y_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) –垂直方向的平面值。`[y_min, y_max, y_step]`
- **x_length** ( _float_ _|_ _None_ ) – 平面的宽度。
- **y_length** ( _float_ _|_ _None_ ) – 平面的高度。
- **background_line_style** ( _dict_ _|_ _None_ ) – 影响平面背景线构造的参数。
- **faded_line_style** ( _dict_ _|_ _None_ ) – 与 类似`background_line_style`，影响场景背景线的构造。
- **faded_line_ratio** ( _int_ ) – 确定背景线内的框数：`2`= 4 个框，`3`= 9 个框。
- **make_smooth_after_applying_functions** ( _bool_ ) – 目前不起作用。
- **kwargs** – 要传递给 的附加参数[`Axes`]()。


> 笔记

> 如果`x_length`或`y_length`未定义，则会自动计算它们，使每个轴上的一个单位为 1 个马尼姆单位长。


例子

示例：NumberPlaneExample

![NumberPlaneExample-1.png](../../static/NumberPlaneExample-1.png)

```py
from manim import *

class NumberPlaneExample(Scene):
    def construct(self):
        number_plane = NumberPlane(
            background_line_style={
                "stroke_color": TEAL,
                "stroke_width": 4,
                "stroke_opacity": 0.6
            }
        )
        self.add(number_plane)
```


示例：NumberPlaneScaled 

![NumberPlaneScaled-1.png](../../static/NumberPlaneScaled-1.png)

```py
from manim import *

class NumberPlaneScaled(Scene):
    def construct(self):
        number_plane = NumberPlane(
            x_range=(-4, 11, 1),
            y_range=(-3, 3, 1),
            x_length=5,
            y_length=2,
        ).move_to(LEFT*3)

        number_plane_scaled_y = NumberPlane(
            x_range=(-4, 11, 1),
            x_length=5,
            y_length=4,
        ).move_to(RIGHT*3)

        self.add(number_plane)
        self.add(number_plane_scaled_y)
```


方法

|||
|-|-|
`get_vector`|
`prepare_for_nonlinear_transform`|


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
