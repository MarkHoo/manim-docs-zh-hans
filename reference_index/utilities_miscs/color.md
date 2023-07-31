# 颜色[#](#module-manim.utils.color "此标题的固定链接")

用于不同颜色模型之间转换的颜色和实用函数。

课程

[`Colors`](manim.utils.color.Colors.html#manim.utils.color.Colors "manim.utils.color.Colors")

预定义颜色的列表。

功能

平均颜色( _\*颜色_)[\[来源\]](../_modules/manim/utils/color.html#average_color)[#](#manim.utils.color.average_color "此定义的固定链接")

参数

**颜色**（_颜色_）–

返回类型

_颜色_

颜色渐变（_参考颜色_，_输出 ​​ 长度_）[\[来源\]](../_modules/manim/utils/color.html#color_gradient)[#](#manim.utils.color.color_gradient "此定义的固定链接")

参数

- **Reference_colors** (_可迭代**\[**颜色\_\_\]_ ) –
- **输出长度**( _int_ ) –

返回类型

列表\[颜色\]

color_to_int*rgb（*颜色\_）[\[来源\]](../_modules/manim/utils/color.html#color_to_int_rgb)[#](#manim.utils.color.color_to_int_rgb "此定义的固定链接")

参数

**颜色**（_颜色_）–

返回类型

_ndarray_

color_to_int*rgba（*颜色*，*不透明度= 1.0\_）[\[来源\]](../_modules/manim/utils/color.html#color_to_int_rgba)[#](#manim.utils.color.color_to_int_rgba "此定义的固定链接")

参数

- **颜色**（_颜色_）–
- **不透明度**（_浮动_）–

返回类型

_ndarray_

color*to_rgb（*颜色\_）[\[来源\]](../_modules/manim/utils/color.html#color_to_rgb)[#](#manim.utils.color.color_to_rgb "此定义的固定链接")

参数

**颜色**(_颜色\_\_|_ _str_ ) –

返回类型

np.ndarray

color*to_rgba（*颜色*， \_alpha = 1*）[\[来源\]](../_modules/manim/utils/color.html#color_to_rgba)[#](#manim.utils.color.color_to_rgba "此定义的固定链接")

参数

- **颜色**(_颜色\_\_|_ _str_ ) –
- **阿尔法**（_浮动_）–

返回类型

np.ndarray

get*shaded_rgb（\_rgb*，_点_， _unit_normal_vect_， _light_source_）[\[来源\]](../_modules/manim/utils/color.html#get_shaded_rgb)[#](#manim.utils.color.get_shaded_rgb "此定义的固定链接")

参数

- **rgb** ( _ndarray_ ) –
- **点**( _ndarray_ ) –
- **unit_normal_vect** ( _ndarray_ ) –
- **light_source** ( _ndarray_ ) –

返回类型

_ndarray_

hex*to_rgb (*十六进制代码\_)[\[来源\]](../_modules/manim/utils/color.html#hex_to_rgb)[#](#manim.utils.color.hex_to_rgb "此定义的固定链接")

参数

**十六进制代码**( _str_ ) –

返回类型

_ndarray_

interpolate*color (*颜色 1* ,*颜色 2* ,*阿尔法\_)[\[来源\]](../_modules/manim/utils/color.html#interpolate_color)[#](#manim.utils.color.interpolate_color "此定义的固定链接")

参数

- **颜色 1**（_颜色_）–
- **颜色 2**（_颜色_）–
- **阿尔法**（_浮动_）–

返回类型

_颜色_

反转颜色（_颜色_）[\[来源\]](../_modules/manim/utils/color.html#invert_color)[#](#manim.utils.color.invert_color "此定义的固定链接")

参数

**颜色**（_颜色_）–

返回类型

_颜色_

打印常量定义( )[\[来源\]](../_modules/manim/utils/color.html#print_constant_definitions)[#](#manim.utils.color.print_constant_definitions "此定义的固定链接")

用于生成以下常量值的简单函数。要运行它，请将此函数和 Colors 类粘贴到文件中并运行它们。

随机明亮颜色( )[\[来源\]](../_modules/manim/utils/color.html#random_bright_color)[#](#manim.utils.color.random_bright_color "此定义的固定链接")

返回类型

_颜色_

随机颜色( )[\[来源\]](../_modules/manim/utils/color.html#random_color)[#](#manim.utils.color.random_color "此定义的固定链接")

返回类型

_颜色_

rgb*to_color ( \_rgb* )[\[来源\]](../_modules/manim/utils/color.html#rgb_to_color)[#](#manim.utils.color.rgb_to_color "此定义的固定链接")

参数

**rgb** (_可迭代\_\_\[_ _float_ _\]_ ) –

返回类型

_颜色_

rgb*to_hex ( \_rgb* )[\[来源\]](../_modules/manim/utils/color.html#rgb_to_hex)[#](#manim.utils.color.rgb_to_hex "此定义的固定链接")

参数

**rgb** (_可迭代\_\_\[_ _float_ _\]_ ) –

返回类型

斯特

rgba*to_color（\_rgba*）[\[来源\]](../_modules/manim/utils/color.html#rgba_to_color)[#](#manim.utils.color.rgba_to_color "此定义的固定链接")

参数

**rgba** (_可迭代\_\_\[_ _float_ _\]_ ) –

返回类型

_颜色_
