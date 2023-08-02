# Mobject

合格名称：`manim.mobject.mobject.Mobject`


```py

```

数学对象：可以在屏幕上显示的对象的基类。

有一个兼容层，允许使用`get_*` 和`set_*`方法获取和设置通用属性。请参阅[`set()`]()了解更多详情。

子对象

所包含的物体。

类型

列表\[ [`Mobject`]()\]

点

物体的点。

也可以看看

[`VMobject`]()

类型

`numpy.ndarray`

方法

[`add`]()

将 mobject 添加为子对象。

[`add_animation_override`]()

添加动画覆盖。

[`add_background_rectangle`]()

添加一个背景矩形作为子对象。

`add_background_rectangle_to_family_members_with_points`

`add_background_rectangle_to_submobjects`

`add_n_more_submobjects`

[`add_to_back`]()

将所有传递的 mobject 添加到子 mobject 的后面。

[`add_updater`]()

向此 mobject 添加更新功能。

[`align_data`]()

将此 mobject 的数据与另一个 mobject 对齐。

[`align_on_border`]()

方向只需是指向 2d 平面中的边或角的向量。

`align_points`

`align_points_with_larger`

`align_submobjects`

[`align_to`]()

将对象与另一个对象[`Mobject`]()在某个方向上对齐。

[`animation_override_for`]()

返回为此类定义特定动画覆盖的函数。

[`apply_complex_function`]()

将复杂函数应用于[`Mobject`]().

`apply_function`

`apply_function_to_position`

`apply_function_to_submobject_positions`

`apply_matrix`

`apply_over_attr_arrays`

`apply_points_function_about_point`

[`apply_to_family`]()

递归地将函数应用于`self`每个带有点的子对象。

[`arrange`]()

[`Mobject`]()在屏幕上并排排序。

[`arrange_in_grid`]()

将子对象排列在网格中。

[`arrange_submobjects`]()

[`submobjects`]()安排一个小缓冲区的位置。

[`become`]()

编辑点、颜色和子对象以使其与其他对象相同[`Mobject`]()

`center`

[`clear_updaters`]()

删除所有更新程序。

[`copy`]()

创建并返回包含[`Mobject`]()所有[`submobjects`]().

`fade`

`fade_to`

`family_members_with_points`

[`flip`]()

围绕其中心翻转/镜像对象。

[`generate_points`]()

初始化[`points`]()并因此初始化形状。

`generate_target`

[`get_all_points`]()

返回此 mobject 和所有子 mobject 的所有点。

`get_array_attrs`

[`get_bottom`]()

获取边界框的底部坐标[`Mobject`]()

`get_boundary_point`

[`get_center`]()

获取中心坐标

`get_center_of_mass`

[`get_color`]()

返回的颜色[`Mobject`]()

[`get_coord`]()

旨在概括`get_x`,`get_y`和`get_z`

[`get_corner`]()

获取特定方向的角坐标。

[`get_critical_point`]()

想象一个包围 的盒子[`Mobject`]()。

[`get_edge_center`]()

获取特定方向的边缘坐标。

[`get_end`]()

返回笔画围绕端点的点[`Mobject`]()。

`get_extremum_along_dim`

`get_family`

`get_family_updaters`

`get_group_class`

`get_image`

[`get_left`]()

获取边界框的左坐标[`Mobject`]()

[`get_merged_array`]()

返回此 mobject 和所有子 mobject 的所有给定属性。

[`get_midpoint`]()

获取形成 的路径中间的坐标 [`Mobject`]()。

[`get_mobject_type_class`]()

返回此 mobject 类型的基类。

[`get_nadir`]()

获取 3D 边界框的最低点（与天顶相对）坐标[`Mobject`]()。

`get_num_points`

`get_pieces`

[`get_point_mobject`]()

最简单的[`Mobject`]()就是转化为自我或转化为自我。

`get_points_defining_boundary`

[`get_right`]()

获取边界框的正确坐标[`Mobject`]()

[`get_start`]()

返回围绕笔划的起始点[`Mobject`]()。

[`get_start_and_end`]()

以 的形式返回笔划的起点和终点`tuple`。

[`get_time_based_updaters`]()

使用该参数返回所有更新程序`dt`。

[`get_top`]()

获取边界框的顶部坐标[`Mobject`]()

[`get_updaters`]()

返回所有更新程序。

[`get_x`]()

[`Mobject`]()返回 as 中心的 x 坐标`float`

[`get_y`]()

[`Mobject`]()返回 as 中心的 y 坐标`float`

[`get_z`]()

[`Mobject`]()返回 as 中心的 z 坐标`float`

`get_z_index_reference_point`

[`get_zenith`]()

获取 3D 边界框的天顶坐标[`Mobject`]()。

[`has_no_points`]()

检查是否*不*包含点。[`Mobject`]()

[`has_points`]()

检查是否[`Mobject`]()包含点。

[`has_time_based_updater`](")

测试是否`self`有基于时间的更新程序。

[`init_colors`]()

初始化颜色。

[`insert`]()

将 mobject 插入到 self.submobjects 的特定位置

[`interpolate`]()

将其转换为和[`Mobject`]()之间的插值。` mobject1``mobject2 `

`interpolate_color`

[`invert`](")

反转 的列表[`submobjects`]()。

`is_off_screen`

[`length_over_dim`]()

[`Mobject`]()测量某个方向上的长度。

[`match_color`]()

将颜色与另一个颜色相匹配[`Mobject`]()。

[`match_coord`]()

将坐标与另一个 的坐标相匹配[`Mobject`]()。

[`match_depth`]()

将深度与另一个深度相匹配[`Mobject`]()。

[`match_dim_size`]()

将指定的维度与另一个 的维度进行匹配[`Mobject`]()。

[`match_height`]()

将高度与另一个高度匹配[`Mobject`]()。

[`match_points`]()

编辑点、位置和子对象使其与另一个相同[`Mobject`]()，同时保持样式不变。

[`match_updaters`]()

匹配给定 mobject 的更新程序。

[`match_width`]()

将宽度与另一个 的宽度匹配[`Mobject`]()。

[`match_x`]()

匹配 x 坐标。

[`match_y`]()

匹配 y 坐标。

[`match_z`]()

匹配 z 坐标。

[`move_to`]()

将中心移动[`Mobject`]()到某个坐标。

[`next_to`]()

将其移动到另一个坐标或坐标[`Mobject`]()旁边。[`Mobject`]()

`nonempty_submobjects`

[`null_point_align`]()

如果一个[`Mobject`]()有点与一个没有点对齐，则将两者视为组，并将有点的一个推入其自己的子对象列表中。

`point_from_proportion`

`pose_at_angle`

`proportion_from_point`

`push_self_into_submobjects`

`put_start_and_end_on`

[`reduce_across_dimension`]()

查找此对象和子对象中所有点的维度的最小值或最大值。

[`remove`]()

删除[`submobjects`]().

[`remove_updater`]()

删除更新程序。

[`repeat`]()

这可以使过渡动画更好

`repeat_submobject`

`replace`

`rescale_to_fit`

[`reset_points`]()

设置[`points`]()为空数组。

[`restore`]()

恢复之前用 保存的状态[`save_state()`]()。

[`resume_updating`]()

启用从更新程序和动画的更新。

`reverse_points`

[`rotate`]()

[`Mobject`]()围绕某个点旋转。

[`rotate_about_origin`]()

绕原点旋转[`Mobject`]()，原点位于 \[0,0,0\]。

[`save_image`]()

仅将其所在位置的图像保存[`Mobject`]()到 png 文件中。

[`save_state`]()

保存当前状态（位置、颜色和大小）。

[`scale`]()

按一个因子缩放大小。

[`scale_to_fit_depth`]()

缩放[`Mobject`]()以适应深度，同时保持宽度/高度成比例。

[`scale_to_fit_height`]()

缩放[`Mobject`]()以适应高度，同时保持宽度/深度成比例。

[`scale_to_fit_width`]()

缩放[`Mobject`]()以适应宽度，同时保持高度/深度成比例。

[`set`]()

设置属性。

[`set_color`]()

条件是接受一个参数 (x, y, z) 的函数。

`set_color_by_gradient`

`set_colors_by_radial_gradient`

`set_coord`

[`set_default`]()

设置关键字参数的默认值。

`set_submobject_colors_by_gradient`

`set_submobject_colors_by_radial_gradient`

[`set_x`]()

[`Mobject`]()设置(`int`或`float`)中心的 x 值

[`set_y`]()

[`Mobject`]()设置(`int`或`float`)中心的 y 值

[`set_z`]()

[`Mobject`]()设置(`int`或`float`)中心的 z 值

[`set_z_index`]()

[`Mobject`]()将的设置为 z_index_value`z_index`中指定的值。

[`set_z_index_by_z_coordinate`]()

将[`Mobject`]()'sz 坐标设置为 的值`z_index`。

[`shift`]()

按给定向量移位。

`shift_onto_screen`

`show`

[`shuffle`]()

随机排列 的列表[`submobjects`]()。

[`shuffle_submobjects`]()

打乱顺序[`submobjects`]()

[`sort`]()

[`submobjects`]()通过 定义的函数对的列表进行排序`submob_func`。

[`sort_submobjects`]()

排序[`submobjects`]()

`space_out_submobjects`

`split`

`stretch`

`stretch_about_point`

[`stretch_to_fit_depth`]()

拉伸[`Mobject`]()以适应深度，而不保持宽度/高度成比例。

[`stretch_to_fit_height`]()

拉伸[`Mobject`]()以适应高度，而不保持宽度/深度成比例。

[`stretch_to_fit_width`]()

拉伸[`Mobject`]()以适应宽度，而不保持高度/深度成比例。

`surround`

[`suspend_updating`]()

禁用更新程序和动画的更新。

`throw_error_if_no_points`

`to_corner`

`to_edge`

`to_original_color`

[`update`]()

应用所有更新程序。

`wag`

属性

[`animate`]()

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

[`depth`]()

对象的深度。

[`height`]()

mobject 的高度。

[`width`]()

mobject 的宽度。

添加（_\* mobjects_）

将 mobject 添加为子对象。

mobjects 添加到[`submobjects`]().

mobject 的子类可以实现`+`和`+=`删除方法。

参数

**mobjects** ( [_Mobject_]() ) – 要添加的 mobject。

退货

`self`

返回类型

[`Mobject`]()

提高

- **ValueError** – 当 mobject 尝试添加自身时。
- **TypeError** – 当尝试添加不是 的实例的对象时[`Mobject`]()。

笔记

一个 mobject 不能包含它自己，也不能多次包含一个子对象。如果显示父级对象，则新添加的子级对象也会显示（即它们会自动添加到父级场景中）。

也可以看看

[`remove()`](),[`add_to_back()`]()

例子

```py

```


不会再次添加重复项：

```py

```


将对象添加到自身会引发错误：

```py

```

给定的 mobject 不能作为子对象两次添加到某个父对象：

```py

```


_类方法_ add*animation_override（\_animation_class*， _override_func_）

添加动画覆盖。

这不适用于子类。

参数

- **Animation_class** ( _type_ _\[_ [_Animation_]() _\]_ ) – 要覆盖的动画类型
- **override_func** ( _Callable_ _\[_ _\[_ [_Mobject_]() _,_ _..._ _\]_ _,_ [_Animation_]() _\]_ ) – 返回动画替换默认动画的函数。它传递给动画构造函数的参数。

提高

**MultiAnimationOverrideException** – 如果覆盖的动画已被覆盖。

add*background_rectangle (*颜色=无*,*不透明度= 0.75* , *\*\* kwargs\_ )

添加一个背景矩形作为子对象。

背景矩形添加在其他子对象后面。

这可用于增加嘈杂背景前的对象可见性。

参数

- **color** ( [_Colors_]() _|_ _None_ ) – 背景矩形的颜色
- **opacity** ( _float_ ) – 背景矩形的不透明度
- **kwargs** – 传递给 BackgroundRectangle 构造函数的附加关键字参数

退货

`self`

返回类型

[`Mobject`]()

也可以看看

[`add_to_back()`](),[`BackgroundRectangle`]()

add*to_back ( *\* mobjects\_ )

将所有传递的 mobject 添加到子 mobject 的后面。

如果[`submobjects`]()已经包含给定的 mobject，它们只是移到后面。

参数

**mobjects** ( [_Mobject_]() ) – 要添加的 mobject。

退货

`self`

返回类型

[`Mobject`]()

笔记

从技术上讲，这是通过将 mobject 添加（或移动）到 的头部来完成的[`submobjects`]()。首先渲染此列表的头部，这将相应的 mobject 放置在后续列表成员的后面。

提高

- **ValueError** – 当 mobject 尝试添加自身时。
- **TypeError** – 当尝试添加不是 的实例的对象时[`Mobject`]()。

参数

**mobjects** ( [_Mobject_]() ) –

笔记

一个 mobject 不能包含它自己，也不能多次包含一个子对象。如果显示父级对象，则新添加的子级对象也会显示（即它们会自动添加到父级场景中）。

也可以看看

[`remove()`](),[`add()`]()

add*updater ( \_update_function* ,_索引= None_ , _call_updater = False_ )

向此 mobject 添加更新功能。

更新函数，简称更新器，是在每一帧中应用于 Mobject 的函数。

参数

- **update_function** ( _Updater_ ) – 要添加的更新函数。每当[`update()`]()调用时，都会使用 `self`第一个参数来调用此更新函数。更新程序可以有第二个参数`dt`。如果使用此参数，则会使用第二个值来调用它`dt`，该值通常表示自上次调用以来的时间（以秒为单位）[`update()`]()。
- **index** ( _int_ _|_ _None_ ) – 应添加新更新程序的索引`self.updaters`。如果`index`是的话`None`，更新程序将添加在最后。
- **call_updater** ( _bool_ ) – 最初是否调用更新程序。如果`True`，将使用 调用更新程序`dt=0`。

退货

`self`

返回类型

[`Mobject`]()

例子

示例：NextToUpdater

```py

```


示例：DtUpdater 
```py

```

也可以看看

[`get_updaters()`](), [`remove_updater()`](),[`UpdateFromFunc`]()

对齐数据（_mobject_， _skip_point_alignment = False_）

将此 mobject 的数据与另一个 mobject 对齐。

之后，这两个 mobject 将具有相同数量的子对象（请参阅`align_submobjects()`）和相同的父结构（请参阅 [`null_point_align()`]()）。如果`skip_point_alignment`为 false，它们也将具有相同数量的点数（请参阅[`align_points()`]()）。

参数

- **mobject** ( [_Mobject_]() ) – 该 mobject 应与其对齐的另一个 mobject。
- **Skip_point_alignment** ( _bool_ ) – 控制是否跳过计算量大的点对齐（默认值：False）。

边界对齐（_方向_， _buff = 0.5_）

方向只需是指向 2d 平面中的边或角的向量。

align*to ( \_mobject_or_point* ,_方向= array(\[0., 0., 0.\])_ )

将对象与另一个对象[`Mobject`]()在某个方向上对齐。

示例： mob1.align_to(mob2, UP) 垂直移动 mob1，使其顶部边缘与 mob2 的顶部边缘对齐。

参数

**mobject_or_point** ( [_Mobject_]() _|_ _np.ndarray_ _|\_\_列表_) –

_属性_ 动画*： \_AnimationBuilder | T* 

用于对 的任何方法的应用程序进行动画处理`self`。

任何调用的方法`animate`都会转换为将该方法应用于 mobject 本身的动画。

例如，`square.set_fill(WHITE)`设置正方形的填充颜色，同时`square.animate.set_fill(WHITE)`为该动作设置动画。

可以通过链接将多个方法放入单个动画中：

self.play(my_mobject.animate.shift(RIGHT).rotate(PI))

Copy to clipboard

警告

[`Mobject`]()不鼓励在一次调用中传递多个动画，[`play()`]()并且很可能无法正常工作。而不是写一个像这样的动画


```py

```


利用方法链。

可以传递给的关键字参数[`Scene.play()`]()可以在访问后直接传递`.animate`，如下所示：


```py

```


`.animate`当您希望以不同方式执行同时调用的动画时，这尤其有用：


```py

```


也可以看看

[`override_animate()`]()

例子

示例：AnimateExample 

```py

```


示例：AnimateChain 示例

```py

```


示例：AnimateWithArgsExample

```py

```


警告

`.animate`

[`Mobject`]()将在应用到它之前的点 `.animate`和应用到它之后的点之间插入`.animate`。当尝试沿路径或旋转进行插值时，这可能会导致意外行为。如果您希望动画考虑之间的点，请考虑使用 [`ValueTracker`]()更新程序。

_类方法_ animation*override_for ( \_animation_class* )

返回为此类定义特定动画覆盖的函数。

参数

**Animation_class** ( _type_ _\[_ [_Animation_]() _\]_ ) – 应返回覆盖函数的动画类。

退货

该函数返回覆盖动画，或者`None`如果没有定义此类动画覆盖。

返回类型

可选\[可调用\[\[ [Mobject]() , …\],[动画]()\]\]

apply*complex_function (*函数*, *\*\* kwargs\_ )

将复杂函数应用于[`Mobject`](). x 和 y 坐标分别对应于实部和虚部。

例子

示例：ApplyFuncExample 

```py

```


适用于家庭（_功能_）

递归地将函数应用于`self`每个带有点的子对象。

参数

**func** ( _Callable_ _\[_ _\[_ [_Mobject_]() _\]_ _,_ _None_ _\]_ ) – 应用于每个 mobject 的函数。`func`获取相应的（子）对象作为参数传递。

退货

`self`

返回类型

[`Mobject`]()

也可以看看

`family_members_with_points()`

排列(_方向= array(\[1., 0., 0.\])_ , _buff = 0.25_ , _center = True_ , _\*\* kwargs_ )

[`Mobject`]()在屏幕上并排排序。

例子

示例：示例

![示例-1.png](../_images/Example-1.png)

```py

```


参数

**方向**(_序列\_\_\[_ _float_ _\]_ ) –

array*in_grid ( \_rows = None* , _cols = None_ , _buff = 0.25_ , _cell_alignment = array(\[0., 0., 0.\])_ , _row_alignments = None_ , _col_alignments = None_ , _row_heights = None_ , _col_widths = None_ , _flow_order = 'rd '_ , _\*\* kwargs_ )

将子对象排列在网格中。

参数

- **rows** ( _int_ _|_ _None_ ) – 网格中的行数。
- **cols** ( _int_ _|_ _None_ ) – 网格中的列数。
- **buff** ( _float_ _|_ _tuple_ _\[_ _float_ _,_ _float_ _\]_ ) – 网格单元之间的间隙。要在水平和垂直方向指定不同的缓冲区，可以给出两个值的元组 \- 。`(row, col)`
- **cell_alignment** ( _np.ndarray_ ) – 每个子对象在其网格单元中对齐的方式。
- **row_alignments** ( _str_ _|_ _None_ ) – 每行的垂直对齐方式（从上到下）。接受以下字符：`"u"`\- 向上、`"c"`\- 居中、`"d"`\- 向下。
- **col_alignments** ( _str_ _|_ _None_ ) – 每列的水平对齐方式（从左到右）。接受以下字符`"l"`\- 左、 `"c"`\- 中、`"r"`\- ​​ 右。
- **row_heights** ( _Iterable_ _\[_ _float_ _|_ _None_ _\]_ _|_ _None_ ) – 定义某些行的高度列表（从上到下）。如果列表包含 `None`，则相应的行将根据该行中最高的元素自动适应其高度。
- **col_widths** ( _Iterable_ _\[_ _float_ _|_ _None_ _\]_ _|_ _None_ ) – 定义某些列的宽度列表（从左到右）。如果列表包含`None`，则相应的列将根据该列中最宽的元素自动适应其宽度。
- **flow_order** ( _str_ ) – 子对象填充网格的顺序。可以是以下值之一：“rd”、“dr”、“ld”、“dl”、“ru”、“ur”、“lu”、“ul”。（“rd” -> 向右填充然后向下填充）

退货

`self`

返回类型

[`Mobject`]()

提高

- **ValueError** – 如果`rows`和`cols`太小而无法容纳所有子对象。
- **ValueError** – 如果`cols`、`col_alignments`和`col_widths`或`rows`、 `row_alignments`和 的`row_heights`大小不匹配。

笔记

如果仅隐式设置`cols`和之一`rows`，则将选择另一个足够大的值以适合所有子对象。如果两者均未设置，则它们将被选择为大致相同，趋于`cols`\> `rows`（仅仅是因为视频的宽度大于高度）。

如果 和`cell_alignment`/`row_alignments`都`col_alignments`被定义，则后者具有更高的优先级。

例子

示例：示例框

![ExampleBoxes-1.png](../_images/ExampleBoxes-1.png)

```py

```


示例：排列网格

![ArrangeInGrid-1.png](../_images/ArrangeInGrid-1.png)

```py

```

array*submobjects ( *\* args* , *\\*\* kwargs\_ )

[`submobjects`]()安排一个小缓冲区的位置。

例子

示例：ArrangeSumobjects 示例

![ArrangeSumobjectsExample-1.png](../_images/ArrangeSumobjectsExample-1.png)

```py

```


成为（_mobject_、 _copy_submobjects = True_、 _match_height = False_、 _match_width = False_、 _match_depth = False_、 _match_center = False_、 _stretch = False_）

编辑点、颜色和子对象以使其与其他对象相同[`Mobject`]()

笔记

如果 match_height 和 match_width 都是，`True`那么转换后将[`Mobject`]() 首先匹配高度，然后匹配宽度

参数

- **match_height** ( _bool_ ) – 如果`True`，则转换后的[`Mobject`]()高度将与原始高度匹配
- **match_width** ( _bool_ ) – 如果`True`，则转换后的宽度[`Mobject`]()将与原始宽度匹配
- **match_depth** ( _bool_ ) – 如果`True`，则转换后的深度[`Mobject`]()将与原始深度匹配
- **match_center** ( _bool_ ) – 如果`True`，则变换后的图像[`Mobject`]()将与原始图像的中心匹配
- **stretch** ( _bool_ ) – 如果`True`，则变换后的图像[`Mobject`]()将拉伸以适合原始图像的比例
- **mobject** ( [_Mobject_]() ) –
- **copy_submobjects** ( _bool_ ) –

例子

示例：成为场景

```py

```


清除更新程序（_递归= True_）

删除所有更新程序。

参数

**recursive** ( _bool_ ) – 是否递归调用`clear_updaters`所有子对象。

退货

`self`

返回类型

[`Mobject`]()

也可以看看

[`remove_updater()`](), [`add_updater()`](),[`get_updaters()`]()

复制( )

创建并返回包含[`Mobject`]()所有 [`submobjects`]().

退货

副本。

返回类型

[`Mobject`]()

参数

**自我**( _T_ ) –

笔记

克隆最初在场景中不可见，即使原始版本可见。

_属性_ 深度

对象的深度。

返回类型

`float`

也可以看看

[`length_over_dim()`]()

翻转(_轴=数组(\[0., 1., 0.\])_ , _\*\* kwargs_ )

围绕其中心翻转/镜像对象。

例子

示例：FlipExample 

![FlipExample-1.png](../_images/FlipExample-1.png)

```py

```


生成点( )

初始化[`points`]()并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

获取所有点( )

返回此 mobject 和所有子 mobject 的所有点。

可能包含重复项；该顺序是子对象的深度优先（前序）遍历。

返回类型

_ndarray_

获取底部( )

获取边界框的底部坐标[`Mobject`]()

返回类型

_ndarray_

获取中心( )

获取中心坐标

返回类型

_ndarray_

获取颜色( )

返回的颜色[`Mobject`]()

get*coord (*暗淡*,*方向= array(\[0., 0., 0.\])\_ )

旨在概括`get_x`,`get_y`和`get_z`

获取角点（_方向_）

获取特定方向的角坐标。

返回类型

_ndarray_

获取关键点（_方向_）

想象一个包围 的盒子[`Mobject`]()。这样的盒子有 9 个“临界点”：4 个角、4 个边缘中心、中心。这将沿着给定方向返回其中之一。

```py

```


获取边缘中心（_方向_）

获取特定方向的边缘坐标。

返回类型

_ndarray_

获取结束( )

返回笔画围绕端点的点[`Mobject`]()。

获取左( )

获取边界框的左坐标[`Mobject`]()

返回类型

_ndarray_

获取合并数组（_数组属性_）

返回此 mobject 和所有子 mobject 的所有给定属性。

可能包含重复项；该顺序是子对象的深度优先（前序）遍历。

返回类型

_ndarray_

获取中点( )

获取形成 的路径中间的坐标 [`Mobject`]()。

例子

示例：角度中点

![AngleMidPoint-1.png](../_images/AngleMidPoint-1.png)

```py

```


返回类型

_ndarray_

_静态_ get_mobject_type_class ( )

返回此 mobject 类型的基类。

获取最低点( )

获取 3D 边界框的最低点（与天顶相对）坐标[`Mobject`]()。

返回类型

_ndarray_

get*point_mobject（*中心=无\_）

最简单的[`Mobject`]()就是转化为自我或转化为自我。应由适当类型的点

获得权利( )

获取边界框的正确坐标[`Mobject`]()

返回类型

_ndarray_

获取开始（）

返回围绕笔划的起始点[`Mobject`]()。

获取开始和结束( )

以 的形式返回笔划的起点和终点`tuple`。

get_time_based_updaters ( )

使用该参数返回所有更新程序`dt`。

更新程序使用此参数作为时间差的输入。

退货

基于时间的更新程序列表。

返回类型

列表\[ `Callable`\]

也可以看看

[`get_updaters()`](),[`has_time_based_updater()`](")

获取顶部( )

获取边界框的顶部坐标[`Mobject`]()

返回类型

_ndarray_

获取更新者( )

返回所有更新程序。

退货

更新者列表。

返回类型

列表\[ `Callable`\]

也可以看看

[`add_updater()`](),[`get_time_based_updaters()`]()

get*x (*方向=数组(\[0., 0., 0.\])\_ )

[`Mobject`]()返回 as 中心的 x 坐标`float`

返回类型

_浮动 64_

get*y (*方向= array(\[0., 0., 0.\])\_ )

[`Mobject`]()返回 as 中心的 y 坐标`float`

返回类型

_浮动 64_

get*z (*方向= array(\[0., 0., 0.\])\_ )

[`Mobject`](")返回 as 中心的 z 坐标`float`

返回类型

_浮动 64_

获取天顶( )

获取 3D 边界框的天顶坐标[`Mobject`]()。

返回类型

_ndarray_

有*无*点( )

检查是否*不*包含点。[`Mobject`]()

返回类型

布尔值

有\_点( )

检查是否[`Mobject`]()包含点。

返回类型

布尔值

has_time_based_updater ( )

测试是否`self`有基于时间的更新程序。

退货

**class** –`True`如果至少有一个更新程序使用该`dt`参数，`False` 否则。

返回类型

布尔值

也可以看看

[`get_time_based_updaters()`]()

_属性_ 高度

mobject 的高度。

返回类型

`float`

例子

示例：高度示例

```py

```


也可以看看

[`length_over_dim()`](")

初始化颜色( )

初始化颜色。

被创造召唤。这是一个空方法，可以由子类实现。

插入（_索引_， _mobject_）

将 mobject 插入到 self.submobjects 的特定位置

实际上只是调用 ，其中有一个列表。` self.submobjects.insert(index, mobject)``self.submobjects `

高度改编自`Mobject.add`.

参数

- **index** ( _int_ ) – 所在索引
- **mobject** ( [_Mobject_]() ) – 要插入的 mobject。

插值（_mobject1_、 _mobject2_、 _alpha_、 _path_func=<函数 插值>_）

将其转换为 和[`Mobject`]()之间的插值。` mobject1``mobject2 `

例子

示例：点插值

![DotInterpolation-1.png](../_images/DotInterpolation-1.png)

```py

```


反转（_递归=假_）

反转 的列表[`submobjects`]()。

参数

**递归**– 如果`True`，则该对象家族的所有子对象列表都将反转。

例子

示例：InvertSumobjectsExample 

```py

```


length*over_dim（*暗淡\_）

[`Mobject`]()测量某个方向上的长度。

匹配颜色（_mobject_）

将颜色与另一个颜色相匹配[`Mobject`]()。

参数

**mobject** ( [_Mobject_]() ) –

match*coord ( \_mobject* ,_昏暗_,_方向= array(\[0., 0., 0.\])_ )

将坐标与另一个 的坐标相匹配[`Mobject`]()。

参数

**mobject** ( [_Mobject_]() ) –

匹配深度（_mobject_， _\*\* kwargs_）

将深度与另一个深度相匹配[`Mobject`]()。

参数

**mobject** ( [_Mobject_]() ) –

match*dim_size ( \_mobject* ,_暗淡_, _\*\* kwargs_ )

将指定的维度与另一个 的维度进行匹配[`Mobject`]()。

参数

**mobject** ( [_Mobject_]() ) –

match*height ( \_mobject* , _\*\* kwargs_ )

将高度与另一个高度匹配[`Mobject`]()。

参数

**mobject** ( [_Mobject_]() ) –

match*points ( \_mobject* , _copy_submobjects = True_ )

编辑点、位置和子对象使其与另一个相同[`Mobject`]()，同时保持样式不变。

例子

示例：比赛点场景

```py

```


参数

- **mobject** ( [_Mobject_]() ) –
- **copy_submobjects** ( _bool_ ) –

match*updaters（\_mobject*）

匹配给定 mobject 的更新程序。

参数

**mobject** ( [_Mobject_]() ) – 更新程序匹配的 mobject。

退货

`self`

返回类型

[`Mobject`]()

笔记

子对象的所有更新程序都将被删除，但仅匹配给定对象的更新程序，而不是其子对象的更新程序。

也可以看看

[`add_updater()`](),[`clear_updaters()`]()

match*width ( \_mobject* , _\*\* kwargs_ )

将宽度与另一个 的宽度匹配[`Mobject`]()。

参数

**mobject** ( [_Mobject_]() ) –

match*x ( \_mobject* ,_方向= array(\[0., 0., 0.\])_ )

匹配 x 坐标。到 x 坐标。另一个[`Mobject`]().

参数

**mobject** ( [_Mobject_]() ) –

match*y ( \_mobject* ,_方向= array(\[0., 0., 0.\])_ )

匹配 y 坐标。到 x 坐标。另一个[`Mobject`]().

参数

**mobject** ( [_Mobject_]() ) –

match*z ( \_mobject* ,_方向= array(\[0., 0., 0.\])_ )

匹配 z 坐标。到 x 坐标。另一个[`Mobject`]().

参数

**mobject** ( [_Mobject_]() ) –

move*to ( \_point_or_mobject* , _aligned_edge = array(\[0., 0., 0.\])_ , _coor_mask = array(\[1, 1, 1\])_ )

将中心移动[`Mobject`]()到某个坐标。

next*to ( \_mobject_or_point*， _Direction = array(\[1., 0., 0.\])_， _buff = 0.25_， _aligned_edge = array(\[0., 0., 0.\])_， _submobject_to_align = None_， _index_of_submobject_to_align = None_， _coor_mask =数组(\[1,1,1 \] )_ )

将其移动到另一个坐标或坐标[`Mobject`]()旁边。[`Mobject`]()

例子

示例：几何形状

![GeometricShapes-1.png](../_images/GeometricShapes-1.png)

```py

```

null*point_align ( \_mobject* )

如果一个[`Mobject`]()有点与一个没有点对齐，则将两者视为组，并将有点的一个推入其自己的子对象列表中。

退货

`self`

返回类型

[`Mobject`]()

参数

**mobject** ( [_Mobject_]() ) –

reduce*across_dimension ( \_reduce_func* ,_暗淡_)

查找此对象和子对象中所有点的维度的最小值或最大值。

参数

**暗淡**（_int_） –

返回类型

漂浮

删除（_\* mobjects_）

删除[`submobjects`]().

mobjects 将从 中删除[`submobjects`]()（如果存在）。

mobject 的子类可以实现`-`和`-=`删除方法。

参数

**mobjects** ( [_Mobject_]() ) – 要删除的 mobject。

退货

`self`

返回类型

[`Mobject`]()

也可以看看

[`add()`]()

删除*更新程序（*更新函数\_）

删除更新程序。

如果多次应用相同的更新程序，则每个实例都会被删除。

参数

**update_function** ( _Union_ _\[_ _Callable_ _\[_ _\[_ [_Mobject_]() _\]_ _,_ _None_ _\]_ _,_ _Callable_ _\[_ _\[_ [_Mobject_]() _,_ _float_ _\]_ _,_ _None_ _\]_ _\]_ ) – 要删除的更新函数。

退货

`self`

返回类型

[`Mobject`]()

也可以看看

[`clear_updaters()`](), [`add_updater()`](),[`get_updaters()`]()

重复（_数_）

这可以使过渡动画更好

参数

**计数**( _int_ ) –

重置点( )

设置[`points`]()为空数组。

恢复( )


恢复之前用 保存的状态[`save_state()`]()。

恢复更新（_递归=真_）

启用从更新程序和动画的更新。

参数

**recursive** ( _bool_ ) – 是否递归地启用所有子对象的更新。

退货

`self`

返回类型

[`Mobject`]()

也可以看看

[`suspend_updating()`](),[`add_updater()`]()

旋转(_角度_,_轴= array(\[0., 0., 1.\])_ , _about_point = None_ , _\*\* kwargs_ )

[`Mobject`]()围绕某个点旋转。

参数

**about_point** (_序列\_\_\[_ _float_ _\]_ _|_ _None_ ) –

rotate*about_origin (*角度*,*轴= array(\[0., 0., 1.\])* ,\*轴= \[\]\_ )

绕原点旋转[`Mobject`]()，原点位于 \[0,0,0\]。

保存图像（_名称=无_）

仅将其所在位置的图像保存[`Mobject`]()到 png 文件中。

保存状态( )

保存当前状态（位置、颜色和大小）。可以用 恢复[`restore()`]()。

比例（_比例因子_， _\*\* kwargs_）

按一个因子缩放大小。

默认行为是围绕 mobject 的中心进行缩放。

参数

- **scale_factor** ( _float_ ) – 比例因子 α。如果 0<|α|<1，mobject 将缩小，并且对于|α|>1 它会成长。此外，如果 α<0，mobject 也被翻转。
- **kwargs** – 传递给 `apply_points_function_about_point()`.

退货

`self`

返回类型

[`Mobject`]()

例子

示例：MobjectScaleExample 

![MobjectScaleExample-1.png](../_images/MobjectScaleExample-1.png)

```py

```

也可以看看

[`move_to()`]()

缩放到适合深度（_深度_， _\*\* kwargs_）

缩放[`Mobject`]()以适应深度，同时保持宽度/高度成比例。

scale_to_fit*height (*高度*, *\*\* kwargs\_ )

缩放[`Mobject`]()以适应高度，同时保持宽度/深度成比例。

退货

`self`

返回类型

[`Mobject`]()

例子

```py

```


scale_to_fit*width（*宽度*， *\*\* kwargs\_）

缩放[`Mobject`]()以适应宽度，同时保持高度/深度成比例。

退货

`self`

返回类型

[`Mobject`]()

例子

```py

```


设置( _\*\* kwargs_ )

设置属性。

即`my_mobject.set(foo=1)`适用。`my_mobject.foo = 1`

[`animate`]()这可以方便地与动画设置属性一起使用。

除了此方法之外，还有一个兼容层，允许使用`get_*`和`set_*`方法获取和设置通用属性。例如：

```py

```


该兼容层不会干扰任何 `get_*`显`set_*`式定义的方法。

警告

此兼容层用于向后兼容，不保证保留。如果适用，请优先选择正常或使用[`set()`]()方法获取/设置属性。

参数

\***\*kwargs** – 要设置的属性和相应的值。

退货

`self`

返回类型

[`Mobject`]()

例子

```py

```


set*color（*颜色= '#FFFF00'*，*系列= True\_）

条件是接受一个参数 (x, y, z) 的函数。这里它只是递归到子对象，但是在子类中，这应该基于颜色的内部工作原理进一步实现

参数

- **颜色**（_颜色_）–
- **家庭**(_布尔_) –

_类方法_ set*default ( *\*\* kwargs\_ )

设置关键字参数的默认值。

如果在没有任何附加关键字参数的情况下调用此方法，则恢复该类的初始化方法的原始默认值。

参数

**kwargs** – 传递任何关键字参数将更新此类初始化函数的关键字参数的默认值。

例子

```py

```


示例：更改默认文本颜色

![ChangedDefaultTextcolor-1.png](../_images/ChangedDefaultTextcolor-1.png)

```py

```

set*x ( \_x* ,_方向= array(\[0., 0., 0.\])_ )

[`Mobject`]()设置(`int`或`float`)中心的 x 值

set*y ( \_y* ,_方向= array(\[0., 0., 0.\])_ )

[`Mobject`]()设置(`int`或`float`)中心的 y 值

set*z ( \_z* ,_方向= array(\[0., 0., 0.\])_ )

[`Mobject`](")设置(`int`或`float`)中心的 z 值

set*z_index ( \_z_index_value* , _family = True_ )

[`Mobject`]()将的设置为 z_index_value`z_index`中指定的值。

参数

- **z_index_value** ( _float_ ) – set 的新值`z_index`。
- **family** ( _bool_ ) – 如果为`True`，`z_index`则还设置所有子对象的值。

退货

Mobject 本身在`z_index`设置之后。用于链接目的。（返回自我。）

返回类型

[`Mobject`]()

例子

示例：SetZIndex 

![SetZIndex-1.png](../_images/SetZIndex-1.png)

```py

```


按 z 坐标设置 z 索引( )

将[`Mobject`]()'sz 坐标设置为 的值`z_index`。

退货

Mobject 本身在`z_index`设置之后。（返回自我。）

返回类型

[`Mobject`]()

移位（_\*向量_）

按给定向量移位。

参数

**向量**( _ndarray_ ) – 要移动的向量。如果给出多个向量，则将它们相加。

退货

`self`

返回类型

[`Mobject`]()

也可以看看

[`move_to()`]()

随机播放（_递归=假_）

随机排列 的列表[`submobjects`]()。

shuffle*submobjects ( *\* args* , *\*\* kwargs\_ )

打乱顺序[`submobjects`]()

例子

示例：ShuffleSubmobjects 示例

```py

```


排序( _point_to_num_func=<function Mobject.<lambda>>_ , _submob_func=None_ )

[`submobjects`]()通过 定义的函数对的列表进行排序`submob_func`。

sort*submobjects ( *\* args* , *\*\* kwargs\_ )

排序[`submobjects`]()

拉伸到适合深度（_深度_， _\*\* kwargs_）

拉伸[`Mobject`]()以适应深度，而不保持宽度/高度成比例。

拉伸到适合高度（_高度_， _\*\* kwargs_）

拉伸[`Mobject`]()以适应高度，而不保持宽度/深度成比例。

退货

`self`

返回类型

[`Mobject`]()

例子

```py

```


拉伸到适合宽度（_宽度_， _\*\* kwargs_）

拉伸[`Mobject`]()以适应宽度，而不保持高度/深度成比例。

退货

`self`

返回类型

[`Mobject`]()

例子

```py

```


暂停更新（_递归= True_）

禁用更新程序和动画的更新。

参数

**recursive** ( _bool_ ) – 是否递归地暂停所有子对象的更新。

退货

`self`

返回类型

[`Mobject`]()

也可以看看

[`resume_updating()`](),[`add_updater()`]()

更新（_dt = 0_，_递归= True_）

应用所有更新程序。

如果更新暂停，则不执行任何操作。

参数

- **dt** ( _float_`dt` ) –传递给更新函数的参数。通常这是自上次调用 以来的时间（以秒为单位）`update`。
- **recursive** ( _bool_ ) – 是否递归更新所有子对象。

退货

`self`

返回类型

[`Mobject`]()

也可以看看

[`add_updater()`](),[`get_updaters()`]()

_属性_ 宽度

mobject 的宽度。

返回类型

`float`

例子

示例：宽度示例

```py

```


也可以看看

[`length_over_dim()`]()
