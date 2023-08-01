# 整数矩阵

合格名称：`manim.mobject.matrix.IntegerMatrix`

_类_ IntegerMatrix (_矩阵_, _element_to_mobject=<class 'manim.mobject.text.numbers.Integer'>_ , _\*\*kwargs_ )[\[来源\]](../_modules/manim/mobject/matrix.html#IntegerMatrix)[#](#manim.mobject.matrix.IntegerMatrix "此定义的固定链接")

基地：[`Matrix`](manim.mobject.matrix.Matrix.html#manim.mobject.matrix.Matrix "manim.mobject.matrix.Matrix")

一个在屏幕上显示带有整数条目的矩阵的 mobject。

例子

示例：IntegerMatrix 示例[¶](#integermatrixexample)

![../_images/IntegerMatrixExample-1.png](../_images/IntegerMatrixExample-1.png)

from manim import \*

class IntegerMatrixExample(Scene):
def construct(self):
m0 = IntegerMatrix(
\[\[3.7, 2\], \[42.2, 12\]\],
left_bracket="(",
right_bracket=")")
self.add(m0)

Copy to clipboard

如果矩阵中有小数项，则进行四舍五入。

参数

- **矩阵**( _Iterable_ ) – numpy 二维数组或列表列表
- **element_to_mobject** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 要使用的 Mobject，默认为 Integer

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
