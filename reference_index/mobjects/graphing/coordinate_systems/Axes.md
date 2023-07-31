# 轴[#](#axes "此标题的固定链接")

合格名称：`manim.mobject.graphing.coordinate\_systems.Axes`

_类_ 轴（_x_range = None_， _y_range = None_， _x_length = 12_， _y_length = 6_， _axis_config = None_， _x_axis_config = None_， _y_axis_config = None_， _Tips = True_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#Axes)[#](#manim.mobject.graphing.coordinate_systems.Axes "此定义的固定链接")

基地：[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup"),[`CoordinateSystem`](manim.mobject.graphing.coordinate_systems.CoordinateSystem.html#manim.mobject.graphing.coordinate_systems.CoordinateSystem "manim.mobject.graphing.coordinate_systems.坐标系统")

创建一组轴。

参数

- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – x 轴的值。`(x_min, x_max, x_step)`
- **y_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – y 轴的值。`(y_min, y_max, y_step)`
- **x_length** ( _float_ _|_ _None_ ) – x 轴的长度。
- **y_length** ( _float_ _|_ _None_ ) – y 轴的长度。
- **axis_config** ( _dict_ _|_ _None_ ) – 要传递给[`NumberLine`](manim.mobject.graphing.number_line.NumberLine.html#manim.mobject.graphing.number_line.NumberLine "manim.mobject.graphing.number_line.NumberLine")影响两个轴的参数。
- **x_axis_config** ( _dict_ _|_ _None_ ) – 传递给[`NumberLine`](manim.mobject.graphing.number_line.NumberLine.html#manim.mobject.graphing.number_line.NumberLine "manim.mobject.graphing.number_line.NumberLine")影响 x 轴的参数。
- **y_axis_config** ( _dict_ _|_ _None_ ) – 传递给[`NumberLine`](manim.mobject.graphing.number_line.NumberLine.html#manim.mobject.graphing.number_line.NumberLine "manim.mobject.graphing.number_line.NumberLine")影响 y 轴的参数。
- **Tips** ( _bool_ ) – 是否在两个轴上都包含提示。
- **kwargs** – 要传递给[`CoordinateSystem`](manim.mobject.graphing.coordinate_systems.CoordinateSystem.html#manim.mobject.graphing.coordinate_systems.CoordinateSystem "manim.mobject.graphing.coordinate_systems.坐标系统")和的附加参数[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")。

例子

示例：LogScalingExample [¶](#logscalingexample)

![../_images/LogScalingExample-1.png](../_images/LogScalingExample-1.png)

from manim import \*

class LogScalingExample(Scene):
def construct(self):
ax = Axes(
x_range=\[0, 10, 1\],
y_range=\[-2, 6, 1\],
tips=False,
axis_config={"include_numbers": True},
y_axis_config={"scaling": LogBase(custom_labels=True)},
)

        \# x_min must be > 0 because log is undefined at 0.
        graph = ax.plot(lambda x: x ** 2, x_range=\[0.001, 10\], use_smoothing=False)
        self.add(ax, graph)

Copy to clipboard

样式参数可以传递给[`NumberLine`](manim.mobject.graphing.number_line.NumberLine.html#manim.mobject.graphing.number_line.NumberLine "manim.mobject.graphing.number_line.NumberLine") 表示轴的底层 mobject：

示例：AxesWithDifferentTips [¶](#axeswithdifferenttips)

![../_images/AxesWithDifferentTips-1.png](../_images/AxesWithDifferentTips-1.png)

from manim import \*

class AxesWithDifferentTips(Scene):
def construct(self):
ax = Axes(axis_config={'tip_shape': StealthTip})
self.add(ax)

Copy to clipboard

方法

[`coords_to_point`](#manim.mobject.graphing.coordinate_systems.Axes.coords_to_point "manim.mobject.graphing.coordinate_systems.Axes.coords_to_point")

接受来自轴的坐标并返回相对于场景的点。

[`get_axes`](#manim.mobject.graphing.coordinate_systems.Axes.get_axes "manim.mobject.graphing.coordinate_systems.Axes.get_axes")

获取轴。

[`get_axis_labels`](#manim.mobject.graphing.coordinate_systems.Axes.get_axis_labels "manim.mobject.graphing.coordinate_systems.Axes.get_axis_labels")

定义图表的 x 轴和 y 轴标签。

[`plot_line_graph`](#manim.mobject.graphing.coordinate_systems.Axes.plot_line_graph "manim.mobject.graphing.coordinate_systems.Axes.plot_line_graph")

绘制折线图。

[`point_to_coords`](#manim.mobject.graphing.coordinate_systems.Axes.point_to_coords "manim.mobject.graphing.coordinate_systems.Axes.point_to_coords")

接受场景中的一个点并返回其相对于轴的坐标。

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

坐标到点( _\*坐标_)[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#Axes.coords_to_point)[#](#manim.mobject.graphing.coordinate_systems.Axes.coords_to_point "此定义的固定链接")

接受来自轴的坐标并返回相对于场景的点。

参数

**coords** ( _float_ _|**序列**\[_ _float_ _\]_ _|**序列**\[**序列**\[_ _float_ _\]_ _\]_ _|_ _np.ndarray_ ) –

该坐标。每个坐标作为单独的参数传递：。`ax.coords_to_point(1, 2, 3)`

还接受坐标列表

`ax.coords_to_point( [x_0, x_1, ...], [y_0, y_1, ...], ... )`

`ax.coords_to_point( [[x_0, y_0, z_0], [x_1, y_1, z_1]] )`

退货

相对于场景坐标系的点。数组的形状将与输入的形状相似。

返回类型

np.ndarray

例子

> > \> from manim import Axes
> > \> import numpy as np
> > \> ax = Axes()
> > \> np.around(ax.coords_to_point(1, 0, 0), 2)
> > array(\[0.86, 0. , 0. \])
> > \> np.around(ax.coords_to_point(\[\[0, 1\], \[1, 1\], \[1, 0\]\]), 2)
> > array(\[\[0. , 0.75, 0. \],
> > \[0.86, 0.75, 0. \],
> > \[0.86, 0. , 0. \]\])
> > \> np.around(
> > ... ax.coords_to_point(\[0, 1, 1\], \[1, 1, 0\]), 2
> > ... ) \# Transposed version of the above
> > array(\[\[0. , 0.86, 0.86\],
> > \[0.75, 0.75, 0. \],
> > \[0\. , 0. , 0. \]\])

Copy to clipboard

示例：CoordsToPointExample [¶](#coordstopointexample)

![../_images/CoordsToPointExample-1.png](../_images/CoordsToPointExample-1.png)

from manim import \*

class CoordsToPointExample(Scene):
def construct(self):
ax = Axes().add_coordinates()

        \# a dot with respect to the axes
        dot_axes = Dot(ax.coords\_to\_point(2, 2), color=GREEN)
        lines = ax.get\_lines\_to_point(ax.c2p(2,2))

        \# a dot with respect to the scene
        \# the default plane corresponds to the coordinates of the scene.
        plane = NumberPlane()
        dot_scene = Dot((2,2,0), color=RED)

        self.add(plane, dot_scene, ax, dot_axes, lines)

Copy to clipboard

获取轴( )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#Axes.get_axes)[#](#manim.mobject.graphing.coordinate_systems.Axes.get_axes "此定义的固定链接")

获取轴。

退货

一对轴。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

get*axis_labels ( \_x_label = 'x'* , _y_label = 'y'_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#Axes.get_axis_labels)[#](#manim.mobject.graphing.coordinate_systems.Axes.get_axis_labels "此定义的固定链接")

定义图表的 x 轴和 y 轴标签。

为了增强对标签位置的控制，请使用[`get_x_axis_label()`](manim.mobject.graphing.coordinate_systems.CoordinateSystem.html#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_x_axis_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_x_axis_label")和 [`get_y_axis_label()`](manim.mobject.graphing.coordinate_systems.CoordinateSystem.html#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_y_axis_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_y_axis_label")。

参数

- **x_label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – x\_轴的标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **y_label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – y 轴的标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")x_axis 和 y_axis 的标签。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

也可以看看

[`get_x_axis_label()`](manim.mobject.graphing.coordinate_systems.CoordinateSystem.html#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_x_axis_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_x_axis_label") [`get_y_axis_label()`](manim.mobject.graphing.coordinate_systems.CoordinateSystem.html#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_y_axis_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_y_axis_label")

例子

示例：GetAxisLabelsExample [¶](#getaxislabelsexample)

![../_images/GetAxisLabelsExample-1.png](../_images/GetAxisLabelsExample-1.png)

from manim import \*

class GetAxisLabelsExample(Scene):
def construct(self):
ax = Axes()
labels = ax.get_axis_labels(
Tex("x-axis").scale(0.7), Text("y-axis").scale(0.45)
)
self.add(ax, labels)

Copy to clipboard

plot*line_graph ( \_x_values* , _y_values_ , _z_values = None_ , _line_color = '#FFFF00'_ , _add_vertex_dots = True_ , _vertex_dot_radius = 0.08_ , _vertex_dot_style = None_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#Axes.plot_line_graph)[#](#manim.mobject.graphing.coordinate_systems.Axes.plot_line_graph "此定义的固定链接")

绘制折线图。

`x_values`该图连接了 zipping 、`y_values`和形成的顶点 `z_values`。如果设置为，还会[`Dots`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")在顶点处添加。` add_vertex_dots``True `

参数

- **x_values** ( _Iterable_ _\[_ _float_ _\]_ ) – 沿 x 轴的可迭代值。
- **y_values** ( _Iterable_ _\[_ _float_ _\]_ ) – 沿 y 轴的可迭代值。
- **z_values** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 沿 z 轴的可迭代值（如果 z_values 为 None，则为零）。
- **line_color** ( _Color_ ) – 折线图的颜色。
- **add_vertex_dots** ( _bool_ ) – 是否[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")在每个顶点添加。
- **vertex_dot_radius** ( _float_[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot") ) –每个顶点的半径。
- **vertex_dot_style** ( _dict_ _|_ _None_ ) – 要传递到[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")每个顶点的样式参数。
- **kwargs** – 要传递到[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject").

退货

包含线和点（如果指定）的 VDict。可以通过以下方式访问该线路：`line_graph["line_graph"]`。可以通过以下方式访问这些点：`line_graph["vertex_dots"]`。

返回类型

[`VDict`](manim.mobject.types.vectorized_mobject.VDict.html#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")

例子

示例：LineGraph 示例[¶](#linegraphexample)

![../_images/LineGraphExample-1.png](../_images/LineGraphExample-1.png)

from manim import \*

class LineGraphExample(Scene):
def construct(self):
plane = NumberPlane(
x_range = (0, 7),
y_range = (0, 5),
x_length = 7,
axis_config={"include_numbers": True},
)
plane.center()
line_graph = plane.plot_line_graph(
x_values = \[0, 1.5, 2, 2.8, 4, 6.25\],
y_values = \[1, 3, 2.25, 4, 2.5, 1.75\],
line_color=GOLD_E,
vertex_dot_style=dict(stroke_width=3, fill_color=PURPLE),
stroke_width = 4,
)
self.add(plane, line_graph)

Copy to clipboard

点到坐标（_点_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#Axes.point_to_coords)[#](#manim.mobject.graphing.coordinate_systems.Axes.point_to_coords "此定义的固定链接")

接受场景中的一个点并返回其相对于轴的坐标。

参数

**point** ( _Sequence_ _\[_ _float_ _\]_ ) – 点，即`RIGHT`或。还接受点列表作为。` [0, 1, 0]``[RIGHT, [0, 1, 0]] `

退货

轴上的坐标，即。或者如果点是点列表，则为坐标列表。`[4.0, 7.0]`

返回类型

np.ndarray\[浮点数\]

例子

> > \> from manim import Axes, RIGHT
> > \> import numpy as np
> > \> ax = Axes(x_range=\[0, 10, 2\])
> > \> np.around(ax.point_to_coords(RIGHT), 2)
> > array(\[5.83, 0. \])
> > \> np.around(ax.point_to_coords(\[\[0, 0, 1\], \[1, 0, 0\]\]), 2)
> > array(\[\[5. , 0. \],
> > \[5.83, 0. \]\])

Copy to clipboard

示例：PointToCoordsExample [¶](#pointtocoordsexample)

![../_images/PointToCoordsExample-1.png](../_images/PointToCoordsExample-1.png)

from manim import \*

class PointToCoordsExample(Scene):
def construct(self):
ax = Axes(x_range=\[0, 10, 2\]).add_coordinates()
circ = Circle(radius=0.5).shift(UR \* 2)

        \# get the coordinates of the circle with respect to the axes
        coords = np.around(ax.point\_to\_coords(circ.get_right()), decimals=2)

        label = (
            Matrix(\[\[coords\[0\]\], \[coords\[1\]\]\]).scale(0.75).next_to(circ, RIGHT)
        )

        self.add(ax, circ, label, Dot(circ.get_right()))

Copy to clipboard
