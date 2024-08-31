# 矢量化点

合格名称：`manim.mobject.types.vectorized\_mobject.VectorizedPoint`


```py
class VectorizedPoint(location=array([0., 0., 0.]), color='#000000', fill_opacity=0, stroke_width=0, artificial_width=0.01, artificial_height=0.01, **kwargs)
```

Bases: `VMobject`

方法


`get_location`

`set_location`


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
[`height`]()|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
[`width`]()|mobject 的宽度。



`basecls`

[`VMobject`]()的别名

_属性_ height

mobject 的高度。

返回类型

`float`


例子

示例：高度示例

```py
from manim import *

class HeightExample(Scene):
    def construct(self):
        decimal = DecimalNumber().to_edge(UP)
        rect = Rectangle(color=BLUE)
        rect_copy = rect.copy().set_stroke(GRAY, opacity=0.5)

        decimal.add_updater(lambda d: d.set_value(rect.height))

        self.add(rect_copy, rect, decimal)
        self.play(rect.animate.set(height=5))
        self.wait()
```


> 也可以看看

> `length_over_dim()`

_属性_ width

mobject 的宽度。

返回类型

`float`


例子

示例：宽度示例

```py
from manim import *

class WidthExample(Scene):
    def construct(self):
        decimal = DecimalNumber().to_edge(UP)
        rect = Rectangle(color=BLUE)
        rect_copy = rect.copy().set_stroke(GRAY, opacity=0.5)

        decimal.add_updater(lambda d: d.set_value(rect.width))

        self.add(rect_copy, rect, decimal)
        self.play(rect.animate.set(width=7))
        self.wait()
```


> 也可以看看

> `length_over_dim()`
