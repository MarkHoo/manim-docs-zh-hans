# 应用矩阵[#](#applymatrix "此标题的固定链接")

合格名称：`manim.animation.transform.ApplyMatrix`

_类_ ApplyMatrix ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#ApplyMatrix)[#](#manim.animation.transform.ApplyMatrix "此定义的固定链接")

基地：[`ApplyPointwiseFunction`](manim.animation.transform.ApplyPointwiseFunction.html#manim.animation.transform.ApplyPointwiseFunction "manim.animation.transform.ApplyPointwiseFunction")

对 mobject 应用矩阵变换。

参数

- **矩阵**——变换矩阵。
- **对象**– [`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject").
- **about_point** – 变换的原点。默认为`ORIGIN`.
- **kwargs** – 传递给 的更多关键字参数[`ApplyPointwiseFunction`](manim.animation.transform.ApplyPointwiseFunction.html#manim.animation.transform.ApplyPointwiseFunction "manim.animation.transform.ApplyPointwiseFunction")。

例子

示例：ApplyMatrixExample [¶](#applymatrixexample)

from manim import \*

class ApplyMatrixExample(Scene):
def construct(self):
matrix = \[\[1, 1\], \[0, 2/3\]\]
self.play(ApplyMatrix(matrix, Text("Hello World!")), ApplyMatrix(matrix, NumberPlane()))

Copy to clipboard

方法

`initialize_matrix`

属性

`path_arc`

`path_func`
