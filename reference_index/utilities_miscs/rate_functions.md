# 速率函数[#](#module-manim.utils.rate_functions "此标题的固定链接")

速率函数的选择，即动画的*速度曲线。*[请在 https://easings.net/](https://easings.net/)找到标准列表。这是非标准的图片

示例：RateFuncExample [¶](#ratefuncexample)

![../_images/RateFuncExample-1.png](../_images/RateFuncExample-1.png)

from manim import \*

class RateFuncExample(Scene):
def construct(self):
x = VGroup()
for k, v in rate_functions.\_\_dict\_\_.items():
if "function" in str(v):
if (
not k.startswith("\_\_")
and not k.startswith("sqrt")
and not k.startswith("bezier")
):
try:
rate_func = v
plot = (
ParametricFunction(
lambda x: \[x, rate_func(x), 0\],
t_range=\[0, 1, .01\],
use_smoothing=False,
color=YELLOW,
)
.stretch_to_fit_width(1.5)
.stretch_to_fit_height(1)
)
plot_bg = SurroundingRectangle(plot).set_color(WHITE)
plot_title = (
Text(rate_func.\_\_name\_\_, weight=BOLD)
.scale(0.5)
.next_to(plot_bg, UP, buff=0.1)
)
x.add(VGroup(plot_bg, plot, plot_title))
except: \# because functions \`not_quite_there\`, \`function squish_rate_func\` are not working.
pass
x.arrange_in_grid(cols=8)
x.height = config.frame_height
x.width = config.frame_width
x.move_to(ORIGIN).scale(0.95)
self.add(x)

Copy to clipboard

标准缓动函数主要有 3 种：

1.  Ease In - 动画有一个平稳的开始。
2.  Ease Out - 动画有一个平滑的结尾。
3.  Ease In Out - 动画有一个平滑的开始和平滑的结束。

笔记

标准函数不会导出，因此要使用它们，您可以执行以下操作：rate_func=rate_functions.ease_in_sine 另一方面，更常用的非标准函数被导出并可以直接使用。

示例：RateFunctions1 示例[¶](#ratefunctions1example)

from manim import \*

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
            MoveAlongPath(dot1, line1, rate_func=rate_functions.ease\_in\_sine),
            MoveAlongPath(dot2, line2, rate_func=rate_functions.ease\_out\_sine),
            MoveAlongPath(dot3, line3, rate_func=rate_functions.ease\_in\_out_sine),
            run_time=7
        )
        self.wait()

Copy to clipboard

功能

双平滑( _t_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#double_smooth)[#](#manim.utils.rate_functions.double_smooth "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

轻松返回（_t_）[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_back)[#](#manim.utils.rate_functions.ease_in_back "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*in_bounce ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_bounce)[#](#manim.utils.rate_functions.ease_in_bounce "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

循环中的缓和( _t_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_circ)[#](#manim.utils.rate_functions.ease_in_circ "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

三次方缓和( _t_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_cubic)[#](#manim.utils.rate_functions.ease_in_cubic "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

弹性( _t_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_elastic)[#](#manim.utils.rate_functions.ease_in_elastic "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

轻松在世博会( _t_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_expo)[#](#manim.utils.rate_functions.ease_in_expo "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*back ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_back)[#](#manim.utils.rate_functions.ease_in_out_back "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*bounce ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_bounce)[#](#manim.utils.rate_functions.ease_in_out_bounce "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*circ ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_circ)[#](#manim.utils.rate_functions.ease_in_out_circ "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*cubic ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_cubic)[#](#manim.utils.rate_functions.ease_in_out_cubic "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*elastic ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_elastic)[#](#manim.utils.rate_functions.ease_in_out_elastic "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*expo ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_expo)[#](#manim.utils.rate_functions.ease_in_out_expo "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*quad ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_quad)[#](#manim.utils.rate_functions.ease_in_out_quad "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*quart ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_quart)[#](#manim.utils.rate_functions.ease_in_out_quart "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*quint ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_quint)[#](#manim.utils.rate_functions.ease_in_out_quint "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease_in_out*sine ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_out_sine)[#](#manim.utils.rate_functions.ease_in_out_sine "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*in_quad ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_quad)[#](#manim.utils.rate_functions.ease_in_quad "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*in_quart ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_quart)[#](#manim.utils.rate_functions.ease_in_quart "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*in_quint ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_quint)[#](#manim.utils.rate_functions.ease_in_quint "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

正弦缓和( _t_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_in_sine)[#](#manim.utils.rate_functions.ease_in_sine "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_back ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_back)[#](#manim.utils.rate_functions.ease_out_back "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_bounce ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_bounce)[#](#manim.utils.rate_functions.ease_out_bounce "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_circ ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_circ)[#](#manim.utils.rate_functions.ease_out_circ "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_cubic ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_cubic)[#](#manim.utils.rate_functions.ease_out_cubic "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_elastic ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_elastic)[#](#manim.utils.rate_functions.ease_out_elastic "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_expo ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_expo)[#](#manim.utils.rate_functions.ease_out_expo "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_quad ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_quad)[#](#manim.utils.rate_functions.ease_out_quad "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_quart ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_quart)[#](#manim.utils.rate_functions.ease_out_quart "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_quint ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_quint)[#](#manim.utils.rate_functions.ease_out_quint "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

ease*out_sine ( \_t* )[\[来源\]](../_modules/manim/utils/rate_functions.html#ease_out_sine)[#](#manim.utils.rate_functions.ease_out_sine "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

指数衰减( _t_ , _half_life = 0.1_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#exponential_decay)[#](#manim.utils.rate_functions.exponential_decay "此定义的固定链接")

参数

- **t**（_浮动_）–
- **half_life** (_浮点数_) –

返回类型

漂浮

线性（_t_）[\[来源\]](../_modules/manim/utils/rate_functions.html#linear)[#](#manim.utils.rate_functions.linear "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

徘徊( _t_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#lingering)[#](#manim.utils.rate_functions.lingering "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

not*quite_there ( \_func=<函数 平滑>* ,_比例=0.7_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#not_quite_there)[#](#manim.utils.rate_functions.not_quite_there "此定义的固定链接")

参数

- **func** (_可调用\_\_\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) –
- **比例**（_浮动_）–

返回类型

_可调用_\[\[float\], float\]

running*start ( \_t* , _pull_factor = \- 0.5_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#running_start)[#](#manim.utils.rate_functions.running_start "此定义的固定链接")

参数

- **t**（_浮动_）–
- **pull_factor** (_浮点数_) –

返回类型

_可迭代_

rush*from ( \_t* ,_拐点= 10.0_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#rush_from)[#](#manim.utils.rate_functions.rush_from "此定义的固定链接")

参数

- **t**（_浮动_）–
- **变形**（_浮动_）–

返回类型

漂浮

rush*into ( \_t* ,_拐点= 10.0_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#rush_into)[#](#manim.utils.rate_functions.rush_into "此定义的固定链接")

参数

- **t**（_浮动_）–
- **变形**（_浮动_）–

返回类型

漂浮

慢速进入（_t_）[\[来源\]](../_modules/manim/utils/rate_functions.html#slow_into)[#](#manim.utils.rate_functions.slow_into "此定义的固定链接")

参数

**t**（_浮动_）–

返回类型

漂浮

平滑（_t_，_拐点= 10.0_）[\[来源\]](../_modules/manim/utils/rate_functions.html#smooth)[#](#manim.utils.rate_functions.smooth "此定义的固定链接")

参数

- **t**（_浮动_）–
- **变形**（_浮动_）–

返回类型

漂浮

挤压速率函数（_函数_， _a = 0.4_， _b = 0.6_）[\[来源\]](../_modules/manim/utils/rate_functions.html#squish_rate_func)[#](#manim.utils.rate_functions.squish_rate_func "此定义的固定链接")

参数

- **func** (_可调用\_\_\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) –
- **一个**（_浮动_）–
- **b**（_浮动_）–

返回类型

_可调用_\[\[float\], float\]

There*and_back ( \_t* ,_变形= 10.0_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#there_and_back)[#](#manim.utils.rate_functions.there_and_back "此定义的固定链接")

参数

- **t**（_浮动_）–
- **变形**（_浮动_）–

返回类型

漂浮

There*and_back_with_pause ( \_t* , _pause_ratio = 0.3333333333333333_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#there_and_back_with_pause)[#](#manim.utils.rate_functions.there_and_back_with_pause "此定义的固定链接")

参数

- **t**（_浮动_）–
- **暂停比率**（_浮动_）–

返回类型

漂浮

单位间隔（_函数_）[\[来源\]](../_modules/manim/utils/rate_functions.html#unit_interval)[#](#manim.utils.rate_functions.unit_interval "此定义的固定链接")

摆动( _t_ ,_摆动= 2_ )[\[来源\]](../_modules/manim/utils/rate_functions.html#wiggle)[#](#manim.utils.rate_functions.wiggle "此定义的固定链接")

参数

- **t**（_浮动_）–
- **摆动**（_浮动_）–

返回类型

漂浮

零（_函数_）[\[来源\]](../_modules/manim/utils/rate_functions.html#zero)[#](#manim.utils.rate_functions.zero "此定义的固定链接")
