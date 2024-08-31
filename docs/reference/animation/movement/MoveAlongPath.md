# 沿路径移动

合格名称：`manim.animation.movement.MoveAlongPath`

```py
class MoveAlongPath(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Animation`

使一个 mobject 沿着另一 mobject 的路径移动。.. 标题:: 示例

示例：MoveAlongPathExample 

```py
from manim import *

class MoveAlongPathExample(Scene):
    def construct(self):
        d1 = Dot().set_color(ORANGE)
        l1 = Line(LEFT, RIGHT)
        l2 = VMobject()
        self.add(d1, l1, l2)
        l2.add_updater(lambda x: x.become(Line(LEFT, d1.get_center()).set_color(ORANGE)))
        self.play(MoveAlongPath(d1, l1), rate_func=linear)
```

方法

|||
|-|-|
[`interpolate_mobject`]()|根据 alpha 值对 mobject 进行插值`Animation`。



`interpolate_mobject(alpha)`

根据 alpha 值对 mobject 进行插值`Animation`。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

None
