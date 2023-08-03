# 日志库

合格名称：`manim.mobject.graphing.scale.LogBase`


```py
class LogBase(base=10, custom_labels=True)
```

Bases: `_ScaleBase`

对数图/函数的刻度。

参数

- **base** ( _float_ ) – 日志的底数，默认为 10。
- **custom_labels** ( _bool_ ) – 用于[`Axes`]()：是否包含`LaTeX`轴标签，默认为 True。


例子

```py
func = ParametricFunction(lambda x: x, scaling=LogBase(base=2))
```

方法

|||
|-|-|
[`function`]()|缩放值以适合对数刻度。\`\`self.function(5)==10\*\*5\`\`
[`get_custom_labels`]()|生成 10^2 形式的自定义整数标签
[`inverse_function`]()|`function`的反函数。



`function(value)`

缩放值以适合对数刻度。\`\`self.function(5)==10\*\*5\`\`

参数

**值**（_浮点数_）–

返回类型

漂浮


```py
get_custom_labels(val_range, unit_decimal_places=0, **base_config)
```
生成. [`Integer`]()\_`10^2`

参数

- **val_range** ( _Iterable_ _\[_ _float_ _\]_ ) – 用于创建标签的可迭代值。确定指数。
- **unit_decimal_places** ( _int_ ) – 指数中包含的小数位数
- **base_config** ( _dict_ _\[_ _str_ _,_ _Any_ _\]_ ) – 要传递给的附加参数[`Integer`]()。

返回类型

list\[ [Mobject]() \]


`inverse_function(value)`

`function`的反函数
。该值必须大于 0

参数

**value**（_float_）–

返回类型

float
