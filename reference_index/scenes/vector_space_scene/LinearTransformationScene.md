# 线性变换场景

合格名称：`manim.scene.vector\_space\_scene.LinearTransformationScene`

```py
class LinearTransformationScene(include_background_plane=True, include_foreground_plane=True, background_plane_kwargs=None, foreground_plane_kwargs=None, show_coordinates=False, show_basis_vectors=True, basis_vector_stroke_width=6, i_hat_color='#83C167', j_hat_color='#FC6255', leave_ghost_vectors=False, **kwargs)
```

Bases: `VectorScene`

该场景包含特殊方法，使其特别适合显示线性变换。

参数

- **include_background_plane** ( _bool_ ) – 是否在场景中包含背景平面。
- **include_foreground_plane** ( _bool_ ) – 是否在场景中包含前景平面。
- **background_plane_kwargs** ( _dict_ _|_ _None_ ) – 要传递到`NumberPlane`调整背景平面的参数。
- **foreground_plane_kwargs** ( _dict_ _|_ _None_ ) – 要传递到`NumberPlane`调整前景平面的参数。
- **show_coordinates** ( _bool_ ) – 是否包含背景平面的坐标。
- **show_basis_vectors** ( _bool_ ) – 是否显示基础 x_axis ->`i_hat`和 y_axis ->`j_hat`向量。
- **basic_vector_lines_width** ( _float_ ) –`stroke_width`基础向量的宽度。
- **i_hat_color** ( _Color_ ) – 向量的颜色`i_hat`。
- **j_hat_color** ( _Color_ ) – 矢量的颜色`j_hat`。
- **leave_ghost_vectors** ( _bool_ ) – 指示变换后基向量的先前位置。


例子

示例：LinearTransformationSceneExample 

```py
from manim import *

class LinearTransformationSceneExample(LinearTransformationScene):
    def __init__(self):
        LinearTransformationScene.__init__(
            self,
            show_coordinates=True,
            leave_ghost_vectors=True,
        )

    def construct(self):
        matrix = [[1, 1], [0, 1]]
        self.apply_matrix(matrix)
        self.wait()
```


方法

|||
|-|-|
[`add_background_mobject`]()|将 mobject 添加到特殊列表 self.background_mobjects。
[`add_foreground_mobject`]()|将 mobject 添加到特殊列表 self.foreground_mobjects。
[`add_moving_mobject`]()|将 mobject 添加到特殊列表 self.movi​​ng_mobject，并向 mobject 添加一个名为 mobject.target 的属性，该属性跟踪 mobject 将移动到什么或变成什么等。
[`add_special_mobjects`]()|如果这些 mobject 具有额外的重要性，则将 mobject 添加到可以跟踪的单独列表中。
[`add_title`]()|添加一个标题，缩放后，添加一个背景矩形，将其移动到顶部并将其添加到 foreground_mobjects，将其添加为 self 的局部变量。
[`add_transformable_label`]()|创建向量的可变形标签并为其添加动画的方法。
[`add_transformable_mobject`]()|将 mobject 添加到特殊列表 self.transformable_mobjects。
[`add_unit_square`]()|通过 self.get_unit_square 将单位方块添加到场景中。
[`add_vector`]()|将向量添加到场景中，并将其放入特殊列表 self.movi​​ng_vectors 中。
[`apply_function`]()|将给定的函数应用于 self.transformable_mobjects 中的每个 mobject，并播放显示此效果的动画。
[`apply_inverse`]()|此方法将由传递的矩阵的逆表示的线性变换应用于数平面及其上的每个向量/相似对象。
[`apply_inverse_transpose`]()|将给定转置矩阵表示的变换的逆应用于数平面及其上的每个向量/相似对象。
[`apply_matrix`]()|将给定矩阵表示的变换应用于数平面及其上的每个向量/相似对象。
[`apply_nonlinear_transformation`]()|将给定函数表示的非线性变换应用于数平面及其上的每个向量/相似对象。
[`apply_transposed_matrix`]()|将给定转置矩阵表示的变换应用于数字平面及其上的每个向量/相似对象。
[`get_matrix_transformation`]()|返回与传递的矩阵表示的线性变换相对应的函数。
[`get_moving_mobject_movement`]()|此方法返回一个动画，将“self.movi​​ng_mobjects”中的 mobject 移动到其相应的 .target 值。
[`get_piece_movement`]()|此方法返回一个动画，该动画将任意 mobject 以“片段”形式移动到其相应的 .target 值。
[`get_transformable_label_movement`]()|此方法返回一个动画，将“self.transformable_labels”中的所有标签移动到其相应的 .target 。
[`get_transposed_matrix_transformation`]()|返回与传递的转置矩阵表示的线性变换相对应的函数。
[`get_unit_square`]()|返回当前 NumberPlane 的单位正方形。
[`get_vector_movement`]()|此方法返回一个动画，该动画将“self.movi​​ng_vectors”中的 mobject 移动到其相应的 .target 值。
[`setup`]()|这意味着由通常子类化的任何场景来实现，并且在调用构造方法之前涉及一些常见的设置。
`update_default_configs`|
[`write_vector_coordinates`]()|将向量写入屏幕并将其添加到特殊列表 self.foreground_mobjects 后，返回一个指示向量坐标的列矩阵



属性

`camera`


add*background_mobject ( *\\* mobjects\_ )

将 mobject 添加到特殊列表 self.background_mobjects。

参数

**\*mobjects** ( [_Mobject_]() ) – 要添加到列表中的 mobject。

add*foreground_mobject ( *\\* mobjects\_ )

将 mobject 添加到特殊列表 self.foreground_mobjects。

参数

**\*mobjects** ( [_Mobject_]() ) – 要添加到列表的 mobject

add*moving_mobject ( \_mobject* , _target_mobject = None_ )

将 mobject 添加到特殊列表 self.movi​​ng_mobject，并向 mobject 添加一个名为 mobject.target 的属性，该属性跟踪 mobject 将移动到什么或变成什么等。

参数

- **mobject** ( [_Mobject_]() ) – 要添加到列表的 mobject
- **target_mobject** ( [_Mobject_]() _|_ _None_ ) – moving_mobject 的去向等。

add*special_mobjects ( \_mob_list* , _\* mob_to_add_ )

如果这些 mobject 具有额外的重要性，则将 mobject 添加到可以跟踪的单独列表中。

参数

- **mob_list** ( _list_ ) – 您想要添加这些 mobject 的特殊列表。
- **\*mobs_to_add** ( [_Mobject_]() ) – 要添加的 mobject。

add*title（*标题*， \_scale_factor = 1.5*， _animate = False_）

添加一个标题，缩放后，添加一个背景矩形，将其移动到顶部并将其添加到 foreground_mobjects，将其添加为 self 的局部变量。返回场景。

参数

- **title** ( _str_ _|_ [_MathTex_]() _|_ [_Tex_]() ) – 标题应该是什么。
- **scale_factor** ( _float_ ) – 标题应缩放多少。
- **animate** ( _bool_ ) – 是否为添加添加动画。

返回

添加了标题的场景。

返回类型

[线性变换场景]()

add*transformable_label（*向量*，*标签*， \\_transformation_name = 'L'*， _new_label = None_， _\*\* kwargs_）

创建向量的可变形标签并为其添加动画的方法。

参数

- **矢量**( [_Vector_]() ) – 必须添加标签的矢量。
- **label** ( [_MathTex_]() _|_ _str_ ) – 标签的 MathTex/字符串。
- **conversion_name** ( _str_ _|_ [_MathTex_]() ) – 为转换提供标签的名称。
- **new_label** ( _str_ _|_ [_MathTex_]() _|_ _None_ ) – 线性变换后标签应显示的内容
- \***\*kwargs** – get_vector_label 的任何有效关键字参数

返回

标签的 MathTex。

返回类型

[`MathTex`]()

add*transformable_mobject ( *\\* mobjects\_ )

将 mobject 添加到特殊列表 self.transformable_mobjects。

参数

**\*mobjects** ( [_Mobject_]() ) – 要添加到列表中的 mobject。

add*unit_square (*动画= False* , *\\*\* kwargs\_ )

通过 self.get_unit_square 将单位方块添加到场景中。

参数

- **animate** ( _bool_ ) – 是否使用 DrawBorderThenFill 为添加添加动画。
- \***\*kwargs** – self.get_unit_square() 的任何有效关键字参数

返回

单位正方形。

返回类型

[正方形]()

add*vector（*矢量*，*颜色= '#FFFF00'_， _\\*\* kwargs\_）

将向量添加到场景中，并将其放入特殊列表 self.movi​​ng_vectors 中。

参数

- **vector** ( [_Arrow_]() _|_ _list_ _|_ _tuple_ _|_ _np.ndarray_ ) – 它可以是预先制作的图形向量，也可以是一个坐标。
- **color** ( _str_ ) – 向量的十六进制颜色的字符串。仅当“向量”不是箭头时才考虑这一点。默认为黄色。
- \***\*kwargs** – VectorScene.add_vector 的任何有效关键字参数。

返回

代表向量的箭头。

返回类型

[箭]()

apply*function（*函数*， \_added_anims = \[\]*， _\\*\* kwargs_）

将给定的函数应用于 self.transformable_mobjects 中的每个 mobject，并播放显示此效果的动画。

参数

- **function** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 影响 self.transformable_mobjects 中每个 mobject 的每个点的函数。
- **selected_anims** ( _list_ ) – 需要与此同时播放的任何其他动画。
- \***\*kwargs** – self.play() 调用的任何有效关键字参数。

apply*inverse（*矩阵*， *\\*\* kwargs\_）

此方法将由传递的矩阵的逆表示的线性变换应用于数平面及其上的每个向量/相似对象。

参数

- **Matrix** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要应用其逆矩阵。
- \***\*kwargs** – self.apply_matrix() 的任何有效关键字参数

apply*inverse_transpose ( \_t_matrix* , _\*\* kwargs_ )

将给定转置矩阵表示的变换的逆应用于数平面及其上的每个向量/相似对象。

参数

- **t_matrix** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 矩阵。
- \***\*kwargs** – self.apply_transpose_matrix() 的任何有效关键字参数

apply*matrix (*矩阵*, *\\*\* kwargs\_ )

将给定矩阵表示的变换应用于数平面及其上的每个向量/相似对象。

参数

- **矩阵**( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 矩阵。
- \***\*kwargs** – self.apply_transpose_matrix() 的任何有效关键字参数

apply*nonlinear_transformation（*函数*， *\\*\* kwargs\_）

将给定函数表示的非线性变换应用于数平面及其上的每个向量/相似对象。

参数

- **function** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 函数。
- \***\*kwargs** – self.apply_function() 的任何有效关键字参数

apply*transpose_matrix (*转置矩阵*, *\\*\* kwargs\_ )

将给定转置矩阵表示的变换应用于数字平面及其上的每个向量/相似对象。

参数

- **transpose_matrix** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 矩阵。
- \***\*kwargs** – self.apply_function() 的任何有效关键字参数

获取矩阵变换（_矩阵_）

返回与传递的矩阵表示的线性变换相对应的函数。

参数

**矩阵**( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 矩阵。

get_moving_mobject*movement ( \_func* )

此方法返回一个动画，将“self.movi​​ng_mobjects”中的 mobject 移动到其相应的 .target 值。func 是一个确定 .target 去向的函数。

参数

**func** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 确定移动对象的 .target 去向的函数。

返回

运动的动画。

返回类型

[动画片]()

get*piece_movement (*件\_)

此方法返回一个动画，该动画将任意 mobject 以“片段”形式移动到其相应的 .target 值。如果 self.leave_ghost_vectors 为 True，则原始位置/mobject 的重影将留在屏幕上

参数

**pieces** ( _list_ _|_ _tuple_ _|_ _np.ndarray_ ) – 必须显示运动的棋子。

返回

运动的动画。

返回类型

[动画片]()

get_transformable_label_movement ( )

此方法返回一个动画，将“self.transformable_labels”中的所有标签移动到其相应的 .target 。

返回

运动的动画。

返回类型

[动画片]()

获取转置矩阵变换（_转置矩阵_）

返回与传递的转置矩阵表示的线性变换相对应的函数。

参数

**transpose_matrix** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 矩阵。

get*unit_square（*颜色= '#FFFF00'*，*不透明度= 0.3*，\*描边宽度= 3\_）

返回当前 NumberPlane 的单位正方形。

参数

- **color** ( _str_ ) – 所需颜色的十六进制颜色代码的字符串。
- **opacity** ( _float_ ) – 正方形的不透明度
- **stroke_width** ( _float_ ) – 正方形边框的描边宽度（以像素为单位）

返回类型

[正方形]()

获取向量运动（_函数_）

此方法返回一个动画，将“self.movi​​ng_vectors”中的 mobject 移动到其相应的 .target 值。func 是一个确定 .target 去向的函数。

参数

**func** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 确定移动对象的 .target 去向的函数。

返回

运动的动画。

返回类型

[动画片]()

设置( )

这意味着由通常子类化的任何场景来实现，并且在调用构造方法之前涉及一些常见的设置。

write*向量*坐标（_向量_， _\*\* kwargs_）

将向量写入屏幕并将其添加到特殊列表 self.foreground_mobjects 后，返回一个指示向量坐标的列矩阵

参数

- **矢量**([_箭头_]()) – 代表矢量的箭头。
- \***\*kwargs** – VectorScene.write_vector_coordinates 的任何有效关键字参数

返回

表示向量的列矩阵。

返回类型

[矩阵]()
