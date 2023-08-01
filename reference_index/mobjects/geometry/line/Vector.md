# 矢量

合格名称：`manim.mobject.geometry.line.Vector`

_类_ Vector (_方向= array(\[1., 0., 0.\])_ , _buff = 0_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Vector)[#](#manim.mobject.geometry.line.Vector "此定义的固定链接")

基地：[`Arrow`](manim.mobject.geometry.line.Arrow.html#manim.mobject.geometry.line.Arrow "manim.mobject.geometry.line.Arrow")

专门用于图形的向量。

参数

- **Direction** ( _list_ _|_ _np.ndarray_ ) – 箭头的方向。
- **buff** ( _float_ ) – 向量与其端点的距离。
- **kwargs** – 要传递给的附加参数[`Arrow`](manim.mobject.geometry.line.Arrow.html#manim.mobject.geometry.line.Arrow "manim.mobject.geometry.line.Arrow")

例子

示例：矢量示例[¶](#vectorexample)

![../_images/VectorExample-1.png](../_images/VectorExample-1.png)

from manim import \*

class VectorExample(Scene):
def construct(self):
plane = NumberPlane()
vector_1 = Vector(\[1,2\])
vector_2 = Vector(\[-5,-2\])
self.add(plane, vector_1, vector_2)

Copy to clipboard

方法

[`coordinate_label`](#manim.mobject.geometry.line.Vector.coordinate_label "manim.mobject.geometry.line.Vector.coordinate_label")

根据向量的坐标创建标签。

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

坐标标签（_整数标签=真_， _n_dim = 2_，_颜色=无_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Vector.coordinate_label)[#](#manim.mobject.geometry.line.Vector.coordinate_label "此定义的固定链接")

根据向量的坐标创建标签。

参数

- **integer_labels** ( _bool_ ) – 是否将坐标舍入为整数。
- **n_dim** ( _int_ ) – 向量的维数。
- **color** ( _Color_ _|_ _None_ ) – 设置标签的颜色，可选。
- **kwargs** – 要传递给 的附加参数[`Matrix`](manim.mobject.matrix.Matrix.html#manim.mobject.matrix.Matrix "manim.mobject.matrix.Matrix")。

退货

标签。

返回类型

[`Matrix`](manim.mobject.matrix.Matrix.html#manim.mobject.matrix.Matrix "manim.mobject.matrix.Matrix")

例子

示例：矢量坐标标签[¶](#vectorcoordinatelabel)

![../_images/VectorCooperativeLabel-1.png](../_images/VectorCoordinateLabel-1.png)

from manim import \*

class VectorCoordinateLabel(Scene):
def construct(self):
plane = NumberPlane()

        vec_1 = Vector(\[1, 2\])
        vec_2 = Vector(\[-3, -2\])
        label_1 = vec_1.coordinate_label()
        label_2 = vec_2.coordinate_label(color=YELLOW)

        self.add(plane, vec_1, vec_2, label_1, label_2)

Copy to clipboard
