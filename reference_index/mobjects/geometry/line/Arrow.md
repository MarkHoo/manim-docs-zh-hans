# 箭头

合格名称：`manim.mobject.geometry.line.Arrow`

```py
class Arrow(*args, stroke_width=6, buff=0.25, max_tip_length_to_length_ratio=0.25, max_stroke_width_to_length_ratio=5, **kwargs)
```

Bases: Line

一个箭头。

参数

- **args** ( _Any_ ) – 要传递给 的参数[`Line`]()。
- **stroke_width** ( _float_ ) – 箭头的粗细。受 影响`max_stroke_width_to_length_ratio`。
- **buff** ( _float_ ) – 箭头距起点和终点的距离。
- **max_tip_length_to_length_ratio** ( _float_ ) –`tip_length`随着箭头的长度缩放。增加该比率会提高 的最大值`tip_length`。
- **max_lines_width_to_length_ratio** ( _float_ ) –`stroke_width`随着箭头的长度缩放。增加该比率会与 的最大值成比例`stroke_width`。
- **kwargs** – 要传递给 的附加参数[`Line`]()。

> 也可以看看

> `ArrowTip` `CurvedArrow`

例子

示例：箭头示例

![ArrowExample-1.png](../static/ArrowExample-1.png)


```py
from manim import *

from manim.mobject.geometry.tips import ArrowSquareTip
class ArrowExample(Scene):
    def construct(self):
        arrow_1 = Arrow(start=RIGHT, end=LEFT, color=GOLD)
        arrow_2 = Arrow(start=RIGHT, end=LEFT, color=GOLD, tip_shape=ArrowSquareTip).shift(DOWN)
        g1 = Group(arrow_1, arrow_2)

        # the effect of buff
        square = Square(color=MAROON_A)
        arrow_3 = Arrow(start=LEFT, end=RIGHT)
        arrow_4 = Arrow(start=LEFT, end=RIGHT, buff=0).next_to(arrow_1, UP)
        g2 = Group(arrow_3, arrow_4, square)

        # a shorter arrow has a shorter tip and smaller stroke width
        arrow_5 = Arrow(start=ORIGIN, end=config.top).shift(LEFT * 4)
        arrow_6 = Arrow(start=config.top + DOWN, end=config.top).shift(LEFT * 3)
        g3 = Group(arrow_5, arrow_6)

        self.add(Group(g1, g2, g3).arrange(buff=2))
```


示例：箭头示例

![ArrowExample-2.png](../static/ArrowExample-2.png)


```py
from manim import *

class ArrowExample(Scene):
    def construct(self):
        left_group = VGroup()
        # As buff increases, the size of the arrow decreases.
        for buff in np.arange(0, 2.2, 0.45):
            left_group += Arrow(buff=buff, start=2 * LEFT, end=2 * RIGHT)
        # Required to arrange arrows.
        left_group.arrange(DOWN)
        left_group.move_to(4 * LEFT)

        middle_group = VGroup()
        # As max_stroke_width_to_length_ratio gets bigger,
        # the width of stroke increases.
        for i in np.arange(0, 5, 0.5):
            middle_group += Arrow(max_stroke_width_to_length_ratio=i)
        middle_group.arrange(DOWN)

        UR_group = VGroup()
        # As max_tip_length_to_length_ratio increases,
        # the length of the tip increases.
        for i in np.arange(0, 0.3, 0.1):
            UR_group += Arrow(max_tip_length_to_length_ratio=i)
        UR_group.arrange(DOWN)
        UR_group.move_to(4 * RIGHT + 2 * UP)

        DR_group = VGroup()
        DR_group += Arrow(start=LEFT, end=RIGHT, color=BLUE, tip_shape=ArrowSquareTip)
        DR_group += Arrow(start=LEFT, end=RIGHT, color=BLUE, tip_shape=ArrowSquareFilledTip)
        DR_group += Arrow(start=LEFT, end=RIGHT, color=YELLOW, tip_shape=ArrowCircleTip)
        DR_group += Arrow(start=LEFT, end=RIGHT, color=YELLOW, tip_shape=ArrowCircleFilledTip)
        DR_group.arrange(DOWN)
        DR_group.move_to(4 * RIGHT + 2 * DOWN)

        self.add(left_group, middle_group, UR_group, DR_group)
```


方法

|||
|-|-|
[`get_default_tip_length`]()|返回箭头的默认 tip_length。
[`get_normal_vector`]()|返回向量的法线。
[`reset_normal_vector`]()|重置向量的法线
[`scale`]()|缩放箭头，但保持笔划宽度和箭头尖端大小固定。


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


`get_default_tip_length()`

返回箭头的默认 tip_length。

例子

```sh
>>> Arrow().get_default_tip_length()
0.35
```

返回类型

float

`get_normal_vector()`

返回向量的法线。

例子

```sh
>>> np.round(Arrow().get_normal_vector()) + 0. # add 0. to avoid negative 0 in output
array([ 0.,  0., -1.])
```

返回类型

_ndarray_

`reset_normal_vector()`

重置向量的法线

`scale(factor, scale_tips=False, **kwargs)`

缩放箭头，但保持笔划宽度和箭头尖端大小固定。

> 也可以看看

> [`scale()`]()

例子

```sh
>>> arrow = Arrow(np.array([-1, -1, 0]), np.array([1, 1, 0]), buff=0)
>>> scaled_arrow = arrow.scale(2)
>>> np.round(scaled_arrow.get_start_and_end(), 8) + 0
array([[-2., -2.,  0.],
       [ 2.,  2.,  0.]])
>>> arrow.tip.length == scaled_arrow.tip.length
True
```


使用默认方法手动缩放对象 [`scale()`]()不具有相同的属性：


```sh
>>> new_arrow = Arrow(np.array([-1, -1, 0]), np.array([1, 1, 0]), buff=0)
>>> another_scaled_arrow = VMobject.scale(new_arrow, 2)
>>> another_scaled_arrow.tip.length == arrow.tip.length
False
```

