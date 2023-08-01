# 弧


合格名称：`manim.mobject.geometry.arc.Arc`

_类_ 弧(_半径= 1.0_ ,_起始角度= 0_ ,_角度= 1.5707963267948966_ , _num_components = 9_ , _arc_center = array(\[0., 0., 0.\])_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Arc)[#](#manim.mobject.geometry.arc.Arc "此定义的固定链接")

基地：[`TipableVMobject`](manim.mobject.geometry.arc.TipableVMobject.html#manim.mobject.geometry.arc.TipableVMobject "manim.mobject.geometry.arc.TipableVMobject")

一个圆弧。

例子

角度 Pi 的简单弧线。

示例：ArcExample [¶](#arcexample)

![../_images/ArcExample-1.png](../_images/ArcExample-1.png)

from manim import *

class ArcExample(Scene):
    def construct(self):
        self.add(Arc(angle=PI))

Copy to clipboard

方法

  

[`generate_points`](#manim.mobject.geometry.arc.Arc.generate_points "manim.mobject.geometry.arc.Arc.generate_points")

初始化`points`并因此初始化形状。

[`get_arc_center`](#manim.mobject.geometry.arc.Arc.get_arc_center "manim.mobject.geometry.arc.Arc.get_arc_center")

查看前两个锚点的法线，并找到它们的交点

`init_points`

`move_arc_center_to`

`stop_angle`

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

参数

**半径**（_浮动_）–

生成点( )[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Arc.generate_points)[#](#manim.mobject.geometry.arc.Arc.generate_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

get\_arc\_center（_警告= True_）[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Arc.get_arc_center)[#](#manim.mobject.geometry.arc.Arc.get_arc_center "此定义的固定链接")

查看前两个锚点的法线，并找到它们的交点