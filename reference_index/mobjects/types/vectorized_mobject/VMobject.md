# VMobject

合格名称：`manim.mobject.types.vectorized\_mobject.VMobject`


```py

```

矢量化对象。

参数

- **background_lines_color** – 背景描边的目的是使某些内容不会重叠填充，例如针对某些纹理背景的文本。
- **sheen_factor** – 当设置颜色 c 时，将通过使用 sheen_factor 将 c 插值到白色计算出第二种颜色，并且显示将在 sheen_direction 方向上渐变到该第二种颜色。
- **close_new_points** – 表示它不会显示，但它应该计入父对象的路径中
- **tolerance_for_point_equality** – 这是在一个像素内
- **joint_type** ( [_LineJointType_](manim.constants.LineJointType.html#manim.constants.LineJointType "manim.constants.LineJointType") _|_ _None_ ) – 用于连接此矢量化 mobject 的曲线段的线接头类型。请参阅[`LineJointType`](manim.constants.LineJointType.html#manim.constants.LineJointType "manim.constants.LineJointType") 参考资料 选项。

方法

`add_cubic_bezier_curve`

[`add_cubic_bezier_curve_to`](#manim.mobject.types.vectorized_mobject.VMobject.add_cubic_bezier_curve_to "manim.mobject.types.vectorized_mobject.VMobject.add_cubic_bezier_curve_to")

将三次贝塞尔曲线添加到路径中。

`add_cubic_bezier_curves`

[`add_line_to`](#manim.mobject.types.vectorized_mobject.VMobject.add_line_to "manim.mobject.types.vectorized_mobject.VMobject.add_line_to")

添加一条从 VMobject 的最后一个点到给定点的直线。

`add_points_as_corners`

[`add_quadratic_bezier_curve_to`](#manim.mobject.types.vectorized_mobject.VMobject.add_quadratic_bezier_curve_to "manim.mobject.types.vectorized_mobject.VMobject.add_quadratic_bezier_curve_to")

将二次贝塞尔曲线添加到路径中。

[`add_smooth_curve_to`](#manim.mobject.types.vectorized_mobject.VMobject.add_smooth_curve_to "manim.mobject.types.vectorized_mobject.VMobject.add_smooth_curve_to")

从给定点创建平滑曲线并将其添加到 VMobject。

`add_subpath`

[`align_points`](#manim.mobject.types.vectorized_mobject.VMobject.align_points "manim.mobject.types.vectorized_mobject.VMobject.align_points")

向 self 和 vmobject 添加点，以便它们都具有相同数量的子路径，并且每个相应的子路径都包含相同数量的点。

`align_rgbas`

`append_points`

`append_vectorized_mobject`

`apply_function`

[`change_anchor_mode`](#manim.mobject.types.vectorized_mobject.VMobject.change_anchor_mode "manim.mobject.types.vectorized_mobject.VMobject.change_anchor_mode")

更改贝塞尔曲线的锚定模式。

`clear_points`

`close_path`

`color_using_background_image`

`consider_points_equals`

[`consider_points_equals_2d`](#manim.mobject.types.vectorized_mobject.VMobject.consider_points_equals_2d "manim.mobject.types.vectorized_mobject.VMobject.consider_points_equals_2d")

确定两个点是否足够接近以被视为相等。

`fade`

[`force_direction`](#manim.mobject.types.vectorized_mobject.VMobject.force_direction "manim.mobject.types.vectorized_mobject.VMobject.force_direction")

确保点的方向是顺时针或逆时针。

[`gen_cubic_bezier_tuples_from_points`](#manim.mobject.types.vectorized_mobject.VMobject.gen_cubic_bezier_tuples_from_points "manim.mobject.types.vectorized_mobject.VMobject.gen_cubic_bezier_tuples_from_points")

从点数组返回贝塞尔曲线元组。

`gen_subpaths_from_points_2d`

[`generate_rgbas_array`](#manim.mobject.types.vectorized_mobject.VMobject.generate_rgbas_array "manim.mobject.types.vectorized_mobject.VMobject.generate_rgbas_array")

第一个 arg 可以是颜色，也可以是颜色元组/列表。

[`get_anchors`](#manim.mobject.types.vectorized_mobject.VMobject.get_anchors "manim.mobject.types.vectorized_mobject.VMobject.get_anchors")

返回形成 VMobject 的曲线的锚点。

[`get_anchors_and_handles`](#manim.mobject.types.vectorized_mobject.VMobject.get_anchors_and_handles "manim.mobject.types.vectorized_mobject.VMobject.get_anchors_and_handles")

返回 anchors1、handles1、handles2、anchors2，其中 (anchors1\[i\]、handles1\[i\]、handles2\[i\]、anchors2\[i\]) 是为 range(0, len(锚 1))

[`get_arc_length`](#manim.mobject.types.vectorized_mobject.VMobject.get_arc_length "manim.mobject.types.vectorized_mobject.VMobject.get_arc_length")

返回整条曲线的近似长度。

`get_background_image`

[`get_color`](#manim.mobject.types.vectorized_mobject.VMobject.get_color "manim.mobject.types.vectorized_mobject.VMobject.get_color")

返回的颜色[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

`get_cubic_bezier_tuples`

`get_cubic_bezier_tuples_from_points`

[`get_curve_functions`](#manim.mobject.types.vectorized_mobject.VMobject.get_curve_functions "manim.mobject.types.vectorized_mobject.VMobject.get_curve_functions")

获取 mobject 曲线的函数。

[`get_curve_functions_with_lengths`](#manim.mobject.types.vectorized_mobject.VMobject.get_curve_functions_with_lengths "manim.mobject.types.vectorized_mobject.VMobject.get_curve_functions_with_lengths")

获取 mobject 的函数和曲线长度。

[`get_direction`](#manim.mobject.types.vectorized_mobject.VMobject.get_direction "manim.mobject.types.vectorized_mobject.VMobject.get_direction")

用于[`shoelace_direction()`](manim.utils.space_ops.html#manim.utils.space_ops.shoelace_direction "manim.utils.space_ops.shoelac_direction")计算方向。

[`get_end_anchors`](#manim.mobject.types.vectorized_mobject.VMobject.get_end_anchors "manim.mobject.types.vectorized_mobject.VMobject.get_end_anchors")

返回贝塞尔曲线的末端锚点。

[`get_fill_color`](#manim.mobject.types.vectorized_mobject.VMobject.get_fill_color "manim.mobject.types.vectorized_mobject.VMobject.get_fill_color")

如果有多种颜色（对于渐变），则返回第一个颜色

`get_fill_colors`

`get_fill_opacities`

[`get_fill_opacity`](#manim.mobject.types.vectorized_mobject.VMobject.get_fill_opacity "manim.mobject.types.vectorized_mobject.VMobject.get_fill_opacity")

如果有多个不透明度，则返回第一个

`get_fill_rgbas`

`get_gradient_start_and_end_points`

`get_group_class`

`get_last_point`

[`get_mobject_type_class`](#manim.mobject.types.vectorized_mobject.VMobject.get_mobject_type_class "manim.mobject.types.vectorized_mobject.VMobject.get_mobject_type_class")

返回此 mobject 类型的基类。

[`get_nth_curve_function`](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_function "manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_function")

返回第 n 条曲线的表达式。

[`get_nth_curve_function_with_length`](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_function_with_length "manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_function_with_length")

返回第 n 条曲线的表达式及其（近似）长度。

[`get_nth_curve_length`](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_length "manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_length")

返回第 n 条曲线的（近似）长度。

[`get_nth_curve_length_pieces`](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_length_pieces "manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_length_pieces")

返回用于长度近似的短线长度数组。

[`get_nth_curve_points`](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_points "manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_points")

返回定义 vmobject 第 n 条曲线的点。

[`get_num_curves`](#manim.mobject.types.vectorized_mobject.VMobject.get_num_curves "manim.mobject.types.vectorized_mobject.VMobject.get_num_curves")

返回 vmobject 的曲线数。

[`get_point_mobject`](#manim.mobject.types.vectorized_mobject.VMobject.get_point_mobject "manim.mobject.types.vectorized_mobject.VMobject.get_point_mobject")

最简单的[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")就是转化为自我或转化为自我。

`get_points_defining_boundary`

`get_sheen_direction`

`get_sheen_factor`

[`get_start_anchors`](#manim.mobject.types.vectorized_mobject.VMobject.get_start_anchors "manim.mobject.types.vectorized_mobject.VMobject.get_start_anchors")

返回贝塞尔曲线的起始锚点。

`get_stroke_color`

`get_stroke_colors`

`get_stroke_opacities`

`get_stroke_opacity`

`get_stroke_rgbas`

`get_stroke_width`

`get_style`

[`get_subcurve`](#manim.mobject.types.vectorized_mobject.VMobject.get_subcurve "manim.mobject.types.vectorized_mobject.VMobject.get_subcurve")

返回区间 \[a, b\] 之间 VMobject 的子曲线。

[`get_subpaths`](#manim.mobject.types.vectorized_mobject.VMobject.get_subpaths "manim.mobject.types.vectorized_mobject.VMobject.get_subpaths")

返回由 VMobject 的曲线形成的子路径。

`get_subpaths_from_points`

`has_new_path_started`

[`init_colors`](#manim.mobject.types.vectorized_mobject.VMobject.init_colors "manim.mobject.types.vectorized_mobject.VMobject.init_colors")

初始化颜色。

[`insert_n_curves`](#manim.mobject.types.vectorized_mobject.VMobject.insert_n_curves "manim.mobject.types.vectorized_mobject.VMobject.insert_n_curves")

将 n 条曲线插入到 vmobject 的贝塞尔曲线中。

[`insert_n_curves_to_point_list`](#manim.mobject.types.vectorized_mobject.VMobject.insert_n_curves_to_point_list "manim.mobject.types.vectorized_mobject.VMobject.insert_n_curves_to_point_list")

给定定义贝塞尔曲线（锚点和手柄）的 k 个点数组，返回精确定义 k + n 贝塞尔曲线的点。

`interpolate_color`

`is_closed`

`make_jagged`

`make_smooth`

`match_background_image`

`match_style`

[`point_from_proportion`](#manim.mobject.types.vectorized_mobject.VMobject.point_from_proportion "manim.mobject.types.vectorized_mobject.VMobject.point_from_proportion")

获取沿 路径的一定比例的点[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

[`pointwise_become_partial`](#manim.mobject.types.vectorized_mobject.VMobject.pointwise_become_partial "manim.mobject.types.vectorized_mobject.VMobject.pointwise_become_partial")

给定两个边界 a 和 b，将自身 vmobject 的点转换为相对于边界作为参数传递的 vmobject 的点。

[`proportion_from_point`](#manim.mobject.types.vectorized_mobject.VMobject.proportion_from_point "manim.mobject.types.vectorized_mobject.VMobject.proportion_from_point")

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")返回沿特定给定点所在路径的比例。

[`resize_points`](#manim.mobject.types.vectorized_mobject.VMobject.resize_points "manim.mobject.types.vectorized_mobject.VMobject.resize_points")

调整锚点和手柄数组的大小以具有指定的大小。

[`reverse_direction`](#manim.mobject.types.vectorized_mobject.VMobject.reverse_direction "manim.mobject.types.vectorized_mobject.VMobject.reverse_direction")

通过反转点顺序来恢复点方向。

[`rotate`](#manim.mobject.types.vectorized_mobject.VMobject.rotate "manim.mobject.types.vectorized_mobject.VMobject.rotate")

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")围绕某个点旋转。

[`rotate_sheen_direction`](#manim.mobject.types.vectorized_mobject.VMobject.rotate_sheen_direction "manim.mobject.types.vectorized_mobject.VMobject.rotate_sheen_direction")

旋转应用光泽的方向。

[`scale_handle_to_anchor_distances`](#manim.mobject.types.vectorized_mobject.VMobject.scale_handle_to_anchor_distances "manim.mobject.types.vectorized_mobject.VMobject.scale_handle_to_anchor_distances")

如果给定手柄点 H 与其关联的锚点 A 之间的距离为 d，则它将 H 更改为距 A 的距离因子 \*d，但从 A 到 H 的线不会改变。

[`set_anchors_and_handles`](#manim.mobject.types.vectorized_mobject.VMobject.set_anchors_and_handles "manim.mobject.types.vectorized_mobject.VMobject.set_anchors_and_handles")

给定两组锚点和句柄，对它们进行处理以将它们设置为 VMobject 的锚点和句柄。

`set_background_stroke`

[`set_color`](#manim.mobject.types.vectorized_mobject.VMobject.set_color "manim.mobject.types.vectorized_mobject.VMobject.set_color")

条件是接受一个参数 (x, y, z) 的函数。

[`set_fill`](#manim.mobject.types.vectorized_mobject.VMobject.set_fill "manim.mobject.types.vectorized_mobject.VMobject.set_fill")

设置 的填充颜色和填充不透明度[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

`set_opacity`

`set_points`

[`set_points_as_corners`](#manim.mobject.types.vectorized_mobject.VMobject.set_points_as_corners "manim.mobject.types.vectorized_mobject.VMobject.set_points_as_corners")

给定一个点数组，将它们设置为 vmobject 的角点。

`set_points_smoothly`

`set_shade_in_3d`

[`set_sheen`](#manim.mobject.types.vectorized_mobject.VMobject.set_sheen "manim.mobject.types.vectorized_mobject.VMobject.set_sheen")

从某个方向应用颜色渐变。

[`set_sheen_direction`](#manim.mobject.types.vectorized_mobject.VMobject.set_sheen_direction "manim.mobject.types.vectorized_mobject.VMobject.set_sheen_direction")

设置应用光泽的方向。

`set_stroke`

`set_style`

`start_new_path`

`update_rgbas_array`

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

[`fill_color`](#manim.mobject.types.vectorized_mobject.VMobject.fill_color "manim.mobject.types.vectorized_mobject.VMobject.fill_color")

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。

add*cubic_bezier_curve_to（*手柄 1*，*手柄 2*，*锚点\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.add_cubic_bezier_curve_to)[#](#manim.mobject.types.vectorized_mobject.VMobject.add_cubic_bezier_curve_to "此定义的固定链接")

将三次贝塞尔曲线添加到路径中。

注意：第一个锚点不是参数，因为默认情况下是最后一个子路径的末尾！

参数

- **handle1** ( _ndarray_ ) – 第一个句柄
- **handle2** ( _ndarray_ ) – 第二个句柄
- **锚**( _ndarray_ ) – 锚

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

添加线到（_点_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.add_line_to)[#](#manim.mobject.types.vectorized_mobject.VMobject.add_line_to "此定义的固定链接")

添加一条从 VMobject 的最后一个点到给定点的直线。

参数

**point** ( _ndarray_ ) – 直线的终点。

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

add*quadratic_bezier_curve_to（*手柄*，*锚点\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.add_quadratic_bezier_curve_to)[#](#manim.mobject.types.vectorized_mobject.VMobject.add_quadratic_bezier_curve_to "此定义的固定链接")

将二次贝塞尔曲线添加到路径中。

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

参数

- **句柄**( _ndarray_ ) –
- **锚点**( _ndarray_ ) –

add_smooth_curve*to ( *\*点\_)[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.add_smooth_curve_to)[#](#manim.mobject.types.vectorized_mobject.VMobject.add_smooth_curve_to "此定义的固定链接")

从给定点创建平滑曲线并将其添加到 VMobject。如果传入两个点，第一个点将被解释为句柄，第二个点将被解释为锚点。

参数

**点**( _array_ ) – 用于添加平滑曲线的点（锚点和手柄，或只是锚点）

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

提高

**ValueError** – 如果给出 0 或超过 2 分。

对齐点（_vmobject_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.align_points)[#](#manim.mobject.types.vectorized_mobject.VMobject.align_points "此定义的固定链接")

向 self 和 vmobject 添加点，以便它们都具有相同数量的子路径，并且每个相应的子路径都包含相同数量的点。

通过沿着子路径均匀细分曲线或通过创建由重复的单个点组成的新子路径来添加点。

参数

**vmobject** ( [_VMobject_](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) – 用来对齐点的对象。

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

更改锚点模式（_模式_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.change_anchor_mode)[#](#manim.mobject.types.vectorized_mobject.VMobject.change_anchor_mode "此定义的固定链接")

更改贝塞尔曲线的锚定模式。这将修改手柄。

只能有两种模式：“锯齿状”和“平滑”。

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

参数

**模式**( _str_ ) –

考虑\_points*equals*2d（\_p0*， \_p1*）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.consider_points_equals_2d)[#](#manim.mobject.types.vectorized_mobject.VMobject.consider_points_equals_2d "此定义的固定链接")

确定两个点是否足够接近以被视为相等。

这使用了 np.isclose() 中的算法，但在此处针对 2D 点情况进行了扩展。NumPy 对于这样一个小问题来说有点过分了。:param p0: 第一个点 :param p1: 第二个点

退货

两点是否接近。

返回类型

布尔值

参数

- **p0** ( _ndarray_ ) –
- **p1** ( _ndarray_ ) –

_属性_ 填充颜色[#](#manim.mobject.types.vectorized_mobject.VMobject.fill_color "此定义的固定链接")

如果有多种颜色（对于渐变），则返回第一个颜色

力方向（_目标方向_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.force_direction)[#](#manim.mobject.types.vectorized_mobject.VMobject.force_direction "此定义的固定链接")

确保点的方向是顺时针或逆时针。

参数

**target_direction** ( _str_ ) –`"CW"`或`"CCW"`。

gen_cubic_bezier_tuples_from*points（*点\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.gen_cubic_bezier_tuples_from_points)[#](#manim.mobject.types.vectorized_mobject.VMobject.gen_cubic_bezier_tuples_from_points "此定义的固定链接")

从点数组返回贝塞尔曲线元组。

self.points 是 mobject 贝塞尔曲线的锚点和句柄的列表（即 \[anchor1、handle1、handle2、anchor2、anchor3 ..\]）。该算法基本上通过每 n 取一个元素来检索它们，其中 n 是贝塞尔曲线的控制点数量。

参数

**点**( _ndarray_ ) – 将从中提取控制点的点。

退货

贝塞尔曲线控制点。

返回类型

_元组_

generate*rgbas_array（*颜色*，*不透明度\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.generate_rgbas_array)[#](#manim.mobject.types.vectorized_mobject.VMobject.generate_rgbas_array "此定义的固定链接")

第一个 arg 可以是颜色，也可以是颜色元组/列表。同样，不透明度可以是一个浮点数，也可以是浮点数的元组。如果 self.sheen_factor 不为零，并且只传入一种颜色，则会自动为渐变添加第二种稍浅的颜色

获取锚点( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_anchors)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_anchors "此定义的固定链接")

返回形成 VMobject 的曲线的锚点。

退货

锚。

返回类型

np.ndarray

获取锚点和句柄( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_anchors_and_handles)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_anchors_and_handles "此定义的固定链接")

返回 anchors1、handles1、handles2、anchors2，其中 (anchors1\[i\]、handles1\[i\]、handles2\[i\]、anchors2\[i\]) 是为 range(0, len(锚 1))

退货

锚点和手柄的可迭代。

返回类型

_可迭代_\[np.ndarray\]

get*arc_length ( \_sample_points_per_curve = None* )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_arc_length)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_arc_length "此定义的固定链接")

返回整条曲线的近似长度。

参数

**Sample_points_per_curve** ( _int_ _|_ _None_ ) – 用于近似长度的每条曲线的样本点数。更多的点会产生更好的近似值。

退货

的长度[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

返回类型

漂浮

获取颜色( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_color)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_color "此定义的固定链接")

返回的颜色[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

获取曲线函数( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_curve_functions)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_curve_functions "此定义的固定链接")

获取 mobject 曲线的函数。

退货

曲线的函数。

返回类型

_可迭代_\[_可调用_\[\[float\], np.ndarray\]\]

get*curve_functions_with_lengths ( *\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_curve_functions_with_lengths)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_curve_functions_with_lengths "此定义的固定链接")

获取 mobject 的函数和曲线长度。

参数

\***\*kwargs** – 传递给的关键字参数[`get_nth_curve_function_with_length()`](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_function_with_length "manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_function_with_length")

退货

曲线的函数和长度。

返回类型

_可迭代_\[_元组_\[_可调用_\[\[float\], np.ndarray\], float\]\]

获取方向( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_direction)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_direction "此定义的固定链接")

用于[`shoelace_direction()`](manim.utils.space_ops.html#manim.utils.space_ops.shoelace_direction "manim.utils.space_ops.shoelac_direction")计算方向。点的方向决定了绘制对象的方向，顺时针还是逆时针。

例子

a 的默认方向[`Circle`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")是逆时针：


```py

```


退货

要么`"CW"`要么`"CCW"`.

返回类型

`str`

获取结束锚点( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_end_anchors)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_end_anchors "此定义的固定链接")

返回贝塞尔曲线的末端锚点。

退货

启动锚点

返回类型

np.ndarray

获取填充颜色( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_fill_color)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_fill_color "此定义的固定链接")

如果有多种颜色（对于渐变），则返回第一个颜色

获取填充不透明度( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_fill_opacity)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_fill_opacity "此定义的固定链接")

如果有多个不透明度，则返回第一个

_静态_ get_mobject_type_class ( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_mobject_type_class)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_mobject_type_class "此定义的固定链接")

返回此 mobject 类型的基类。

获取第 n 条曲线函数( _n_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_nth_curve_function)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_function "此定义的固定链接")

返回第 n 条曲线的表达式。

参数

**n** ( _int_ ) – 所需曲线的索引。

退货

第 n 条贝塞尔曲线的表达式。

返回类型

_可调用_\[浮动\]

get*nth_curve_function_with*length（\_n*，*样本点=无\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_nth_curve_function_with_length)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_function_with_length "此定义的固定链接")

返回第 n 条曲线的表达式及其（近似）长度。

参数

- **n** ( _int_ ) – 所需曲线的索引。
- **Sample_points** ( _int_ _|_ _None_ ) – 采样以查找长度的点数。

退货

- **curve** ( _typing.Callable\[\[float\], np.ndarray\]_ ) – 第 n 条曲线的函数。
- **length** ( `float`) – 第 n 条曲线的长度。

返回类型

元组\[_可调用_\[\[float\], np.ndarray\], float\]

get*nth_curve*length（\_n*，*样本点=无\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_nth_curve_length)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_length "此定义的固定链接")

返回第 n 条曲线的（近似）长度。

参数

- **n** ( _int_ ) – 所需曲线的索引。
- **Sample_points** ( _int_ _|_ _None_ ) – 采样以查找长度的点数。

退货

**length** – 第 n 条曲线的长度。

返回类型

`float`

get*nth_curve_length_pieces（\_n*， _sample_points = None_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_nth_curve_length_pieces)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_length_pieces "此定义的固定链接")

返回用于长度近似的短线长度数组。

参数

- **n** ( _int_ ) – 所需曲线的索引。
- **Sample_points** ( _int_ _|_ _None_ ) – 采样以查找长度的点数。

退货

第 n 条曲线的短长度片段。

返回类型

np.ndarray

获取第 n 个曲线点( _n_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_nth_curve_points)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_nth_curve_points "此定义的固定链接")

返回定义 vmobject 第 n 条曲线的点。

参数

**n** ( _int_ ) – 所需贝塞尔曲线的索引。

退货

定义第 n 条贝塞尔曲线的点（锚点、手柄）

返回类型

np.ndarray

获取曲线数( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_num_curves)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_num_curves "此定义的固定链接")

返回 vmobject 的曲线数。

退货

曲线数量。vmobject 的。

返回类型

整数

get*point_mobject（*中心=无\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_point_mobject)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_point_mobject "此定义的固定链接")

最简单的[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")就是转化为自我或转化为自我。应由适当类型的点

获取开始锚点( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_start_anchors)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_start_anchors "此定义的固定链接")

返回贝塞尔曲线的起始锚点。

退货

启动锚点

返回类型

np.ndarray

获取子曲线（_a_， _b_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_subcurve)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_subcurve "此定义的固定链接")

返回区间 \[a, b\] 之间 VMobject 的子曲线。曲线本身就是一个 VMobject。

参数

- **a** ( _float_ ) – 下限。
- **b** ( _float_ ) – 上限。

退货

\[a, b\] 之间的子曲线

返回类型

[虚拟机对象](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

获取子路径( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.get_subpaths)[#](#manim.mobject.types.vectorized_mobject.VMobject.get_subpaths "此定义的固定链接")

返回由 VMobject 的曲线形成的子路径。

子路径是曲线范围，每对连续曲线的终点/起点重合。

退货

子路径。

返回类型

_元组_

init*colors ( \_propagate_colors = True* )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.init_colors)[#](#manim.mobject.types.vectorized_mobject.VMobject.init_colors "此定义的固定链接")

初始化颜色。

被创造召唤。这是一个空方法，可以由子类实现。

insert*n_curves ( \_n* )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.insert_n_curves)[#](#manim.mobject.types.vectorized_mobject.VMobject.insert_n_curves "此定义的固定链接")

将 n 条曲线插入到 vmobject 的贝塞尔曲线中。

参数

**n** ( _int_ ) – 要插入的曲线数。

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

insert*n_curves_to_point*list（\_n*，*点\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.insert_n_curves_to_point_list)[#](#manim.mobject.types.vectorized_mobject.VMobject.insert_n_curves_to_point_list "此定义的固定链接")

给定定义贝塞尔曲线（锚点和手柄）的 k 个点数组，返回精确定义 k + n 贝塞尔曲线的点。

参数

- **n** ( _int_ ) – 所需曲线的数量。
- **点**( _ndarray_ ) – 起点。

退货

生成积分。

返回类型

np.ndarray

比例点( _alpha_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.point_from_proportion)[#](#manim.mobject.types.vectorized_mobject.VMobject.point_from_proportion "此定义的固定链接")

获取沿 路径的一定比例的点[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

参数

**alpha** ( _float_ ) – 沿路径的比例[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

退货

上的点[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

返回类型

`numpy.ndarray`

提高

- **ValueError** – 如果`alpha`不在 0 和 1 之间。
- **例外**\- 如果[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")没有分数。

pointwise*become_partial ( \_vmobject* , _a_ , _b_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.pointwise_become_partial)[#](#manim.mobject.types.vectorized_mobject.VMobject.pointwise_become_partial "此定义的固定链接")

给定两个边界 a 和 b，将自身 vmobject 的点转换为相对于边界作为参数传递的 vmobject 的点。这里的点代表贝塞尔曲线的控制点（锚点和手柄）

参数

- **vmobject** ( [_VMobject_](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) – 将用作模型的 vmobject。
- **a** ( _float_ ) – 上限。
- **b** ( _float_ ) – 下限

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

从点开始的比例（_点_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.proportion_from_point)[#](#manim.mobject.types.vectorized_mobject.VMobject.proportion_from_point "此定义的固定链接")

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") 返回沿特定给定点所在路径的比例。

参数

**point** ( _Iterable_ _\[_ _float_ _|_ _int_ _\]_ ) – 点的笛卡尔坐标，该点可能位于也可能不位于[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

退货

沿路径的比例[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

返回类型

漂浮

提高

- **ValueError** – 如果`point`不在曲线上。
- **例外**\- 如果[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")没有分数。

resize*points ( \_new_length* , _resize_func=<函数 resize_array>_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.resize_points)[#](#manim.mobject.types.vectorized_mobject.VMobject.resize_points "此定义的固定链接")

调整锚点和手柄数组的大小以具有指定的大小。

参数

- **new_length** ( _int_ ) – 新的（总）点数。
- **resize_func** ( _Callable_ _\[_ _\[_ _ndarray_ _,_ _int_ _\]_ _,_ _ndarray_ _\]_ ) – 将 Numpy 数组（点）和整数（目标大小）映射到 Numpy 数组的函数。默认实现是基于 Numpy 的`resize`函数。

反向方向( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.reverse_direction)[#](#manim.mobject.types.vectorized_mobject.VMobject.reverse_direction "此定义的固定链接")

通过反转点顺序来恢复点方向。

退货

返回自我。

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

例子

示例：改变方向[¶](#changeofdirection)


```py

```


旋转(_角度_,_轴= array(\[0., 0., 1.\])_ , _about_point = None_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.rotate)[#](#manim.mobject.types.vectorized_mobject.VMobject.rotate "此定义的固定链接")

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")围绕某个点旋转。

参数

- **角度**（_浮动_）–
- **轴**( _np.ndarray_ ) –
- **about_point** (_序列\_\_\[_ _float_ _\]_ _|_ _None_ ) –

rotate*sheen_direction (*角度*,*轴= array(\[0., 0., 1.\])_ , \_family = True_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.rotate_sheen_direction)[#](#manim.mobject.types.vectorized_mobject.VMobject.rotate_sheen_direction "此定义的固定链接")

旋转应用光泽的方向。

参数

- **angle** ( _float_ ) – 光泽方向旋转的角度。
- **axis** ( _ndarray_ ) – 旋转轴。

例子

正常使用：

Circle().set_sheen_direction(UP).rotate_sheen_direction(PI)

Copy to clipboard

也可以看看

[`set_sheen_direction()`](#manim.mobject.types.vectorized_mobject.VMobject.set_sheen_direction "manim.mobject.types.vectorized_mobject.VMobject.set_sheen_direction")

scale*handle_to_anchor_distances（*因子\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.scale_handle_to_anchor_distances)[#](#manim.mobject.types.vectorized_mobject.VMobject.scale_handle_to_anchor_distances "此定义的固定链接")

如果给定手柄点 H 与其关联的锚点 A 之间的距离为 d，则它将 H 更改为距 A 的距离因子 \*d，但从 A 到 H 的线不会改变。这在应用（可微）函数的上下文中最有用，以保留相切属性。人们会将所有手柄拉近其锚点，应用该功能，然后再次将它们推出。

参数

**Factor** ( _float_ ) – 用于缩放的因子。

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

set_anchors_and*handles（*锚点 1*，*手柄 1*，*手柄 2*，*锚点 2\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.set_anchors_and_handles)[#](#manim.mobject.types.vectorized_mobject.VMobject.set_anchors_and_handles "此定义的固定链接")

给定两组锚点和句柄，对它们进行处理以将它们设置为 VMobject 的锚点和句柄。

anchors1\[i\]、handles1\[i\]、handles2\[i\] 和 anchors2\[i\] 定义 vmobject 的第 i 条贝塞尔曲线。有四个硬编码参数，这是一个问题，因为它使得每条三次曲线的点数不能从 4 个更改（两个锚点和两个手柄）。

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

参数

- **锚 1**（_序列\_\_\[_ _float_ _\]_）-
- **句柄 1**（_序列\_\_\[_ _float_ _\]_）-
- **句柄 2**（_序列\_\_\[_ _float_ _\]_）-
- **锚点 2**（_序列\_\_\[_ _float_ _\]_）–

set*color (*颜色*,*系列= True\_ )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.set_color)[#](#manim.mobject.types.vectorized_mobject.VMobject.set_color "此定义的固定链接")

条件是接受一个参数 (x, y, z) 的函数。这里它只是递归到子对象，但是在子类中，这应该基于颜色的内部工作原理进一步实现

set*fill（*颜色=无*，*不透明度=无*，*族=真\_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.set_fill)[#](#manim.mobject.types.vectorized_mobject.VMobject.set_fill "此定义的固定链接")

设置 的填充颜色和填充不透明度[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

参数

- **color** ( _str_ _|_ _None_ ) – 的填充颜色[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。
- **opacity** ( _float_ _|_ _None_ ) – 填充 的不透明度[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。
- **family** ( _bool_ ) – 如果为`True`，则还设置所有子对象的填充颜色。

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

例子

示例：设置填充[¶](#setfill)

![../_images/SetFill-1.png](../_images/SetFill-1.png)


```py

```


也可以看看

`set_style()`

set_points_as*corners (*点\_)[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.set_points_as_corners)[#](#manim.mobject.types.vectorized_mobject.VMobject.set_points_as_corners "此定义的固定链接")

给定一个点数组，将它们设置为 vmobject 的角点。

为了实现这一点，该算法将手柄设置为与锚点对齐，以便生成的贝塞尔曲线将成为两个锚点之间的线段。

参数

**points** ( _Sequence_ _\[_ _float_ _\]_ ) – 将被设置为角点的点数组。

退货

`self`

返回类型

[`VMobject`](#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

set*sheen (*因子*,*方向= None* , \_family = True* )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.set_sheen)[#](#manim.mobject.types.vectorized_mobject.VMobject.set_sheen "此定义的固定链接")

从某个方向应用颜色渐变。

参数

- **Factor** ( _float_ ) – 应用的光泽/渐变程度。如果为负，则渐变从黑色开始，如果为正，则渐变从白色开始并更改为当前颜色。
- **Direction** (_可选\_\_\[_ _ndarray_ _\]_ ) – 应用渐变的方向。

例子

示例：SetSheen [¶](#setsheen)

![../_images/SetSheen-1.png](../_images/SetSheen-1.png)


```py

```


set*sheen_direction (*方向*, \_family = True* )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VMobject.set_sheen_direction)[#](#manim.mobject.types.vectorized_mobject.VMobject.set_sheen_direction "此定义的固定链接")

设置应用光泽的方向。

参数

**Direction** ( _ndarray_ ) – 应用渐变的方向。

例子

正常使用：


```py

```


也可以看看

[`set_sheen()`](#manim.mobject.types.vectorized_mobject.VMobject.set_sheen "manim.mobject.types.vectorized_mobject.VMobject.set_sheen"),[`rotate_sheen_direction()`](#manim.mobject.types.vectorized_mobject.VMobject.rotate_sheen_direction "manim.mobject.types.vectorized_mobject.VMobject.rotate_sheen_direction")
