# 写

合格名称：`manim.animation.creation.Write`

```py
class Write(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `DrawBorderThenFill`

模拟手写[`Text`]()或手绘[`VMobject`]()。


例子

示例：ShowWrite 

```py
from manim import *

class ShowWrite(Scene):
    def construct(self):
        self.play(Write(Text("Hello", font_size=144)))
```


示例：ShowWriteReversed 

```py
from manim import *

class ShowWriteReversed(Scene):
    def construct(self):
        self.play(Write(Text("Hello", font_size=144), reverse=True, remover=False))
```


测试

检查创建空[`Write`]()动画是否有效：

```sh
>>> from manim import Write, Text
>>> Write(Text(''))
Write(Text(''))
```


方法

|||
|-|-|
[`begin`]()|开始动画。
[`finish`]()|完成动画。
`reverse_submobjects`|



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
