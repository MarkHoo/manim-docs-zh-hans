# 线性基础

合格名称：`manim.mobject.graphing.scale.LinearBase`


```py
class LinearBase(scale_factor=1.0)
```

Bases: `_ScaleBase`

默认缩放类别。

参数

**scale_factor** ( _float_ ) – 线性函数的斜率，默认为 1.0

方法

|||
|-|-|
[`function`]()|将值乘以比例因子。
[`inverse_function`]()|函数的反函数。


`function(value)`

将值乘以比例因子。

参数

**value** ( _float_ ) – 要乘以比例因子的值。

返回类型

float


`inverse_function(value)`

函数的反函数。将值除以比例因子。

参数

**value** ( _float_ ) – 要除以比例因子的值。

返回类型

float
