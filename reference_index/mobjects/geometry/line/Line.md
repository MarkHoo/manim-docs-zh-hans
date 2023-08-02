# 行

合格名称：`manim.mobject.geometry.line.Line`

```py
class Line(start=array([- 1., 0., 0.]), end=array([1., 0., 0.]), buff=0, path_arc=None, **kwargs)
```

Bases: `TipableVMobject`

方法

|||
|-|-|
[`generate_points`]()|初始化`points`并因此初始化形状。
`get_angle`|
[`get_projection`]()|返回点到直线上的投影。
`get_slope`|
`get_unit_vector`|
`get_vector`|
[`init_points`]()|初始化`points`并因此初始化形状。
[`put_start_and_end_on`]()|设置直线的起点和终点坐标。
`set_angle`|
`set_length`|
`set_path_arc`|
`set_points_by_ends`|


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

`get_projection(point)`

返回点到直线上的投影。

参数

**point** ( _Sequence_ _\[_ _float_ _\]_ ) – 线投影到的点。

返回类型

_Sequence_\[float\]


`init_points()`

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

`put_start_and_end_on(start, end)`

设置直线的起点和终点坐标。

例子

示例：线示例

```py
from manim import *

class LineExample(Scene):
    def construct(self):
        d = VGroup()
        for i in range(0,10):
            d.add(Dot())
        d.arrange_in_grid(buff=1)
        self.add(d)
        l= Line(d[0], d[1])
        self.add(l)
        self.wait()
        l.put_start_and_end_on(d[1].get_center(), d[2].get_center())
        self.wait()
        l.put_start_and_end_on(d[4].get_center(), d[7].get_center())
        self.wait()
```


参数

- **start**（_Sequence**\[**float\_\_\]_）–
- **end**（_Sequence**\[**float\_\_\]_）–
