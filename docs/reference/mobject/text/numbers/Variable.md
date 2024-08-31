# 变量

合格名称：`manim.mobject.text.numbers.Variable`


```py
class Variable(var, label, var_type=<class 'manim.mobject.text.numbers.DecimalNumber'>, num_decimal_places=2, **kwargs)
```

Bases: `VMobject`

一个用于显示文本的类，该文本显示“label = value”，并且值从[`ValueTracker`]().

参数

- **var** ( _float_ ) – 您需要跟踪和显示的初始值。
- **label** ( _str_ _|_ [_Tex_]() _|_ [_MathTex_]() _|_ [_Text_]() _|_ [_SingleStringMathTex_]() ) – 变量的标签。原始字符串被转换为[`MathTex`]()对象。
- **var_type** ( [_DecimalNumber_]() _|_ [_Integer_]() ) – 用于显示数字的类。默认为[`DecimalNumber`]().
- **num_decimal_places** ( _int_ ) – 要在变量中显示的小数位数。默认为 2。如果 var_type 为[`Integer`]()，则忽略此参数。
- **kwargs** – 要传递给~.Mobject 的其他参数。


`label`

变量的标签，例如。`x = ...`

类型

Union\[ `str`, [`Tex`](), [`MathTex`](), [`Text`](), [`SingleStringMathTex`]()\]


`tracker`

对于更新屏幕上变量的值很有用。

类型

[`ValueTracker`]()


`value`

变量值的 tex。

类型

Union\[ [`DecimalNumber`](), [`Integer`]()\]

例子

正常使用：

```py
# DecimalNumber type
var = 0.5
on_screen_var = Variable(var, Text("var"), num_decimal_places=3)
# Integer type
int_var = 0
on_screen_int_var = Variable(int_var, Text("int_var"), var_type=Integer)
# Using math mode for the label
on_screen_int_var = Variable(int_var, "{a}_{i}", var_type=Integer)
```


示例：VariablesWithValueTracker

```py
from manim import *

class VariablesWithValueTracker(Scene):
    def construct(self):
        var = 0.5
        on_screen_var = Variable(var, Text("var"), num_decimal_places=3)

        # You can also change the colours for the label and value
        on_screen_var.label.set_color(RED)
        on_screen_var.value.set_color(GREEN)

        self.play(Write(on_screen_var))
        # The above line will just display the variable with
        # its initial value on the screen. If you also wish to
        # update it, you can do so by accessing the `tracker` attribute
        self.wait()
        var_tracker = on_screen_var.tracker
        var = 10.5
        self.play(var_tracker.animate.set_value(var))
        self.wait()

        int_var = 0
        on_screen_int_var = Variable(
            int_var, Text("int_var"), var_type=Integer
        ).next_to(on_screen_var, DOWN)
        on_screen_int_var.label.set_color(RED)
        on_screen_int_var.value.set_color(GREEN)

        self.play(Write(on_screen_int_var))
        self.wait()
        var_tracker = on_screen_int_var.tracker
        var = 10.5
        self.play(var_tracker.animate.set_value(var))
        self.wait()

        # If you wish to have a somewhat more complicated label for your
        # variable with subscripts, superscripts, etc. the default class
        # for the label is MathTex
        subscript_label_var = 10
        on_screen_subscript_var = Variable(subscript_label_var, "{a}_{i}").next_to(
            on_screen_int_var, DOWN
        )
        self.play(Write(on_screen_subscript_var))
        self.wait()
```


示例：变量示例

```py
from manim import *

class VariableExample(Scene):
    def construct(self):
        start = 2.0

        x_var = Variable(start, 'x', num_decimal_places=3)
        sqr_var = Variable(start**2, 'x^2', num_decimal_places=3)
        Group(x_var, sqr_var).arrange(DOWN)

        sqr_var.add_updater(lambda v: v.tracker.set_value(x_var.tracker.get_value()**2))

        self.add(x_var, sqr_var)
        self.play(x_var.tracker.animate.set_value(5), run_time=2, rate_func=linear)
        self.wait(0.1)
```


方法



属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。
