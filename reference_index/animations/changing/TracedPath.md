# 追踪路径

合格名称：`manim.animation.changing.TracedPath`

```py
class TracedPath(traced_point_func, stroke_width=2, stroke_color='#FFFFFF', dissipating_time=None, **kwargs)
```
Bases: `VMobject`

跟踪函数调用返回的点的路径。

参数

- **traced_point_func** ( _Callable_ ) – 要跟踪的函数。
- **Stroke_width** ( _float_ ) – 轨迹的宽度。
- **stroke_color** ( _Color_ ) – 轨迹的颜色。
- **dissipating_time** ( _float_ _|_ _None_ ) – 路径消散所需的时间。默认设置为`None` 禁用耗散。

例子

示例：TracedPathExample

```py
from manim import *

class TracedPathExample(Scene):
    def construct(self):
        circ = Circle(color=RED).shift(4*LEFT)
        dot = Dot(color=RED).move_to(circ.get_start())
        rolling_circle = VGroup(circ, dot)
        trace = TracedPath(circ.get_start)
        rolling_circle.add_updater(lambda m: m.rotate(-0.3))
        self.add(trace, rolling_circle)
        self.play(rolling_circle.animate.shift(8*RIGHT), run_time=4, rate_func=linear)
```

示例：DissipatingPathExample 

```py
from manim import *

class DissipatingPathExample(Scene):
    def construct(self):
        a = Dot(RIGHT * 2)
        b = TracedPath(a.get_center, dissipating_time=0.5, stroke_opacity=[0, 1])
        self.add(a, b)
        self.play(a.animate(path_arc=PI / 4).shift(LEFT * 2))
        self.play(a.animate(path_arc=-PI / 4).shift(LEFT * 2))
        self.wait()
```

方法

|||
|-|-|
`update_path`|

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
