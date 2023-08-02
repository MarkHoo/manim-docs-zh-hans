# 变量

合格名称：`manim.mobject.text.numbers.Variable`


```py

```

一个用于显示文本的类，该文本显示“label = value”，并且值从[`ValueTracker`](manim.mobject.value_tracker.ValueTracker.html#manim.mobject.value_tracker.ValueTracker "manim.mobject.value_tracker.ValueTracker").

参数

- **var** ( _float_ ) – 您需要跟踪和显示的初始值。
- **label** ( _str_ _|_ [_Tex_](manim.mobject.text.tex_mobject.Tex.html#manim.mobject.text.tex_mobject.Tex "manim.mobject.text.tex_mobject.Tex") _|_ [_MathTex_](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex") _|_ [_Text_](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text") _|_ [_SingleStringMathTex_](manim.mobject.text.tex_mobject.SingleStringMathTex.html#manim.mobject.text.tex_mobject.SingleStringMathTex "manim.mobject.text.tex_mobject.SingleStringMathTex") ) – 变量的标签。原始字符串被转换为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")对象。
- **var_type** ( [_DecimalNumber_](manim.mobject.text.numbers.DecimalNumber.html#manim.mobject.text.numbers.DecimalNumber "manim.mobject.text.numbers.DecimalNumber") _|_ [_Integer_](manim.mobject.text.numbers.Integer.html#manim.mobject.text.numbers.Integer "manim.mobject.text.numbers.Integer") ) – 用于显示数字的类。默认为[`DecimalNumber`](manim.mobject.text.numbers.DecimalNumber.html#manim.mobject.text.numbers.DecimalNumber "manim.mobject.text.numbers.DecimalNumber").
- **num_decimal_places** ( _int_ ) – 要在变量中显示的小数位数。默认为 2。如果 var_type 为[`Integer`](manim.mobject.text.numbers.Integer.html#manim.mobject.text.numbers.Integer "manim.mobject.text.numbers.Integer")，则忽略此参数。
- **kwargs** – 要传递给~.Mobject 的其他参数。

标签[#](#manim.mobject.text.numbers.Variable.label "此定义的固定链接")

变量的标签，例如。`x = ...`

类型

联盟\[ `str`, [`Tex`](manim.mobject.text.tex_mobject.Tex.html#manim.mobject.text.tex_mobject.Tex "manim.mobject.text.tex_mobject.Tex"), [`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex"), [`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text"), [`SingleStringMathTex`](manim.mobject.text.tex_mobject.SingleStringMathTex.html#manim.mobject.text.tex_mobject.SingleStringMathTex "manim.mobject.text.tex_mobject.SingleStringMathTex")\]

追踪器[#](#manim.mobject.text.numbers.Variable.tracker "此定义的固定链接")

对于更新屏幕上变量的值很有用。

类型

[`ValueTracker`](manim.mobject.value_tracker.ValueTracker.html#manim.mobject.value_tracker.ValueTracker "manim.mobject.value_tracker.ValueTracker")

值[#](#manim.mobject.text.numbers.Variable.value "此定义的固定链接")

变量值的 tex。

类型

联盟\[ [`DecimalNumber`](manim.mobject.text.numbers.DecimalNumber.html#manim.mobject.text.numbers.DecimalNumber "manim.mobject.text.numbers.DecimalNumber"), [`Integer`](manim.mobject.text.numbers.Integer.html#manim.mobject.text.numbers.Integer "manim.mobject.text.numbers.Integer")\]

例子

正常使用：


```py

```


示例：VariablesWithValueTracker

```py

```


示例：变量示例

```py

```


方法

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
