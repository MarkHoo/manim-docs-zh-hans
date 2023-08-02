# 小数

合格名称：`manim.mobject.text.numbers.DecimalNumber`


```py

```

表示十进制数的 mobject。

例子

示例：MovingSquareWithUpdaters 

```py

```


方法

`get_value`

`increment_value`

[`set_value`](#manim.mobject.text.numbers.DecimalNumber.set_value "manim.mobject.text.numbers.DecimalNumber.set_value")

将 的值设置[`DecimalNumber`](#manim.mobject.text.numbers.DecimalNumber "manim.mobject.text.numbers.DecimalNumber")为新数字。

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

[`font_size`](#manim.mobject.text.numbers.DecimalNumber.font_size "manim.mobject.text.numbers.DecimalNumber.font_size")

tex mobject 的字体大小。

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。

参数

- **数字**（_浮点数_）–
- **num_decimal_places** ( _int_ ) –
- **mob_class** ( [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) –
- **include_sign** (_布尔_) –
- **group_with_commas** ( _bool_ ) –
- **digital_buff_per_font_unit** (_浮点数_) –
- **show_ellipsis** (_布尔_) –
- **单位**( _str_ _|\_\_无_) –
- **include_background_rectangle** (_布尔_) –
- **edge_to_fix** (_序列\_\_\[_ _float_ _\]_ ) –
- **字体大小**（_浮动_）–
- **笔画宽度**（_浮动_）-
- **fill_opacity** (_浮动_) –

_属性_ 字体大小[#](#manim.mobject.text.numbers.DecimalNumber.font_size "此定义的固定链接")

tex mobject 的字体大小。

设置值（_数字_）[\[来源\]](../_modules/manim/mobject/text/numbers.html#DecimalNumber.set_value)[#](#manim.mobject.text.numbers.DecimalNumber.set_value "此定义的固定链接")

将 的值设置[`DecimalNumber`](#manim.mobject.text.numbers.DecimalNumber "manim.mobject.text.numbers.DecimalNumber")为新数字。

参数

**number** ( _float_ ) – 将覆盖 的当前编号的值[`DecimalNumber`](#manim.mobject.text.numbers.DecimalNumber "manim.mobject.text.numbers.DecimalNumber")。
