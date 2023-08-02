# 矩阵

合格名称：`manim.mobject.matrix.Matrix`


```py

```

在屏幕上显示矩阵的 mobject。

例子

第一个示例显示了该模块的各种用途，而第二个示例则说明了选项 add_background_rectangles_to_entries 和 include_background_rectangle 的使用。

示例：矩阵示例

![MatrixExamples-2.png](../_images/MatrixExamples-2.png)

```py

```


示例：背景矩形示例

![BackgroundRectanglesExample-1.png](../_images/BackgroundRectanglesExample-1.png)

```py

```


参数

- **矩阵**( _Iterable_ ) – numpy 二维数组或列表列表。
- **v_buff** ( _float_ ) – 元素之间的垂直距离，默认为 0.8。
- **h_buff** ( _float_ ) – 元素之间的水平距离，默认为 1.3。
- **括号\_h_buff** ( _float_ ) – 默认情况下，括号与矩阵的距离`MED_SMALL_BUFF`。
- **括号\_v_buff** ( _float_ ) – 默认情况下括号的高度`MED_SMALL_BUFF`。
- **add_background_rectangles_to_entries** ( _bool_ ) –`True`默认情况下是否应将背景矩形添加到条目中`False`。
- **include_background_rectangle** ( _bool_ ) –`True`默认情况下是否应包含背景矩形`False`。
- **element_to_mobject** ( _type_ _\[_ [_MathTex_]() _\]_ ) – 默认情况下用于构造元素的 mobject 类[`MathTex`]()。
- **element_to_mobject_config** ( _dict_`element_to_mobject` ) –默认情况下要传递给构造函数的附加参数`{}`。
- **element_alignment_corner** ( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下元素对齐的角点`DR`。
- **left_bracket** ( _str_ ) – 默认情况下左括号类型`"["`。
- **right_bracket** ( _str_ ) – 默认情况下右括号类型`"]"`。
- **stretch_brackets** ( _bool_ ) –`True`默认情况下是否应该拉伸括号以适应矩阵内容的高度`True`。
- **括号\_config** ( _dict_[`MathTex`]() ) –构造括号时要传递的附加参数。

方法

[`add_background_to_entries`]()

将黑色背景矩形添加到矩阵中，请参阅上面的示例。

[`get_brackets`]()

返回括号 mobject。

[`get_columns`]()

将矩阵的列返回为 VGroup。

[`get_entries`]()

返回矩阵的各个条目。

[`get_mob_matrix`]()

返回底层的生物矩阵 mobjects。

[`get_rows`]()

返回矩阵的行作为 VGroup。

[`set_column_colors`]()

为矩阵的每一列设置单独的颜色。

[`set_row_colors`]()

为矩阵的每一行设置单独的颜色。

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

添加背景到条目( )

将黑色背景矩形添加到矩阵中，请参阅上面的示例。

退货

当前矩阵对象（自身）。

返回类型

[`Matrix`]()

获取括号( )

返回括号 mobject。

退货

每个 VGroup 包含一个括号

返回类型

列表\[ [`VGroup`]()\]

例子

示例：GetBracketsExample 

![GetBracketsExample-1.png](../_images/GetBracketsExample-1.png)

```py

```


获取列( )

将矩阵的列返回为 VGroup。

退货

每个 VGroup 包含矩阵的一列。

返回类型

列表\[ [`VGroup`]()\]

例子

示例：获取列示例

![GetColumnsExample-1.png](../_images/GetColumnsExample-1.png)

```py

```


获取条目( )

返回矩阵的各个条目。

退货

包含矩阵条目的 VGroup。

返回类型

[`VGroup`]()

例子

示例：GetEntriesExample 

![GetEntriesExample-1.png](../_images/GetEntriesExample-1.png)

```py

```


获取生物矩阵( )

返回底层的生物矩阵 mobjects。

退货

每个 VGroup 包含矩阵的一行。

返回类型

列表\[ [`VGroup`]()\]

获取行数( )

返回矩阵的行作为 VGroup。

退货

每个 VGroup 包含矩阵的一行。

返回类型

列表\[ [`VGroup`]()\]

例子

示例：GetRowsExample 

![GetRowsExample-1.png](../_images/GetRowsExample-1.png)

```py

```


set*column_colors ( *\*颜色\_)

为矩阵的每一列设置单独的颜色。

参数

**颜色**( _str_ ) – 颜色列表；指定的每种颜色对应于一列。

退货

当前矩阵对象（自身）。

返回类型

[`Matrix`]()

例子

示例：SetColumnColorsExample 

![SetColumnColorsExample-1.png](../_images/SetColumnColorsExample-1.png)

```py

```

set*row_colors ( *\*颜色\_)

为矩阵的每一行设置单独的颜色。

参数

**颜色**( _str_ ) – 颜色列表；指定的每种颜色对应一行。

退货

当前矩阵对象（自身）。

返回类型

[`Matrix`]()

例子

示例：SetRowColorsExample 

![SetRowColorsExample-1.png](../_images/SetRowColorsExample-1.png)

```py

```
