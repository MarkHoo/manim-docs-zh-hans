# 向量场景

合格名称：`manim.scene.vector\_space\_scene.VectorScene`

```py
class VectorScene(basis_vector_stroke_width=6, **kwargs)
```

Bases: `Scene`


方法

|||
|-|-|
[`add_axes`]()|将一对轴添加到场景中。
[`add_plane`]()|将 NumberPlane 对象添加到背景。
[`add_vector`]()|将向量添加到平面后返回向量。
[`coords_to_vector`]()|该方法将向量写为列矩阵（以下称为标签），逐一获取其中的值，并形成构成向量的 x 和 y 分量的相应行。
[`get_basis_vector_labels`]()|返回基本向量的命名标签。
[`get_basis_vectors`]()|返回基向量 (1,0) 和 (0,1) 的 VGroup
[`get_vector`]()|给定输入数值向量，返回平面上的箭头。
[`get_vector_label`]()|返回传递的向量的命名标签。
[`label_vector`]()|用于创建向量标签并为其添加动画的快捷方法。
[`lock_in_faded_grid`]()|此方法冻结已经在后台的 NumberPlane 和 Axes，并将新的、可操作的添加到前台。
`position_x_coordinate`|
`position_y_coordinate`|
[`show_ghost_movement`]()|此方法播放一个动画，部分显示整个平面沿特定向量的方向移动。
[`vector_to_coords`]()|此方法将向量显示为基于 Vector() 的向量，然后显示构成向量的 x 和 y 分量的相应线。
[`write_vector_coordinates`]()|将向量写入屏幕后，返回指示向量坐标的列矩阵。


属性

`camera`



`add_axes(animate=False, color='#FFFFFF', **kwargs)`

将一对轴添加到场景中。

参数

- **animate** ( _bool_ ) – 是否通过 Create 对轴的添加进行动画处理。
- **color** ( _bool_ ) – 轴的颜色。默认为白色。


`add_plane(animate=False, **kwargs)`

将 NumberPlane 对象添加到背景。

参数

- **animate** ( _bool_ ) – 是否通过 Create 为添加平面添加动画。
- **\*\*kwargs** – NumberPlane 接受的任何有效关键字参数。

返回

NumberPlane 对象。

返回类型

[NumberPlane]()


`add_vector(vector, color='#FFFF00', animate=True, **kwargs)`

将向量添加到平面后返回向量。

参数

- **vector** ( [_Arrow_]() _|_ _list_ _|_ _tuple_ _|_ _np.ndarray_ ) – 它可以是预先制作的图形向量，也可以是一个坐标。
- **color** ( _str_ ) – 向量的十六进制颜色的字符串。仅当“向量”不是箭头时才考虑这一点。默认为黄色。
- **animate** ( _bool_ ) – 是否使用 GrowArrow 对向量的相加进行动画处理
- \***\*kwargs** – Arrow 的任何有效关键字参数。仅当向量不是箭头时才考虑这些。

返回

代表向量的箭头。

返回类型

[Arrow]()


`coords_to_vector(vector, coords_start=array([2., 2., 0.]), clean_up=True)`

该方法将向量写为列矩阵（以下称为标签），逐一获取其中的值，并形成构成向量的 x 和 y 分量的相应行。然后，在屏幕上的线条之间创建基于 Vector() 的向量。

参数

- **vector** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要显示的向量。
- **coords_start** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 以数字方式显示向量的标签位置的起点。默认为 2 _ RIGHT + 2 _ UP 或 (2,2)
- **clean_up** ( _bool_ ) – 是否删除此方法完成后执行的任何操作。


`get_basis_vector_labels(**kwargs)`

返回基本向量的命名标签。

参数

**\*\*kwargs** –

get_vector_label 的任何有效关键字参数：

vector, label (str,MathTex) at_tip (bool=False), direction (str=”left”), rotate (bool), color (str), label_scale_factor=VECTOR_LABEL_SCALE_FACTOR (int, float),


`get_basis_vectors(i_hat_color='#83C167', j_hat_color='#FC6255')`

返回基向量 (1,0) 和 (0,1) 的 VGroup

参数

- **i_hat_color** ( _str_ ) – 用于 x 方向基本向量的十六进制颜色
- **j_hat_color** ( _str_ ) – 用于 y 方向基本向量的十六进制颜色

返回

表示基向量的向量 Mobject 的 VGroup。

返回类型

[VGroup]()



`get_vector(numerical_vector, **kwargs)`

给定输入数值向量，返回平面上的箭头。

参数

- **numeric_vector** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要绘制的向量。
- **\*\*kwargs** – Arrow 的任何有效关键字参数。

返回

代表向量的箭头。

返回类型

[Arrow]()


```py
get_vector_label(vector, label, at_tip=False, direction='left', rotate=False, color=None, label_scale_factor=0.8)
```

返回传递的向量的命名标签。

参数

- **vector**( [_Vector_]() ) – 要获取其标签的向量对象。
- **at_tip** ( _bool_ ) – 是否将标签放置在向量的顶端。
- **Direction** ( _str_ ) – 标签是否应位于向量的“左侧”或右侧。
- **rotate** ( _bool_ ) – 是否旋转它以与向量对齐。
- **color** ( _str_ _|_ _None_ ) – 标签的颜色。
- **label_scale_factor** ( _float_ ) – 标签缩放的程度。

返回

标签的 MathTex。

返回类型

[MathTex]()


`label_vector(vector, label, animate=True, **kwargs)`

用于创建向量标签并为其添加动画的快捷方法。

参数

- **vector**( [_Vector_]() ) – 必须添加标签的向量。
- **label** ( [_MathTex_]() _|_ _str_ ) – 标签的 MathTex/字符串。
- **animate** ( _bool_ ) – 是否使用 Write 对标签进行动画处理
- **\*\*kwargs** – get_vector_label 的任何有效关键字参数

返回

标签的 MathTex。

返回类型

[`MathTex`]()



`lock_in_faded_grid(dimness=0.7, axes_dimness=0.5)`

此方法冻结已经在后台的 NumberPlane 和 Axes，并将新的、可操作的添加到前台。

参数

- **dimness**( _float_ ) – NumberPlane 所需的暗度
- **axes_dimness** ( _float_ ) – 轴所需的暗度。


`show_ghost_movement(vector)`

此方法播放一个动画，部分显示整个平面沿特定向量的方向移动。当您希望传达在一个方向上移动整个平面而不实际移动平面的想法时，这非常有用。

参数

**vector** ( [_Arrow_]() _|_ _list_ _|_ _tuple_ _|_ _np.ndarray_ ) – 指示移动方向的向量。


`vector_to_coords(vector, integer_labels=True, clean_up=True)`

此方法将向量显示为基于 Vector() 的向量，然后显示构成向量的 x 和 y 分量的相应线。然后，在 Vector 头部附近创建一个列矩阵（以下称为标签）。

参数

- **vector** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要显示的向量。
- **integer_labels** ( _bool_ ) – 是否对显示的值进行四舍五入。向量标签中最接近的整数
- **clean_up** ( _bool_ ) – 是否删除此方法完成后执行的任何操作。


`write_vector_coordinates(vector, **kwargs)`

将向量写入屏幕后，返回指示向量坐标的列矩阵。

参数

- **vector**([_Arrow_]()) – 代表向量的箭头。
- \***\*kwargs** – 任何有效的关键字参数[`coordinate_label()`]()：

返回

表示向量的列矩阵。

返回类型

[`Matrix`]()
