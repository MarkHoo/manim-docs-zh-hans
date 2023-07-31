# 矢量场景[#](#vectorscene "此标题的固定链接")

合格名称：`manim.scene.vector\_space\_scene.VectorScene`

_类_ VectorScene ( _basic_vector_lines_width = 6_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene)[#](#manim.scene.vector_space_scene.VectorScene "此定义的固定链接")

基地：[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")

方法

[`add_axes`](#manim.scene.vector_space_scene.VectorScene.add_axes "manim.scene.vector_space_scene.VectorScene.add_axes")

将一对轴添加到场景中。

[`add_plane`](#manim.scene.vector_space_scene.VectorScene.add_plane "manim.scene.vector_space_scene.VectorScene.add_plane")

将 NumberPlane 对象添加到背景。

[`add_vector`](#manim.scene.vector_space_scene.VectorScene.add_vector "manim.scene.vector_space_scene.VectorScene.add_vector")

将向量添加到平面后返回向量。

[`coords_to_vector`](#manim.scene.vector_space_scene.VectorScene.coords_to_vector "manim.scene.vector_space_scene.VectorScene.coords_to_vector")

该方法将向量写为列矩阵（以下称为标签），逐一获取其中的值，并形成构成向量的 x 和 y 分量的相应行。

[`get_basis_vector_labels`](#manim.scene.vector_space_scene.VectorScene.get_basis_vector_labels "manim.scene.vector_space_scene.VectorScene.get_basis_vector_labels")

返回基本向量的命名标签。

[`get_basis_vectors`](#manim.scene.vector_space_scene.VectorScene.get_basis_vectors "manim.scene.vector_space_scene.VectorScene.get_basis_vectors")

返回基向量 (1,0) 和 (0,1) 的 VGroup

[`get_vector`](#manim.scene.vector_space_scene.VectorScene.get_vector "manim.scene.vector_space_scene.VectorScene.get_vector")

给定输入数值向量，返回平面上的箭头。

[`get_vector_label`](#manim.scene.vector_space_scene.VectorScene.get_vector_label "manim.scene.vector_space_scene.VectorScene.get_vector_label")

返回传递的向量的命名标签。

[`label_vector`](#manim.scene.vector_space_scene.VectorScene.label_vector "manim.scene.vector_space_scene.VectorScene.label_vector")

用于创建矢量标签并为其添加动画的快捷方法。

[`lock_in_faded_grid`](#manim.scene.vector_space_scene.VectorScene.lock_in_faded_grid "manim.scene.vector_space_scene.VectorScene.lock_in_faded_grid")

此方法冻结已经在后台的 NumberPlane 和 Axes，并将新的、可操作的添加到前台。

`position_x_coordinate`

`position_y_coordinate`

[`show_ghost_movement`](#manim.scene.vector_space_scene.VectorScene.show_ghost_movement "manim.scene.vector_space_scene.VectorScene.show_ghost_movement")

此方法播放一个动画，部分显示整个平面沿特定向量的方向移动。

[`vector_to_coords`](#manim.scene.vector_space_scene.VectorScene.vector_to_coords "manim.scene.vector_space_scene.VectorScene.vector_to_coords")

此方法将向量显示为基于 Vector() 的向量，然后显示构成向量的 x 和 y 分量的相应线。

[`write_vector_coordinates`](#manim.scene.vector_space_scene.VectorScene.write_vector_coordinates "manim.scene.vector_space_scene.VectorScene.write_vector_坐标")

将向量写入屏幕后，返回指示向量坐标的列矩阵。

属性

`camera`

add*axes (*动画= False* ,*颜色= '#FFFFFF'_ , _\*\* kwargs\_ )[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.add_axes)[#](#manim.scene.vector_space_scene.VectorScene.add_axes "此定义的固定链接")

将一对轴添加到场景中。

参数

- **animate** ( _bool_ ) – 是否通过 Create 对轴的添加进行动画处理。
- **color** ( _bool_ ) – 轴的颜色。默认为白色。

add*plane (*动画= False* , *\*\* kwargs\_ )[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.add_plane)[#](#manim.scene.vector_space_scene.VectorScene.add_plane "此定义的固定链接")

将 NumberPlane 对象添加到背景。

参数

- **animate** ( _bool_ ) – 是否通过 Create 为添加平面添加动画。
- \***\*kwargs** – NumberPlane 接受的任何有效关键字参数。

退货

NumberPlane 对象。

返回类型

[数字平面](manim.mobject.graphing.coordinate_systems.NumberPlane.html#manim.mobject.graphing.coordinate_systems.NumberPlane "manim.mobject.graphing.coordinate_systems.NumberPlane")

add*vector（*向量*，*颜色= '#FFFF00'*，*动画= True*， *\*\* kwargs\_）[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.add_vector)[#](#manim.scene.vector_space_scene.VectorScene.add_vector "此定义的固定链接")

将向量添加到平面后返回向量。

参数

- **vector** ( [_Arrow_](manim.mobject.geometry.line.Arrow.html#manim.mobject.geometry.line.Arrow "manim.mobject.geometry.line.Arrow") _|_ _list_ _|_ _tuple_ _|_ _np.ndarray_ ) – 它可以是预先制作的图形向量，也可以是一个坐标。
- **color** ( _str_ ) – 向量的十六进制颜色的字符串。仅当“向量”不是箭头时才考虑这一点。默认为黄色。
- **animate** ( _bool_ ) – 是否使用 GrowArrow 对向量的相加进行动画处理
- \***\*kwargs** – Arrow 的任何有效关键字参数。仅当向量不是箭头时才考虑这些。

退货

代表向量的箭头。

返回类型

[箭](manim.mobject.geometry.line.Arrow.html#manim.mobject.geometry.line.Arrow "manim.mobject.geometry.line.Arrow")

coords*to_vector (*向量*, \_coords_start = array(\[2., 2., 0.\])* , _clean_up = True_ )[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.coords_to_vector)[#](#manim.scene.vector_space_scene.VectorScene.coords_to_vector "此定义的固定链接")

该方法将向量写为列矩阵（以下称为标签），逐一获取其中的值，并形成构成向量的 x 和 y 分量的相应行。然后，在屏幕上的线条之间创建基于 Vector() 的向量。

参数

- **vector** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要显示的向量。
- **coords_start** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 以数字方式显示向量的标签位置的起点。默认为 2 _ RIGHT + 2 _ UP 或 (2,2)
- **clean_up** ( _bool_ ) – 是否删除此方法完成后执行的任何操作。

get_basis_vector*labels ( *\*\* kwargs\_ )[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.get_basis_vector_labels)[#](#manim.scene.vector_space_scene.VectorScene.get_basis_vector_labels "此定义的固定链接")

返回基本向量的命名标签。

参数

\***\*夸格斯**–

get_vector_label 的任何有效关键字参数：

矢量、标签 (str,MathTex) at_tip (bool=False)、方向 (str=”left”)、旋转 (bool)、颜色 (str)、label_scale_factor=VECTOR_LABEL_SCALE_FACTOR (int, float)、

get*basis_vectors ( \_i_hat_color = '#83C167'* , _j_hat_color = '#FC6255'_ )[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.get_basis_vectors)[#](#manim.scene.vector_space_scene.VectorScene.get_basis_vectors "此定义的固定链接")

返回基向量 (1,0) 和 (0,1) 的 VGroup

参数

- **i_hat_color** ( _str_ ) – 用于 x 方向基本向量的十六进制颜色
- **j_hat_color** ( _str_ ) – 用于 y 方向基本向量的十六进制颜色

退货

表示基向量的向量 Mobject 的 VGroup。

返回类型

[V 组](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

获取向量（_数值向量_， _\*\* kwargs_）[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.get_vector)[#](#manim.scene.vector_space_scene.VectorScene.get_vector "此定义的固定链接")

给定输入数值向量，返回平面上的箭头。

参数

- **numeric_vector** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要绘制的向量。
- \***\*kwargs** – Arrow 的任何有效关键字参数。

退货

代表向量的箭头。

返回类型

[箭](manim.mobject.geometry.line.Arrow.html#manim.mobject.geometry.line.Arrow "manim.mobject.geometry.line.Arrow")

get*vector_label (*向量*,*标签*, \_at_tip = False* ,_方向= 'left'_ ,_旋转= False_ ,_颜色= None_ , _label_scale_factor = 0.8_ )[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.get_vector_label)[#](#manim.scene.vector_space_scene.VectorScene.get_vector_label "此定义的固定链接")

返回传递的向量的命名标签。

参数

- **矢量**( [_Vector_](manim.mobject.geometry.line.Vector.html#manim.mobject.geometry.line.Vector "manim.mobject.geometry.line.Vector") ) – 要获取其标签的矢量对象。
- **at_tip** ( _bool_ ) – 是否将标签放置在向量的顶端。
- **Direction** ( _str_ ) – 标签是否应位于向量的“左侧”或右侧。
- **rotate** ( _bool_ ) – 是否旋转它以与向量对齐。
- **color** ( _str_ _|_ _None_ ) – 标签的颜色。
- **label_scale_factor** ( _float_ ) – 标签缩放的程度。

退货

标签的 MathTex。

返回类型

[数学文本](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")

label*vector（*向量*，*标签*，*动画= True*， *\*\* kwargs\_）[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.label_vector)[#](#manim.scene.vector_space_scene.VectorScene.label_vector "此定义的固定链接")

用于创建矢量标签并为其添加动画的快捷方法。

参数

- **矢量**( [_Vector_](manim.mobject.geometry.line.Vector.html#manim.mobject.geometry.line.Vector "manim.mobject.geometry.line.Vector") ) – 必须添加标签的矢量。
- **label** ( [_MathTex_](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex") _|_ _str_ ) – 标签的 MathTex/字符串。
- **animate** ( _bool_ ) – 是否使用 Write 对标签进行动画处理
- \***\*kwargs** – get_vector_label 的任何有效关键字参数

退货

标签的 MathTex。

返回类型

[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")

lock_in_faded*grid（*暗度= 0.7*， \_axes_dimness = 0.5*）[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.lock_in_faded_grid)[#](#manim.scene.vector_space_scene.VectorScene.lock_in_faded_grid "此定义的固定链接")

此方法冻结已经在后台的 NumberPlane 和 Axes，并将新的、可操作的添加到前台。

参数

- **暗度**( _float_ ) – NumberPlane 所需的暗度
- **axes_dimness** ( _float_ ) – 轴所需的暗度。

show*ghost_movement（*矢量\_）[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.show_ghost_movement)[#](#manim.scene.vector_space_scene.VectorScene.show_ghost_movement "此定义的固定链接")

此方法播放一个动画，部分显示整个平面沿特定向量的方向移动。当您希望传达在一个方向上移动整个平面而不实际移动平面的想法时，这非常有用。

参数

**vector** ( [_Arrow_](manim.mobject.geometry.line.Arrow.html#manim.mobject.geometry.line.Arrow "manim.mobject.geometry.line.Arrow") _|_ _list_ _|_ _tuple_ _|_ _np.ndarray_ ) – 指示移动方向的向量。

vector*to_coords（*向量*， \_integer_labels = True*， _clean_up = True_）[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.vector_to_coords)[#](#manim.scene.vector_space_scene.VectorScene.vector_to_coords "此定义的固定链接")

此方法将向量显示为基于 Vector() 的向量，然后显示构成向量的 x 和 y 分量的相应线。然后，在 Vector 头部附近创建一个列矩阵（以下称为标签）。

参数

- **vector** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要显示的向量。
- **integer_labels** ( _bool_ ) – 是否对显示的值进行四舍五入。向量标签中最接近的整数
- **clean_up** ( _bool_ ) – 是否删除此方法完成后执行的任何操作。

write*向量*坐标（_向量_， _\*\* kwargs_）[\[来源\]](../_modules/manim/scene/vector_space_scene.html#VectorScene.write_vector_coordinates)[#](#manim.scene.vector_space_scene.VectorScene.write_vector_coordinates "此定义的固定链接")

将向量写入屏幕后，返回指示向量坐标的列矩阵。

参数

- **矢量**([_箭头_](manim.mobject.geometry.line.Arrow.html#manim.mobject.geometry.line.Arrow "manim.mobject.geometry.line.Arrow")) – 代表矢量的箭头。
- \***\*kwargs** – 任何有效的关键字参数[`coordinate_label()`](manim.mobject.geometry.line.Vector.html#manim.mobject.geometry.line.Vector.coordinate_label "manim.mobject.geometry.line.Vector.coordinate_label")：

退货

表示向量的列矩阵。

返回类型

[`Matrix`](manim.mobject.matrix.Matrix.html#manim.mobject.matrix.Matrix "manim.mobject.matrix.Matrix")
