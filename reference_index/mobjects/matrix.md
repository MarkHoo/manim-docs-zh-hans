# 矩阵[#](#module-manim.mobject.matrix "此标题的固定链接")

表示矩阵的 Mobject。

例子

示例：矩阵示例[¶](#matrixexamples)

![../_images/MatrixExamples-1.png](../_images/MatrixExamples-1.png)

from manim import \*

class MatrixExamples(Scene):
def construct(self):
m0 = Matrix(\[\["\\\pi", 0\], \[-1, 1\]\])
m1 = IntegerMatrix(\[\[1.5, 0.\], \[12, -1.3\]\],
left_bracket="(",
right_bracket=")")
m2 = DecimalMatrix(
\[\[3.456, 2.122\], \[33.2244, 12.33\]\],
element_to_mobject_config={"num_decimal_places": 2},
left_bracket="\\\{",
right_bracket="\\\}")
m3 = MobjectMatrix(
\[\[Circle().scale(0.3), Square().scale(0.3)\],
\[MathTex("\\\pi").scale(2), Star().scale(0.3)\]\],
left_bracket="\\\langle",
right_bracket="\\\rangle")
g = Group(m0, m1, m2, m3).arrange_in_grid(buff=2)
self.add(g)

Copy to clipboard

课程

[`DecimalMatrix`](manim.mobject.matrix.DecimalMatrix.html#manim.mobject.matrix.DecimalMatrix "manim.mobject.matrix.DecimalMatrix")

一个在屏幕上显示带有十进制条目的矩阵的 mobject。

[`IntegerMatrix`](manim.mobject.matrix.IntegerMatrix.html#manim.mobject.matrix.IntegerMatrix "manim.mobject.matrix.IntegerMatrix")

一个在屏幕上显示带有整数条目的矩阵的 mobject。

[`Matrix`](manim.mobject.matrix.Matrix.html#manim.mobject.matrix.Matrix "manim.mobject.matrix.Matrix")

在屏幕上显示矩阵的 mobject。

[`MobjectMatrix`](manim.mobject.matrix.MobjectMatrix.html#manim.mobject.matrix.MobjectMatrix "manim.mobject.matrix.MobjectMatrix")

在屏幕上显示 mobject 条目矩阵的 mobject。

功能

get*det_text（*矩阵*，*行列式=无*， \_background_rect = False*， _initial_scale_factor = 2_）[\[来源\]](../_modules/manim/mobject/matrix.html#get_det_text)[#](#manim.mobject.matrix.get_det_text "此定义的固定链接")

创建行列式的辅助函数。

参数

- **矩阵**( [_Matrix_](manim.mobject.matrix.Matrix.html#manim.mobject.matrix.Matrix "manim.mobject.matrix.Matrix") ) – 要创建其行列式的矩阵
- **行列式**( _int_ _|_ _str_ _|_ _None_ ) – 矩阵行列式的值
- **background_rect** ( _bool_ ) – 背景矩形
- **initial_scale_factor** ( _float_ ) – 矩阵中文本的比例

退货

包含行列式的 VGroup

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：行列式矩阵[¶](#determinantofamatrix)

![../_images/DeterminantOfAMatrix-1.png](../_images/DeterminantOfAMatrix-1.png)

from manim import \*

class DeterminantOfAMatrix(Scene):
def construct(self):
matrix = Matrix(\[
\[2, 0\],
\[-1, 1\]
\])

        \# scaling down the \`det\` string
        det = get\_det\_text(matrix,
                    determinant=3,
                    initial\_scale\_factor=1)

        \# must add the matrix
        self.add(matrix)
        self.add(det)

Copy to clipboard

矩阵到对象（_矩阵_）[\[来源\]](../_modules/manim/mobject/matrix.html#matrix_to_mobject)[#](#manim.mobject.matrix.matrix_to_mobject "此定义的固定链接")

矩阵到文本字符串（_矩阵_）[\[来源\]](../_modules/manim/mobject/matrix.html#matrix_to_tex_string)[#](#manim.mobject.matrix.matrix_to_tex_string "此定义的固定链接")
