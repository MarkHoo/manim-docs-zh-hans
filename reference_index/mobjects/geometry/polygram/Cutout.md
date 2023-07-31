# 剪纸[#](#cutout "此标题的固定链接")

合格名称：`manim.mobject.geometry.polygram.Cutout`

_类_ Cutout ( _main_shape_ , _\* mobjects_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/polygram.html#Cutout)[#](#manim.mobject.geometry.polygram.Cutout "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

具有较小切口的形状。

参数

- **main_shape** ( [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) – 用于制作切口的主要形状。
- **mobjects** ( [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) – 要从 中切出的较小形状`main_shape`。
- **kwargs** – 传递给 的构造函数的更多关键字参数 [`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

警告

从技术上讲，此类的行为类似于对称差异：如果 的部分`mobjects`不在 中`main_shape`，这些部分将被添加到结果 中[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

例子

示例：Cutout 示例[¶](#cutoutexample)

from manim import \*

class CutoutExample(Scene):
def construct(self):
s1 = Square().scale(2.5)
s2 = Triangle().shift(DOWN + RIGHT).scale(0.5)
s3 = Square().shift(UP + RIGHT).scale(0.5)
s4 = RegularPolygon(5).shift(DOWN + LEFT).scale(0.5)
s5 = RegularPolygon(6).shift(UP + LEFT).scale(0.5)
c = Cutout(s1, s2, s3, s4, s5, fill_opacity=1, color=BLUE, stroke_color=RED)
self.play(Write(c), run_time=4)
self.wait()

Copy to clipboard

方法

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