# 环形扇区

合格名称：`manim.mobject.geometry.arc.AnnularSector`

```py
class AnnularSector(inner_radius=1, outer_radius=2, angle=1.5707963267948966, start_angle=0, fill_opacity=1, stroke_width=0, color='#FFFFFF', **kwargs)
```

Bases: `Arc`

参数

- **inside_radius** – 环形扇区的内半径。
- **outer_radius** – 环形扇区的外半径。
- **angle**– 环形扇区的顺时针角度。
- **start_angle** – 环形扇区的起始顺时针角度。
- **fill_opacity** – 环形扇区填充颜色的不透明度。
- **Stroke_width** – 环形扇区的描边宽度。
- **color**– 填充到环形扇区的颜色。

例子

示例：环形扇区示例

![AnnularSectorExample-1.png](../../static/AnnularSectorExample-1.png)

```py
from manim import *

class AnnularSectorExample(Scene):
    def construct(self):
        # Changes background color to clearly visualize changes in fill_opacity.
        self.camera.background_color = WHITE

        # The default parameter start_angle is 0, so the AnnularSector starts from the +x-axis.
        s1 = AnnularSector(color=YELLOW).move_to(2 * UL)

        # Different inner_radius and outer_radius than the default.
        s2 = AnnularSector(inner_radius=1.5, outer_radius=2, angle=45 * DEGREES, color=RED).move_to(2 * UR)

        # fill_opacity is typically a number > 0 and <= 1. If fill_opacity=0, the AnnularSector is transparent.
        s3 = AnnularSector(inner_radius=1, outer_radius=1.5, angle=PI, fill_opacity=0.25, color=BLUE).move_to(2 * DL)

        # With a negative value for the angle, the AnnularSector is drawn clockwise from the start value.
        s4 = AnnularSector(inner_radius=1, outer_radius=1.5, angle=-3 * PI / 2, color=GREEN).move_to(2 * DR)

        self.add(s1, s2, s3, s4)
```

方法

|||
|-|-|
[`generate_points`]()|初始化`points`并因此初始化形状。
[`init_points`]()|初始化`points`并因此初始化形状。

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


`generate_points()`

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

`init_points()`

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。
