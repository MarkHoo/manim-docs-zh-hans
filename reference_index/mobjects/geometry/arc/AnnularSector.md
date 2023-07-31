# 环形扇区[#](#annularsector "此标题的固定链接")

合格名称：`manim.mobject.geometry.arc.AnnularSector`

_类_ AnnularSector (_内部半径= 1_，_外部半径= 2_，_角度= 1.5707963267948966_，_开始角度= 0_，_填充不透明度= 1_，_描边宽度= 0_，_颜色= '#FFFFFF'_， _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/arc.html#AnnularSector)[#](#manim.mobject.geometry.arc.AnnularSector "此定义的固定链接")

基地：[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc")

参数

- **inside_radius** – 环形扇区的内半径。
- **outer_radius** – 环形扇区的外半径。
- **角度**– 环形扇区的顺时针角度。
- **start_angle** – 环形扇区的起始顺时针角度。
- **fill_opacity** – 环形扇区填充颜色的不透明度。
- **Stroke_width** – 环形扇区的描边宽度。
- **颜色**– 填充到环形扇区的颜色。

例子

示例：环形扇区示例[¶](#annularsectorexample)

![../_images/AnnularSectorExample-1.png](../_images/AnnularSectorExample-1.png)

from manim import \*

class AnnularSectorExample(Scene):
def construct(self):
\# Changes background color to clearly visualize changes in fill_opacity.
self.camera.background_color = WHITE

        \# The default parameter start_angle is 0, so the AnnularSector starts from the +x-axis.
        s1 = AnnularSector(color=YELLOW).move_to(2 * UL)

        \# Different inner\_radius and outer\_radius than the default.
        s2 = AnnularSector(inner_radius=1.5, outer_radius=2, angle=45 * DEGREES, color=RED).move_to(2 * UR)

        \# fill\_opacity is typically a number > 0 and <= 1. If fill\_opacity=0, the AnnularSector is transparent.
        s3 = AnnularSector(inner_radius=1, outer_radius=1.5, angle=PI, fill_opacity=0.25, color=BLUE).move_to(2 * DL)

        \# With a negative value for the angle, the AnnularSector is drawn clockwise from the start value.
        s4 = AnnularSector(inner_radius=1, outer_radius=1.5, angle=-3 * PI / 2, color=GREEN).move_to(2 * DR)

        self.add(s1, s2, s3, s4)

Copy to clipboard

方法

[`generate_points`](#manim.mobject.geometry.arc.AnnularSector.generate_points "manim.mobject.geometry.arc.AnnularSector.generate_points")

初始化`points`并因此初始化形状。

[`init_points`](#manim.mobject.geometry.arc.AnnularSector.init_points "manim.mobject.geometry.arc.AnnularSector.init_points")

初始化`points`并因此初始化形状。

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

生成点( )[\[来源\]](../_modules/manim/mobject/geometry/arc.html#AnnularSector.generate_points)[#](#manim.mobject.geometry.arc.AnnularSector.generate_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

初始化点（）[#](#manim.mobject.geometry.arc.AnnularSector.init_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。
