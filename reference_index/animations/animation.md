# 动画

对对象进行动画处理。

Classes

|||
|-|-|
[`Animation`]()|一部动画。
[`Wait`]()|“无操作”动画。

功能

覆盖*动画（*动画类\_）

装饰器用于将方法标记为特定[`Animation`]()类型的覆盖。

应该只用于装饰从 派生的类的方法[`Mobject`]()。 `Animation`覆盖被继承到`Mobject`定义它们的人的子类。它们不会覆盖`Animation`它们覆盖的子类。

> 也可以看看

> [`add_animation_override()`]()

参数

**Animation_class** ( _type_ _\[_ [_Animation_]() _\]_ ) – 要覆盖的动画。

退货

真正的装饰者。这将该方法标记为覆盖动画。

返回类型

可调用\[\[可调用\], 可调用\]

例子

[![视频缩略图]()](https://docs.manim.community/en/stable/reference/OverrideAnimationExample-1.mp4)

示例：OverrideAnimationExample

```py
from manim import *

class MySquare(Square):
    @override_animation(FadeIn)
    def _fade_in_override(self, **kwargs):
        return Create(self, **kwargs)

class OverrideAnimationExample(Scene):
    def construct(self):
        self.play(FadeIn(MySquare()))
```

准备动画（_动画_）

返回未更改的动画，或从传递的动画工厂构建的动画。

例子

```sh
>>> from manim import Square, FadeIn
>>> s = Square()
>>> prepare_animation(FadeIn(s))
FadeIn(Square)
```

```sh
>>> prepare_animation(s.animate.scale(2).rotate(42))
_MethodAnimation(Square)
```

```sh
>>> prepare_animation(42)
Traceback (most recent call last):
...
TypeError: Object 42 cannot be converted to an animation
```

参数

**anim** ([_动画_]()_|_ _mobject.\_AnimationBuilder_ ) –

返回类型

[动画片]()
