# 日志库[#](#logbase "此标题的固定链接")

合格名称：`manim.mobject.graphing.scale.LogBase`

LogBase*类*（_基数= 10_， _custom_labels = True_）[\[来源\]](../_modules/manim/mobject/graphing/scale.html#LogBase)[#](#manim.mobject.graphing.scale.LogBase "此定义的固定链接")

基地：`_ScaleBase`

对数图/函数的刻度。

参数

- **base** ( _float_ ) – 日志的底数，默认为 10。
- **custom_labels** ( _bool_ ) – 用于[`Axes`](manim.mobject.graphing.coordinate_systems.Axes.html#manim.mobject.graphing.coordinate_systems.Axes "manim.mobject.graphing.coordinate_systems.Axes")：是否包含`LaTeX`轴标签，默认为 True。

例子

func = ParametricFunction(lambda x: x, scaling=LogBase(base=2))

Copy to clipboard

方法

[`function`](#manim.mobject.graphing.scale.LogBase.function "manim.mobject.graphing.scale.LogBase.function")

缩放值以适合对数刻度。\`\`self.function(5)==10\*\*5\`\`

[`get_custom_labels`](#manim.mobject.graphing.scale.LogBase.get_custom_labels "manim.mobject.graphing.scale.LogBase.get_custom_labels")

生成. [`Integer`](manim.mobject.text.numbers.Integer.html#manim.mobject.text.numbers.Integer "manim.mobject.text.numbers.Integer")\_`10^2`

[`inverse_function`](#manim.mobject.graphing.scale.LogBase.inverse_function "manim.mobject.graphing.scale.LogBase.inverse_function")

的逆`function`。

函数（_值_）[\[来源\]](../_modules/manim/mobject/graphing/scale.html#LogBase.function)[#](#manim.mobject.graphing.scale.LogBase.function "此定义的固定链接")

缩放值以适合对数刻度。\`\`self.function(5)==10\*\*5\`\`

参数

**值**（_浮点数_）–

返回类型

漂浮

get*custom_labels ( \_val_range* , _unit_decimal_places = 0_ , _\*\* base_config_ )[\[来源\]](../_modules/manim/mobject/graphing/scale.html#LogBase.get_custom_labels)[#](#manim.mobject.graphing.scale.LogBase.get_custom_labels "此定义的固定链接")

生成. [`Integer`](manim.mobject.text.numbers.Integer.html#manim.mobject.text.numbers.Integer "manim.mobject.text.numbers.Integer")\_`10^2`

参数

- **val_range** ( _Iterable_ _\[_ _float_ _\]_ ) – 用于创建标签的可迭代值。确定指数。
- **unit_decimal_places** ( _int_ ) – 指数中包含的小数位数
- **base_config** ( _dict_ _\[_ _str_ _,_ _Any_ _\]_ ) – 要传递给的附加参数[`Integer`](manim.mobject.text.numbers.Integer.html#manim.mobject.text.numbers.Integer "manim.mobject.text.numbers.Integer")。

返回类型

列表\[ [Mobject](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") \]

反函数（_值_）[\[来源\]](../_modules/manim/mobject/graphing/scale.html#LogBase.inverse_function)[#](#manim.mobject.graphing.scale.LogBase.inverse_function "此定义的固定链接")

的逆`function`。该值必须大于 0

参数

**值**（_浮点数_）–

返回类型

漂浮
