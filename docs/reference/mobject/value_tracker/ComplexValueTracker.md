# 复杂值追踪器

合格名称：`manim.mobject.value\_tracker.ComplexValueTracker`


```py
class ComplexValueTracker(value=0, **kwargs)
```

Bases: `ValueTracker`

跟踪复值参数。

当通过 设置该值时`animate`，该值将从源点到目标点采取直线路径。


例子

示例：ComplexValueTrackerExample 

```py
from manim import *

class ComplexValueTrackerExample(Scene):
    def construct(self):
        tracker = ComplexValueTracker(-2+1j)
        dot = Dot().add_updater(
            lambda x: x.move_to(tracker.points)
        )

        self.add(NumberPlane(), dot)

        self.play(tracker.animate.set_value(3+2j))
        self.play(tracker.animate.set_value(tracker.get_value() * 1j))
        self.play(tracker.animate.set_value(tracker.get_value() - 2j))
        self.play(tracker.animate.set_value(tracker.get_value() / (-2 + 3j)))
```


方法

|||
|-|-|
[`get_value`]()|获取此值跟踪器的当前值（复数形式）。
[`set_value`]()|为 ComplexValueTracker 设置新的复数值


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`depth`|对象的深度。
`height`|mobject 的高度。
`width`|mobject 的宽度。



`get_value()`

获取此值跟踪器的当前值（复数形式）。

该值在内部存储为点数组 \[a, b, 0\]。可以直接访问它以几何方式表示值，请参阅使用示例。


`set_value(z)`

为 ComplexValueTracker 设置新的复数值
