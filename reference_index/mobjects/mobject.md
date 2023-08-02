# 对象

可显示对象的基类。

Classes

[`Group`]()|多个组合在一起[`Mobjects`]()。
[`Mobject`]()|数学对象：可以在屏幕上显示的对象的基类。


Functions

`override_animate(method)`

用于重写方法动画的装饰器。

这允许指定一个方法（返回），当装饰方法与用于动画方法应用程序的语法[`Animation`]()一起使用时调用该方法。`.animate`

> 也可以看看

> [`Mobject.animate`]()

> 笔记

> 重写方法不能与使用语法链接的普通方法或其他重写方法组合`.animate`。

例子

示例：AnimationOverrideExample

```py
from manim import *

class CircleWithContent(VGroup):
    def __init__(self, content):
        super().__init__()
        self.circle = Circle()
        self.content = content
        self.add(self.circle, content)
        content.move_to(self.circle.get_center())

    def clear_content(self):
        self.remove(self.content)
        self.content = None

    @override_animate(clear_content)
    def _clear_content_animation(self, anim_args=None):
        if anim_args is None:
            anim_args = {}
        anim = Uncreate(self.content, **anim_args)
        self.clear_content()
        return anim

class AnimationOverrideExample(Scene):
    def construct(self):
        t = Text("hello!")
        my_mobject = CircleWithContent(t)
        self.play(Create(my_mobject))
        self.play(my_mobject.animate.clear_content())
        self.wait()
```
