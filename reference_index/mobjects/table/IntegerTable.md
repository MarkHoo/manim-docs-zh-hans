# 整数表

合格名称：`manim.mobject.table.IntegerTable`


```py
class IntegerTable(table, element_to_mobject=<class 'manim.mobject.text.numbers.Integer'>, **kwargs)
```

Bases: `Table`

[`Table`]()与 一起使用的专用对象[`Integer`]()。


例子

示例：IntegerTableExample 

![IntegerTableExample-1.png](../static/IntegerTableExample-1.png)

```py
from manim import *

class IntegerTableExample(Scene):
    def construct(self):
        t0 = IntegerTable(
            [[0,30,45,60,90],
            [90,60,45,30,0]],
            col_labels=[
                MathTex("\\frac{\sqrt{0}}{2}"),
                MathTex("\\frac{\sqrt{1}}{2}"),
                MathTex("\\frac{\sqrt{2}}{2}"),
                MathTex("\\frac{\sqrt{3}}{2}"),
                MathTex("\\frac{\sqrt{4}}{2}")],
            row_labels=[MathTex("\sin"), MathTex("\cos")],
            h_buff=1,
            element_to_mobject_config={"unit": "^{\circ}"})
        self.add(t0)
```


element_to_mobject 设置[`Table`]()为的特殊情况。如果表中有小数条目，则四舍五入。[`Integer`]()

参数

- **table** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _|_ _str_ _\]_ _\]_ ) – 二维数组或列表列表。表的内容必须是 的有效输入[`Integer`]()。
- **element_to_mobject** ( _Callable_ _\[_ _\[_ _float_ _|_ _str_ _\]_ _,_ [_VMobject_]() _\]_ ) –[`Mobject`]()应用于表条目的类。设置为[`Integer`]().
- **kwargs** – 要传递给 的附加参数[`Table`]()。


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
