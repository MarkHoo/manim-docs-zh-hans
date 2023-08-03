# SVGM 对象

合格名称：`manim.mobject.svg.svg\_mobject.SVGMobject`


```py
class SVGMobject(file_name=None, should_center=True, height=2, width=None, color=None, opacity=None, fill_color=None, fill_opacity=None, stroke_color=None, stroke_opacity=None, stroke_width=None, svg_default=None, path_string_config=None, use_svg_cache=True, **kwargs)
```

Bases: `VMobject`

通过导入 SVG 文件创建的矢量化对象。

参数

- **file_name** ( _str_ _|_ _os.PathLike_ _|_ _None_ ) – SVG 文件的路径。
- **should_center** ( _bool_ ) – 导入后 mobject 是否应居中。
- **height** ( _float_ _|_ _None_ ) – mobject 的目标高度，默认设置为 2 Manim 单位。如果高度和宽度都设置为`None`，则导入 mobject 时不会进行缩放。
- **width** ( _float_ _|_ _None_ ) – mobject 的目标宽度，`None`默认设置为。如果高度和宽度都设置为`None`，则导入 mobject 时不会进行缩放。
- **color** ( _str_ _|_ _None_ ) – mobject 的颜色（填充颜色和描边颜色）。如果 `None`（默认），则使用 SVG 文件中设置的颜色。
- **opacity** ( _float_ _|_ _None_ ) – mobject 的不透明度（填充和描边不透明度）。如果`None`（默认），则使用 SVG 文件中设置的不透明度。
- **fill_color** ( _str_ _|_ _None_ ) – mobject 的填充颜色。如果`None`（默认），则使用 SVG 文件中设置的填充颜色。
- **fill_opacity** ( _float_ _|_ _None_ ) – mobject 的填充不透明度。如果`None`（默认），则使用 SVG 文件中设置的填充不透明度。
- **stroke_color** ( _str_ _|_ _None_ ) – mobject 的描边颜色。如果`None`（默认），则使用 SVG 文件中设置的描边颜色。
- **stroke_opacity** ( _float_ _|_ _None_ ) – mobject 的描边不透明度。如果`None`（默认），则使用 SVG 文件中设置的描边不透明度。
- **stroke_width** ( _float_ _|_ _None_ ) – mobject 的描边宽度。如果`None`（默认），则使用 SVG 文件中设置的描边宽度值。
- **svg_default** ( _dict_ _|_ _None_ ) – 一个字典，其中定义了 SVG 文件中元素的未指定属性的后备值。如果 `None`（默认），`color`、`opacity`、`fill_color` `fill_opacity`、`stroke_color`、 和`stroke_opacity` 设置为`None`，并且`stroke_width`设置为 0。
- **path_string_config** ( _dict_ _|_ _None_[`VMobjectFromSVGPath`]() ) – 带有传递给用于导入路径元素的关键字参数的字典 。如果`None`（默认），则不传递任何附加参数。
- **use_svg_cache** ( _bool_ ) – 如果 True （默认），svg 输入（例如 file_name、设置）将用作键，并且将使用该键保存创建的 mobject 的副本，以便在需要处理相同输入时快速检索之后。对于仅使用一次的大型 SVG，可以省略此操作以提高性能。
- **kwargs** – 传递给父类的进一步参数。

方法

|||
|-|-|
[`apply_style_to_mobject`]()|将 SVG 样式信息应用到转换后的 mobject。
[`ellipse_to_mobject`]()|将椭圆或圆形元素转换为矢量化对象。
[`generate_config_style_dict`]()|生成一个包含默认样式信息的字典。
[`generate_mobject`]()|解析 SVG 并将其元素转换为子对象。
[`get_file_path`]()|根据指定的文件名搜索现有文件。
[`get_mobjects_from`]()|将 SVG 的元素转换为 mobject 列表。
[`handle_transform`]()|将 SVG 转换应用于转换后的 mobject。
[`init_svg_mobject`]()|检查 SVG 是否已导入，如果没有则生成它。
[`line_to_mobject`]()|将线元素转换为矢量化对象。
[`modify_xml_tree`]()|修改 SVG 元素树以包含默认样式信息。
[`move_into_position`]()|缩放生成的 mobject 并将其移动到位。
[`path_to_mobject`]()|将路径元素转换为矢量化 mobject。
[`polygon_to_mobject`]()|将多边形元素转换为矢量化对象。
[`polyline_to_mobject`]()|将折线元素转换为矢量化对象。
[`rect_to_mobject`]()|将矩形元素转换为矢量化对象。
[`text_to_mobject`]()|将文本元素转换为矢量化对象。


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
[`hash_seed`]()|表示生成的对象点结果的唯一哈希值。
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


`static apply_style_to_mobject(mob, shape)`

将 SVG 样式信息应用到转换后的 mobject。

参数

- **mob** ( [_VMobject_]() ) – 转换后的 mobject。
- **shape** ( _GraphicObject_ ) – 已解析的 SVG 元素。

返回类型

[_VMobject_]()


`static ellipse_to_mobject(ellipse)`

将椭圆或圆形元素转换为矢量化对象。

参数

**ellipse** ( _se.Ellipse_ _|_ _se.Circle_ ) – 解析的 SVG 椭圆或圆。

返回类型

[Circle]()


`generate_config_style_dict()`

生成一个包含默认样式信息的字典。

返回类型

dict\[str, str\]


`generate_mobject()`

解析 SVG 并将其元素转换为子对象。

返回类型

None


`get_file_path()`

根据指定的文件名搜索现有文件。

返回类型

_Path_


`get_mobjects_from(svg)`

将 SVG 的元素转换为 mobject 列表。

参数

**svg** ( _se.SVG_ ) – 解析后的 SVG 文件。

返回类型

list\[ [VMobject]() \]


`static handle_transform(mob, matrix)`

将 SVG 转换应用于转换后的 mobject。

参数

- **mob** ( [_VMobject_]() ) – 转换后的 mobject。
- **matrix**( _Matrix_ ) – 由 SVG 变换确定的变换矩阵。

返回类型

[_VMobject_]()


_属性_ hash_seed: tuple

表示生成的对象点结果的唯一哈希值。

用作`SVG_HASH_TO_MOB_MAP`缓存字典中的键。



`init_svg_mobject(use_svg_cache)`

检查 SVG 是否已导入，如果没有则生成它。


> 也可以看看

> [`SVGMobject.generate_mobject()`]()

参数

**use_svg_cache** ( _bool_ ) –

返回类型

None


`static line_to_mobject(line)`

将线元素转换为矢量化对象。

参数

**line** ( _Line_ ) – 已解析的 SVG 行。

返回类型

[_Line_]()


`modify_xml_tree(element_tree)`

修改 SVG 元素树以包含默认样式信息。

参数

**element_tree** ( _ElementTree_ ) – 从 SVG 文件解析的元素树。

返回类型

_ElementTree_



`move_into_position()`

缩放生成的 mobject 并将其移动到位。

返回类型

None


`path_to_mobject(path)`

将路径元素转换为矢量化 mobject。

参数

**path** ( _Path_ ) – 解析的 SVG 路径。

返回类型

[_VMobjectFromSVGPath_]()



`static polygon_to_mobject(polygon)`

将多边形元素转换为矢量化对象。

参数

**Polygon** ( _Polygon_ ) – 解析的 SVG 多边形。

返回类型

[_Polygon_]()


`polyline_to_mobject(polyline)`

将折线元素转换为矢量化对象。

参数

**polyline**( _Polyline_ ) – 解析的 SVG 折线。

返回类型

[_VMobject_]()



`static rect_to_mobject(rect)`

将矩形元素转换为矢量化对象。

参数

**rect** ( _Rect_ ) – 解析后的 SVG 矩形。

返回类型

[_Rectangle_]()


`static text_to_mobject(text)`

将文本元素转换为矢量化对象。

> 警告

> 尚未实现。

参数

**text** ( _Text_ ) – 解析的 SVG 文本。
