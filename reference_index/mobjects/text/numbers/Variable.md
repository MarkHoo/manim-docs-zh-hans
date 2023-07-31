# 变量[#](#variable "此标题的固定链接")

合格名称：`manim.mobject.text.numbers.Variable`

_类_ 变量（_var_、 _label_、 _var_type=<class 'manim.mobject.text.numbers.DecimalNumber'>_、 _num_decimal_places=2_、 _\*\*kwargs_）[\[来源\]](../_modules/manim/mobject/text/numbers.html#Variable)[#](#manim.mobject.text.numbers.Variable "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

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

\# DecimalNumber type
var = 0.5
on_screen_var = Variable(var, Text("var"), num_decimal_places=3)
\# Integer type
int*var = 0
on_screen_int_var = Variable(int_var, Text("int_var"), var_type=Integer)
\# Using math mode for the label
on_screen_int_var = Variable(int_var, "{a}*{i}", var_type=Integer)

Copy to clipboard

示例：VariablesWithValueTracker [¶](#variableswithvaluetracker)

from manim import \*

class VariablesWithValueTracker(Scene):
def construct(self):
var = 0.5
on_screen_var = Variable(var, Text("var"), num_decimal_places=3)

        \# You can also change the colours for the label and value
        on\_screen\_var.label.set_color(RED)
        on\_screen\_var.value.set_color(GREEN)

        self.play(Write(on\_screen\_var))
        \# The above line will just display the variable with
        \# its initial value on the screen. If you also wish to
        \# update it, you can do so by accessing the \`tracker\` attribute
        self.wait()
        var_tracker = on\_screen\_var.tracker
        var = 10.5
        self.play(var_tracker.animate.set_value(var))
        self.wait()

        int_var = 0
        on\_screen\_int_var = Variable(
            int_var, Text("int_var"), var_type=Integer
        ).next_to(on\_screen\_var, DOWN)
        on\_screen\_int_var.label.set_color(RED)
        on\_screen\_int_var.value.set_color(GREEN)

        self.play(Write(on\_screen\_int_var))
        self.wait()
        var_tracker = on\_screen\_int_var.tracker
        var = 10.5
        self.play(var_tracker.animate.set_value(var))
        self.wait()

        \# If you wish to have a somewhat more complicated label for your
        \# variable with subscripts, superscripts, etc. the default class
        \# for the label is MathTex
        subscript\_label\_var = 10
        on\_screen\_subscript_var = Variable(subscript\_label\_var, "{a}_{i}").next_to(
            on\_screen\_int_var, DOWN
        )
        self.play(Write(on\_screen\_subscript_var))
        self.wait()

Copy to clipboard

示例：变量示例[¶](#variableexample)

from manim import \*

class VariableExample(Scene):
def construct(self):
start = 2.0

        x_var = Variable(start, 'x', num\_decimal\_places=3)
        sqr_var = Variable(start**2, 'x^2', num\_decimal\_places=3)
        Group(x_var, sqr_var).arrange(DOWN)

        sqr_var.add_updater(lambda v: v.tracker.set_value(x_var.tracker.get_value()**2))

        self.add(x_var, sqr_var)
        self.play(x_var.tracker.animate.set_value(5), run_time=2, rate_func=linear)
        self.wait(0.1)

Copy to clipboard

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
