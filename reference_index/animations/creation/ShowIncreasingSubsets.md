# 显示增加子集

合格名称：`manim.animation.creation.ShowIncreasingSubsets`

```py
class ShowIncreasingSubsets(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Animation`

一次显示一个子对象，使所有先前的子对象显示在屏幕上。


例子

示例：显示 IncreasingSubsetsScene 

```py
from manim import *

class ShowIncreasingSubsetsScene(Scene):
    def construct(self):
        p = VGroup(Dot(), Square(), Triangle())
        self.add(p)
        self.play(ShowIncreasingSubsets(p))
        self.wait()
```

方法

|||
|-|-|
[`interpolate_mobject`]()|根据 alpha 值对 mobject 进行插值`Animation`。
`update_submobject_list`|



`interpolate_mobject(alpha)`

根据 alpha 值对 mobject 进行插值`Animation`。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

None
