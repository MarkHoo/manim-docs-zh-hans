# 弧


合格名称：`manim.mobject.geometry.arc.Arc`

```py
class Arc(radius=1.0, start_angle=0, angle=1.5707963267948966, num_components=9, arc_center=array([0., 0., 0.]), **kwargs)
```

Bases: TipableVMobject

一个圆弧。

例子

角度 Pi 的简单弧线。

示例：ArcExample 

![ArcExample-1.png](../static/ArcExample-1.png)

```py
from manim import *

class ArcExample(Scene):
    def construct(self):
        self.add(Arc(angle=PI))
```

方法

|||
|-|-|
[`generate_points`]()|初始化`points`并因此初始化形状。
[`get_arc_center`]()|查看前两个锚点的法线，并找到它们的交点
`init_points`|
`move_arc_center_to`|
`stop_angle`|

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


参数

**radius**（_float_）–

`generate_points()`

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

`get_arc_center(warning=True)`

查看前两个锚点的法线，并找到它们的交点

