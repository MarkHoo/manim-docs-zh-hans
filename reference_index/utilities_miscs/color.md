# Color

用于不同Color模型之间转换的Color和实用函数。

Classes

|||
|-|-|
[`Colors`]()|预定义Color的列表。

Functions

`average_color(*colors)`

参数

**colors**（_Color_）–

返回类型

_Color_

`color_gradient(reference_colors, length_of_output)`

参数

- **Reference_colors** (_Iterable**\[**Color\_\_\]_ ) –
- **length_of_output**( _int_ ) –

返回类型

list\[Color\]

`color_to_int_rgb(color)`

参数

**color**（_Color_）–

返回类型

_ndarray_

`color_to_int_rgba(color, opacity=1.0)`

参数

- **color**（_Color_）–
- **opacity**（_float_）–

返回类型

_ndarray_

`color_to_rgb(color)`

参数

**color**(_Color\_\_|_ _str_ ) –

返回类型

np.ndarray


`color_to_rgba(color, alpha=1)`

参数

- **color**(_Color\_\_|_ _str_ ) –
- **alpha**（_float_）–

返回类型

np.ndarray


`get_shaded_rgb(rgb, point, unit_normal_vect, light_source)`

参数

- **rgb** ( _ndarray_ ) –
- **point**( _ndarray_ ) –
- **unit_normal_vect** ( _ndarray_ ) –
- **light_source** ( _ndarray_ ) –

返回类型

_ndarray_


`hex_to_rgb(hex_code)`

参数

**hex_code**( _str_ ) –

返回类型

_ndarray_


`interpolate_color(color1, color2, alpha)`

参数

- **Color 1**（_Color_）–
- **Color 2**（_Color_）–
- **alpha**（_float_）–

返回类型

_Color_


`invert_color(color)`

参数

**color**（_Color_）–

返回类型

_Color_


`print_constant_definitions()`

用于生成以下常量值的简单函数。要运行它，请将此函数和 Colors 类粘贴到文件中并运行它们。


`random_bright_color()`

返回类型

_Color_


`random_color()`

返回类型

_Color_


`rgb_to_color(rgb)`

参数

**rgb** (_Iterable\_\_\[_ _float_ _\]_ ) –

返回类型

_Color_


`rgb_to_hex(rgb)`

参数

**rgb** (_Iterable\_\_\[_ _float_ _\]_ ) –

返回类型

str


`rgba_to_color(rgba)`

参数

**rgba** (_Iterable\_\_\[_ _float_ _\]_ ) –

返回类型

_Color_
