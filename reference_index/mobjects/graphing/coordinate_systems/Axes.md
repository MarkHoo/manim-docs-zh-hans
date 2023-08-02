# 轴

合格名称：`manim.mobject.graphing.coordinate\_systems.Axes`

```py

```

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

![LogScalingExample-1.png](../static/LogScalingExample-1.png)

```py

```


样式参数可以传递给[`NumberLine`]() 表示轴的底层 mobject：

示例：AxesWithDifferentTips 

![AxesWithDifferentTips-1.png](../static/AxesWithDifferentTips-1.png)

```py

```


方法

[`coords_to_point`]()

接受来自轴的坐标并返回相对于场景的点。

[`get_axes`]()

获取轴。

[`get_axis_labels`]()

定义图表的 x 轴和 y 轴标签。

[`plot_line_graph`]()

绘制折线图。

[`point_to_coords`]()

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

坐标到点( _\*坐标_)

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

```py

```


示例：CoordsToPointExample 

![CoordsToPointExample-1.png](../static/CoordsToPointExample-1.png)

```py

```

获取轴( )

获取轴。

退货

一对轴。

返回类型

[`VGroup`]()

get*axis_labels ( \_x_label = 'x'* , _y_label = 'y'_ )

定义图表的 x 轴和 y 轴标签。

为了增强对标签位置的控制，请使用[`get_x_axis_label()`]()和 [`get_y_axis_label()`]()。

参数

- **x_label** ( _float_ _|_ _str_ _|_ [_Mobject_]() ) – x\_轴的标签。默认为[`MathTex`]()for`str`和`float`输入。
- **y_label** ( _float_ _|_ _str_ _|_ [_Mobject_]() ) – y 轴的标签。默认为[`MathTex`]()for`str`和`float`输入。

退货

[`VGroup`]()x_axis 和 y_axis 的标签。

返回类型

[`VGroup`]()

也可以看看

[`get_x_axis_label()`]() [`get_y_axis_label()`]()

例子

示例：GetAxisLabelsExample 

![GetAxisLabelsExample-1.png](../static/GetAxisLabelsExample-1.png)

```py

```


plot*line_graph ( \_x_values* , _y_values_ , _z_values = None_ , _line_color = '#FFFF00'_ , _add_vertex_dots = True_ , _vertex_dot_radius = 0.08_ , _vertex_dot_style = None_ , _\*\* kwargs_ )

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

退货

包含线和点（如果指定）的 VDict。可以通过以下方式访问该线路：`line_graph["line_graph"]`。可以通过以下方式访问这些点：`line_graph["vertex_dots"]`。

返回类型

[`VDict`]()

例子

示例：LineGraph 示例

![LineGraphExample-1.png](../static/LineGraphExample-1.png)

```py

```


点到坐标（_点_）

接受场景中的一个点并返回其相对于轴的坐标。

参数

**point** ( _Sequence_ _\[_ _float_ _\]_ ) – 点，即`RIGHT`或。还接受点列表作为。` [0, 1, 0]``[RIGHT, [0, 1, 0]] `

退货

轴上的坐标，即。或者如果点是点列表，则为坐标列表。`[4.0, 7.0]`

返回类型

np.ndarray\[浮点数\]

例子

```py

```


示例：PointToCoordsExample

![PointToCoordsExample-1.png](../static/PointToCoordsExample-1.png)

```py

```
