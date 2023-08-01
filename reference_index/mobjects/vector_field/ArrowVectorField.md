# 箭头向量字段

合格名称：`manim.mobject.vector\_field.ArrowVectorField`

_类_ ArrowVectorField ( _func, color=None, color_scheme=None, min_color_scheme_value=0, max_color_scheme_value=2, 颜色=\['#236B8E', '#83C167', '#FFFF00', '#FC6255'\], x_range=None, y_range =无， z_range =无， Three_dimensions = False， length_func = <函数 ArrowVectorField.<lambda >>， opacity = 1.0， vector_config =无， \*\* kwargs_）[\[来源\]](../_modules/manim/mobject/vector_field.html#ArrowVectorField)[#](#manim.mobject.vector_field.ArrowVectorField "此定义的固定链接")

基地：[`VectorField`](manim.mobject.vector_field.VectorField.html#manim.mobject.vector_field.VectorField "manim.mobject.vector_field.VectorField")

A[`VectorField`](manim.mobject.vector_field.VectorField.html#manim.mobject.vector_field.VectorField "manim.mobject.vector_field.VectorField")由一组变化向量表示。

矢量场始终基于定义[`Vector`](manim.mobject.geometry.line.Vector.html#manim.mobject.geometry.line.Vector "manim.mobject.geometry.line.Vector")每个位置的函数。该函数的值显示为向量网格。默认情况下，每个向量的颜色由其大小决定。然而，可以使用其他配色方案。

参数

- **func** ( _Callable_ _\[_ _\[_ _np.ndarray_ _\]_ _,_ _np.ndarray_ _\]_ ) – 定义向量场每个位置的变化率的函数。
- **color** ( _Color_ _|_ _None_ ) – 矢量场的颜色。如果设置，则禁用特定于位置的着色。
- **color_scheme** ( _Callable_ _\[_ _\[_ _np.ndarray_ _\]_ _,_ _float_ _\]_ _|_ _None_ ) – 将向量映射到单个值的函数。该值给出使用 min_color_scheme_value、max_color_scheme_value 和 Colors 定义的颜色渐变中的位置。
- **min_color_scheme_value** ( *float ) – 要映射到*颜色中第一个颜色的 color_scheme 函数的值。较低的值也会导致渐变的第一种颜色。
- **max_color_scheme_value** ( *float ) – 要映射到*颜色中最后一个颜色的 color_scheme 函数的值。较高的值也会导致渐变的最后一种颜色。
- **颜色**( _Sequence_ _\[_ _Color_ _\]_ ) – 定义矢量场颜色渐变的颜色。
- **x_range** ( _Sequence_ _\[_ _float_ _\]_ ) – x_min、x_max、delta_x 的序列
- **y_range** ( _Sequence_ _\[_ _float_ _\]_ ) – y_min、y_max、delta_y 的序列
- **z_range** ( _Sequence_ _\[_ _float_ _\]_ ) – z_min、z_max、delta_z 的序列
- **Three_dimensions** ( _bool_ ) – 启用 Three_dimensions。默认设置为 False，如果 z_range 不为 None，则自动变为 True。
- **length_func** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) – 确定向量显示大小的函数。传递向量的实际大小，返回的值将用作向量的显示大小。默认情况下，这用于限制矢量的显示大小以减少混乱。
- **opacity** ( _float_ ) – 箭头的不透明度。
- **vector_config** ( _dict_ _|_ _None_ ) – 要传递给[`Vector`](manim.mobject.geometry.line.Vector.html#manim.mobject.geometry.line.Vector "manim.mobject.geometry.line.Vector")构造函数的附加参数
- **kwargs** – 要传递给[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")构造函数的附加参数

例子

示例：基本用法[¶](#basicusage)

![../_images/BasicUsage-1.png](../_images/BasicUsage-1.png)

from manim import \*

class BasicUsage(Scene):
def construct(self):
func = lambda pos: ((pos\[0\] _ UR + pos\[1\] _ LEFT) - pos) / 3
self.add(ArrowVectorField(func))

Copy to clipboard

示例：调整大小和间距[¶](#sizingandspacing)

from manim import \*

class SizingAndSpacing(Scene):
def construct(self):
func = lambda pos: np.sin(pos\[0\] / 2) _ UR + np.cos(pos\[1\] / 2) _ LEFT
vf = ArrowVectorField(func, x_range=\[-7, 7, 1\])
self.add(vf)
self.wait()

        length_func = lambda x: x / 3
        vf2 = ArrowVectorField(func, x_range=\[-7, 7, 1\], length_func=length_func)
        self.play(vf.animate.become(vf2))
        self.wait()

Copy to clipboard

示例：着色[¶](#coloring)

![../_images/着色-1.png](../_images/Coloring-1.png)

from manim import \*

class Coloring(Scene):
def construct(self):
func = lambda pos: pos - LEFT _ 5
colors = \[RED, YELLOW, BLUE, DARK_GRAY\]
min_radius = Circle(radius=2, color=colors\[0\]).shift(LEFT _ 5)
max_radius = Circle(radius=10, color=colors\[-1\]).shift(LEFT \* 5)
vf = ArrowVectorField(
func, min_color_scheme_value=2, max_color_scheme_value=10, colors=colors
)
self.add(vf, min_radius, max_radius)

Copy to clipboard

方法

[`get_vector`](#manim.mobject.vector_field.ArrowVectorField.get_vector "manim.mobject.vector_field.ArrowVectorField.get_vector")

在矢量场中创建一个矢量。

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

获取向量（_点_）[\[来源\]](../_modules/manim/mobject/vector_field.html#ArrowVectorField.get_vector)[#](#manim.mobject.vector_field.ArrowVectorField.get_vector "此定义的固定链接")

在矢量场中创建一个矢量。

创建的向量基于向量场的函数，并以给定点为根。颜色和长度符合该矢量场的规范。

参数

**point** ( _ndarray_ ) – 向量的根点。
