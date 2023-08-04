# 变换匹配形状

合格名称：`manim.animation.transform\_matching\_parts.TransformMatchingShapes`

```py
class TransformMatchingShapes(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `TransformMatchingAbstractBase`

试图通过匹配组的子对象的形状来变换组的动画。

如果归一化后（即，平移到原点后，将子对象高度固定为 1 个单位，并将坐标四舍五入到小数点后三位）匹配，则两个子对象匹配。

> 也可以看看

> [`TransformMatchingAbstractBase`]()


例子

示例：字谜

```py
from manim import *

class Anagram(Scene):
    def construct(self):
        src = Text("the morse code")
        tar = Text("here come dots")
        self.play(Write(src))
        self.wait(0.5)
        self.play(TransformMatchingShapes(src, tar, path_arc=PI/2))
        self.wait(0.5)
```


方法

`get_mobject_key`
`get_mobject_parts`
