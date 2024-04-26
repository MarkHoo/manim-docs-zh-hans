# core

Manim 的（内部）颜色数据结构和一些用于颜色转换的实用程序。

该模块包含 的实现[`ManimColor`]()，内部用于表示颜色的数据结构。

使用这些颜色的首选方法是从 manim 导入它们的常量：

```sh
>>> from manim import RED, GREEN, BLUE
>>> print(RED)
#FC6255
```

请注意，这种方式使用大写的颜色名称。

笔记

“C”类型的颜色有一个别名，等于不带字母的颜色名称，例如 GREEN = GREEN_C

模块属性

`ParsableManimColor`

ParsableManimColor 是可解析为 manim 中颜色的所有类型的表示形式

课程

[`ManimColor`]()

颜色的内部表示。

功能

平均颜色( _\*颜色_)

确定给定参数的平均颜色

返回：

输入的平均颜色

返回类型：

[Manim色彩]()

参数：

**颜色**( _Union_ _\[_ [_ManimColor_]() _,_ _int_ _,_ _str_ _,**元组**\[_ _int_ _,_ _int_ _,_ _int_ _\]_ _,**元组**\[_ _float_ _,_ _float_ _,_ _float_ _\]_ _,**元组**\[_ _int_ _,_ _int_ _,_ _int_ _,_ _int_ _\]_ _,**元组**\[_ _float_ _,_ _float_ _,_ _float_ _,_ _float_ _\]_ _,_ _ndarray_ _\[**任何**,_ _dtype_ _\[_ _int64_ _\]_ _\]_ _,_ _ndarray_ _\[**任何**,_ _dtype_ _\[_ _float64_ _\]_ _\]_ _\]_ ) –

颜色渐变（_参考颜色_，_输出​​长度_）

创建在输入颜色数组与特定颜色数量之间插值的颜色列表

参数：

- **Reference_colors** ( _Sequence_ _\[_ _ParsableManimColor_ _\]_ ) – 要在之间插值或分开的颜色
- **length_of_output** ( _int_ ) – 输出应具有的颜色数量，最好多于输入

返回：

具有插值颜色的 ManimColor 列表

返回类型：

列表\[ [ManimColor]() \] |[Manim色彩]()

color_to_int*rgb（*颜色\_）

用于函数式编程的辅助函数请`to_int_rgb()`参阅[`ManimColor`]()

参数：

**颜色**( _ParsableManimColor_ ) – 一种颜色

返回：

对应的int rgb数组

返回类型：

RGB_Array_Int

color_to_int*rgba（*颜色*， \_alpha = 1.0*）

用于函数式编程的辅助函数请`to_int_rgba_with_alpha()`参阅[`ManimColor`]()

参数：

- **颜色**( _ParsableManimColor_ ) – 一种颜色
- **alpha** ( _float_ _,\_\_可选_) – 颜色中使用的 alpha 值，默认为 1.0

返回：

对应的int rgba数组

返回类型：

RGBA_Array_Int

color*to_rgb（*颜色\_）

用于函数式编程的辅助函数请`to_rgb()`参阅[`ManimColor`]()

参数：

**颜色**( _ParsableManimColor_ ) – 一种颜色

返回：

对应的rgb数组

返回类型：

RGB_Array_Float

color*to_rgba（*颜色*， \_alpha = 1*）

用于函数式编程的辅助函数请`to_rgba_with_alpha()`参阅[`ManimColor`]()

参数：

- **颜色**( _ParsableManimColor_ ) – 一种颜色
- **alpha** ( _float_ _,\_\_可选_) – 颜色中使用的 alpha 值，默认为 1

返回：

对应的rgba数组

返回类型：

RGBA_Array_Float

get*shaded_rgb（\_rgb*，_点_， _unit_normal_vect_， _light_source_）

参数：

- **rgb** ( _ndarray_ _\[**任何**,_ _dtype_ _\[**任何**\]_ _\]_ ) –
- **点**( _ndarray_ _\[**任何**,_ _dtype_ _\[**任何**\]_ _\]_ ) –
- **unit_normal_vect** ( _ndarray_ _\[**任何**,_ _dtype_ _\[**任何**\]_ _\]_ ) –
- **light_source** ( _ndarray_ _\[**任何**,_ _dtype_ _\[**任何**\]_ _\]_ ) –

返回类型：

_ndarray_ \[_任何_, _dtype_ \[ _float64_ \]\]

hex_to_rgb (十六*进制代码*)

用于函数式编程的辅助函数请`to_hex()`参阅[`ManimColor`]()

参数：

**hex_code** ( _str_ ) – 表示颜色的十六进制字符串

返回：

RGB数组代表颜色

返回类型：

RGB_Array_Float

interpolate*arrays ( \_arr1* , _arr2_ , _alpha_ )

Manim 中使用的辅助函数可在两个对象之间平滑淡入淡出

参数：

- **arr1** ( _npt.NDArray_ _\[_ _Any_ _\]_ ) – 第一个颜色数组
- **arr2** ( _npt.NDArray_ _\[_ _Any_ _\]_ ) – 第二个颜色数组
- **alpha** ( _float_ ) – 两个输入之间的插值点对应的 alpha 值

返回：

to 数组的插值

返回类型：

np.ndarray

interpolate*color (*颜色 1* ,*颜色 2* ,*阿尔法\_)

用于插入两个 ManimColor 并获取结果的独立函数，请`interpolate()`参阅[`ManimColor`]()

参数：

- **color1** ( [_ManimColor_]() ) – 第一个 ManimColor
- **color2** ( [_ManimColor_]() ) – 第二个 ManimColor
- **alpha** ( _float_ ) – 确定颜色之间插值点的 alpha 值

返回：

插值 ManimColor

返回类型：

[Manim色彩]()

反转颜色（_颜色_）

用于函数式编程的辅助函数请`invert()`参阅[`ManimColor`]()

参数：

**颜色**( [_ManimColor_]() ) – ManimColor

返回：

线性反转的 ManimColor

返回类型：

[Manim色彩](manim.utils.color.core.ManimColor.html#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor")

随机明亮颜色( )

返回给你一个随机的明亮颜色

警告

此操作非常昂贵，请记住性能损失。

返回：

明亮的 ManimColor

返回类型：

[Manim色彩](manim.utils.color.core.ManimColor.html#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor")

随机颜色( )

返回一个随机的 ManimColor

警告

此操作非常昂贵，请记住性能损失。

返回：

_描述_

返回类型：

[Manim色彩]()

rgb*to_color ( \_rgb* )

用于函数式编程的辅助函数请`from_rgb()`参阅[`ManimColor`]()

参数：

**rgb** ( _RGB_Array_Float_ _|_ _RGB_Tuple_Float_ ) – 3 个元素可迭代

返回：

具有相应值的 ManimColor

返回类型：

[Manim色彩]()

rgb*to_hex ( \_rgb* )

用于函数式编程的辅助函数请`from_rgb()`参阅[`ManimColor`]()

参数：

**rgb** ( _RGB_Array_Float_ _|_ _RGB_Tuple_Float_ ) – 3 个元素可迭代

返回：

颜色的十六进制表示，请`to_hex()`参阅[`ManimColor`]()

返回类型：

斯特

rgba*to_color（\_rgba*）

用于函数式编程的辅助函数请`from_rgba()`参阅[`ManimColor`]()

参数：

**rgba** ( _RGBA_Array_Float_ _|_ _RGBA_Tuple_Float_ ) – 4 个元素可迭代

返回：

具有相应值的 ManimColor

返回类型：

[Manim色彩]()
