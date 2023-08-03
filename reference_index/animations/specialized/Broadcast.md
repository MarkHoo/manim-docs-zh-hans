# 广播

合格名称：`manim.animation.specialized.Broadcast`

```py
class Broadcast(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `LaggedStart`

广播一个从 an 开始的 mobject `initial_width`，直到 mobject 的实际大小。

参数

- **mobject** – 要广播的 mobject。
- **focus_point** – 广播的中心，默认为 ORIGIN。
- **n_mobs** – 从焦点出现的 mobject 数量，默认为 5。
- **initial_opacity** – 从广播中发出的 mobjects 的起始笔画不透明度，默认为 1。
- **Final_opacity** – 从广播中发出的 mobjects 最终笔画不透明度，默认为 0。
- **initial_width** – mobjects 的初始宽度，默认为 0.0。
- **remover** – 动画结束后是否应将 mobject 从场景中删除，默认为 True。
- **lag_ratio** – mobject 每次迭代之间的时间，默认为 0.2。
- **run_time** – 动画的总持续时间，默认为 3。
- **kwargs** – 要传递给 的附加参数[`LaggedStart`]()。


例子

示例：广播示例

```py
from manim import *

class BroadcastExample(Scene):
    def construct(self):
        mob = Circle(radius=4, color=TEAL_A)
        self.play(Broadcast(mob))
```

方法
