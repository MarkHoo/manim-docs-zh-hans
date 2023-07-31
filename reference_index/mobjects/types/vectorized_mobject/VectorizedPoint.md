# 矢量化点[#](#vectorizedpoint "此标题的固定链接")

合格名称：`manim.mobject.types.vectorized\_mobject.VectorizedPoint`

_类_ VectorizedPoint (_位置= array(\[0., 0., 0.\])_ ,_颜色= '#000000'_ , _fill_opacity = 0_ ,_描边宽度= 0_ ,_人工宽度= 0.01_ ,_人工高度= 0.01_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VectorizedPoint)[#](#manim.mobject.types.vectorized_mobject.VectorizedPoint "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

方法

`get_location`

`set_location`

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

[`height`](#manim.mobject.types.vectorized_mobject.VectorizedPoint.height "manim.mobject.types.vectorized_mobject.VectorizedPoint.height")

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

[`width`](#manim.mobject.types.vectorized_mobject.VectorizedPoint.width "manim.mobject.types.vectorized_mobject.VectorizedPoint.width")

mobject 的宽度。

基数[#](#manim.mobject.types.vectorized_mobject.VectorizedPoint.basecls "此定义的固定链接")

的别名[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

_属性_ 高度[#](#manim.mobject.types.vectorized_mobject.VectorizedPoint.height "此定义的固定链接")

mobject 的高度。

返回类型

`float`

例子

示例：高度示例[¶](#heightexample)

from manim import \*

class HeightExample(Scene):
def construct(self):
decimal = DecimalNumber().to_edge(UP)
rect = Rectangle(color=BLUE)
rect_copy = rect.copy().set_stroke(GRAY, opacity=0.5)

        decimal.add_updater(lambda d: d.set_value(rect.height))

        self.add(rect_copy, rect, decimal)
        self.play(rect.animate.set(height=5))
        self.wait()

Copy to clipboard

也可以看看

`length_over_dim()`

_属性_ 宽度[#](#manim.mobject.types.vectorized_mobject.VectorizedPoint.width "此定义的固定链接")

mobject 的宽度。

返回类型

`float`

例子

示例：宽度示例[¶](#widthexample)

from manim import \*

class WidthExample(Scene):
def construct(self):
decimal = DecimalNumber().to_edge(UP)
rect = Rectangle(color=BLUE)
rect_copy = rect.copy().set_stroke(GRAY, opacity=0.5)

        decimal.add_updater(lambda d: d.set_value(rect.width))

        self.add(rect_copy, rect, decimal)
        self.play(rect.animate.set(width=7))
        self.wait()

Copy to clipboard

也可以看看

`length_over_dim()`
