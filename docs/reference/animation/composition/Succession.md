# 继承

合格名称：`manim.animation.composition.Succession`

```py
class Succession(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `AnimationGroup`

连续播放一系列动画。

参数

- **animations**[`Animation`]()–要播放的对象序列。
- **lag_ratio**–

  定义动画应用于子对象之前的延迟。lag_ratio `n.nn`表示当前动画播放完毕后将播放`nnn%`下一个动画。默认为 1.0，这意味着下一个动画将在当前动画播放 100% 时开始。

  这不会影响动画的总运行时间。相反，会调整各个动画的运行时间，以便完整的动画具有定义的运行时间。

例子

示例：继承示例

```py
from manim import *

class SuccessionExample(Scene):
    def construct(self):
        dot1 = Dot(point=LEFT * 2 + UP * 2, radius=0.16, color=BLUE)
        dot2 = Dot(point=LEFT * 2 + DOWN * 2, radius=0.16, color=MAROON)
        dot3 = Dot(point=RIGHT * 2 + DOWN * 2, radius=0.16, color=GREEN)
        dot4 = Dot(point=RIGHT * 2 + UP * 2, radius=0.16, color=YELLOW)
        self.add(dot1, dot2, dot3, dot4)

        self.play(Succession(
            dot1.animate.move_to(dot2),
            dot2.animate.move_to(dot3),
            dot3.animate.move_to(dot4),
            dot4.animate.move_to(dot1)
        ))
```

方法

|||
|-|-|
[`begin`]()|开始动画。
[`finish`]()|完成动画。
[`interpolate`]()|设置动画进度。
[`next_animation`]()|继续下一个动画。
`update_active_animation`|
[`update_mobjects`]()|更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。



`begin()`

开始动画。

该方法在动画播放时被调用。尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。

返回类型

None


`finish()`

完成动画。

动画结束时会调用此方法。

返回类型

None


`interpolate(alpha)`

设置动画进度。

动画期间的每一帧都会调用此方法。

参数

**alpha** ( _float_ ) – 设置动画的相对时间，0 表示开始，1 表示结束。

返回类型

None


`next_animation()`

继续下一个动画。

当活动动画结束时立即调用此方法。

返回类型

None


`update_mobjects(dt)`

更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。请注意，由于通常（总是？） self.mobject 会在动画期间暂停其更新，因此这对 self.mobject None作用。

参数

**dt**（_float_）–

返回类型

None
