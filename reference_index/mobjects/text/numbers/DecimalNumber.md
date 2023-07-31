# 小数[#](#decimalnumber "此标题的固定链接")

合格名称：`manim.mobject.text.numbers.DecimalNumber`

_类_ DecimalNumber ( _number=0_ , _num_decimal_places=2_ , _mob_class=<class 'manim.mobject.text.tex_mobject.MathTex'>_ , _include_sign=False_ , _group_with_commas=True_ , _digital_buff_per_font_unit=0.001_ , _show_ellipsis=False_ , _unit=None_ , _include_background_rectangle=假_， _edge_to_fix = array（\[-1。_， _0。_， _0。\]）_， _font_size = 48_，_行程宽度= 0_， _fill_opacity = 1.0_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/text/numbers.html#DecimalNumber)[#](#manim.mobject.text.numbers.DecimalNumber "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

表示十进制数的 mobject。

例子

示例：MovingSquareWithUpdaters [¶](#movingsquarewithupdaters)

from manim import \*

class MovingSquareWithUpdaters(Scene):
def construct(self):
decimal = DecimalNumber(
0,
show_ellipsis=True,
num_decimal_places=3,
include_sign=True,
)
square = Square().to_edge(UP)

        decimal.add_updater(lambda d: d.next_to(square, RIGHT))
        decimal.add_updater(lambda d: d.set_value(square.get_center()\[1\]))
        self.add(square, decimal)
        self.play(
            square.animate.to_edge(DOWN),
            rate_func=there\_and\_back,
            run_time=5,
        )
        self.wait()

Copy to clipboard

方法

`get_value`

`increment_value`

[`set_value`](#manim.mobject.text.numbers.DecimalNumber.set_value "manim.mobject.text.numbers.DecimalNumber.set_value")

将 的值设置[`DecimalNumber`](#manim.mobject.text.numbers.DecimalNumber "manim.mobject.text.numbers.DecimalNumber")为新数字。

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

[`font_size`](#manim.mobject.text.numbers.DecimalNumber.font_size "manim.mobject.text.numbers.DecimalNumber.font_size")

tex mobject 的字体大小。

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。

参数

- **数字**（_浮点数_）–
- **num_decimal_places** ( _int_ ) –
- **mob_class** ( [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) –
- **include_sign** (_布尔_) –
- **group_with_commas** ( _bool_ ) –
- **digital_buff_per_font_unit** (_浮点数_) –
- **show_ellipsis** (_布尔_) –
- **单位**( _str_ _|\_\_无_) –
- **include_background_rectangle** (_布尔_) –
- **edge_to_fix** (_序列\_\_\[_ _float_ _\]_ ) –
- **字体大小**（_浮动_）–
- **笔画宽度**（_浮动_）-
- **fill_opacity** (_浮动_) –

_属性_ 字体大小[#](#manim.mobject.text.numbers.DecimalNumber.font_size "此定义的固定链接")

tex mobject 的字体大小。

设置值（_数字_）[\[来源\]](../_modules/manim/mobject/text/numbers.html#DecimalNumber.set_value)[#](#manim.mobject.text.numbers.DecimalNumber.set_value "此定义的固定链接")

将 的值设置[`DecimalNumber`](#manim.mobject.text.numbers.DecimalNumber "manim.mobject.text.numbers.DecimalNumber")为新数字。

参数

**number** ( _float_ ) – 将覆盖 的当前编号的值[`DecimalNumber`](#manim.mobject.text.numbers.DecimalNumber "manim.mobject.text.numbers.DecimalNumber")。
