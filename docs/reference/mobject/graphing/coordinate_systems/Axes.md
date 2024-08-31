# 轴

合格名称：`manim.mobject.graphing.coordinate\_systems.Axes`

```py
class Axes(x_range=None, y_range=None, x_length=12, y_length=6, axis_config=None, x_axis_config=None, y_axis_config=None, tips=True, **kwargs)
```

Bases: `VGroup`, `CoordinateSystem`

创建一组轴。

参数

- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – x 轴的值。`(x_min, x_max, x_step)`
- **y_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – y 轴的值。`(y_min, y_max, y_step)`
- **x_length** ( _float_ _|_ _None_ ) – x 轴的长度。
- **y_length** ( _float_ _|_ _None_ ) – y 轴的长度。
- **axis_config** ( _dict_ _|_ _None_ ) – 要传递给[`NumberLine`]()影响两个轴的参数。
- **x_axis_config** ( _dict_ _|_ _None_ ) – 传递给[`NumberLine`]()影响 x 轴的参数。
- **y_axis_config** ( _dict_ _|_ _None_ ) – 传递给[`NumberLine`]()影响 y 轴的参数。
- **Tips** ( _bool_ ) – 是否在两个轴上都包含提示。
- **kwargs** – 要传递给[`CoordinateSystem`]()和的附加参数[`VGroup`]()。

例子

示例：LogScalingExample 

![LogScalingExample-1.png](../../static/LogScalingExample-1.png)

```py
from manim import *

class LogScalingExample(Scene):
    def construct(self):
        ax = Axes(
            x_range=[0, 10, 1],
            y_range=[-2, 6, 1],
            tips=False,
            axis_config={"include_numbers": True},
            y_axis_config={"scaling": LogBase(custom_labels=True)},
        )

        # x_min must be > 0 because log is undefined at 0.
        graph = ax.plot(lambda x: x ** 2, x_range=[0.001, 10], use_smoothing=False)
        self.add(ax, graph)
```


样式参数可以传递给[`NumberLine`]() 表示轴的底层 mobject：

示例：AxesWithDifferentTips 

![AxesWithDifferentTips-1.png](../../static/AxesWithDifferentTips-1.png)

```py
from manim import *

class AxesWithDifferentTips(Scene):
    def construct(self):
        ax = Axes(axis_config={'tip_shape': StealthTip})
        self.add(ax)
```


方法

|||
|-|-|
[`coords_to_point`]()|接受来自轴的坐标并返回相对于场景的点。
[`get_axes`]()|获取轴。
[`get_axis_labels`]()|定义图表的 x 轴和 y 轴标签。
[`plot_line_graph`]()|绘制折线图。
[`point_to_coords`]()|接受场景中的一个点并返回其相对于轴的坐标。


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


`coords_to_point(*coords)`

接受来自轴的坐标并返回相对于场景的点。

参数

**coords** ( _float | Sequence[float] | Sequence[Sequence[float]] | np.ndarray_ ) –

该坐标。每个坐标作为单独的参数传递：。`ax.coords_to_point(1, 2, 3)`

还接受坐标列表

`ax.coords_to_point( [x_0, x_1, ...], [y_0, y_1, ...], ... )`

`ax.coords_to_point( [[x_0, y_0, z_0], [x_1, y_1, z_1]] )`

返回

相对于场景坐标系的点。数组的形状将与输入的形状相似。

返回类型

np.ndarray

例子

```py
from manim import Axes
import numpy as np
ax = Axes()
np.around(ax.coords_to_point(1, 0, 0), 2)
array([0.86, 0.  , 0.  ])
np.around(ax.coords_to_point([[0, 1], [1, 1], [1, 0]]), 2)
array([[0.  , 0.75, 0.  ],
       [0.86, 0.75, 0.  ],
       [0.86, 0.  , 0.  ]])
np.around(
    ax.coords_to_point([0, 1, 1], [1, 1, 0]), 2
)  # Transposed version of the above
array([[0.  , 0.86, 0.86],
       [0.75, 0.75, 0.  ],
       [0.  , 0.  , 0.  ]])
```


示例：CoordsToPointExample 

![CoordsToPointExample-1.png](../../static/CoordsToPointExample-1.png)

```py
from manim import *

class CoordsToPointExample(Scene):
    def construct(self):
        ax = Axes().add_coordinates()

        # a dot with respect to the axes
        dot_axes = Dot(ax.coords_to_point(2, 2), color=GREEN)
        lines = ax.get_lines_to_point(ax.c2p(2,2))

        # a dot with respect to the scene
        # the default plane corresponds to the coordinates of the scene.
        plane = NumberPlane()
        dot_scene = Dot((2,2,0), color=RED)

        self.add(plane, dot_scene, ax, dot_axes, lines)
```


`get_axes()`

获取轴。

返回

一对轴。

返回类型

[`VGroup`]()


`get_axis_labels(x_label='x', y_label='y')`

定义图表的 x 轴和 y 轴标签。

为了增强对标签位置的控制，请使用[`get_x_axis_label()`]()和 [`get_y_axis_label()`]()。

参数

- **x_label** ( _float_ _|_ _str_ _|_ [_Mobject_]() ) – x\_轴的标签。默认为[`MathTex`]()for`str`和`float`输入。
- **y_label** ( _float_ _|_ _str_ _|_ [_Mobject_]() ) – y 轴的标签。默认为[`MathTex`]()for`str`和`float`输入。

返回

[`VGroup`]()x_axis 和 y_axis 的标签。

返回类型

[`VGroup`]()



>也可以看看

> [`get_x_axis_label()`]() [`get_y_axis_label()`]()

例子

示例：GetAxisLabelsExample 

![GetAxisLabelsExample-1.png](../../static/GetAxisLabelsExample-1.png)

```py
from manim import *

class GetAxisLabelsExample(Scene):
    def construct(self):
        ax = Axes()
        labels = ax.get_axis_labels(
            Tex("x-axis").scale(0.7), Text("y-axis").scale(0.45)
        )
        self.add(ax, labels)
```


```py
plot_line_graph(x_values, y_values, z_values=None, line_color='#FFFF00', add_vertex_dots=True, vertex_dot_radius=0.08, vertex_dot_style=None, **kwargs)
```

绘制折线图。

`x_values`该图连接了 zipping 、`y_values`和形成的顶点 `z_values`。如果设置为，还会[`Dots`]()在顶点处添加。` add_vertex_dots``True `

参数

- **x_values** ( _Iterable_ _\[_ _float_ _\]_ ) – 沿 x 轴的可迭代值。
- **y_values** ( _Iterable_ _\[_ _float_ _\]_ ) – 沿 y 轴的可迭代值。
- **z_values** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 沿 z 轴的可迭代值（如果 z_values 为 None，则为零）。
- **line_color** ( _Color_ ) – 折线图的颜色。
- **add_vertex_dots** ( _bool_ ) – 是否[`Dot`]()在每个顶点添加。
- **vertex_dot_radius** ( _float_[`Dot`]() ) –每个顶点的半径。
- **vertex_dot_style** ( _dict_ _|_ _None_ ) – 要传递到[`Dot`]()每个顶点的样式参数。
- **kwargs** – 要传递到[`VMobject`]().

返回

包含线和点（如果指定）的 VDict。可以通过以下方式访问该线路：`line_graph["line_graph"]`。可以通过以下方式访问这些点：`line_graph["vertex_dots"]`。

返回类型

[`VDict`]()


例子

示例：LineGraph 示例

![LineGraphExample-1.png](../../static/LineGraphExample-1.png)

```py
from manim import *

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
            x_values = [0, 1.5, 2, 2.8, 4, 6.25],
            y_values = [1, 3, 2.25, 4, 2.5, 1.75],
            line_color=GOLD_E,
            vertex_dot_style=dict(stroke_width=3,  fill_color=PURPLE),
            stroke_width = 4,
        )
        self.add(plane, line_graph)
```


`point_to_coords(point)`

接受场景中的一个点并返回其相对于轴的坐标。

参数

**point** ( _Sequence_ _\[_ _float_ _\]_ ) – 点，即`RIGHT`或。还接受点列表作为。` [0, 1, 0]``[RIGHT, [0, 1, 0]] `

返回

轴上的坐标，即。或者如果点是点列表，则为坐标列表。`[4.0, 7.0]`

返回类型

np.ndarray[float]


例子

```py
from manim import Axes, RIGHT
import numpy as np
ax = Axes(x_range=[0, 10, 2])
np.around(ax.point_to_coords(RIGHT), 2)
array([5.83, 0.  ])
np.around(ax.point_to_coords([[0, 0, 1], [1, 0, 0]]), 2)
array([[5.  , 0.  ],
       [5.83, 0.  ]])
```


示例：PointToCoordsExample

![PointToCoordsExample-1.png](../../static/PointToCoordsExample-1.png)

```py
from manim import *

class PointToCoordsExample(Scene):
    def construct(self):
        ax = Axes(x_range=[0, 10, 2]).add_coordinates()
        circ = Circle(radius=0.5).shift(UR * 2)

        # get the coordinates of the circle with respect to the axes
        coords = np.around(ax.point_to_coords(circ.get_right()), decimals=2)

        label = (
            Matrix([[coords[0]], [coords[1]]]).scale(0.75).next_to(circ, RIGHT)
        )

        self.add(ax, circ, label, Dot(circ.get_right()))
```
