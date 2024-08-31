# Manim颜色

合格名称：`manim.utils.color.core.ManimColor`

ManimColor*类*（_值_， _alpha = 1.0_）

基地：`object`

颜色的内部表示。

ManimColor 类是表示颜色的主类。它的内部表示是一个 4 元素浮点数组，对应于 \[r,g,b,a\] 值，其中 r,g,b,a 可以在 0 到 1 之间。

这样做是为了通过在整数和浮点数之间不断进行转换（这会引入错误）来减少颜色不一致的数量。

该类可以接受任何类型的值`ParsableManimColor`，即

ManimColor、int、str、RGB_Tuple_Int、RGB_Tuple_Float、RGBA_Tuple_Int、RGBA_Tuple_Float、RGB_Array_Int、RGB_Array_Float、RGBA_Array_Int、RGBA_Array_Float

ManimColor 本身只接受奇异值，如果可能的话，会直接将它们解释为单一颜色。将字符串传递给 ManimColor 时要小心，它可能会给颜色处理带来很大的开销。

如果您想解析颜色列表，请使用该函数[`parse()`]()，其中[`ManimColor`]()假设您将传递颜色列表，因此数组不会被解释为单一颜色。

警告

如果您向其传递一个数字数组，[`parse()`]()它将将该数组中的 r、g、b、a 数字解释为颜色，因此您得到的不是预期的单一颜色，而是具有 4 种颜色的数组。

有关转换行为，请参阅 \_internal 函数以获取更多文档

参数：

- **value** ( _ParsableManimColor_ _|_ _None_ ) – 颜色的某种表示形式（例如，字符串或合适的元组）。
- **alpha** ( _float_ ) – 颜色的不透明度。默认情况下，颜色是完全不透明的（值 1.0）。

方法

[`from_hex`]()

从十六进制字符串创建 Manim 颜色，允许使用 # 和 0x 前缀

[`from_hsv`]()

从 HSV 数组创建 ManimColor

[`from_rgb`]()

从 RGB 数组创建 ManimColor。

[`from_rgba`]()

从 RGBA 数组创建 ManimColor。

[`gradient`]()

目前尚未实现，请参阅[`color_gradient()`]()目前的工作实现

[`interpolate`]()

在当前和给定 ManimColor 之间进行插值并返回插值颜色

[`invert`]()

返回颜色的线性反转版本（无就地更改）

[`parse`]()

处理颜色列表或单一颜色的解析。

[`to_hex`]()

将 manim 颜色转换为颜色的十六进制表示形式

[`to_hsv`]()

将 Manim 颜色转换为 HSV 数组。

[`to_int_rgb`](#manim.utils.color.core.ManimColor.to_int_rgb "manim.utils.color.core.ManimColor.to_int_rgb")

将当前ManimColor转换为int的rgb数组

[`to_int_rgba`](#manim.utils.color.core.ManimColor.to_int_rgba "manim.utils.color.core.ManimColor.to_int_rgba")

将当前ManimColor转换为int的rgba数组

[`to_int_rgba_with_alpha`](#manim.utils.color.core.ManimColor.to_int_rgba_with_alpha "manim.utils.color.core.ManimColor.to_int_rgba_with_alpha")

将当前 ManimColor 转换为 rgba 整数数组，[`to_int_rgba()`](#manim.utils.color.core.ManimColor.to_int_rgba "manim.utils.color.core.ManimColor.to_int_rgba")但您可以更改 alpha 值。

[`to_integer`](#manim.utils.color.core.ManimColor.to_integer "manim.utils.color.core.ManimColor.to_integer")

将当前 ManimColor 转换为整数

[`to_rgb`](#manim.utils.color.core.ManimColor.to_rgb "manim.utils.color.core.ManimColor.to_rgb")

将当前 ManimColor 转换为 rgb 浮点数数组

[`to_rgba`](#manim.utils.color.core.ManimColor.to_rgba "manim.utils.color.core.ManimColor.to_rgba")

将当前 ManimColor 转换为 rgba 浮点数数组

[`to_rgba_with_alpha`](#manim.utils.color.core.ManimColor.to_rgba_with_alpha "manim.utils.color.core.ManimColor.to_rgba_with_alpha")

将当前 ManimColor 转换为 float 的 rgba 数组，[`to_rgba()`](#manim.utils.color.core.ManimColor.to_rgba "manim.utils.color.core.ManimColor.to_rgba")但您可以更改 alpha 值。

_静态_ \_internal*from_hex_string（*十六进制*，*阿尔法\_）

用于将十六进制字符串转换为 ManimColor 的内部表示形式的内部函数。

警告

这不接受十六进制字符串前面的任何前缀，例如 # 或类似的前缀。这仅适用于原始六角部分

_仅限内部使用_

参数：

- **hex** ( _str_ ) – 要解析的十六进制字符串
- **alpha** ( _float_ ) – 用于颜色的 alpha 值

返回：

内部颜色表示

返回类型：

ManimColor内部

_静态_ \_internal*from_int_rgb（\_rgb*， _alpha = 1.0_）

用于将 rgb 整数元组转换为 ManimColor 的内部表示形式的内部函数。

_仅限内部使用_

参数：

- **rgb** ( _RGB_Tuple_Int_ ) – 要解析的整数 rgb 元组
- **alpha** ( _float_ _,\_\_可选_) – 可选的 alpha 值，默认为 1.0

返回：

内部颜色表示

返回类型：

ManimColor内部

_静态_ \_internal*from_int_rgba（\_rgba*）

用于将 rgba 整数元组转换为 ManimColor 的内部表示形式的内部函数。

_仅限内部使用_

参数：

**rgba** ( _RGBA_Tuple_Int_ ) – 要解析的 int rgba 元组

返回：

内部颜色表示

返回类型：

ManimColor内部

_静态_ \_internal*from*rgb ( \_rgb* , \_alpha = 1.0* )

用于将浮点数的 rgb 元组转换为 ManimColor 的内部表示的内部函数。

_仅限内部使用_

参数：

- **rgb** ( _RGB_Tuple_Float_ ) – 要解析的 float rgb 元组
- **alpha** ( _float_ _,\_\_可选_) – 可选的 alpha 值，默认为 1.0

返回：

内部颜色表示

返回类型：

ManimColor内部

_静态_ \_internal_from*rgba（\_rgba*）

用于将浮点数的 rgba 元组转换为 ManimColor 的内部表示的内部函数。

_仅限内部使用_

参数：

**rgba** ( _RGBA_Tuple_Float_ ) – 要解析的 int rgba 元组

返回：

内部颜色表示

返回类型：

ManimColor内部

_静态_ \_internal_from*string（*名称\_）

用于将字符串转换为 ManimColor 的内部表示形式的内部函数。这不用于十六进制字符串，请参考`_internal_from_hex()`此功能。

_仅限内部使用_

参数：

**name** ( _str_ ) – 要解析为颜色的颜色名称。请参阅文档页面中的不同颜色模块来查找相应的颜色名称。

返回：

内部颜色表示

返回类型：

ManimColor内部

加薪：

**ValueError** – 如果 manim 中不存在颜色名称，则引发 ValueError

_属性_ \_internal*value *: ndarray \[ Any , dtype \[ float64 \] \]\_ 

返回当前 Manim 颜色的内部值 \[r,g,b,a\] 浮点数组

返回：

内部颜色表示

返回类型：

ManimColor内部

_类方法_ from*hex (*十六进制*, \_alpha = 1.0* )

从十六进制字符串创建 Manim 颜色，允许使用 # 和 0x 前缀

参数：

- **hex** ( _str_ ) – 要转换的十六进制字符串（目前仅支持 6 个半字节）
- **alpha** ( _float_ _,\_\_可选_) – 用于十六进制字符串的 alpha 值，默认为 1.0

返回：

由十六进制字符串表示的 ManimColor

返回类型：

[曼尼姆色彩]()

_类方法_ from*hsv ( \_hsv* , _alpha = 1.0_ )

从 HSV 数组创建 ManimColor

参数：

- **hsv** ( _HSV_Array_Float_ _|_ _HSV_Tuple_Float_ ) – 包含 0-1 浮点数的任何 3 元素可迭代
- **alpha** ( _float_ _,\_\_可选_) – 要使用的 alpha 值，默认为 1.0

返回：

ManimColor 与 HSV 对应的 RGB 值

返回类型：

[曼尼姆色彩]()

_类方法_ from*rgb ( \_rgb* , _alpha = 1.0_ )

从 RGB 数组创建 ManimColor。自动判断int/float类型

警告

如果您想要整数，请确保您的元素不是浮点数。 5.0 将导致输入被解释为浮点 rgb 数组，其值为 5.0 而不是整数 5

参数：

- **rgb** ( _RGB_Array_Float_ _|_ _RGB_Tuple_Float_ _|_ _RGB_Array_Int_ _|_ _RGB_Tuple_Int_ ) – 任意 3 个元素可迭代
- **alpha** ( _float_ _,\_\_可选_) – 颜色中使用的 alpha 值，默认为 1.0

返回：

返回 ManimColor 对象

返回类型：

[曼尼姆色彩](#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor")

_类方法_ from*rgba ( \_rgba* )

从 RGBA 数组创建 ManimColor。自动判断int/float类型

警告

如果您想要整数，请确保您的元素不是浮点数。 5.0 将导致输入被解释为浮点 rgb 数组，其值为 5.0 而不是整数 5

参数：

**rgba** ( _RGBA_Array_Float_ _|_ _RGBA_Tuple_Float_ _|_ _RGBA_Array_Int_ _|_ _RGBA_Tuple_Int_ ) – 任意 4 个元素可迭代

返回：

返回 ManimColor 对象

返回类型：

[曼尼姆色彩](#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor")

_静态_ 渐变（_颜色_、_长度_）

目前尚未实现，请参阅[`color_gradient()`](manim.utils.color.core.html#manim.utils.color.core.color_gradient "manim.utils.color.core.color_gradient")目前的工作实现

参数：

- **颜色**(_列表\_\_\[_ [_manim.utils.color.core.ManimColor_](#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor") _\]_ ) –
- **长度**( _int_ ) –

插值（_其他_，_阿尔法_）

在当前和给定 ManimColor 之间进行插值并返回插值颜色

参数：

- **other** ( [_ManimColor_](#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor") ) – 用于插值的其他 ManimColor
- **阿尔法**（_浮动_）–

  rgba 色彩空间中连接两种颜色的线上的点，即插值点

  0对应当前ManimColor，1对应其他ManimColor

返回：

插值 ManimColor

返回类型：

[曼尼姆色彩](#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor")

反转（_with_alpha = False_）

返回颜色的线性反转版本（无就地更改）

参数：

**with_alpha** ( _bool_ _,\_\_可选_) –

如果为 true，则 alpha 值也会反转，默认为 False

笔记

这可能会导致意外的行为，即对象不会显示，因为它们的 alpha 值突然变为 0 或非常低。将其设置为 true 时请记住这一点

返回：

线性反转的 ManimColor

返回类型：

[曼尼姆色彩](#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor")

_classmethod_ parse ( _color :可选\[ Union \[ [ManimColor](#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor") , int , str ,元组\[ int , int , int \] ,元组\[ float , float , float \] ,元组\[ int , int , int , int \] ,元组\[ float , float , float , float \] , ndarray \[ Any , dtype \[ int64 \] \] , ndarray \[ Any , dtype \[ float64 \] \] \] \]_ , _alpha : float = 1.0_ ) → Self[\[来源\]](../_modules/manim/utils/color/core.html#ManimColor.parse)[#](#manim.utils.color.core.ManimColor.parse "此定义的固定链接")

_classmethod_ parse ( _color : Sequence \[ Union \[ [ManimColor](#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor") , int , str , Tuple \[ int , int , int \] , Tuple \[ float , float , float \] , Tuple \[ int , int , int , int \] , Tuple \[ float , float , float , float \] , ndarray \[ Any , dtype \[ int64 \] \] , ndarray \[ Any , dtype \[ float64 \] \] \] \]_ , _alpha : float = 1.0_ ) → list \[ Self \]

处理颜色列表或单一颜色的解析。

参数：

- **color** – 要解析的颜色或颜色列表。请注意，此函数不能接受 rgba 元组。它将假设您的意思是 list\[ManimColor\] 并将返回 ManimColors 列表。
- **alpha** – 传递单一颜色时使用的 alpha 值。或者如果传递颜色列表来设置所有颜色的值。

返回：

根据输入，颜色列表或单一颜色

返回类型：

[曼尼姆色彩](#manim.utils.color.core.ManimColor "manim.utils.color.core.ManimColor")

to*hex ( \_with_alpha = False* )

将 manim 颜色转换为颜色的十六进制表示形式

参数：

**with_alpha** ( _bool_ _,\_\_可选_) – 将结果从 6 个值更改为 8 个值，其中最后 2 个半字节表示 0-255 的 alpha 值，默认为 False

返回：

以 # 开头的十六进制字符串，有 6 或 8 个半字节，具体取决于您的输入，默认为 6，即 #XXXXXX

返回类型：

斯特

to_hsv ( )

将 Manim 颜色转换为 HSV 数组。

笔记

请注意，这会返回一个\[h, s, v\]形式的数组，其中元素是浮点数。这可能会令人困惑，因为 rgb 也可以是浮点数数组，因此您可能需要通过键入变量来注释代码中此函数的用法，以便`HSV_Array_Float`区分 rgb 数组和 hsv 数组

返回：

包含 3 个 float 类型元素（范围从 0 到 1）的 hsv 数组

返回类型：

HSV_Array_Float

to_int_rgb ( )

将当前ManimColor转换为int的rgb数组

返回：

具有 3 个 int 类型元素的 RGB 数组

返回类型：

RGB_Array_Int

to_int_rgba ( )

将当前ManimColor转换为int的rgba数组

返回：

具有 4 个 int 类型元素的 rgba 数组

返回类型：

RGBA_Array_Int

to*int_rgba_with_alpha (*阿尔法\_)

将当前 ManimColor 转换为 rgba 整数数组，[`to_int_rgba()`](#manim.utils.color.core.ManimColor.to_int_rgba "manim.utils.color.core.ManimColor.to_int_rgba")但您可以更改 alpha 值。

参数：

**alpha** ( _float_ ) – 用于返回值的 alpha 值。 （会自动从 0-1 缩放到 0-255，所以只需传递 0-1）

返回：

具有 4 个 int 类型元素的 rgba 数组

返回类型：

RGBA_Array_Int

到\_整数( )

将当前 ManimColor 转换为整数

返回：

- _int_ – 颜色的整数表示
- _..警告::_ – 这将仅返回颜色的 RGB 部分

返回类型：

整数

to_rgb ( )

将当前 ManimColor 转换为 rgb 浮点数数组

返回：

具有 3 个 float 类型元素的 RGB 数组

返回类型：

RGB_Array_Float

to_rgba ( )

将当前 ManimColor 转换为 rgba 浮点数数组

返回：

具有 4 个 float 类型元素的 RGBA 数组

返回类型：

RGBA_Array_Float

to_rgba_with*alpha (*阿尔法\_)

将当前 ManimColor 转换为 float 的 rgba 数组，[`to_rgba()`](#manim.utils.color.core.ManimColor.to_rgba "manim.utils.color.core.ManimColor.to_rgba")但您可以更改 alpha 值。

参数：

**alpha** ( _float_ ) – 返回值中使用的 alpha 值

返回：

具有 4 个 float 类型元素的 RGBA 数组

返回类型：

RGBA_Array_Float
