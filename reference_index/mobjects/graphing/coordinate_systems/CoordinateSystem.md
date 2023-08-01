# 坐标系

合格名称：`manim.mobject.graphing.coordinate\_systems.CoordinateSystem`

坐标系统*类*（_x_range = None_， _y_range = None_， _x_length = None_， _y_length = None_，_维度= 2_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem "此定义的固定链接")

基地：`object`

Axes 和 NumberPlane 的抽象基类。

例子

示例：CoordSysExample [¶](#coordsysexample)

![../_images/CoordSysExample-1.png](../_images/CoordSysExample-1.png)

from manim import \*

class CoordSysExample(Scene):
def construct(self):
\# the location of the ticks depends on the x_range and y_range.
grid = Axes(
x_range=\[0, 1, 0.05\], \# step size determines num_decimal_places.
y_range=\[0, 1, 0.05\],
x_length=9,
y_length=5.5,
axis_config={
"numbers_to_include": np.arange(0, 1 + 0.1, 0.1),
"font_size": 24,
},
tips=False,
)

        \# Labels for the x-axis and y-axis.
        y_label = grid.get\_y\_axis_label("y", edge=LEFT, direction=LEFT, buff=0.4)
        x_label = grid.get\_x\_axis_label("x")
        grid_labels = VGroup(x_label, y_label)

        graphs = VGroup()
        for n in np.arange(1, 20 + 0.5, 0.5):
            graphs += grid.plot(lambda x: x ** n, color=WHITE)
            graphs += grid.plot(
                lambda x: x ** (1 / n), color=WHITE, use_smoothing=False
            )

        \# Extra lines and labels for point (1,1)
        graphs += grid.get\_horizontal\_line(grid.c2p(1, 1, 0), color=BLUE)
        graphs += grid.get\_vertical\_line(grid.c2p(1, 1, 0), color=BLUE)
        graphs += Dot(point=grid.c2p(1, 1, 0), color=YELLOW)
        graphs += Tex("(1,1)").scale(0.75).next_to(grid.c2p(1, 1, 0))
        title = Title(
            \# spaces between braces to prevent SyntaxError
            r"Graphs of $y=x^{ {1}\\over{n} }$ and $y=x^n (n=1,2,3,...,20)$",
            include_underline=False,
            font_size=40,
        )

        self.add(title, graphs, grid, grid_labels)

Copy to clipboard

方法

[`add_coordinates`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.add_coordinates "manim.mobject.graphing.coordinate_systems.CooperativeSystem.add_coordinates")

向轴添加标签。

[`angle_of_tangent`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.angle_of_tangent "manim.mobject.graphing.coordinate_systems.CooperativeSystem.angle_of_tangent")

返回特定 x 值处绘制曲线的切线与 x 轴的角度。

[`c2p`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.c2p "manim.mobject.graphing.coordinate_systems.CooperativeSystem.c2p")

缩写为`coords_to_point()`

`coords_to_point`

[`get_T_label`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_T_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_T_label")

创建一个带标签的三角形标记，该标记具有从 x 轴到给定 x 值处的曲线的垂直线。

[`get_area`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_area "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_area")

返回[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon")代表传递的图形下方的区域。

`get_axes`

`get_axis`

`get_axis_labels`

[`get_graph_label`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_graph_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_graph_label")

为传递的图形创建一个正确定位的标签，带有可选的点。

[`get_horizontal_line`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_horizontal_line "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_horizo​​ntal_line")

从 y 轴到场景中给定点的水平线。

[`get_line_from_axis_to_point`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_line_from_axis_to_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_line_from_axis_to_point")

返回从给定轴到场景中的点的直线。

[`get_lines_to_point`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_lines_to_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_lines_to_point")

生成从轴到点的水平线和垂直线。

[`get_origin`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_origin "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_origin")

获取 的起源[`Axes`](manim.mobject.graphing.coordinate_systems.Axes.html#manim.mobject.graphing.coordinate_systems.Axes "manim.mobject.graphing.coordinate_systems.Axes")。

[`get_riemann_rectangles`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_riemann_rectangles "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_riemann_rectangles")

生成[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")给定曲线的黎曼矩形。

[`get_secant_slope_group`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_secant_slope_group "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_secant_slope_group")

创建代表 dx 和 df 的两条线，即 dx 和 df 的标签，以及

[`get_vertical_line`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_vertical_line "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_vertical_line")

从 x 轴到场景中给定点的垂直线。

[`get_vertical_lines_to_graph`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_vertical_lines_to_graph "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_vertical_lines_to_graph")

获取从 x 轴到曲线的多条直线。

`get_x_axis`

[`get_x_axis_label`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_x_axis_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_x_axis_label")

生成 x 轴标签。

`get_x_unit_size`

`get_y_axis`

[`get_y_axis_label`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_y_axis_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_y_axis_label")

生成 y 轴标签。

`get_y_unit_size`

`get_z_axis`

[`i2gc`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.i2gc "manim.mobject.graphing.coordinate_systems.CooperativeSystem.i2gc")

别名为[`input_to_graph_coords()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.input_to_graph_coords "manim.mobject.graphing.coordinate_systems.CooperativeSystem.input_to_graph_coords").

[`i2gp`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.i2gp "manim.mobject.graphing.coordinate_systems.CooperativeSystem.i2gp")

别名为[`input_to_graph_point()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.input_to_graph_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.input_to_graph_point").

[`input_to_graph_coords`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.input_to_graph_coords "manim.mobject.graphing.coordinate_systems.CooperativeSystem.input_to_graph_coords")

根据给定的 x 值返回图形上点的轴相对坐标的元组。

[`input_to_graph_point`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.input_to_graph_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.input_to_graph_point")

`graph`返回值对应的点的坐标`x`。

[`p2c`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.p2c "manim.mobject.graphing.coordinate_systems.CooperativeSystem.p2c")

缩写为`point_to_coords()`

[`plot`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot "manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot")

基于函数生成曲线。

[`plot_antiderivative_graph`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_antiderivative_graph "manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_antiderivative_graph")

绘制反导数图。

[`plot_derivative_graph`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_derivative_graph "manim.mobject.graphing.coordinate_systems.CooperativeSystem.plot_derivative_graph")

返回所传递图形的导数曲线。

[`plot_implicit_curve`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_implicit_curve "manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_implicit_curve")

创建隐函数的曲线。

[`plot_parametric_curve`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_parametric_curve "manim.mobject.graphing.coordinate_systems.CooperativeSystem.plot_parametric_curve")

参数曲线。

[`plot_polar_graph`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_polar_graph "manim.mobject.graphing.coordinate_systems.CooperativeSystem.plot_polar_graph")

极坐标图。

[`plot_surface`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_surface "manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_surface")

基于函数生成表面。

`point_to_coords`

[`point_to_polar`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.point_to_polar "manim.mobject.graphing.cooperative_systems.CooperativeSystem.point_to_极地")

从一点获取极坐标。

[`polar_to_point`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.polar_to_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.polar_to_point")

从极坐标获取点。

[`pr2pt`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.pr2pt "manim.mobject.graphing.coordinate_systems.CooperativeSystem.pr2pt")

缩写为[`polar_to_point()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.polar_to_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.polar_to_point")

[`pt2pr`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.pt2pr "manim.mobject.graphing.coordinate_systems.CooperativeSystem.pt2pr")

缩写为[`point_to_polar()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.point_to_polar "manim.mobject.graphing.cooperative_systems.CooperativeSystem.point_to_极地")

[`slope_of_tangent`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.slope_of_tangent "manim.mobject.graphing.coordinate_systems.CooperativeSystem.slope_of_tangent")

返回绘制曲线在特定 x 值处的切线斜率。

添加坐标（_\* axes_numbers_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.add_coordinates)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.add_coordinates "此定义的固定链接")

向轴添加标签。用于`Axes.coordinate_labels`在创建后访问坐标。

参数

**axes_numbers** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ _|_ _dict_ _\[_ _float_ _,_ _str_ _|_ _float_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _\]_ ) – 要添加到轴的数字。用于`None`表示带有默认标签的轴。

例子

ax = ThreeDAxes()
x_labels = range(-4, 5)
z_labels = range(-4, 4, 2)
ax.add_coordinates(x_labels, None, z_labels) \# default y labels, custom x & z labels
ax.add_coordinates(x_labels) \# only x labels

Copy to clipboard

您还可以使用字典专门控制标签的位置和值。

ax = Axes(x_range=\[0, 7\])
x_pos = \[x for x in range(1, 8)\]

\# strings are automatically converted into a Tex mobject.
x_vals = \["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"\]
x_dict = dict(zip(x_pos, x_vals))
ax.add_coordinates(x_dict)

Copy to clipboard

切线角度( _x_ ,_图形_, _dx = 1e-08_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.angle_of_tangent)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.angle_of_tangent "此定义的固定链接")

返回特定 x 值处绘制曲线的切线与 x 轴的角度。

参数

- **x** ( _float_ ) – 切线必须接触曲线的 x 值。
- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) –[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")要计算其正切的图。
- **dx** ( _float ) –_ x 的变化，用于确定曲线切线的角度。

退货

曲线的切线角度。

返回类型

`float`

例子

ax = Axes()
curve = ax.plot(lambda x: x\*\*2)
ax.angle_of_tangent(x=3, graph=curve)
\# 1.4056476493802699

Copy to clipboard

c2p ( _\*坐标_)[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.c2p)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.c2p "此定义的固定链接")

缩写为`coords_to_point()`

get*T_label ( \_x_val*、 _graph_、 _label=None_、 _label_color=None_、 _triangle_size=0.25_、 _triangle_color='#FFFFFF'_、 _line_func=<class 'manim.mobject.geometry.line.Line'>_、 _line_color='#FFFF00'_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_T_label)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_T_label "此定义的固定链接")

创建一个带标签的三角形标记，该标记具有从 x 轴到给定 x 值处的曲线的垂直线。

参数

- **x_val** ( _float_ ) – 沿着曲线构建标签、直线和三角形的位置。
- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) –[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")为其构造标签。
- **label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _|_ _None_ ) – 垂直线和三角形的标签。
- **label_color** ( _Color_ _|_ _None_ ) – 标签的颜色。
- **triangle_size** ( _float_ ) – 三角形的大小。
- **triangle_color** ( _Color_ _|_ _None_ ) – 三角形的颜色。
- **line_func** ( [_Line_](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line") ) – 用于构造垂直线的函数。
- **line_color** ( _Color_ ) – 垂直线的颜色。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")标签、三角形和垂直线 mobjects 的 A。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：TLabelExample [¶](#tlabelexample)

![../_images/TLabelExample-1.png](../_images/TLabelExample-1.png)

from manim import \*

class TLabelExample(Scene):
def construct(self):
\# defines the axes and linear function
axes = Axes(x_range=\[-1, 10\], y_range=\[-1, 10\], x_length=9, y_length=6)
func = axes.plot(lambda x: x, color=BLUE)
\# creates the T_label
t_label = axes.get_T_label(x_val=4, graph=func, label=Tex("x-value"))
self.add(axes, func, t_label)

Copy to clipboard

get*area (*图形*, \_x_range =无*,_颜色= \['#58C4DD', '#83C167'\]_ ,_不透明度= 0.3_ ,_有界图=无_, _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_area)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_area "此定义的固定链接")

返回[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon")代表传递的图形下方的区域。

参数

- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) – 需要获取面积的图形/曲线。
- **x_range** ( _tuple_ _\[_ _float_ _,_ _float_ _\]_ _|_ _None_ ) – 区域的最小和最大 x 值的范围。。`x_range = [x_min, x_max]`
- **color** ( _Color_ _|_ _Iterable_ _\[_ _Color_ _\]_ ) – 区域的颜色。如果提供了颜色列表，则创建渐变。
- **opacity** ( _float_ ) – 区域的不透明度。
- **bounded_graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) – 如果指定了辅助函数`graph`，则包围两条曲线之间的区域。
- **kwargs** – 传递给[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon").

退货

代表[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon")地区。

返回类型

[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon")

提高

**ValueError** – 当 x_range 不匹配时（区域 x_range、图形的 x_range 或有界图的 x_range）。

例子

示例：获取区域示例[¶](#getareaexample)

![../_images/GetAreaExample-1.png](../_images/GetAreaExample-1.png)

from manim import \*

class GetAreaExample(Scene):
def construct(self):
ax = Axes().add*coordinates()
curve = ax.plot(lambda x: 2 * np.sin(x), color=DARK*BLUE)
area = ax.get_area(
curve,
x_range=(PI / 2, 3 * PI / 2),
color=(GREEN_B, GREEN_D),
opacity=1,
)

        self.add(ax, curve, area)

Copy to clipboard

get*graph_label ( \_graph* , _label = 'f(x)'_ , _x_val = None_ , _Direction = array(\[1., 0., 0.\])_ , _buff = 0.25_ , _color = None_ , _dot = False_ , _dot_config = None_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_graph_label)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_graph_label "此定义的固定链接")

为传递的图形创建一个正确定位的标签，带有可选的点。

参数

- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) – 曲线。
- **label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 函数曲线的标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **x_val** ( _float_ _|_ _None_ ) – 沿定位标签的曲线的 x_value。
- **Direction** ( _Sequence_ _\[_ _float_ _\]_ ) – 笛卡尔位置，相对于标签所在的曲线 –\> `LEFT`, `RIGHT`。
- **buff** ( _float_ ) – 曲线和标签之间的距离。
- **color** ( _Color_ _|_ _None_ ) – 标签的颜色。默认为曲线的颜色。
- **dot** ( _bool_ ) – 是否在图表上的点处添加点。
- **dot_config** ( _dict_ _|_ _None_ ) – 要传递给的附加参数[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")。

退货

定位标签 和[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")，如果适用。

返回类型

`Mobject`

例子

示例：GetGraphLabelExample [¶](#getgraphlabelexample)

![../_images/GetGraphLabelExample-1.png](../_images/GetGraphLabelExample-1.png)

from manim import \*

class GetGraphLabelExample(Scene):
def construct(self):
ax = Axes()
sin = ax.plot(lambda x: np.sin(x), color=PURPLE_B)
label = ax.get_graph_label(
graph=sin,
label= MathTex(r"\\frac{\\pi}{2}"),
x_val=PI / 2,
dot=True,
direction=UR,
)

        self.add(ax, sin, label)

Copy to clipboard

get*horizo​​ntal_line (*点*, *\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_horizontal_line)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_horizontal_line "此定义的固定链接")

从 y 轴到场景中给定点的水平线。

参数

- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 将绘制水平线的点。
- **kwargs** – 要传递给 的附加参数[`get_line_from_axis_to_point`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_line_from_axis_to_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_line_from_axis_to_point")。

退货

从 y 轴到该点的水平线。

返回类型

`Line`

例子

示例：获取水平线示例[¶](#gethorizontallineexample)

![../_images/GetHorizo​​ntalLineExample-1.png](../_images/GetHorizontalLineExample-1.png)

from manim import \*

class GetHorizontalLineExample(Scene):
def construct(self):
ax = Axes().add_coordinates()
point = ax.c2p(-4, 1.5)

        dot = Dot(point)
        line = ax.get\_horizontal\_line(point, line_func=Line)

        self.add(ax, line, dot)

Copy to clipboard

get*line_from_axis_to*point (*索引*,*点*, \_line_func=<class 'manim.mobject.geometry.line.DashedLine'>* , \_line_config=None* , _color=None_ , _stroke_width=2_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_line_from_axis_to_point)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_line_from_axis_to_point "此定义的固定链接")

返回从给定轴到场景中的点的直线。

参数

- **index** ( _int_ ) – 指定绘制线条的轴。0 = x*轴, 1 = y*轴
- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 将绘制线条的点。
- **line_func** ( [_Line_](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line") ) –用于构造线条的 mobject 函数。
- **line_config** ( _dict_ _|_ _None_ ) – 传递给的可选参数`line_func`。
- **color** ( _Color_ _|_ _None_ ) – 线条的颜色。
- **Stroke_width** ( _float_ ) – 线条的描边宽度。

退货

从轴到点的线。

返回类型

[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")

也可以看看

[`get_vertical_line()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_vertical_line "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_vertical_line") [`get_horizontal_line()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_horizontal_line "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_horizo​​ntal_line")

get_lines_to*point (*点*, *\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_lines_to_point)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_lines_to_point "此定义的固定链接")

生成从轴到点的水平线和垂直线。

参数

- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 场景中的一个点。
- **kwargs** – 要传递给的附加参数[`get_line_from_axis_to_point()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_line_from_axis_to_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_line_from_axis_to_point")

退货

A[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")水平线和垂直线。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

也可以看看

[`get_vertical_line()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_vertical_line "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_vertical_line") [`get_horizontal_line()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_horizontal_line "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_horizo​​ntal_line")

例子

示例：GetLinesToPointExample [¶](#getlinestopointexample)

![../_images/GetLinesToPointExample-1.png](../_images/GetLinesToPointExample-1.png)

from manim import \*

class GetLinesToPointExample(Scene):
def construct(self):
ax = Axes()
circ = Circle(radius=0.5).move_to(\[-4, -1.5, 0\])

        lines_1 = ax.get\_lines\_to_point(circ.get_right(), color=GREEN_B)
        lines_2 = ax.get\_lines\_to_point(circ.get_corner(DL), color=BLUE_B)
        self.add(ax, lines_1, lines_2, circ)

Copy to clipboard

获取原点( )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_origin)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_origin "此定义的固定链接")

获取 的起源[`Axes`](manim.mobject.graphing.coordinate_systems.Axes.html#manim.mobject.graphing.coordinate_systems.Axes "manim.mobject.graphing.coordinate_systems.Axes")。

退货

中心点。

返回类型

np.ndarray

get*riemann_rectangles (*图形*, \_x_range = None* , _dx = 0.1_ , _input_sample_type = 'left'_ ,_笔画宽度= 1_ ,_笔画颜色= '#000000'_ , _fill_opacity = 1_ , _color = array(\['#58C4DD', '#83C167'\], dtype ='<U7')_、 _show_signed_area = True_、 _bounded_graph = None_、 _blend = False_、_宽度比例因子= 1.001_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_riemann_rectangles)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_riemann_rectangles "此定义的固定链接")

生成[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")给定曲线的黎曼矩形。

参数

- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) – 其面积将由黎曼矩形近似的图。
- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 矩形的最小和最大 x 值。。`x_range = [x_min, x_max]`
- **dx** ( _float_ _|_ _None_ ) – 分隔每个矩形的 x 值的变化。
- **input_sample_type** ( _str_ ) – 可以是`"left"`,`"right"`或 中的任何一个`"center"`。指每个黎曼矩形的高度的采样点位于分区线段内部的位置。
- **stroke_width** ( _float_ ) – 矩形边框的描边宽度。
- **stroke_color** ( _Color_ ) – 矩形边框的颜色。
- **fill_opacity** ( _float_ ) – 矩形的不透明度。
- **color** ( _Iterable_ _\[_ _Color_ _\]_ _|_ _Color_ ) – 矩形的颜色。如果传递多种颜色，则创建平衡的渐变。
- **show_signed_area** ( _bool_ ) – 通过反转颜色来指示曲线低于 x 轴时的负面积。
- **Blend** ( _bool_ ) – 设置`stroke_color`为`fill_color`，混合矩形而没有明显的分离。
- **bounded_graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) – 如果指定了辅助图，则包围两条曲线之间的区域。
- **width_scale_factor** ( _float_ ) – 矩形宽度缩放的因子。

退货

A[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")包含黎曼矩形。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：GetRiemannRectanglesExample [¶](#getriemannrectanglesexample)

![../_images/GetRiemannRectanglesExample-1.png](../_images/GetRiemannRectanglesExample-1.png)

from manim import \*

class GetRiemannRectanglesExample(Scene):
def construct(self):
ax = Axes(y_range=\[-2, 10\])
quadratic = ax.plot(lambda x: 0.5 \* x \*\* 2 - 0.5)

        \# the rectangles are constructed from their top right corner.
        \# passing an iterable to \`color\` produces a gradient
        rects_right = ax.get\_riemann\_rectangles(
            quadratic,
            x_range=\[-4, -3\],
            dx=0.25,
            color=(TEAL, BLUE_B, DARK_BLUE),
            input\_sample\_type="right",
        )

        \# the colour of rectangles below the x-axis is inverted
        \# due to show\_signed\_area
        rects_left = ax.get\_riemann\_rectangles(
            quadratic, x_range=\[-1.5, 1.5\], dx=0.15, color=YELLOW
        )

        bounding_line = ax.plot(
            lambda x: 1.5 * x, color=BLUE_B, x_range=\[3.3, 6\]
        )
        bounded_rects = ax.get\_riemann\_rectangles(
            bounding_line,
            bounded_graph=quadratic,
            dx=0.15,
            x_range=\[4, 5\],
            show\_signed\_area=False,
            color=(MAROON_A, RED_B, PURPLE_D),
        )

        self.add(
            ax, bounding_line, quadratic, rects_right, rects_left, bounded_rects
        )

Copy to clipboard

get*secant_slope*group ( \_x* , \_graph* , _dx = None_ , _dx_line_color = '#FFFF00'_ , _dy_line_color = None_ , _dx_label = None_ , _dy_label = None_ , _include_secant_line = True_ , _secant_line_color = '#83C167'_ , _secant_line_length = 10_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_secant_slope_group)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_secant_slope_group "此定义的固定链接")

创建代表 dx 和 df 的两条线，即 dx 和 df 的标签，以及

特定 x 值处曲线的割线。

参数

- **x** ( _float_ ) – 割线首次与图形相交的 x 值。
- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) – 将找到割线的曲线。
- **dx** ( _float_ _|_ _None_ ) –割线退出后 x 的变化。
- **dx_line_color** ( \_Color ) – 指示\_x 变化的线条颜色。
- **dy_line_color** ( _Color_ _|_ \_None ) – 指示\_y 变化的线条颜色。默认为 的颜色`graph`。
- **dx_label** ( _float_ _|_ _str_ _|_ _None ) –_ dx 线的标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **dy_label** ( _float_ _|_ _str_ _|_ _None ) –_ dy 线的标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **include_secant_line** ( _bool_ ) – 是否在图形中包含割线，或者仅包含 df/dx 线和标签。
- **secant_line_color** ( _Color_ ) – 割线的颜色。
- **secant_line_length** ( _float_ ) – 割线的长度。

退货

包含以下元素的组：dx_line、df_line，以及（如果适用）`dx_label`, `df_label`, secant_line。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：GetSecantSlopeGroupExample [¶](#getsecantslopegroupexample)

![../_images/GetSecantSlopeGroupExample-1.png](../_images/GetSecantSlopeGroupExample-1.png)

from manim import \*

class GetSecantSlopeGroupExample(Scene):
def construct(self):
ax = Axes(y_range=\[-1, 7\])
graph = ax.plot(lambda x: 1 / 4 \* x \*\* 2, color=BLUE)
slopes = ax.get_secant_slope_group(
x=2.0,
graph=graph,
dx=1.0,
dx_label=Tex("dx = 1.0"),
dy_label="dy",
dx_line_color=GREEN_B,
secant_line_length=4,
secant_line_color=RED_D,
)

        self.add(ax, graph, slopes)

Copy to clipboard

get*vertical_line（*点*， *\*\* kwargs\_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_vertical_line)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_vertical_line "此定义的固定链接")

从 x 轴到场景中给定点的垂直线。

参数

- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 将绘制垂直线的点。
- **kwargs** – 要传递给 的附加参数[`get_line_from_axis_to_point`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_line_from_axis_to_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_line_from_axis_to_point")。

退货

从 x 轴到该点的垂直线。

返回类型

`Line`

例子

示例：获取垂直线示例[¶](#getverticallineexample)

![../_images/GetVerticalLineExample-1.png](../_images/GetVerticalLineExample-1.png)

from manim import \*

class GetVerticalLineExample(Scene):
def construct(self):
ax = Axes().add_coordinates()
point = ax.coords_to_point(-3.5, 2)

        dot = Dot(point)
        line = ax.get\_vertical\_line(point, line_config={"dashed_ratio": 0.85})

        self.add(ax, line, dot)

Copy to clipboard

get*vertical_lines_to_graph (*图形*, \_x_range = None* , _num_lines = 20_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_vertical_lines_to_graph)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_vertical_lines_to_graph "此定义的固定链接")

获取从 x 轴到曲线的多条直线。

参数

- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) – 线条沿其放置的图形。
- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 包含以下行的下限和上限的列表：。`x_range = [x_min, x_max]`
- **num_lines** ( _int_ ) – 均匀间隔的行数。
- **kwargs** – 要传递给 的附加参数[`get_vertical_line()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_vertical_line "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_vertical_line")。

退货

均匀[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")间隔线的 。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：GetVerticalLinesToGraph [¶](#getverticallinestograph)

![../_images/GetVerticalLinesToGraph-1.png](../_images/GetVerticalLinesToGraph-1.png)

from manim import \*

class GetVerticalLinesToGraph(Scene):
def construct(self):
ax = Axes(
x_range=\[0, 8.0, 1\],
y_range=\[-1, 1, 0.2\],
axis_config={"font_size": 24},
).add_coordinates()

        curve = ax.plot(lambda x: np.sin(x) / np.e ** 2 * x)

        lines = ax.get\_vertical\_lines\_to\_graph(
            curve, x_range=\[0, 4\], num_lines=30, color=BLUE
        )

        self.add(ax, curve, lines)

Copy to clipboard

get*x_axis*label (*标签*,*边缘= array(\[1., 1., 0.\])* ,*方向= array(\[1., 1., 0.\])* , \_buff = 0.1* , *\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_x_axis_label)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_x_axis_label "此定义的固定链接")

生成 x 轴标签。

参数

- **label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **edge** ( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下将添加标签的 x 轴边缘`UR`。
- **方向**( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下，允许从边缘进一步定位标签`UR`。
- **buff** ( _float_ ) – 标签与线条的距离。

退货

定位的标签。

返回类型

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

例子

示例：GetXAxisLabelExample [¶](#getxaxislabelexample)

![../_images/GetXAxisLabelExample-1.png](../_images/GetXAxisLabelExample-1.png)

from manim import \*

class GetXAxisLabelExample(Scene):
def construct(self):
ax = Axes(x_range=(0, 8), y_range=(0, 5), x_length=8, y_length=5)
x_label = ax.get_x_axis_label(
Tex("$x$-values").scale(0.65), edge=DOWN, direction=DOWN, buff=0.5
)
self.add(ax, x_label)

Copy to clipboard

get*y_axis*label (*标签*,*边缘= array(\[1., 1., 0.\])* ,*方向= array(\[1., 0.5, 0.\])* , \_buff = 0.1* , *\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.get_y_axis_label)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_y_axis_label "此定义的固定链接")

生成 y 轴标签。

参数

- **label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **edge** ( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下将添加标签的 x 轴边缘`UR`。
- **方向**( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下允许从边缘进一步定位标签`UR`
- **buff** ( _float_ ) – 标签与线条的距离。

退货

定位的标签。

返回类型

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

例子

示例：GetYAxisLabelExample [¶](#getyaxislabelexample)

![../_images/GetYAxisLabelExample-1.png](../_images/GetYAxisLabelExample-1.png)

from manim import \*

class GetYAxisLabelExample(Scene):
def construct(self):
ax = Axes(x_range=(0, 8), y_range=(0, 5), x_length=8, y_length=5)
y_label = ax.get_y_axis_label(
Tex("$y$-values").scale(0.65).rotate(90 \* DEGREES),
edge=LEFT,
direction=LEFT,
buff=0.3,
)
self.add(ax, y_label)

Copy to clipboard

i2gc（_x_，_图_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.i2gc)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.i2gc "此定义的固定链接")

别名为[`input_to_graph_coords()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.input_to_graph_coords "manim.mobject.graphing.coordinate_systems.CooperativeSystem.input_to_graph_coords").

参数

- **x**（_浮动_）–
- **图**（[_参数函数_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")）–

返回类型

元组

i2gp（_x_，_图_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.i2gp)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.i2gp "此定义的固定链接")

别名为[`input_to_graph_point()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.input_to_graph_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.input_to_graph_point").

参数

- **x**（_浮动_）–
- **图**（[_参数函数_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")）–

返回类型

_ndarray_

input*to_graph*coords（\_x*，*图\_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.input_to_graph_coords)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.input_to_graph_coords "此定义的固定链接")

根据给定的 x 值返回图形上点的轴相对坐标的元组。

例子

> > \> from manim import Axes
> > \> ax = Axes()
> > \> parabola = ax.plot(lambda x: x\*\*2)
> > \> ax.input_to_graph_coords(x=3, graph=parabola)
> > (3, 9)

Copy to clipboard

参数

- **x**（_浮动_）–
- **图**（[_参数函数_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")）–

返回类型

元组

输入到图点（_x_，_图_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.input_to_graph_point)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.input_to_graph_point "此定义的固定链接")

`graph`返回值对应的点的坐标`x`。

参数

- **x** ( _float_ ) – 上点的 x 值`graph`。
- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") _|_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) –[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")点所在的图。

退货

`graph`值对应的点的坐标`x`。

返回类型

`np.ndarray`

提高

**ValueError** – 当目标 x 不在折线图范围内时。

例子

示例：InputToGraphPointExample [¶](#inputtographpointexample)

![../_images/InputToGraphPointExample-1.png](../_images/InputToGraphPointExample-1.png)

from manim import \*

class InputToGraphPointExample(Scene):
def construct(self):
ax = Axes()
curve = ax.plot(lambda x : np.cos(x))

        \# move a square to PI on the cosine curve.
        position = ax.input\_to\_graph_point(x=PI, graph=curve)
        sq = Square(side_length=1, color=YELLOW).move_to(position)

        self.add(ax, curve, sq)

Copy to clipboard

p2c（_点_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.p2c)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.p2c "此定义的固定链接")

缩写为`point_to_coords()`

绘图（_函数_， _x_range = None_， _use_vectorized = False_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.plot)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot "此定义的固定链接")

基于函数生成曲线。

参数

- **function** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) – 用于构造[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction").
- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 曲线沿轴的范围。。`x_range = [x_min, x_max, x_step]`
- **use_vectorized** ( _bool_ ) – 是否将生成的 t 值数组传递给函数。仅当您的函数支持时才使用它。输出应该是形状的 numpy 数组`[y_0, y_1, ...]`
- **kwargs** – 要传递给 的附加参数[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")。

退货

绘制的曲线。

返回类型

[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")

警告

此方法可能无法生成准确的图表，因为 Manim 目前依赖于曲线均匀间隔样本之间的插值，而不是智能绘图。请参阅下面的示例，了解此问题的一些解决方案。

例子

示例：绘图示例[¶](#plotexample)

![../_images/PlotExample-1.png](../_images/PlotExample-1.png)

from manim import \*

class PlotExample(Scene):
def construct(self):
\# construct the axes
ax_1 = Axes(
x_range=\[0.001, 6\],
y_range=\[-8, 2\],
x_length=5,
y_length=3,
tips=False,
)
ax_2 = ax_1.copy()
ax_3 = ax_1.copy()

        \# position the axes
        ax_1.to_corner(UL)
        ax_2.to_corner(UR)
        ax_3.to_edge(DOWN)
        axes = VGroup(ax_1, ax_2, ax_3)

        \# create the logarithmic curves
        def log_func(x):
            return np.log(x)

        \# a curve without adjustments; poor interpolation.
        curve_1 = ax_1.plot(log_func, color=PURE_RED)

        \# disabling interpolation makes the graph look choppy as not enough
        \# inputs are available
        curve_2 = ax_2.plot(log_func, use_smoothing=False, color=ORANGE)

        \# taking more inputs of the curve by specifying a step for the
        \# x_range yields expected results, but increases rendering time.
        curve_3 = ax_3.plot(
            log_func, x_range=(0.001, 6, 0.001), color=PURE_GREEN
        )

        curves = VGroup(curve_1, curve_2, curve_3)

        self.add(axes, curves)

Copy to clipboard

plot*antiderivative_graph（*图*， \_y_intercept = 0*，_样本= 50_， _use_vectorized = False_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.plot_antiderivative_graph)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_antiderivative_graph "此定义的固定链接")

绘制反导数图。

参数

- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) – 将找到反导数的图。
- **y_intercept** ( _float_ ) – 图形与 y 轴相交的 y 值。
- **Samples** ( _int_ ) – 获取图表下方面积的点数。
- **use_vectorized** ( _bool_ ) – 是否使用反导数的矢量化版本。这意味着将生成的 t 值数组传递给函数。仅当您的函数支持时才使用它。输出应该是形状的 numpy 数组`[y_0, y_1, ...]`
- **kwargs** – 的任何有效关键字参数[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")。

退货

反导数的曲线。

返回类型

[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")

笔记

该图是根据参考图下方的面积值绘制的。如果参考图包含来自 x=0 的不可计算区域，结果可能不理想。

例子

示例：反导数示例[¶](#antiderivativeexample)

![../_images/AntiderivativeExample-1.png](../_images/AntiderivativeExample-1.png)

from manim import \*

class AntiderivativeExample(Scene):
def construct(self):
ax = Axes()
graph1 = ax.plot(
lambda x: (x \*\* 2 - 2) / 3,
color=RED,
)
graph2 = ax.plot_antiderivative_graph(graph1, color=BLUE)
self.add(ax, graph1, graph2)

Copy to clipboard

plot*derivative_graph (*图形*,*颜色= '#83C167'_ , _\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.plot_derivative_graph)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_derivative_graph "此定义的固定链接")

返回所传递图形的导数曲线。

参数

- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) – 将找到导数的图表。
- **color** ( _Color_ ) – 导数曲线的颜色。
- **kwargs** – 的任何有效关键字参数[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")。

退货

导数的曲线。

返回类型

[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")

例子

示例：DerivativeGraph 示例[¶](#derivativegraphexample)

![../_images/DerivativeGraphExample-1.png](../_images/DerivativeGraphExample-1.png)

from manim import \*

class DerivativeGraphExample(Scene):
def construct(self):
ax = NumberPlane(y_range=\[-1, 7\], background_line_style={"stroke_opacity": 0.4})

        curve_1 = ax.plot(lambda x: x ** 2, color=PURPLE_B)
        curve_2 = ax.plot\_derivative\_graph(curve_1)
        curves = VGroup(curve_1, curve_2)

        label_1 = ax.get\_graph\_label(curve_1, "x^2", x_val=-2, direction=DL)
        label_2 = ax.get\_graph\_label(curve_2, "2x", x_val=3, direction=RIGHT)
        labels = VGroup(label_1, label_2)

        self.add(ax, curves, labels)

Copy to clipboard

plot*implicit_curve ( \_func* , *min*深度= 5* , \_max_quads = 1500* , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.plot_implicit_curve)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_implicit_curve "此定义的固定链接")

创建隐函数的曲线。

参数

- **func** ( _Callable_ ) – 绘制图形的函数，形式为 f(x, y) = 0。
- **min_depth** ( _int_ ) – 要计算的函数的最小深度。
- **max_quads** ( _int_ ) – 要使用的最大四边形数量。
- **kwargs** – 要传递到 的附加参数`ImplicitFunction`。

返回类型

[_隐式函数_](manim.mobject.graphing.functions.ImplicitFunction.html#manim.mobject.graphing.functions.ImplicitFunction "manim.mobject.graphing.functions.ImplicitFunction")

例子

示例：隐式示例[¶](#implicitexample)

![../_images/ImplicitExample-1.png](../_images/ImplicitExample-1.png)

from manim import \*

class ImplicitExample(Scene):
def construct(self):
ax = Axes()
a = ax.plot*implicit_curve(
lambda x, y: y * (x - y) \*\* 2 - 4 \_ x - 8, color=BLUE
)
self.add(ax, a)

Copy to clipboard

plot*parametric_curve (*函数*, \_use_vectorized = False* , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.plot_parametric_curve)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_parametric_curve "此定义的固定链接")

参数曲线。

参数

- **function** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _ndarray_ _\]_ ) – 将数字映射到坐标系中的点的参数函数。
- **use_vectorized** ( _bool_ ) – 是否将生成的 t 值数组传递给函数。仅当您的函数支持时才使用它。
- **kwargs** – 任何其他关键字参数都会传递到[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction").

返回类型

[_参数函数_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")

例子

示例：参数曲线示例[¶](#parametriccurveexample)

![../_images/ParametricCurveExample-1.png](../_images/ParametricCurveExample-1.png)

from manim import \*

class ParametricCurveExample(Scene):
def construct(self):
ax = Axes()
cardioid = ax.plot*parametric_curve(
lambda t: np.array(
\[
np.exp(1) * np.cos(t) _ (1 - np.cos(t)),
np.exp(1) _ np.sin(t) \_ (1 - np.cos(t)),
0,
\]
),
t_range=\[0, 2 \* PI\],
color="#0FF1CE",
)
self.add(ax, cardioid)

Copy to clipboard

绘图极性图（_r_func_， _theta_range = \[0, 6.283185307179586\]_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.plot_polar_graph)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_polar_graph "此定义的固定链接")

极坐标图。

参数

- **r_func** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) – theta 的函数 r。
- **theta_range** ( _Sequence_ _\[_ _float_ _\]_ ) – theta 的范围为。`theta_range = [theta_min, theta_max, theta_step]`
- **kwargs** – 传递给[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction").

返回类型

[_参数函数_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")

例子

示例：PolarGraph 示例[¶](#polargraphexample)

![../_images/PolarGraphExample-1.png](../_images/PolarGraphExample-1.png)

from manim import \*

class PolarGraphExample(Scene):
def construct(self):
plane = PolarPlane()
r = lambda theta: 2 _ np.sin(theta _ 5)
graph = plane.plot_polar_graph(r, \[0, 2 \* PI\], color=ORANGE)
self.add(plane, graph)

Copy to clipboard

参考：[`PolarPlane`](manim.mobject.graphing.coordinate_systems.PolarPlane.html#manim.mobject.graphing.coordinate_systems.PolarPlane "manim.mobject.graphing.coordinate_systems.PolarPlane")

绘图表面（_函数_， _u_range =无_， _v_range =无_， _colorscale =无_， _colorscale_axis = 2_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.plot_surface)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.plot_surface "此定义的固定链接")

基于函数生成表面。

参数

- **function** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) – 用于构造[`Surface`](manim.mobject.three_d.three_dimensions.Surface.html#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface").
- **u_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 变量的范围`u`：。`(u_min, u_max)`
- **v_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 变量的范围`v`：。`(v_min, v_max)`
- **colorscale** ( _Sequence_ _\[_ _\[_ _color_ _\]_ _,_ _float_ _\]_ _|_ _None_ ) – 表面的颜色。传递颜色列表将按 z 值对表面进行着色。在表单中传递元组列表允许用户定义颜色过渡的枢轴。`(color, pivot)`
- **colorscale_axis** ( _int_ ) – 定义应用色阶的轴（0 = x、1 = y、2 = z），默认为 z 轴 (2)。
- **kwargs** – 要传递给 的附加参数[`Surface`](manim.mobject.three_d.three_dimensions.Surface.html#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。

退货

绘制的曲面。

返回类型

[`Surface`](manim.mobject.three_d.three_dimensions.Surface.html#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")

例子

示例：PlotSurfaceExample [¶](#plotsurfaceexample)

![../_images/PlotSurfaceExample-1.png](../_images/PlotSurfaceExample-1.png)

from manim import \*

class PlotSurfaceExample(ThreeDScene):
def construct(self):
resolution*fa = 16
self.set_camera_orientation(phi=75 * DEGREES, theta=-60 _ DEGREES)
axes = ThreeDAxes(x_range=(-3, 3, 1), y_range=(-3, 3, 1), z_range=(-5, 5, 1))
def param_trig(u, v):
x = u
y = v
z = 2 _ np.sin(x) + 2 \_ np.cos(y)
return z
trig_plane = axes.plot_surface(
param_trig,
resolution=(resolution_fa, resolution_fa),
u_range = (-3, 3),
v_range = (-3, 3),
colorscale = \[BLUE, GREEN, YELLOW, ORANGE, RED\],
)
self.add(axes, trig_plane)

Copy to clipboard

点到极（_点_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.point_to_polar)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.point_to_polar "此定义的固定链接")

从一点获取极坐标。

参数

**point** ( _np.ndarray_ ) – 点。

退货

坐标半径（r）和坐标方位角（θ）。

返回类型

元组\[ `float`, `float`\]

极地到点（_半径_，_方位角_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.polar_to_point)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.polar_to_point "此定义的固定链接")

从极坐标获取点。

参数

- **radius** ( _float_ ) – 坐标半径 (r）。
- **方位角**( _float_ ) – 坐标方位角 (θ）。

退货

重点是。

返回类型

numpy.ndarray

例子

示例：PolarToPointExample [¶](#polartopointexample)

![../_images/PolarToPointExample-1.png](../_images/PolarToPointExample-1.png)

from manim import \*

class PolarToPointExample(Scene):
def construct(self):
polarplane_pi = PolarPlane(azimuth_units="PI radians", size=6)
polartopoint_vector = Vector(polarplane_pi.polar_to_point(3, PI/4))
self.add(polarplane_pi)
self.add(polartopoint_vector)

Copy to clipboard

参考：[`PolarPlane`](manim.mobject.graphing.coordinate_systems.PolarPlane.html#manim.mobject.graphing.coordinate_systems.PolarPlane "manim.mobject.graphing.coordinate_systems.PolarPlane") [`Vector`](manim.mobject.geometry.line.Vector.html#manim.mobject.geometry.line.Vector "manim.mobject.geometry.line.Vector")

pr2pt（_半径_，_方位角_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.pr2pt)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.pr2pt "此定义的固定链接")

缩写为[`polar_to_point()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.polar_to_point "manim.mobject.graphing.coordinate_systems.CooperativeSystem.polar_to_point")

参数

- **半径**（_浮动_）–
- **方位角**（_浮动_）–

返回类型

_ndarray_

pt2pr（_点_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.pt2pr)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.pt2pr "此定义的固定链接")

缩写为[`point_to_polar()`](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.point_to_polar "manim.mobject.graphing.cooperative_systems.CooperativeSystem.point_to_极地")

参数

**点**( _np.ndarray_ ) –

返回类型

元组\[浮点数，浮点数\]

切线斜率( _x_ ,_图形_, _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#CoordinateSystem.slope_of_tangent)[#](#manim.mobject.graphing.coordinate_systems.CoordinateSystem.slope_of_tangent "此定义的固定链接")

返回绘制曲线在特定 x 值处的切线斜率。

参数

- **x** ( _float_ ) – 切线必须接触曲线的 x 值。
- **graph** ( [_ParametricFunction_](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction") ) –[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")要计算其正切的图。

退货

与 x 轴的切线的斜率。

返回类型

`float`

例子

ax = Axes()
curve = ax.plot(lambda x: x\*\*2)
ax.slope_of_tangent(x=-2, graph=curve)
\# -3.5000000259052038

Copy to clipboard
