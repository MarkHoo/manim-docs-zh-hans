# 值追踪器

合格名称：`manim.mobject.value\_tracker.ValueTracker`


```py
class ValueTracker(value=0, **kwargs)
```

Bases: `Mobject`

可用于跟踪（实值）参数的 mobject。对于动画参数更改很有用。

并不意味着要显示。相反，位置编码一些数字，通常是另一个动画或 Continual_animation 用于其更新功能的数字，并且通过将其视为 mobject，它仍然可以像其他任何东西一样进行动画和操作。

使用语法进行动画处理时，该值会不断变化`animate`。


例子

示例：ValueTrackerExample 

```py
from manim import *

class ValueTrackerExample(Scene):
    def construct(self):
        number_line = NumberLine()
        pointer = Vector(DOWN)
        label = MathTex("x").add_updater(lambda m: m.next_to(pointer, UP))

        tracker = ValueTracker(0)
        pointer.add_updater(
            lambda m: m.next_to(
                        number_line.n2p(tracker.get_value()),
                        UP
                    )
        )
        self.add(number_line, pointer,label)
        tracker += 1.5
        self.wait(1)
        tracker -= 4
        self.wait(0.5)
        self.play(tracker.animate.set_value(5)),
        self.wait(0.5)
        self.play(tracker.animate.set_value(3))
        self.play(tracker.animate.increment_value(-2))
        self.wait(0.5)
```

> 笔记

> 您还可以将 ValueTracker 链接到更新程序。在这种情况下，您必须确保将 ValueTracker 添加到场景中`add`


示例：ValueTrackerExample 

```py
from manim import *

class ValueTrackerExample(Scene):
    def construct(self):
        tracker = ValueTracker(0)
        label = Dot(radius=3).add_updater(lambda x : x.set_x(tracker.get_value()))
        self.add(label)
        self.add(tracker)
        tracker.add_updater(lambda mobject, dt: mobject.increment_value(dt))
        self.wait(2)
```


方法

|||
|-|-|
[`get_value`]()|获取此 ValueTracker 的当前值。
[`increment_value`]()|向 ValueTracker 递增（添加）标量值
[`interpolate`]()|将 self 转换为 mobject1 和 mobject2 之间的插值。
[`set_value`]()|为 ValueTracker 设置新的标量值


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`depth`|对象的深度。
`height`|mobject 的高度。
`width`|mobject 的宽度。



`get_value()`

获取此 ValueTracker 的当前值。

返回类型

float



`increment_value(d_value)`

向 ValueTracker 递增（添加）标量值

参数

**d_value** (_float_) –



`interpolate(mobject1, mobject2, alpha, path_func=<function interpolate>)`

将 self 转换为 mobject1 和 mobject2 之间的插值。



`set_value(value)`

为 ValueTracker 设置新的标量值

参数

**value**（_float_）–
