# 表

合格名称：`manim.mobject.table.Table`


```py

```

在屏幕上显示表格的 mobject。

例子

示例：表示例

![TableExamples-2.png](../_images/TableExamples-2.png)

```py

```


示例：背景矩形示例[¶](#backgroundrectanglesexample)

![../_images/BackgroundRectanglesExample-2.png](../_images/BackgroundRectanglesExample-2.png)

```py

```


参数

- **table** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _|_ _str_ _|_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _\]_ ) – 2D 数组或列表列表。表的内容必须是 中可调用集的有效输入`element_to_mobject`。
- **row_labels** ( _Iterable_ _\[_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _|_ _None_ ) –[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")表示每行标签的列表。
- **col_labels** ( _Iterable_ _\[_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _|_ _None_ ) –[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")表示每列标签的列表。
- **top_left_entry** ( [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _|_ _None_ ) – 仅当给出行和列标签时才能指定表的左上角条目。
- **v_buff** ( _float_ ) – 传递给的垂直缓冲区[`arrange_in_grid()`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.arrange_in_grid "manim.mobject.mobject.Mobject.arrange_in_grid")，默认为 0.8。
- **h_buff** ( _float_ ) – 传递给的水平缓冲区[`arrange_in_grid()`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.arrange_in_grid "manim.mobject.mobject.Mobject.arrange_in_grid")，默认为 1.3。
- **include_outer_lines** ( _bool_ ) –`True`表格是否应包含外部行，默认为 False。
- **add_background_rectangles_to_entries** ( _bool_ ) –`True`默认情况下是否应将背景矩形添加到条目中`False`。
- **Entrys_background_color** ( _Color_ ) – 条目的背景颜色（如果`add_background_rectangles_to_entries`是）`True`。
- **include_background_rectangle** ( _bool_ ) –`True`默认情况下表格是否应该有一个背景矩形`False`。
- **background_rectangle_color** ( _Color_ ) – 表格的背景颜色（如果`include_background_rectangle`是）`True`。
- **element_to_mobject** ( _Callable_ _\[_ _\[_ _float_ _|_ _str_ _|_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _,_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ ) –[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")应用于表条目的类。默认情况下[`Paragraph`](manim.mobject.text.text_mobject.Paragraph.html#manim.mobject.text.text_mobject.Paragraph "manim.mobject.text.text_mobject.Paragraph")。对于常见的选择，请参阅[`text_mobject`](manim.mobject.text.text_mobject.html#module-manim.mobject.text.text_mobject "manim.mobject.text.text_mobject")/ [`tex_mobject`](manim.mobject.text.tex_mobject.html#module-manim.mobject.text.tex_mobject "manim.mobject.text.tex_mobject")。
- **element_to_mobject_config** ( _dict_ ) – 自定义配置传递到`element_to_mobject`，默认为 {}。
- **range_in_grid_config** ( _dict_ ) – 传递给 的 Dict [`arrange_in_grid()`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.arrange_in_grid "manim.mobject.mobject.Mobject.arrange_in_grid")，自定义表格的排列。
- **line_config** ( _dict_ ) – 传递给 的 Dit [`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")，自定义表格的行。
- **kwargs** – 要传递给 的附加参数[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")。

方法

[`add_background_to_entries`](#manim.mobject.table.Table.add_background_to_entries "manim.mobject.table.Table.add_background_to_entries")

[`BackgroundRectangle`](manim.mobject.geometry.shape_matchers.BackgroundRectangle.html#manim.mobject.geometry.shape_matchers.BackgroundRectangle "manim.mobject.geometry.shape_matchers.BackgroundRectangle")向表的每个条目添加黑色。

[`add_highlighted_cell`](#manim.mobject.table.Table.add_highlighted_cell "manim.mobject.table.Table.add_highlighted_cell")

通过添加 . 突出显示表格中特定位置的一个单元格[`BackgroundRectangle`](manim.mobject.geometry.shape_matchers.BackgroundRectangle.html#manim.mobject.geometry.shape_matchers.BackgroundRectangle "manim.mobject.geometry.shape_matchers.BackgroundRectangle")。

[`create`](#manim.mobject.table.Table.create "manim.mobject.table.Table.create")

定制的表创建类型函数。

[`get_cell`](#manim.mobject.table.Table.get_cell "manim.mobject.table.Table.get_cell")

[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon")以不带条目的矩形形式返回一个特定单元格。

[`get_col_labels`](#manim.mobject.table.Table.get_col_labels "manim.mobject.table.Table.get_col_labels")

返回表的列标签。

[`get_columns`](#manim.mobject.table.Table.get_columns "manim.mobject.table.Table.get_columns")

将表的列返回为 a [`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")of [`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")。

[`get_entries`](#manim.mobject.table.Table.get_entries "manim.mobject.table.Table.get_entries")

返回表中的各个条目（包括标签）或一个特定条目（如果`pos`设置了参数 ）。

[`get_entries_without_labels`](#manim.mobject.table.Table.get_entries_without_labels "manim.mobject.table.Table.get_entries_without_labels")

返回表中的各个条目（不带标签）或一个特定条目（如果`pos`设置了参数 ）。

[`get_highlighted_cell`](#manim.mobject.table.Table.get_highlighted_cell "manim.mobject.table.Table.get_highlighted_cell")

返回[`BackgroundRectangle`](manim.mobject.geometry.shape_matchers.BackgroundRectangle.html#manim.mobject.geometry.shape_matchers.BackgroundRectangle "manim.mobject.geometry.shape_matchers.BackgroundRectangle")给定位置的单元格的 a。

[`get_horizontal_lines`](#manim.mobject.table.Table.get_horizontal_lines "manim.mobject.table.Table.get_horizo​​ntal_lines")

返回表格的水平线。

[`get_labels`](#manim.mobject.table.Table.get_labels "manim.mobject.table.Table.get_labels")

返回表的标签。

[`get_row_labels`](#manim.mobject.table.Table.get_row_labels "manim.mobject.table.Table.get_row_labels")

返回表的行标签。

[`get_rows`](#manim.mobject.table.Table.get_rows "manim.mobject.table.Table.get_rows")

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")以 a of 形式返回表的行[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")。

[`get_vertical_lines`](#manim.mobject.table.Table.get_vertical_lines "manim.mobject.table.Table.get_vertical_lines")

返回表格的垂直线。

[`scale`](#manim.mobject.table.Table.scale "manim.mobject.table.Table.scale")

按一个因子缩放大小。

[`set_column_colors`](#manim.mobject.table.Table.set_column_colors "manim.mobject.table.Table.set_column_colors")

为表的每一列设置单独的颜色。

[`set_row_colors`](#manim.mobject.table.Table.set_row_colors "manim.mobject.table.Table.set_row_colors")

为表格的每一行设置单独的颜色。

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

添加背景到条目（_颜色= '#000000'_）[\[来源\]](../_modules/manim/mobject/table.html#Table.add_background_to_entries)[#](#manim.mobject.table.Table.add_background_to_entries "此定义的固定链接")

[`BackgroundRectangle`](manim.mobject.geometry.shape_matchers.BackgroundRectangle.html#manim.mobject.geometry.shape_matchers.BackgroundRectangle "manim.mobject.geometry.shape_matchers.BackgroundRectangle")向表的每个条目添加黑色。

参数

**颜色**（_颜色_）–

返回类型

[_桌子_](#manim.mobject.table.Table "manim.mobject.table.Table")

add*highlighted_cell ( \_pos = (1, 1)* , _color = '#FFFF00'_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/table.html#Table.add_highlighted_cell)[#](#manim.mobject.table.Table.add_highlighted_cell "此定义的固定链接")

通过添加 . 突出显示表格中特定位置的一个单元格[`BackgroundRectangle`](manim.mobject.geometry.shape_matchers.BackgroundRectangle.html#manim.mobject.geometry.shape_matchers.BackgroundRectangle "manim.mobject.geometry.shape_matchers.BackgroundRectangle")。

参数

- **pos** ( _Sequence_ _\[_ _int_ _\]_ ) – 表中特定条目的位置。`(1,1)`是表格的左上角条目。
- **颜色**( _Color_ ) – 用于突出显示单元格的颜色。
- **kwargs** – 要传递给 的附加参数[`BackgroundRectangle`](manim.mobject.geometry.shape_matchers.BackgroundRectangle.html#manim.mobject.geometry.shape_matchers.BackgroundRectangle "manim.mobject.geometry.shape_matchers.BackgroundRectangle")。

返回类型

[_桌子_](#manim.mobject.table.Table "manim.mobject.table.Table")

例子

示例：AddHighlightedCellExample [¶](#addhighlightedcellexample)

![../_images/AddHighlightedCellExample-1.png](../_images/AddHighlightedCellExample-1.png)

```py

```


创建（_lag_ratio=1_、 _line_animation=<class 'manim.animation.creation.Create'>_、 _label_animation=<class 'manim.animation.creation.Write'>_、 _element_animation=<class 'manim.animation.creation.Create'>_， _entry_animation=<类 'manim.animation.fading.FadeIn'>_， _\*\*kwargs_）[\[来源\]](../_modules/manim/mobject/table.html#Table.create)[#](#manim.mobject.table.Table.create "此定义的固定链接")

定制的表创建类型函数。

参数

- **lag_ratio** ( _float_ ) – 动画的滞后比率。
- **line_animation** ( _Callable_ _\[_ _\[_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _|_ [_VGroup_](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup") _\]_ _,_ [_Animation_](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation") _\]_ ) – 表格线的动画样式，请参阅[`creation`](manim.animation.creation.html#module-manim.animation.creation "动画创作")示例。
- **label_animation** ( _Callable_ _\[_ _\[_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _|_ [_VGroup_](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup") _\]_ _,_ [_Animation_](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation") _\]_ ) – 表格标签的动画样式，请参阅[`creation`](manim.animation.creation.html#module-manim.animation.creation "动画创作")示例。
- **element_animation** ( _Callable_ _\[_ _\[_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _|_ [_VGroup_](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup") _\]_ _,_ [_Animation_](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation") _\]_ ) – 表格元素的动画样式，请参阅[`creation`](manim.animation.creation.html#module-manim.animation.creation "动画创作")示例。
- **Entry_animation** ( _Callable_ _\[_ _\[_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _|_ [_VGroup_](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup") _\]_ _,_ [_Animation_](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation") _\]_ ) – 表格背景的入口动画，请参见[`creation`](manim.animation.creation.html#module-manim.animation.creation "动画创作")示例。
- **kwargs** – 传递给创建动画的进一步参数。

退货

包含线条和元素创建的动画组。

返回类型

[`AnimationGroup`](manim.animation.composition.AnimationGroup.html#manim.animation.composition.AnimationGroup "manim.animation.composition.AnimationGroup")

例子

示例：创建表示例[¶](#createtableexample)

```py

```


get*cell ( \_pos = (1, 1)* , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_cell)[#](#manim.mobject.table.Table.get_cell "此定义的固定链接")

[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon")以不带条目的矩形形式返回一个特定单元格。

参数

- **pos** ( _Sequence_ _\[_ _int_ _\]_ ) – 表中特定条目的位置。`(1,1)`是表格的左上角条目。
- **kwargs** – 要传递给 的附加参数[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon")。

退货

模仿表格中一个特定单元格的多边形。

返回类型

[`Polygon`](manim.mobject.geometry.polygram.Polygon.html#manim.mobject.geometry.polygram.Polygon "manim.mobject.geometry.polygram.Polygon")

例子

示例：获取单元格示例[¶](#getcellexample)

![../_images/GetCellExample-1.png](../_images/GetCellExample-1.png)

```py

```

获取*列*标签( )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_col_labels)[#](#manim.mobject.table.Table.get_col_labels "此定义的固定链接")

返回表的列标签。

退货

包含表的列标签的 VGroup。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：GetColLabelsExample [¶](#getcollabelsexample)

![../_images/GetColLabelsExample-1.png](../_images/GetColLabelsExample-1.png)

```py

```


获取列( )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_columns)[#](#manim.mobject.table.Table.get_columns "此定义的固定链接")

将表的列返回为 a [`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")of [`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")包含 a 中的每一列[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：获取列示例[¶](#getcolumnsexample)

![../_images/GetColumnsExample-2.png](../_images/GetColumnsExample-2.png)

```py

```

get*entries ( \_pos =无*)[\[来源\]](../_modules/manim/mobject/table.html#Table.get_entries)[#](#manim.mobject.table.Table.get_entries "此定义的固定链接")

返回表中的各个条目（包括标签）或一个特定条目（如果`pos`设置了参数 ）。

参数

**pos** ( _Sequence_ _\[_ _int_ _\]_ _|_ _None_ ) – 表中特定条目的位置。`(1,1)`是表格的左上角条目。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")包含表的所有条目（包括标签）或[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")给定位置的 if`pos`已设置。

返回类型

联盟\[ [`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject"), [`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")\]

例子

示例：GetEntriesExample [¶](#getentriesexample)

![../_images/GetEntriesExample-2.png](../_images/GetEntriesExample-2.png)

```py

```


get_entries_without*labels ( \_pos = None* )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_entries_without_labels)[#](#manim.mobject.table.Table.get_entries_without_labels "此定义的固定链接")

返回表中的各个条目（不带标签）或一个特定条目（如果`pos`设置了参数 ）。

参数

**pos** ( _Sequence_ _\[_ _int_ _\]_ _|_ _None_ ) – 表中特定条目的位置。`(1,1)`是表格的左上角条目（没有标签）。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")包含表的所有条目（无标签）或[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")在给定位置 if`pos`已设置。

返回类型

联盟\[ [`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject"), [`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")\]

例子

示例：GetEntriesWithoutLabelsExample [¶](#getentrieswithoutlabelsexample)

![../_images/GetEntriesWithoutLabelsExample-1.png](../_images/GetEntriesWithoutLabelsExample-1.png)

```py

```


get*highlighted_cell ( \_pos = (1, 1)* , _color = '#FFFF00'_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_highlighted_cell)[#](#manim.mobject.table.Table.get_highlighted_cell "此定义的固定链接")

返回[`BackgroundRectangle`](manim.mobject.geometry.shape_matchers.BackgroundRectangle.html#manim.mobject.geometry.shape_matchers.BackgroundRectangle "manim.mobject.geometry.shape_matchers.BackgroundRectangle")给定位置的单元格的 a。

参数

- **pos** ( _Sequence_ _\[_ _int_ _\]_ ) – 表中特定条目的位置。`(1,1)`是表格的左上角条目。
- **颜色**( _Color_ ) – 用于突出显示单元格的颜色。
- **kwargs** – 要传递给 的附加参数[`BackgroundRectangle`](manim.mobject.geometry.shape_matchers.BackgroundRectangle.html#manim.mobject.geometry.shape_matchers.BackgroundRectangle "manim.mobject.geometry.shape_matchers.BackgroundRectangle")。

返回类型

[_背景矩形_](manim.mobject.geometry.shape_matchers.BackgroundRectangle.html#manim.mobject.geometry.shape_matchers.BackgroundRectangle "manim.mobject.geometry.shape_matchers.BackgroundRectangle")

例子

示例：获取 HighlightedCellExample [¶](#gethighlightedcellexample)

![../_images/GetHighlightedCellExample-1.png](../_images/GetHighlightedCellExample-1.png)

```py

```


获取水平线( )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_horizontal_lines)[#](#manim.mobject.table.Table.get_horizontal_lines "此定义的固定链接")

返回表格的水平线。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")包含表格的所有水平线。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：获取水平线示例[¶](#gethorizontallinesexample)

![../_images/GetHorizo​​ntalLinesExample-1.png](../_images/GetHorizontalLinesExample-1.png)

```py

```


获取标签( )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_labels)[#](#manim.mobject.table.Table.get_labels "此定义的固定链接")

返回表的标签。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")包含表的所有标签。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：GetLabelsExample

![../_images/GetLabelsExample-1.png](../_images/GetLabelsExample-1.png)

```py

```

获取行标签( )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_row_labels)[#](#manim.mobject.table.Table.get_row_labels "此定义的固定链接")

返回表的行标签。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")包含表的行标签。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：GetRowLabelsExample 

![../_images/GetRowLabelsExample-1.png](../_images/GetRowLabelsExample-1.png)

```py

```

获取行数( )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_rows)[#](#manim.mobject.table.Table.get_rows "此定义的固定链接")

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")以 a of 形式返回表的行[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")包含 a 中的每一行[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：GetRowsExample 

![../_images/GetRowsExample-2.png](../_images/GetRowsExample-2.png)

```py

```

获取垂直线( )[\[来源\]](../_modules/manim/mobject/table.html#Table.get_vertical_lines)[#](#manim.mobject.table.Table.get_vertical_lines "此定义的固定链接")

返回表格的垂直线。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")包含表格的所有垂直线。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子

示例：获取垂直线示例[¶](#getverticallinesexample)

![../_images/GetVerticalLinesExample-1.png](../_images/GetVerticalLinesExample-1.png)

```py

```


比例（_比例因子_， _\*\* kwargs_）

按一个因子缩放大小。

默认行为是围绕 mobject 的中心进行缩放。

参数

- **scale_factor** ( _float_ ) – 比例因子 α。如果 0<|α|<1，mobject 将缩小，并且对于|α|>1 它会成长。此外，如果 α<0，mobject 也被翻转。
- **kwargs** – 传递给 `apply_points_function_about_point()`.

退货

`self`

返回类型

`Mobject`

例子

示例：MobjectScaleExample 

![MobjectScaleExample-2.png](../_images/MobjectScaleExample-2.png)

```py

```


也可以看看

`move_to()`

set*column_colors ( *\*颜色\_)[\[来源\]](../_modules/manim/mobject/table.html#Table.set_column_colors)[#](#manim.mobject.table.Table.set_column_colors "此定义的固定链接")

为表的每一列设置单独的颜色。

参数

**颜色**( _Iterable_ _\[_ _Color_ _\]_ ) – 颜色的可迭代；每种颜色对应一列。

返回类型

[_桌子_](#manim.mobject.table.Table "manim.mobject.table.Table")

例子

示例：SetColumnColorsExample [¶](#setcolumncolorsexample)

![../_images/SetColumnColorsExample-2.png](../_images/SetColumnColorsExample-2.png)

```py

```

set*row_colors ( *\*颜色\_)[\[来源\]](../_modules/manim/mobject/table.html#Table.set_row_colors)[#](#manim.mobject.table.Table.set_row_colors "此定义的固定链接")

为表格的每一行设置单独的颜色。

参数

**颜色**( _Iterable_ _\[_ _Color_ _\]_ ) – 颜色的可迭代；每种颜色对应一行。

返回类型

[_桌子_](#manim.mobject.table.Table "manim.mobject.table.Table")

例子

示例：SetRowColorsExample [¶](#setrowcolorsexample)

![../_images/SetRowColorsExample-2.png](../_images/SetRowColorsExample-2.png)

```py

```
