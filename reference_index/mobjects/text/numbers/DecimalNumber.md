# 小数

合格名称：`manim.mobject.text.numbers.DecimalNumber`


```py
class DecimalNumber(number=0, num_decimal_places=2, mob_class=<class 'manim.mobject.text.tex_mobject.MathTex'>, include_sign=False, group_with_commas=True, digit_buff_per_font_unit=0.001, show_ellipsis=False, unit=None, include_background_rectangle=False, edge_to_fix=array([-1., 0., 0.]), font_size=48, stroke_width=0, fill_opacity=1.0, **kwargs)
```

Bases: `VMobject`

表示十进制数的 mobject。

例子

示例：MovingSquareWithUpdaters 

```py
from manim import *

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
        decimal.add_updater(lambda d: d.set_value(square.get_center()[1]))
        self.add(square, decimal)
        self.play(
            square.animate.to_edge(DOWN),
            rate_func=there_and_back,
            run_time=5,
        )
        self.wait()
```


方法

|||
|-|-|
`get_value`|
`increment_value`|
[`set_value`]()|将 的值设置[`DecimalNumber`]()为新数字。


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
[`font_size`]()|tex mobject 的字体大小。
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


参数

- **number**（_float_）–
- **num_decimal_places** ( _int_ ) –
- **mob_class** ( [_VMobject_]() ) –
- **include_sign** (_bool_) –
- **group_with_commas** ( _bool_ ) –
- **digital_buff_per_font_unit** (_float_) –
- **show_ellipsis** (_bool_) –
- **unit**( _str_ _|\_\_None_) –
- **include_background_rectangle** (_bool_) –
- **edge_to_fix** (_Sequence\_\_\[_ _float_ _\]_ ) –
- **font_size**（_float_）–
- **stroke_width**（_float_）-
- **fill_opacity** (_float_) –

_属性_ font_size

tex mobject 的字体大小。


`set_value(number)`

将 的值设置[`DecimalNumber`]()为新数字。

参数

**number** ( _float_ ) – 将覆盖 的当前编号的值[`DecimalNumber`]()。
