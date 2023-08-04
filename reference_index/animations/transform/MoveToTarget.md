# 移动到目标

合格名称：`manim.animation.transform.MoveToTarget`

```py
class MoveToTarget(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Transform`

将 mobject 转换为存储在其`target`属性中的 mobject。

调用该`generate_target()`方法后，`target` mobject 的属性将填充它的副本。修改属性后，播放[`MoveToTarget`]()动画会将原始 mobject 转换为`target`属性中存储的修改后的 mobject。


例子

示例：MoveToTargetExample

```py
from manim import *

class MoveToTargetExample(Scene):
    def construct(self):
        c = Circle()

        c.generate_target()
        c.target.set_fill(color=GREEN, opacity=0.5)
        c.target.shift(2*RIGHT + UP).scale(0.5)

        self.add(c)
        self.play(MoveToTarget(c))
```


方法

`check_validity_of_input`


属性

`path_arc`
`path_func`
