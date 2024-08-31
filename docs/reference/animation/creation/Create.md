# 创建

合格名称：`manim.animation.creation.Create`

```py
class Create(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `ShowPartial`

增量显示 VMobject。

参数

**mobject** – 要设置动画的 VMobject。

提高

**TypeError** – 如果`mobject`不是 的实例[`VMobject`]()。

例子

示例：创建场景

```py
from manim import *

class CreateScene(Scene):
    def construct(self):
        self.play(Create(Square()))
```


> 也可以看看

> [`ShowPassingFlash`]()

方法
