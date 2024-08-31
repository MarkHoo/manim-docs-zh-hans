# VGroup

合格名称：`manim.mobject.types.vectorized\_mobject.VGroup`


```py
class VGroup(*vmobjects, **kwargs)
```

Bases: `VMobject`

一组矢量化的对象。

这可用于将多个[`VMobject`]()实例分组在一起，以便缩放、移动……它们在一起。

笔记

当多次添加相同的 mobject 时，重复的内容将被忽略。用于[`Mobject.copy()`]()创建一个单独的副本，然后可以将其添加到组中。

例子

要添加`VGroup`，您可以使用 [`add()`]()方法，或使用+和+=运算符。`remove()`同样，您可以通过方法或 -和-=运算符减去 VGroup 的元素：

```py
>>> from manim import Triangle, Square, VGroup
>>> vg = VGroup()
>>> triangle, square = Triangle(), Square()
>>> vg.add(triangle)
VGroup(Triangle)
>>> vg + square   # a new VGroup is constructed
VGroup(Triangle, Square)
>>> vg            # not modified
VGroup(Triangle)
>>> vg += square; vg  # modifies vg
VGroup(Triangle, Square)
>>> vg.remove(triangle)
VGroup(Square)
>>> vg - square; # a new VGroup is constructed
VGroup()
>>> vg   # not modified
VGroup(Square)
>>> vg -= square; vg # modifies vg
VGroup()
```


示例：ArcShapeIris 

![ArcShapeIris-1.png](../../static/ArcShapeIris-1.png)

```py
from manim import *

class ArcShapeIris(Scene):
    def construct(self):
        colors = [DARK_BROWN, BLUE_E, BLUE_D, BLUE_A, TEAL_B, GREEN_B, YELLOW_E]
        radius = [1 + rad * 0.1 for rad in range(len(colors))]

        circles_group = VGroup()

        # zip(radius, color) makes the iterator [(radius[i], color[i]) for i in range(radius)]
        circles_group.add(*[Circle(radius=rad, stroke_width=10, color=col)
                            for rad, col in zip(radius, colors)])
        self.add(circles_group)
```


方法

|||
|-|-|
[`add`]()|检查所有传递的元素是否是 VMobject 的实例，然后将它们添加到 submobjects


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。



`add(*vmobjects)`

检查所有传递的元素是否是 VMobject 的实例，然后将它们添加到 submobjects

参数

**vmobjects** ( [_VMobject_]() ) – 要添加的 VMobject 列表

返回类型

[`VGroup`]()

提高

**TypeError** – 如果列表的一个元素不是 VMobject 的实例


例子

示例：添加到 VGroup 

```py
from manim import *

class AddToVGroup(Scene):
    def construct(self):
        circle_red = Circle(color=RED)
        circle_green = Circle(color=GREEN)
        circle_blue = Circle(color=BLUE)
        circle_red.shift(LEFT)
        circle_blue.shift(RIGHT)
        gr = VGroup(circle_red, circle_green)
        gr2 = VGroup(circle_blue) # Constructor uses add directly
        self.add(gr,gr2)
        self.wait()
        gr += gr2 # Add group to another
        self.play(
            gr.animate.shift(DOWN),
        )
        gr -= gr2 # Remove group
        self.play( # Animate groups separately
            gr.animate.shift(LEFT),
            gr2.animate.shift(UP),
        )
        self.play( #Animate groups without modification
            (gr+gr2).animate.shift(RIGHT)
        )
        self.play( # Animate group without component
            (gr-circle_red).animate.shift(RIGHT)
        )
```
