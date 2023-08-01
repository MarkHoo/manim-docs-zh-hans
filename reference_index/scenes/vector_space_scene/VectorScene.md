# 矢量场景

合格名称：`manim.scene.vector\_space\_scene.VectorScene`

```py
class VectorScene(basis_vector_stroke_width=6, **kwargs)
```

Bases: Scene

方法

[`add_axes`]()

将一对轴添加到场景中。

[`add_plane`]()

将 NumberPlane 对象添加到背景。

[`add_vector`]()

将向量添加到平面后返回向量。

[`coords_to_vector`]()

该方法将向量写为列矩阵（以下称为标签），逐一获取其中的值，并形成构成向量的 x 和 y 分量的相应行。

[`get_basis_vector_labels`]()

返回基本向量的命名标签。

[`get_basis_vectors`]()

返回基向量 (1,0) 和 (0,1) 的 VGroup

[`get_vector`]()

给定输入数值向量，返回平面上的箭头。

[`get_vector_label`]()

返回传递的向量的命名标签。

[`label_vector`]()

用于创建矢量标签并为其添加动画的快捷方法。

[`lock_in_faded_grid`]()

此方法冻结已经在后台的 NumberPlane 和 Axes，并将新的、可操作的添加到前台。

`position_x_coordinate`

`position_y_coordinate`

[`show_ghost_movement`]()

此方法播放一个动画，部分显示整个平面沿特定向量的方向移动。

[`vector_to_coords`]()

此方法将向量显示为基于 Vector() 的向量，然后显示构成向量的 x 和 y 分量的相应线。

[`write_vector_coordinates`]()

将向量写入屏幕后，返回指示向量坐标的列矩阵。

属性

`camera`

add*axes (*动画= False* ,*颜色= '#FFFFFF'_ , _\\*\* kwargs\_ )

将一对轴添加到场景中。

参数

- **animate** ( _bool_ ) – 是否通过 Create 对轴的添加进行动画处理。
- **color** ( _bool_ ) – 轴的颜色。默认为白色。

add*plane (*动画= False* , *\\*\* kwargs\_ )

将 NumberPlane 对象添加到背景。

参数

- **animate** ( _bool_ ) – 是否通过 Create 为添加平面添加动画。
- \***\*kwargs** – NumberPlane 接受的任何有效关键字参数。

退货

NumberPlane 对象。

返回类型

[数字平面]()

add*vector（*向量*，*颜色= '#FFFF00'*，*动画= True*， *\\*\* kwargs\_）

将向量添加到平面后返回向量。

参数

- **vector** ( [_Arrow_]() _|_ _list_ _|_ _tuple_ _|_ _np.ndarray_ ) – 它可以是预先制作的图形向量，也可以是一个坐标。
- **color** ( _str_ ) – 向量的十六进制颜色的字符串。仅当“向量”不是箭头时才考虑这一点。默认为黄色。
- **animate** ( _bool_ ) – 是否使用 GrowArrow 对向量的相加进行动画处理
- \***\*kwargs** – Arrow 的任何有效关键字参数。仅当向量不是箭头时才考虑这些。

退货

代表向量的箭头。

返回类型

[箭]()

coords*to_vector (*向量*, \_coords_start = array(\[2., 2., 0.\])* , _clean_up = True_ )

该方法将向量写为列矩阵（以下称为标签），逐一获取其中的值，并形成构成向量的 x 和 y 分量的相应行。然后，在屏幕上的线条之间创建基于 Vector() 的向量。

参数

- **vector** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要显示的向量。
- **coords_start** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 以数字方式显示向量的标签位置的起点。默认为 2 _ RIGHT + 2 _ UP 或 (2,2)
- **clean_up** ( _bool_ ) – 是否删除此方法完成后执行的任何操作。

get_basis_vector*labels ( *\\*\* kwargs\_ )

返回基本向量的命名标签。

参数

\***\*夸格斯**–

get_vector_label 的任何有效关键字参数：

矢量、标签 (str,MathTex) at_tip (bool=False)、方向 (str=”left”)、旋转 (bool)、颜色 (str)、label_scale_factor=VECTOR_LABEL_SCALE_FACTOR (int, float)、

get*basis_vectors ( \_i_hat_color = '#83C167'* , _j_hat_color = '#FC6255'_ )

返回基向量 (1,0) 和 (0,1) 的 VGroup

参数

- **i_hat_color** ( _str_ ) – 用于 x 方向基本向量的十六进制颜色
- **j_hat_color** ( _str_ ) – 用于 y 方向基本向量的十六进制颜色

退货

表示基向量的向量 Mobject 的 VGroup。

返回类型

[V 组]()

获取向量（_数值向量_， _\*\* kwargs_）

给定输入数值向量，返回平面上的箭头。

参数

- **numeric_vector** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要绘制的向量。
- \***\*kwargs** – Arrow 的任何有效关键字参数。

退货

代表向量的箭头。

返回类型

[箭]()

get*vector_label (*向量*,*标签*, \_at_tip = False* ,_方向= 'left'_ ,_旋转= False_ ,_颜色= None_ , _label_scale_factor = 0.8_ )

返回传递的向量的命名标签。

参数

- **矢量**( [_Vector_]() ) – 要获取其标签的矢量对象。
- **at_tip** ( _bool_ ) – 是否将标签放置在向量的顶端。
- **Direction** ( _str_ ) – 标签是否应位于向量的“左侧”或右侧。
- **rotate** ( _bool_ ) – 是否旋转它以与向量对齐。
- **color** ( _str_ _|_ _None_ ) – 标签的颜色。
- **label_scale_factor** ( _float_ ) – 标签缩放的程度。

退货

标签的 MathTex。

返回类型

[数学文本]()

label*vector（*向量*，*标签*，*动画= True*， *\\*\* kwargs\_）

用于创建矢量标签并为其添加动画的快捷方法。

参数

- **矢量**( [_Vector_]() ) – 必须添加标签的矢量。
- **label** ( [_MathTex_]() _|_ _str_ ) – 标签的 MathTex/字符串。
- **animate** ( _bool_ ) – 是否使用 Write 对标签进行动画处理
- \***\*kwargs** – get_vector_label 的任何有效关键字参数

退货

标签的 MathTex。

返回类型

[`MathTex`]()

lock_in_faded*grid（*暗度= 0.7*， \_axes_dimness = 0.5*）

此方法冻结已经在后台的 NumberPlane 和 Axes，并将新的、可操作的添加到前台。

参数

- **暗度**( _float_ ) – NumberPlane 所需的暗度
- **axes_dimness** ( _float_ ) – 轴所需的暗度。

show*ghost_movement（*矢量\_）

此方法播放一个动画，部分显示整个平面沿特定向量的方向移动。当您希望传达在一个方向上移动整个平面而不实际移动平面的想法时，这非常有用。

参数

**vector** ( [_Arrow_]() _|_ _list_ _|_ _tuple_ _|_ _np.ndarray_ ) – 指示移动方向的向量。

vector*to_coords（*向量*， \_integer_labels = True*， _clean_up = True_）

此方法将向量显示为基于 Vector() 的向量，然后显示构成向量的 x 和 y 分量的相应线。然后，在 Vector 头部附近创建一个列矩阵（以下称为标签）。

参数

- **vector** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要显示的向量。
- **integer_labels** ( _bool_ ) – 是否对显示的值进行四舍五入。向量标签中最接近的整数
- **clean_up** ( _bool_ ) – 是否删除此方法完成后执行的任何操作。

write*向量*坐标（_向量_， _\*\* kwargs_）

将向量写入屏幕后，返回指示向量坐标的列矩阵。

参数

- **矢量**([_箭头_]()) – 代表矢量的箭头。
- \***\*kwargs** – 任何有效的关键字参数[`coordinate_label()`]()：

退货

表示向量的列矩阵。

返回类型

[`Matrix`]()
