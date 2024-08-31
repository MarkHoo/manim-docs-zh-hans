# 速率函数

速率函数的选择，即动画的*速度曲线。*[请在 https://easings.net/](https://easings.net/)找到标准列表。这是非标准的图片

示例：RateFuncExample 

![RateFuncExample-1.png](../static/RateFuncExample-1.png)

```py
from manim import *

class RateFuncExample(Scene):
    def construct(self):
        x = VGroup()
        for k, v in rate_functions.__dict__.items():
            if "function" in str(v):
                if (
                    not k.startswith("__")
                    and not k.startswith("sqrt")
                    and not k.startswith("bezier")
                ):
                    try:
                        rate_func = v
                        plot = (
                            ParametricFunction(
                                lambda x: [x, rate_func(x), 0],
                                t_range=[0, 1, .01],
                                use_smoothing=False,
                                color=YELLOW,
                            )
                            .stretch_to_fit_width(1.5)
                            .stretch_to_fit_height(1)
                        )
                        plot_bg = SurroundingRectangle(plot).set_color(WHITE)
                        plot_title = (
                            Text(rate_func.__name__, weight=BOLD)
                            .scale(0.5)
                            .next_to(plot_bg, UP, buff=0.1)
                        )
                        x.add(VGroup(plot_bg, plot, plot_title))
                    except: # because functions `not_quite_there`, `function squish_rate_func` are not working.
                        pass
        x.arrange_in_grid(cols=8)
        x.height = config.frame_height
        x.width = config.frame_width
        x.move_to(ORIGIN).scale(0.95)
        self.add(x)
```

标准缓动函数主要有 3 种：

1.  Ease In - 动画有一个平稳的开始。
2.  Ease Out - 动画有一个平滑的结尾。
3.  Ease In Out - 动画有一个平滑的开始和平滑的结束。

> 笔记
> 标准函数不会导出，因此要使用它们，您可以执行以下操作：rate_func=rate_functions.ease_in_sine 另一方面，更常用的非标准函数被导出并可以直接使用。

示例：RateFunctions1 示例

```py
from manim import *

class RateFunctions1Example(Scene):
    def construct(self):
        line1 = Line(3*LEFT, 3*RIGHT).shift(UP).set_color(RED)
        line2 = Line(3*LEFT, 3*RIGHT).set_color(GREEN)
        line3 = Line(3*LEFT, 3*RIGHT).shift(DOWN).set_color(BLUE)

        dot1 = Dot().move_to(line1.get_left())
        dot2 = Dot().move_to(line2.get_left())
        dot3 = Dot().move_to(line3.get_left())

        label1 = Tex("Ease In").next_to(line1, RIGHT)
        label2 = Tex("Ease out").next_to(line2, RIGHT)
        label3 = Tex("Ease In Out").next_to(line3, RIGHT)

        self.play(
            FadeIn(VGroup(line1, line2, line3)),
            FadeIn(VGroup(dot1, dot2, dot3)),
            Write(VGroup(label1, label2, label3)),
        )
        self.play(
            MoveAlongPath(dot1, line1, rate_func=rate_functions.ease_in_sine),
            MoveAlongPath(dot2, line2, rate_func=rate_functions.ease_out_sine),
            MoveAlongPath(dot3, line3, rate_func=rate_functions.ease_in_out_sine),
            run_time=7
        )
        self.wait()
```

Functions


`double_smooth(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_back(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_bounce(t)`

参数

**t**（_float_）–

返回类型

float

`ease_in_circ(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_cubic(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_elastic(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_expo(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_back(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_bounce(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_circ(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_cubic(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_elastic(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_expo(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_quad(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_quart(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_quint(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_out_sine(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_quad(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_quart(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_quint(t)`

参数

**t**（_float_）–

返回类型

float


`ease_in_sine(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_back(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_bounce(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_circ(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_cubic(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_elastic(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_expo(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_quad(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_quart(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_quint(t)`

参数

**t**（_float_）–

返回类型

float


`ease_out_sine(t)`

参数

**t**（_float_）–

返回类型

float


`exponential_decay(t, half_life=0.1)`

参数

- **t**（_float_）–
- **half_life** (_float_) –

返回类型

float


`linear(t)`

参数

**t**（_float_）–

返回类型

float


`lingering(t)`

参数

**t**（_float_）–

返回类型

float


`not_quite_there(func=<function smooth>, proportion=0.7)`

参数

- **func** (*Callable[[float], float]*) –
- **proportion**（_float_）–

返回类型

*Callable[[float], float]*


`running_start(t, pull_factor=- 0.5)`

参数

- **t**（_float_）–
- **pull_factor** (_float_) –

返回类型

_Iterable_


`rush_from(t, inflection=10.0)`

参数

- **t**（_float_）–
- **inflection**（_float_）–

返回类型

float


`rush_into(t, inflection=10.0)`

参数

- **t**（_float_）–
- **inflection**（_float_）–

返回类型

float


`slow_into(t)`

参数

**t**（_float_）–

返回类型

float


`smooth(t, inflection=10.0)`

参数

- **t**（_float_）–
- **inflection**（_float_）–

返回类型

float


`smoothererstep(t)`

三阶 SmoothStep sigmoid 函数的实现。一阶、二阶和三阶导数（速度、加速度和加加速度）在端点处为零。 https://en.wikipedia.org/wiki/Smoothstep

参数

**t**（_float_）–

返回类型

float


`smootherstep(t)`

二阶 SmoothStep sigmoid 函数的实现。一阶和二阶导数（速度和加速度）在端点处为零。 https://en.wikipedia.org/wiki/Smoothstep

参数

**t**（_float_）–

返回类型

float


`smoothstep(t)`

一阶 SmoothStep sigmoid 函数的实现。一阶导数（速度）在端点处为零。 https://en.wikipedia.org/wiki/Smoothstep

参数

**t**（_float_）–

返回类型

float


`squish_rate_func(func, a=0.4, b=0.6)`

参数

- **func** (_Callable[[float], float]_ ) –
- **a**（_float_）–
- **b**（_float_）–

返回类型

_Callable[[float], float]_



`there_and_back(t, inflection=10.0)`

参数

- **t**（_float_）–
- **inflection**（_float_）–

返回类型

float


`there_and_back_with_pause(t, pause_ratio=0.3333333333333333)`

参数

- **t**（_float_）–
- **pause_ratio**（_float_）–

返回类型

float


`unit_interval(function)`


`wiggle(t, wiggles=2)`

参数

- **t**（_float_）–
- **wiggles**（_float_）–

返回类型

float


`zero(function)`
