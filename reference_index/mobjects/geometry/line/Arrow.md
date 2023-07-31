# 箭头[#](#arrow "此标题的固定链接")

合格名称：`manim.mobject.geometry.line.Arrow`

_类_ 箭头（_\* args_，_笔画宽度= 6_，_缓冲= 0.25_，_最大笔尖长度到长度比= 0.25_，_最大笔划宽度到长度比= 5_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow)[#](#manim.mobject.geometry.line.Arrow "此定义的固定链接")

基地：[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")

一个箭头。

参数

- **args** ( _Any_ ) – 要传递给 的参数[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")。
- **stroke_width** ( _float_ ) – 箭头的粗细。受 影响`max_stroke_width_to_length_ratio`。
- **buff** ( _float_ ) – 箭头距起点和终点的距离。
- **max_tip_length_to_length_ratio** ( _float_ ) –`tip_length`随着箭头的长度缩放。增加该比率会提高 的最大值`tip_length`。
- **max_lines_width_to_length_ratio** ( _float_ ) –`stroke_width`随着箭头的长度缩放。增加该比率会与 的最大值成比例`stroke_width`。
- **kwargs** – 要传递给 的附加参数[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")。

也可以看看

`ArrowTip` `CurvedArrow`

例子

示例：箭头示例[¶](#arrowexample)

![../_images/ArrowExample-1.png](../_images/ArrowExample-1.png)

from manim import \*

from manim.mobject.geometry.tips import ArrowSquareTip
class ArrowExample(Scene):
def construct(self):
arrow_1 = Arrow(start=RIGHT, end=LEFT, color=GOLD)
arrow_2 = Arrow(start=RIGHT, end=LEFT, color=GOLD, tip_shape=ArrowSquareTip).shift(DOWN)
g1 = Group(arrow_1, arrow_2)

        \# the effect of buff
        square = Square(color=MAROON_A)
        arrow_3 = Arrow(start=LEFT, end=RIGHT)
        arrow_4 = Arrow(start=LEFT, end=RIGHT, buff=0).next_to(arrow_1, UP)
        g2 = Group(arrow_3, arrow_4, square)

        \# a shorter arrow has a shorter tip and smaller stroke width
        arrow_5 = Arrow(start=ORIGIN, end=config.top).shift(LEFT * 4)
        arrow_6 = Arrow(start=config.top + DOWN, end=config.top).shift(LEFT * 3)
        g3 = Group(arrow_5, arrow_6)

        self.add(Group(g1, g2, g3).arrange(buff=2))

Copy to clipboard

示例：箭头示例[¶](#arrowexample)

![../_images/ArrowExample-2.png](../_images/ArrowExample-2.png)

from manim import \*

class ArrowExample(Scene):
def construct(self):
left*group = VGroup()
\# As buff increases, the size of the arrow decreases.
for buff in np.arange(0, 2.2, 0.45):
left_group += Arrow(buff=buff, start=2 * LEFT, end=2 \_ RIGHT)
\# Required to arrange arrows.
left_group.arrange(DOWN)
left_group.move_to(4 \* LEFT)

        middle_group = VGroup()
        \# As max\_stroke\_width\_to\_length_ratio gets bigger,
        \# the width of stroke increases.
        for i in np.arange(0, 5, 0.5):
            middle_group += Arrow(max\_stroke\_width\_to\_length_ratio=i)
        middle_group.arrange(DOWN)

        UR_group = VGroup()
        \# As max\_tip\_length\_to\_length_ratio increases,
        \# the length of the tip increases.
        for i in np.arange(0, 0.3, 0.1):
            UR_group += Arrow(max\_tip\_length\_to\_length_ratio=i)
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

Copy to clipboard

方法

[`get_default_tip_length`](#manim.mobject.geometry.line.Arrow.get_default_tip_length "manim.mobject.geometry.line.Arrow.get_default_tip_length")

返回箭头的默认 tip_length。

[`get_normal_vector`](#manim.mobject.geometry.line.Arrow.get_normal_vector "manim.mobject.geometry.line.Arrow.get_normal_vector")

返回向量的法线。

[`reset_normal_vector`](#manim.mobject.geometry.line.Arrow.reset_normal_vector "manim.mobject.geometry.line.Arrow.reset_normal_vector")

重置向量的法线

[`scale`](#manim.mobject.geometry.line.Arrow.scale "manim.mobject.geometry.line.Arrow.scale")

缩放箭头，但保持笔划宽度和箭头尖端大小固定。

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。

获取默认提示长度( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow.get_default_tip_length)[#](#manim.mobject.geometry.line.Arrow.get_default_tip_length "此定义的固定链接")

返回箭头的默认 tip_length。

例子

> > \> Arrow().get_default_tip_length()
> > 0.35

Copy to clipboard

返回类型

漂浮

获取法线向量( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow.get_normal_vector)[#](#manim.mobject.geometry.line.Arrow.get_normal_vector "此定义的固定链接")

返回向量的法线。

例子

> > \> np.round(Arrow().get_normal_vector()) + 0. \# add 0. to avoid negative 0 in output
> > array(\[ 0., 0., -1.\])

Copy to clipboard

返回类型

_ndarray_

重置正常向量( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow.reset_normal_vector)[#](#manim.mobject.geometry.line.Arrow.reset_normal_vector "此定义的固定链接")

重置向量的法线

比例（_因子_， _scale_tips = False_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow.scale)[#](#manim.mobject.geometry.line.Arrow.scale "此定义的固定链接")

缩放箭头，但保持笔划宽度和箭头尖端大小固定。

也可以看看

[`scale()`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.scale "manim.mobject.mobject.Mobject.scale")

例子

> > \> arrow = Arrow(np.array(\[-1, -1, 0\]), np.array(\[1, 1, 0\]), buff=0)
> > \> scaled_arrow = arrow.scale(2)
> > \> np.round(scaled_arrow.get_start_and_end(), 8) + 0
> > array(\[\[-2., -2., 0.\],
> > \[ 2., 2., 0.\]\])
> > \> arrow.tip.length == scaled_arrow.tip.length
> > True

Copy to clipboard

使用默认方法手动缩放对象 [`scale()`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.scale "manim.mobject.mobject.Mobject.scale")不具有相同的属性：

> > \> new_arrow = Arrow(np.array(\[-1, -1, 0\]), np.array(\[1, 1, 0\]), buff=0)
> > \> another_scaled_arrow = VMobject.scale(new_arrow, 2)
> > \> another_scaled_arrow.tip.length == arrow.tip.length
> > False

Copy to clipboard
