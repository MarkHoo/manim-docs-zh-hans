# 取消写入

合格名称：`manim.animation.creation.Unwrite`

```py
class Unwrite(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Write

模拟用手擦除 a[`Text`]()或 a [`VMobject`]()。

参数

**相反**– 设置 True 以使动画首先从最后一个子对象开始擦除。

例子

示例：UnwriteReverseTrue [¶](#unwritereversetrue)

```py
from manim import *

class UnwriteReverseTrue(Scene):
    def construct(self):
        text = Tex("Alice and Bob").scale(3)
        self.add(text)
        self.play(Unwrite(text))
```


示例：UnwriteReverseFalse [¶](#unwritereversefalse)

```py
from manim import *

class UnwriteReverseFalse(Scene):
    def construct(self):
        text = Tex("Alice and Bob").scale(3)
        self.add(text)
        self.play(Unwrite(text, reverse=False))
```


方法
