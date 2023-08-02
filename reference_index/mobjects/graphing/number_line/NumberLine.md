# 数行

合格名称：`manim.mobject.graphing.number\_line.NumberLine`


```py

```

创建带有刻度线的数轴。

参数

- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) –用于创建线条的值。`[x_min, x_max, x_step]`
- **length** ( _float_ _|_ _None_ ) – 数轴的长度。
- **unit_size** ( _float_ ) – 线条的每个刻度之间的距离。如果指定，则被覆盖`length`。
- **include_ticks** ( _bool_ ) – 是否在数轴上包含刻度。
- **tick_size** ( _float_ ) – 每个刻度线的长度。
- **Numbers_with_elongated_ticks** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 具有拉长刻度的特定值的可迭代。
- **long_tick_multiple** ( _int_ ) – 影响细长刻度比常规刻度大多少倍 (2 = 2x)。
- **旋转**( _float_ ) – 线旋转的角度（以弧度为单位）。
- **stroke_width** ( _float_ ) – 线条的粗细。
- **include_tip** ( _bool_ ) – 是否在行尾添加提示。
- **tip_width** ( _float_ ) – 尖端的宽度。
- **tip_height** ( _float_ ) – 尖端的高度。
- **tip_shape** ( _type_ _\[_ [_ArrowTip_]() _\]_ _|_ _None_ ) – 用于构造提示的 mobject 类，或者`None`（默认）用于默认箭头提示。传递的类必须继承自[`ArrowTip`]().
- **include_numbers** ( _bool_ ) – 是否向刻度线添加数字。小数位数由步长决定，可以通过 覆盖此默认值`decimal_number_config`。
- **缩放**( \__ScaleBase_`x_range` ) –值缩放的方式，即[`LogBase`]()对于对数数轴。默认为[`LinearBase`]().
- **font_size** ( _float_ ) – 标签 mobject 的大小。默认为 36。
- **label_direction** ( _Sequence_ _\[_ _float_ _\]_ ) – 在线上添加标签 mobject 的具体位置。
- **label_constructor** ( [_VMobject_]() ) – 确定将用于构造数轴标签的 mobject 类。
- **line_to_number_buff** ( _float_ ) – 线条和标签 mobject 之间的距离。
- **decimal_number_config** ( _dict_ _|_ _None_ ) – 可以传递[`DecimalNumber`]()以影响数字 mobject 的参数。
- **Numbers_to_exclude** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 不添加到数轴的数字的显式迭代。
- **Numbers_to_include** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 要添加到数轴的数字的显式迭代
- **kwargs** – 要传递给 的附加参数[`Line`]()。
- **except_origin_tick** (_布尔_) –

笔记

包含负值和正值的数字范围将从 0 点生成，并且可能不包含最小/最大值处的刻度，因为刻度位置取决于步长。

例子

示例：NumberLine 示例

![NumberLineExample-1.png](../_images/NumberLineExample-1.png)

```py

```

方法

[`add_labels`]()

[`NumberLine`]()使用向 中添加专门定位的标签`dict`。

[`add_numbers`]()

添加[`DecimalNumber`]()代表其在数轴每个刻度处位置的 mobject。

[`add_ticks`]()

在数轴上添加刻度。

`get_labels`

[`get_number_mobject`]()

生成[`DecimalNumber`]()根据 生成的定位 mobject `label_constructor`。

`get_number_mobjects`

[`get_tick`]()

生成一个刻度并将其沿数轴定位。

`get_tick_marks`

[`get_tick_range`]()

`x_range`根据数轴的属性生成在其上绘制标签的值范围。

`get_unit_size`

`get_unit_vector`

[`n2p`]()

的缩写[`number_to_point()`]()。

[`number_to_point`]()

接受沿数轴的值并返回相对于场景的点。

[`p2n`]()

的缩写[`point_to_number()`]()。

[`point_to_number`]()

接受相对于场景的点并返回沿数轴的浮点数。

`rotate_about_number`

`rotate_about_zero`

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

add*labels ( \_dict_values*，_方向= None_， _buff = None_， _font_size = None_， _label_constructor = None_ )

[`NumberLine`]()使用向 中添加专门定位的标签`dict`。创建后可以通过 访问标签`self.labels`。

参数

- **dict_values** ( _dict_ _\[_ _float_ _,_ _str_ _|_ _float_ _|_ [_VMobject_]() _\]_ ) – 一个字典，由数轴上的位置和要添加的 mobject 组成： 。如果值不是 mobject (或)，则将用于构造标签。` {1: Tex("Monday"), 3: Tex("Tuesday")}``label_constructor``str``float `
- **Direction** ( _Sequence_ _\[_ _float_ _\]_ ) – 确定标签位于线条旁边的方向。
- **buff** ( _float_ _|_ _None_ ) – 标签与线条的距离。
- **font_size** ( _float_ _|_ _None_ ) – 要定位的 mobject 的字体大小。
- **label_constructor** ( [_VMobject_]() _|_ _None_ ) –[`VMobject`]()将用于构造标签的类。如果未指定，则默认`label_constructor`为数轴的属性。

提高

**AttributeError** – 如果标签没有属性`font_size`，`AttributeError`则会引发错误。

add*numbers ( \_x_values = None* ,_排除= None_ , _font_size = None_ , _label_constructor = None_ , _\*\* kwargs_ )

添加[`DecimalNumber`]()代表其在数轴每个刻度处位置的 mobject。创建后可以通过 访问这些号码`self.numbers`。

参数

- **x_values** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 用于定位和创建标签的值的可迭代。默认为由产生的输出[`get_tick_range()`]()
- **排除**( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 要排除的值的列表`x_values`。
- **font_size** ( _float_ _|_ _None_ ) – 标签的字体大小。默认`font_size`为数轴的属性。
- **label_constructor** ( [_VMobject_]() _|_ _None_ ) –[`VMobject`]()将用于构造标签的类。如果未指定，则默认`label_constructor`为数轴的属性。

添加标记( )

在数轴上添加刻度。创建后可以通过 访问蜱虫`self.ticks`。

get*number_mobject ( \_x* ,_方向= None_ , _buff = None_ , _font_size = None_ , _label_constructor = None_ , _\*\* number_config_ )

生成[`DecimalNumber`]()根据 生成的定位 mobject `label_constructor`。

参数

- **x** ( _float_ ) – mobject 应定位的 x 值。
- **Direction** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 确定标签位于线条旁边的方向。
- **buff** ( _float_ _|_ _None_ ) – 标签与线条的距离。
- **font_size** ( _float_ _|_ _None_ ) – 标签 mobject 的字体大小。
- **label_constructor** ( [_VMobject_]() _|_ _None_ ) –[`VMobject`]()将用于构造标签的类。如果未指定，则默认`label_constructor`为数轴的属性。

退货

定位的对象。

返回类型

[`DecimalNumber`]()

get*tick（\_x*，_大小=无_）

生成一个刻度并将其沿数轴定位。

参数

- **x** ( _float_ ) – 刻度线的位置。
- **size** ( _float_ _|_ _None_ ) – 刻度缩放的因子。

退货

定位的刻度线。

返回类型

[`Line`](")

获取刻度范围( )

`x_range`根据数轴的属性生成在其上绘制标签的值范围 。

退货

代表数轴上的值的 numpy 浮点数组。

返回类型

np.ndarray

n2p（_数_）

的缩写[`number_to_point()`]()。

参数

**数字**( _float_ _|_ _np.ndarray_ ) –

返回类型

np.ndarray

到点数量(_数量_)

接受沿数轴的值并返回相对于场景的点。

参数

**number** ( _float_ _|_ _np.ndarray_ ) – 要转换为坐标的值。或者值列表。

退货

相对于场景坐标系的点。或者点列表。

返回类型

np.ndarray

例子

```py

```

p2n（_点_）

的缩写[`point_to_number()`]()。

参数

**点**(_序列\_\_\[_ _float_ _\]_ ) –

返回类型

漂浮

点到数字（_点_）

接受相对于场景的点并返回沿数轴的浮点数。

参数

**point** ( _Sequence_ _\[_ _float_ _\]_ ) – 由 组成的值序列。`(x_coord, y_coord, z_coord)`

退货

表示沿数轴的值的浮点数。

返回类型

漂浮

例子

```py

```
