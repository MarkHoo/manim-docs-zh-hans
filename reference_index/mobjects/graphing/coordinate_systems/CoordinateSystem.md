# 坐标系

合格名称：`manim.mobject.graphing.coordinate\_systems.CoordinateSystem`


```py
class CoordinateSystem(x_range=None, y_range=None, x_length=None, y_length=None, dimension=2)
```

Bases: `object`

Axes 和 NumberPlane 的抽象基类。

例子

示例：CoordSysExample

![CoordSysExample-1.png](../../static/CoordSysExample-1.png)

```py
from manim import *

class CoordSysExample(Scene):
    def construct(self):
        # the location of the ticks depends on the x_range and y_range.
        grid = Axes(
            x_range=[0, 1, 0.05],  # step size determines num_decimal_places.
            y_range=[0, 1, 0.05],
            x_length=9,
            y_length=5.5,
            axis_config={
                "numbers_to_include": np.arange(0, 1 + 0.1, 0.1),
                "font_size": 24,
            },
            tips=False,
        )

        # Labels for the x-axis and y-axis.
        y_label = grid.get_y_axis_label("y", edge=LEFT, direction=LEFT, buff=0.4)
        x_label = grid.get_x_axis_label("x")
        grid_labels = VGroup(x_label, y_label)

        graphs = VGroup()
        for n in np.arange(1, 20 + 0.5, 0.5):
            graphs += grid.plot(lambda x: x ** n, color=WHITE)
            graphs += grid.plot(
                lambda x: x ** (1 / n), color=WHITE, use_smoothing=False
            )

        # Extra lines and labels for point (1,1)
        graphs += grid.get_horizontal_line(grid.c2p(1, 1, 0), color=BLUE)
        graphs += grid.get_vertical_line(grid.c2p(1, 1, 0), color=BLUE)
        graphs += Dot(point=grid.c2p(1, 1, 0), color=YELLOW)
        graphs += Tex("(1,1)").scale(0.75).next_to(grid.c2p(1, 1, 0))
        title = Title(
            # spaces between braces to prevent SyntaxError
            r"Graphs of $y=x^{ {1}\over{n} }$ and $y=x^n (n=1,2,3,...,20)$",
            include_underline=False,
            font_size=40,
        )

        self.add(title, graphs, grid, grid_labels)
```


方法

|||
|-|-|
[`add_coordinates`]()|向轴添加标签。
[`angle_of_tangent`]()|返回特定 x 值处绘制曲线的切线与 x 轴的角度。
[`c2p`]()|缩写为`coords_to_point()`
`coords_to_point`|
[`get_T_label`]()|创建一个带标签的三角形标记，该标记具有从 x 轴到给定 x 值处的曲线的垂直线。
[`get_area`]()|返回[`Polygon`]()代表传递的图形下方的区域。
`get_axes`|
`get_axis`|
`get_axis_labels`|
[`get_graph_label`]()|为传递的图形创建一个正确定位的标签，带有可选的点。
[`get_horizontal_line`]()|从 y 轴到场景中给定点的水平线。
[`get_line_from_axis_to_point`]()|返回从给定轴到场景中的点的直线。
[`get_lines_to_point`]()|生成从轴到点的水平线和垂直线。
[`get_origin`]()|获取 的起源[`Axes`]()。
[`get_riemann_rectangles`]()|生成[`VGroup`]()给定曲线的黎曼矩形。
[`get_secant_slope_group`]()|创建代表 dx 和 df 的两条线，即 dx 和 df 的标签，以及
[`get_vertical_line`]()|从 x 轴到场景中给定点的垂直线。
[`get_vertical_lines_to_graph`]()|获取从 x 轴到曲线的多条直线。
`get_x_axis`|
[`get_x_axis_label`]()|生成 x 轴标签。
`get_x_unit_size`|
`get_y_axis`|
[`get_y_axis_label`]()|生成 y 轴标签。
`get_y_unit_size`|
`get_z_axis`|
[`i2gc`]()|别名为[`input_to_graph_coords()`]().
[`i2gp`]()|别名为[`input_to_graph_point()`]().
[`input_to_graph_coords`]()|根据给定的 x 值返回图形上点的轴相对坐标的元组。
[`input_to_graph_point`]()|`graph`返回值对应的点的坐标`x`。
[`p2c`]()|缩写为`point_to_coords()`
[`plot`]()|基于函数生成曲线。
[`plot_antiderivative_graph`]()|绘制反导数图。
[`plot_derivative_graph`]()|返回所传递图形的导数曲线。
[`plot_implicit_curve`]()|创建隐函数的曲线。
[`plot_parametric_curve`]()|参数曲线。
[`plot_polar_graph`]()|极坐标图。
[`plot_surface`]()|基于函数生成表面。
`point_to_coords`|
[`point_to_polar`]()|从一点获取极坐标。
[`polar_to_point`]()|从极坐标获取点。
[`pr2pt`]()|缩写为[`polar_to_point()`]()
[`pt2pr`]()|缩写为[`point_to_polar()`]()
[`slope_of_tangent`]()|返回绘制曲线在特定 x 值处的切线斜率。



`add_coordinates(*axes_numbers, **kwargs)`

向轴添加标签。用于`Axes.coordinate_labels`在创建后访问坐标。

参数

**axes_numbers** ( _Iterable[float] | None | dict[float, str | float | Mobject]_ ) – 要添加到轴的数字。用于`None`表示带有默认标签的轴。

例子

```py
ax = ThreeDAxes()
x_labels = range(-4, 5)
z_labels = range(-4, 4, 2)
ax.add_coordinates(x_labels, None, z_labels)  # default y labels, custom x & z labels
ax.add_coordinates(x_labels)  # only x labels
```


您还可以使用字典专门控制标签的位置和值。

```py
ax = Axes(x_range=[0, 7])
x_pos = [x for x in range(1, 8)]

# strings are automatically converted into a Tex mobject.
x_vals = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
x_dict = dict(zip(x_pos, x_vals))
ax.add_coordinates(x_dict)
```


`angle_of_tangent(x, graph, dx=1e-08)`

返回特定 x 值处绘制曲线的切线与 x 轴的角度。

参数

- **x** ( _float_ ) – 切线必须接触曲线的 x 值。
- **graph** ( [_ParametricFunction_]() ) –[`ParametricFunction`]()要计算其正切的图。
- **dx** ( _float ) –_ x 的变化，用于确定曲线切线的角度。

返回

曲线的切线角度。

返回类型

`float`

例子

```py
ax = Axes()
curve = ax.plot(lambda x: x**2)
ax.angle_of_tangent(x=3, graph=curve)
# 1.4056476493802699
```


`c2p(*coords)`

缩写为`coords_to_point()`


```py
get_T_label(x_val, graph, label=None, label_color=None, triangle_size=0.25, triangle_color='#FFFFFF', line_func=<class 'manim.mobject.geometry.line.Line'>, line_color='#FFFF00')
```

创建一个带标签的三角形标记，该标记具有从 x 轴到给定 x 值处的曲线的垂直线。

参数

- **x_val** ( _float_ ) – 沿着曲线构建标签、直线和三角形的位置。
- **graph** ( [_ParametricFunction_]() ) –[`ParametricFunction`]()为其构造标签。
- **label** ( _float_ _|_ _str_ _|_ [_Mobject_]() _|_ _None_ ) – 垂直线和三角形的标签。
- **label_color** ( _Color_ _|_ _None_ ) – 标签的颜色。
- **triangle_size** ( _float_ ) – 三角形的大小。
- **triangle_color** ( _Color_ _|_ _None_ ) – 三角形的颜色。
- **line_func** ( [_Line_]() ) – 用于构造垂直线的函数。
- **line_color** ( _Color_ ) – 垂直线的颜色。

返回

[`VGroup`]()标签、三角形和垂直线 mobjects 的 A。

返回类型

[`VGroup`]()

例子

示例：TLabelExample

![../../static/TLabelExample-1.png](../../static/TLabelExample-1.png)

```py
from manim import *

class TLabelExample(Scene):
    def construct(self):
        # defines the axes and linear function
        axes = Axes(x_range=[-1, 10], y_range=[-1, 10], x_length=9, y_length=6)
        func = axes.plot(lambda x: x, color=BLUE)
        # creates the T_label
        t_label = axes.get_T_label(x_val=4, graph=func, label=Tex("x-value"))
        self.add(axes, func, t_label)
```


```py
get_area(graph, x_range=None, color=['#58C4DD', '#83C167'], opacity=0.3, bounded_graph=None, **kwargs)
```

返回[`Polygon`]()代表传递的图形下方的区域。

参数

- **graph** ( [_ParametricFunction_]() ) – 需要获取面积的图形/曲线。
- **x_range** ( _tuple_ _\[_ _float_ _,_ _float_ _\]_ _|_ _None_ ) – 区域的最小和最大 x 值的范围。。`x_range = [x_min, x_max]`
- **color** ( _Color_ _|_ _Iterable_ _\[_ _Color_ _\]_ ) – 区域的颜色。如果提供了颜色列表，则创建渐变。
- **opacity** ( _float_ ) – 区域的不透明度。
- **bounded_graph** ( [_ParametricFunction_]() ) – 如果指定了辅助函数`graph`，则包围两条曲线之间的区域。
- **kwargs** – 传递给[`Polygon`]().

返回

代表[`Polygon`]()地区。

返回类型

[`Polygon`]()

提高

**ValueError** – 当 x_range 不匹配时（区域 x_range、图形的 x_range 或有界图的 x_range）。

例子

示例：获取区域示例

![../../static/GetAreaExample-1.png](../../static/GetAreaExample-1.png)

```py
from manim import *

class GetAreaExample(Scene):
    def construct(self):
        ax = Axes().add_coordinates()
        curve = ax.plot(lambda x: 2 * np.sin(x), color=DARK_BLUE)
        area = ax.get_area(
            curve,
            x_range=(PI / 2, 3 * PI / 2),
            color=(GREEN_B, GREEN_D),
            opacity=1,
        )

        self.add(ax, curve, area)
```


```py
get_graph_label(graph, label='f(x)', x_val=None, direction=array([1., 0., 0.]), buff=0.25, color=None, dot=False, dot_config=None)
```

为传递的图形创建一个正确定位的标签，带有可选的点。

参数

- **graph** ( [_ParametricFunction_]() ) – 曲线。
- **label** ( _float_ _|_ _str_ _|_ [_Mobject_]() ) – 函数曲线的标签。默认为[`MathTex`]()for`str`和`float`输入。
- **x_val** ( _float_ _|_ _None_ ) – 沿定位标签的曲线的 x_value。
- **Direction** ( _Sequence_ _\[_ _float_ _\]_ ) – 笛卡尔位置，相对于标签所在的曲线 –\> `LEFT`, `RIGHT`。
- **buff** ( _float_ ) – 曲线和标签之间的距离。
- **color** ( _Color_ _|_ _None_ ) – 标签的颜色。默认为曲线的颜色。
- **dot** ( _bool_ ) – 是否在图表上的点处添加点。
- **dot_config** ( _dict_ _|_ _None_ ) – 要传递给的附加参数[`Dot`]()。

返回

定位标签 和[`Dot`]()，如果适用。

返回类型

`Mobject`

例子

示例：GetGraphLabelExample 

![../../static/GetGraphLabelExample-1.png](../../static/GetGraphLabelExample-1.png)

```py
from manim import *

class GetGraphLabelExample(Scene):
    def construct(self):
        ax = Axes()
        sin = ax.plot(lambda x: np.sin(x), color=PURPLE_B)
        label = ax.get_graph_label(
            graph=sin,
            label= MathTex(r"\frac{\pi}{2}"),
            x_val=PI / 2,
            dot=True,
            direction=UR,
        )

        self.add(ax, sin, label)
```


`get_horizontal_line(point, **kwargs)`

从 y 轴到场景中给定点的水平线。

参数

- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 将绘制水平线的点。
- **kwargs** – 要传递给 的附加参数[`get_line_from_axis_to_point`]()。

返回

从 y 轴到该点的水平线。

返回类型

`Line`


例子

示例：获取水平线示例

![GetHorizontalLineExample-1.png](../../static/GetHorizontalLineExample-1.png)

```py
from manim import *

class GetHorizontalLineExample(Scene):
    def construct(self):
        ax = Axes().add_coordinates()
        point = ax.c2p(-4, 1.5)

        dot = Dot(point)
        line = ax.get_horizontal_line(point, line_func=Line)

        self.add(ax, line, dot)
```


```py
get_line_from_axis_to_point(index, point, line_func=<class 'manim.mobject.geometry.line.DashedLine'>, line_config=None, color=None, stroke_width=2)
```

返回从给定轴到场景中的点的直线。

参数

- **index** ( _int_ ) – 指定绘制线条的轴。0 = x*轴, 1 = y*轴
- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 将绘制线条的点。
- **line_func** ( [_Line_]()[`Line`]() ) –用于构造线条的 mobject 函数。
- **line_config** ( _dict_ _|_ _None_ ) – 传递给的可选参数`line_func`。
- **color** ( _Color_ _|_ _None_ ) – 线条的颜色。
- **Stroke_width** ( _float_ ) – 线条的描边宽度。

返回

从轴到点的线。

返回类型

[`Line`]()


> 也可以看看

> [`get_vertical_line()`]() [`get_horizontal_line()`]()


`get_lines_to_point(point, **kwargs)`

生成从轴到点的水平线和垂直线。

参数

- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 场景中的一个点。
- **kwargs** – 要传递给的附加参数[`get_line_from_axis_to_point()`]()

返回

A[`VGroup`]()水平线和垂直线。

返回类型

[`VGroup`]()


> 也可以看看

> [`get_vertical_line()`]() [`get_horizontal_line()`]()


例子

示例：GetLinesToPointExample 

![GetLinesToPointExample-1.png](../../static/GetLinesToPointExample-1.png)

```py
from manim import *

class GetLinesToPointExample(Scene):
    def construct(self):
        ax = Axes()
        circ = Circle(radius=0.5).move_to([-4, -1.5, 0])

        lines_1 = ax.get_lines_to_point(circ.get_right(), color=GREEN_B)
        lines_2 = ax.get_lines_to_point(circ.get_corner(DL), color=BLUE_B)
        self.add(ax, lines_1, lines_2, circ)
```


`get_origin()`

获取 的起源[`Axes`]()。

返回

中心点。

返回类型

np.ndarray


```py
get_riemann_rectangles(graph, x_range=None, dx=0.1, input_sample_type='left', stroke_width=1, stroke_color='#000000', fill_opacity=1, color=array(['#58C4DD', '#83C167'], dtype='<U7'), show_signed_area=True, bounded_graph=None, blend=False, width_scale_factor=1.001)
```

生成[`VGroup`]()给定曲线的黎曼矩形。

参数

- **graph** ( [_ParametricFunction_]() ) – 其面积将由黎曼矩形近似的图。
- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 矩形的最小和最大 x 值。。`x_range = [x_min, x_max]`
- **dx** ( _float_ _|_ _None_ ) – 分隔每个矩形的 x 值的变化。
- **input_sample_type** ( _str_ ) – 可以是`"left"`,`"right"`或 中的任何一个`"center"`。指每个黎曼矩形的高度的采样点位于分区线段内部的位置。
- **stroke_width** ( _float_ ) – 矩形边框的描边宽度。
- **stroke_color** ( _Color_ ) – 矩形边框的颜色。
- **fill_opacity** ( _float_ ) – 矩形的不透明度。
- **color** ( _Iterable_ _\[_ _Color_ _\]_ _|_ _Color_ ) – 矩形的颜色。如果传递多种颜色，则创建平衡的渐变。
- **show_signed_area** ( _bool_ ) – 通过反转颜色来指示曲线低于 x 轴时的负面积。
- **Blend** ( _bool_ ) – 设置`stroke_color`为`fill_color`，混合矩形而没有明显的分离。
- **bounded_graph** ( [_ParametricFunction_]() ) – 如果指定了辅助图，则包围两条曲线之间的区域。
- **width_scale_factor** ( _float_ ) – 矩形宽度缩放的因子。

返回

A[`VGroup`]()包含黎曼矩形。

返回类型

[`VGroup`]()


例子

示例：GetRiemannRectanglesExample

![GetRiemannRectanglesExample-1.png](../../static/GetRiemannRectanglesExample-1.png)

```py
from manim import *

class GetRiemannRectanglesExample(Scene):
    def construct(self):
        ax = Axes(y_range=[-2, 10])
        quadratic = ax.plot(lambda x: 0.5 * x ** 2 - 0.5)

        # the rectangles are constructed from their top right corner.
        # passing an iterable to `color` produces a gradient
        rects_right = ax.get_riemann_rectangles(
            quadratic,
            x_range=[-4, -3],
            dx=0.25,
            color=(TEAL, BLUE_B, DARK_BLUE),
            input_sample_type="right",
        )

        # the colour of rectangles below the x-axis is inverted
        # due to show_signed_area
        rects_left = ax.get_riemann_rectangles(
            quadratic, x_range=[-1.5, 1.5], dx=0.15, color=YELLOW
        )

        bounding_line = ax.plot(
            lambda x: 1.5 * x, color=BLUE_B, x_range=[3.3, 6]
        )
        bounded_rects = ax.get_riemann_rectangles(
            bounding_line,
            bounded_graph=quadratic,
            dx=0.15,
            x_range=[4, 5],
            show_signed_area=False,
            color=(MAROON_A, RED_B, PURPLE_D),
        )

        self.add(
            ax, bounding_line, quadratic, rects_right, rects_left, bounded_rects
        )
```


```py
get_secant_slope_group(x, graph, dx=None, dx_line_color='#FFFF00', dy_line_color=None, dx_label=None, dy_label=None, include_secant_line=True, secant_line_color='#83C167', secant_line_length=10)
```

创建代表 dx 和 df 的两条线，即 dx 和 df 的标签，以及

特定 x 值处曲线的割线。

参数

- **x** ( _float_ ) – 割线首次与图形相交的 x 值。
- **graph** ( [_ParametricFunction_]() ) – 将找到割线的曲线。
- **dx** ( _float_ _|_ _None_ ) –割线退出后 x 的变化。
- **dx_line_color** ( \_Color ) – 指示\_x 变化的线条颜色。
- **dy_line_color** ( _Color_ _|_ \_None ) – 指示\_y 变化的线条颜色。默认为 的颜色`graph`。
- **dx_label** ( _float_ _|_ _str_ _|_ _None ) –_ dx 线的标签。默认为[`MathTex`]()for`str`和`float`输入。
- **dy_label** ( _float_ _|_ _str_ _|_ _None ) –_ dy 线的标签。默认为[`MathTex`]()for`str`和`float`输入。
- **include_secant_line** ( _bool_ ) – 是否在图形中包含割线，或者仅包含 df/dx 线和标签。
- **secant_line_color** ( _Color_ ) – 割线的颜色。
- **secant_line_length** ( _float_ ) – 割线的长度。

返回

包含以下元素的组：dx_line、df_line，以及（如果适用）`dx_label`, `df_label`, secant_line。

返回类型

[`VGroup`]()


例子

示例：GetSecantSlopeGroupExample 

![GetSecantSlopeGroupExample-1.png](../../static/GetSecantSlopeGroupExample-1.png)

```py
from manim import *

class GetSecantSlopeGroupExample(Scene):
    def construct(self):
        ax = Axes(y_range=[-1, 7])
        graph = ax.plot(lambda x: 1 / 4 * x ** 2, color=BLUE)
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
```


`get_vertical_line(point, **kwargs)`

从 x 轴到场景中给定点的垂直线。

参数

- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 将绘制垂直线的点。
- **kwargs** – 要传递给 的附加参数[`get_line_from_axis_to_point`]()。

返回

从 x 轴到该点的垂直线。

返回类型

`Line`


例子

示例：获取垂直线示例

![GetVerticalLineExample-1.png](../../static/GetVerticalLineExample-1.png)

```py
from manim import *

class GetVerticalLineExample(Scene):
    def construct(self):
        ax = Axes().add_coordinates()
        point = ax.coords_to_point(-3.5, 2)

        dot = Dot(point)
        line = ax.get_vertical_line(point, line_config={"dashed_ratio": 0.85})

        self.add(ax, line, dot)
```


`get_vertical_lines_to_graph(graph, x_range=None, num_lines=20, **kwargs)`

获取从 x 轴到曲线的多条直线。

参数

- **graph** ( [_ParametricFunction_]() ) – 线条沿其放置的图形。
- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 包含以下行的下限和上限的列表：。`x_range = [x_min, x_max]`
- **num_lines** ( _int_ ) – 均匀间隔的行数。
- **kwargs** – 要传递给 的附加参数[`get_vertical_line()`]()。

返回

均匀[`VGroup`]()间隔线的 。

返回类型

[`VGroup`]()

例子

示例：GetVerticalLinesToGraph 

![GetVerticalLinesToGraph-1.png](../../static/GetVerticalLinesToGraph-1.png)

```py
from manim import *

class GetVerticalLinesToGraph(Scene):
    def construct(self):
        ax = Axes(
            x_range=[0, 8.0, 1],
            y_range=[-1, 1, 0.2],
            axis_config={"font_size": 24},
        ).add_coordinates()

        curve = ax.plot(lambda x: np.sin(x) / np.e ** 2 * x)

        lines = ax.get_vertical_lines_to_graph(
            curve, x_range=[0, 4], num_lines=30, color=BLUE
        )

        self.add(ax, curve, lines)
```


```py
get_x_axis_label(label, edge=array([1., 1., 0.]), direction=array([1., 1., 0.]), buff=0.1, **kwargs)
```

生成 x 轴标签。

参数

- **label** ( _float_ _|_ _str_ _|_ [_Mobject_]() ) – 标签。默认为[`MathTex`]()for`str`和`float`输入。
- **edge** ( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下将添加标签的 x 轴边缘`UR`。
- **direction**( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下，允许从边缘进一步定位标签`UR`。
- **buff** ( _float_ ) – 标签与线条的距离。

返回

定位的标签。

返回类型

[`Mobject`]()


例子

示例：GetXAxisLabelExample 

![GetXAxisLabelExample-1.png](../../static/GetXAxisLabelExample-1.png)

```py
from manim import *

class GetXAxisLabelExample(Scene):
    def construct(self):
        ax = Axes(x_range=(0, 8), y_range=(0, 5), x_length=8, y_length=5)
        x_label = ax.get_x_axis_label(
            Tex("$x$-values").scale(0.65), edge=DOWN, direction=DOWN, buff=0.5
        )
        self.add(ax, x_label)
```


```py
get_y_axis_label(label, edge=array([1., 1., 0.]), direction=array([1., 0.5, 0.]), buff=0.1, **kwargs)
```

生成 y 轴标签。

参数

- **label** ( _float_ _|_ _str_ _|_ [_Mobject_]() ) – 标签。默认为[`MathTex`]()for`str`和`float`输入。
- **edge** ( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下将添加标签的 x 轴边缘`UR`。
- **direction**( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下允许从边缘进一步定位标签`UR`
- **buff** ( _float_ ) – 标签与线条的距离。

返回

定位的标签。

返回类型

[`Mobject`]()

例子

示例：GetYAxisLabelExample 

![GetYAxisLabelExample-1.png](../../static/GetYAxisLabelExample-1.png)

```py
from manim import *

class GetYAxisLabelExample(Scene):
    def construct(self):
        ax = Axes(x_range=(0, 8), y_range=(0, 5), x_length=8, y_length=5)
        y_label = ax.get_y_axis_label(
            Tex("$y$-values").scale(0.65).rotate(90 * DEGREES),
            edge=LEFT,
            direction=LEFT,
            buff=0.3,
        )
        self.add(ax, y_label)
```


`i2gc(x, graph)`

别名为[`input_to_graph_coords()`]().

参数

- **x**（_float_）–
- **graph**（[_ParametricFunction_]()）–

返回类型

tuple


`i2gp(x, graph)`

别名为[`input_to_graph_point()`]().

参数

- **x**（_float_）–
- **graph**（[_ParametricFunction_]()）–

返回类型

_ndarray_


`input_to_graph_coords(x, graph)`

根据给定的 x 值返回图形上点的轴相对坐标的元组。

例子

```py
from manim import Axes
ax = Axes()
parabola = ax.plot(lambda x: x**2)
ax.input_to_graph_coords(x=3, graph=parabola)
(3, 9)
```


参数

- **x**（_float_）–
- **graph**（[_ParametricFunction]()）–

返回类型

tuple[float, float]











`input_to_graph_point(x, graph)`

`graph`返回值对应的点的坐标`x`。

参数

- **x** ( _float_ ) – 上点的 x 值`graph`。
- **graph** ( manim.mobject.graphing.functions.ParametricFunction | manim.mobject.types.vectorized_mobject.VMobject ) – 该点所在的`ParametricFunction`。

返回

`graph`值对应的点的坐标`x`。

返回类型

`np.ndarray`

额外：

**ValueError** – 当目标 x 不在折线图范围内时。

例子

示例：InputToGraphPointExample

![InputToGraphPointExample-1.png](../../static/InputToGraphPointExample-1.png)

```py
from manim import *

class InputToGraphPointExample(Scene):
    def construct(self):
        ax = Axes()
        curve = ax.plot(lambda x : np.cos(x))

        # move a square to PI on the cosine curve.
        position = ax.input_to_graph_point(x=PI, graph=curve)
        sq = Square(side_length=1, color=YELLOW).move_to(position)

        self.add(ax, curve, sq)
```

















`p2c(point)`

缩写为`point_to_coords()`

`plot(function, x_range=None, use_vectorized=False, **kwargs)`

基于函数生成曲线。

参数

- **function** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) – 用于构造[`ParametricFunction`]().
- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 曲线沿轴的范围。。`x_range = [x_min, x_max, x_step]`
- **use_vectorized** ( _bool_ ) – 是否将生成的 t 值数组传递给函数。仅当您的函数支持时才使用它。输出应该是形状的 numpy 数组`[y_0, y_1, ...]`
- **kwargs** – 要传递给 的附加参数[`ParametricFunction`]()。

返回

绘制的曲线。

返回类型

[`ParametricFunction`]()

> 警告

> 此方法可能无法生成准确的图表，因为 Manim 目前依赖于曲线均匀间隔样本之间的插值，而不是智能绘图。请参阅下面的示例，了解此问题的一些解决方案。

例子

示例：绘图示例

![PlotExample-1.png](../../static/PlotExample-1.png)

```py
from manim import *

class PlotExample(Scene):
    def construct(self):
        # construct the axes
        ax_1 = Axes(
            x_range=[0.001, 6],
            y_range=[-8, 2],
            x_length=5,
            y_length=3,
            tips=False,
        )
        ax_2 = ax_1.copy()
        ax_3 = ax_1.copy()

        # position the axes
        ax_1.to_corner(UL)
        ax_2.to_corner(UR)
        ax_3.to_edge(DOWN)
        axes = VGroup(ax_1, ax_2, ax_3)

        # create the logarithmic curves
        def log_func(x):
            return np.log(x)

        # a curve without adjustments; poor interpolation.
        curve_1 = ax_1.plot(log_func, color=PURE_RED)

        # disabling interpolation makes the graph look choppy as not enough
        # inputs are available
        curve_2 = ax_2.plot(log_func, use_smoothing=False, color=ORANGE)

        # taking more inputs of the curve by specifying a step for the
        # x_range yields expected results, but increases rendering time.
        curve_3 = ax_3.plot(
            log_func, x_range=(0.001, 6, 0.001), color=PURE_GREEN
        )

        curves = VGroup(curve_1, curve_2, curve_3)

        self.add(axes, curves)
```

```py
plot_antiderivative_graph(graph, y_intercept=0, samples=50, use_vectorized=False, **kwargs)
```
绘制反导数图。

参数

- **graph** ( [_ParametricFunction_]() ) – 将找到反导数的图。
- **y_intercept** ( _float_ ) – 图形与 y 轴相交的 y 值。
- **Samples** ( _int_ ) – 获取图表下方面积的点数。
- **use_vectorized** ( _bool_ ) – 是否使用反导数的矢量化版本。这意味着将生成的 t 值数组传递给函数。仅当您的函数支持时才使用它。输出应该是形状的 numpy 数组`[y_0, y_1, ...]`
- **kwargs** – 的任何有效关键字参数[`ParametricFunction`]()。

返回

反导数的曲线。

返回类型

[`ParametricFunction`]()

> 笔记

> 该图是根据参考图下方的面积值绘制的。如果参考图包含来自 x=0 的不可计算区域，结果可能不理想。

例子

示例：反导数示例

![AntiderivativeExample-1.png](../../static/AntiderivativeExample-1.png)

```py
from manim import *

class AntiderivativeExample(Scene):
    def construct(self):
        ax = Axes()
        graph1 = ax.plot(
            lambda x: (x ** 2 - 2) / 3,
            color=RED,
        )
        graph2 = ax.plot_antiderivative_graph(graph1, color=BLUE)
        self.add(ax, graph1, graph2)
```

`plot_derivative_graph(graph, color='#83C167', **kwargs)`

返回所传递图形的导数曲线。

参数

- **graph** ( [_ParametricFunction_]() ) – 将找到导数的图表。
- **color** ( _Color_ ) – 导数曲线的颜色。
- **kwargs** – 的任何有效关键字参数[`ParametricFunction`]()。

返回

导数的曲线。

返回类型

[`ParametricFunction`]()

例子

示例：DerivativeGraph 示例

![DerivativeGraphExample-1.png](../../static/DerivativeGraphExample-1.png)

```py
from manim import *

class DerivativeGraphExample(Scene):
    def construct(self):
        ax = NumberPlane(y_range=[-1, 7], background_line_style={"stroke_opacity": 0.4})

        curve_1 = ax.plot(lambda x: x ** 2, color=PURPLE_B)
        curve_2 = ax.plot_derivative_graph(curve_1)
        curves = VGroup(curve_1, curve_2)

        label_1 = ax.get_graph_label(curve_1, "x^2", x_val=-2, direction=DL)
        label_2 = ax.get_graph_label(curve_2, "2x", x_val=3, direction=RIGHT)
        labels = VGroup(label_1, label_2)

        self.add(ax, curves, labels)
```


`plot_implicit_curve(func, min_depth=5, max_quads=1500, **kwargs)`

创建隐函数的曲线。

参数

- **func** ( _Callable_ ) – 绘制图形的函数，形式为 f(x, y) = 0。
- **min_depth** ( _int_ ) – 要计算的函数的最小深度。
- **max_quads** ( _int_ ) – 要使用的最大四边形数量。
- **kwargs** – 要传递到 的附加参数`ImplicitFunction`。

返回类型

[_隐式函数_]()

例子

示例：隐式示例

![ImplicitExample-1.png](../../static/ImplicitExample-1.png)

```py
from manim import *

class ImplicitExample(Scene):
    def construct(self):
        ax = Axes()
        a = ax.plot_implicit_curve(
            lambda x, y: y * (x - y) ** 2 - 4 * x - 8, color=BLUE
        )
        self.add(ax, a)
```


`plot_parametric_curve(function, use_vectorized=False, **kwargs)`

参数曲线。

参数

- **function** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _ndarray_ _\]_ ) – 将数字映射到坐标系中的点的参数函数。
- **use_vectorized** ( _bool_ ) – 是否将生成的 t 值数组传递给函数。仅当您的函数支持时才使用它。
- **kwargs** – 任何其他关键字参数都会传递到[`ParametricFunction`]().

返回类型

[_ParametricFunction_]()

例子

示例：参数曲线示例

![ParametricCurveExample-1.png](../../static/ParametricCurveExample-1.png)

```py
from manim import *

class ParametricCurveExample(Scene):
    def construct(self):
        ax = Axes()
        cardioid = ax.plot_parametric_curve(
            lambda t: np.array(
                [
                    np.exp(1) * np.cos(t) * (1 - np.cos(t)),
                    np.exp(1) * np.sin(t) * (1 - np.cos(t)),
                    0,
                ]
            ),
            t_range=[0, 2 * PI],
            color="#0FF1CE",
        )
        self.add(ax, cardioid)
```


`plot_polar_graph(r_func, theta_range=[0, 6.283185307179586], **kwargs)`

极坐标图。

参数

- **r_func** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) – theta 的函数 r。
- **theta_range** ( _Sequence_ _\[_ _float_ _\]_ ) – theta 的范围为。`theta_range = [theta_min, theta_max, theta_step]`
- **kwargs** – 传递给[`ParametricFunction`]().

返回类型

[_ParametricFunction_]()


例子

示例：PolarGraph 示例

![PolarGraphExample-1.png](../../static/PolarGraphExample-1.png)

```py
from manim import *

class PolarGraphExample(Scene):
    def construct(self):
        plane = PolarPlane()
        r = lambda theta: 2 * np.sin(theta * 5)
        graph = plane.plot_polar_graph(r, [0, 2 * PI], color=ORANGE)
        self.add(plane, graph)
```

参考：[`PolarPlane`]()


```py
plot_surface(function, u_range=None, v_range=None, colorscale=None, colorscale_axis=2, **kwargs)
```

基于函数生成表面。

参数

- **function** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) – 用于构造[`Surface`]().
- **u_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 变量的范围`u`：。`(u_min, u_max)`
- **v_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 变量的范围`v`：。`(v_min, v_max)`
- **colorscale** ( _Sequence_ _\[_ _\[_ _color_ _\]_ _,_ _float_ _\]_ _|_ _None_ ) – 表面的颜色。传递颜色列表将按 z 值对表面进行着色。在表单中传递元组列表允许用户定义颜色过渡的枢轴。`(color, pivot)`
- **colorscale_axis** ( _int_ ) – 定义应用色阶的轴（0 = x、1 = y、2 = z），默认为 z 轴 (2)。
- **kwargs** – 要传递给 的附加参数[`Surface`]()。

返回

绘制的曲面。

返回类型

[`Surface`]()


例子

示例：PlotSurfaceExample

![PlotSurfaceExample-1.png](../../static/PlotSurfaceExample-1.png)

```py
from manim import *

class PlotSurfaceExample(ThreeDScene):
    def construct(self):
        resolution_fa = 16
        self.set_camera_orientation(phi=75 * DEGREES, theta=-60 * DEGREES)
        axes = ThreeDAxes(x_range=(-3, 3, 1), y_range=(-3, 3, 1), z_range=(-5, 5, 1))
        def param_trig(u, v):
            x = u
            y = v
            z = 2 * np.sin(x) + 2 * np.cos(y)
            return z
        trig_plane = axes.plot_surface(
            param_trig,
            resolution=(resolution_fa, resolution_fa),
            u_range = (-3, 3),
            v_range = (-3, 3),
            colorscale = [BLUE, GREEN, YELLOW, ORANGE, RED],
            )
        self.add(axes, trig_plane)
```


`point_to_polar(point)`

从一点获取极坐标。

参数

**point** ( _np.ndarray_ ) – 点。

返回

坐标半径（r）和坐标方位角（θ）。

返回类型

Tuple[`float`, `float`]


`polar_to_point(radius, azimuth)`

从极坐标获取点。

参数

- **radius** ( _float_ ) – 坐标半径 (r）。
- **azimuth**( _float_ ) – 坐标方位角 (θ）。

返回

点

返回类型

numpy.ndarray

例子

示例：PolarToPointExample

![PolarToPointExample-1.png](../../static/PolarToPointExample-1.png)

```py
from manim import *

class PolarToPointExample(Scene):
    def construct(self):
        polarplane_pi = PolarPlane(azimuth_units="PI radians", size=6)
        polartopoint_vector = Vector(polarplane_pi.polar_to_point(3, PI/4))
        self.add(polarplane_pi)
        self.add(polartopoint_vector)
```

参考：[`PolarPlane`]() [`Vector`]()


`pr2pt(radius, azimuth)`

缩写为[`polar_to_point()`]()

参数

- **radius **（_float_）–
- **azimuth**（_float_）–

返回类型

_ndarray_


`pt2pr(point)`

缩写为[`point_to_polar()`]()

参数

**point**( _np.ndarray_ ) –

返回类型

tuple[float, float]


`slope_of_tangent(x, graph, **kwargs)`

返回绘制曲线在特定 x 值处的切线斜率。

参数

- **x** ( _float_ ) – 切线必须接触曲线的 x 值。
- **graph** ( [_ParametricFunction_]() ) –[`ParametricFunction`]()要计算其正切的图。

返回

与 x 轴的切线的斜率。

返回类型

`float`

例子

```py
ax = Axes()
curve = ax.plot(lambda x: x**2)
ax.slope_of_tangent(x=-2, graph=curve)
# -3.5000000259052038
```

