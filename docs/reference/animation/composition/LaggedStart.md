# 滞后开始

合格名称：`manim.animation.composition.LaggedStart`

```py
class LaggedStart(mobject=None, *args, use_override=True, **kwargs)
```
Bases: `AnimationGroup`

[`Animation`]()根据 调整一系列的时序`lag_ratio`。

参数

- **animations**[`Animation`]()–要播放的对象序列。
- **lag_ratio**–

  定义动画应用于子对象之前的延迟。lag_ratio `n.nn`表示当前动画播放完毕后将播放`nnn%`下一个动画。默认为 0.05，这意味着下一个动画将在当前动画播放完 5% 时开始。

  这不会影响动画的总运行时间。相反，会调整各个动画的运行时间，以便完整的动画具有定义的运行时间。


例子

示例：LaggedStartExample 

```py
from manim import *

class LaggedStartExample(Scene):
    def construct(self):
        title = Text("lag_ratio = 0.25").to_edge(UP)

        dot1 = Dot(point=LEFT * 2 + UP, radius=0.16)
        dot2 = Dot(point=LEFT * 2, radius=0.16)
        dot3 = Dot(point=LEFT * 2 + DOWN, radius=0.16)
        line_25 = DashedLine(
            start=LEFT + UP * 2,
            end=LEFT + DOWN * 2,
            color=RED
        )
        label = Text("25%", font_size=24).next_to(line_25, UP)
        self.add(title, dot1, dot2, dot3, line_25, label)

        self.play(LaggedStart(
            dot1.animate.shift(RIGHT * 4),
            dot2.animate.shift(RIGHT * 4),
            dot3.animate.shift(RIGHT * 4),
            lag_ratio=0.25,
            run_time=4
        ))
```

方法
