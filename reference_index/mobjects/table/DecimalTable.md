# 十进制表

合格名称：`manim.mobject.table.DecimalTable`


```py
class DecimalTable(table, element_to_mobject=<class 'manim.mobject.text.numbers.DecimalNumber'>, element_to_mobject_config={'num_decimal_places': 1}, **kwargs)
```

Bases: `Table`

[`Table`]()用于[`DecimalNumber`]()显示十进制条目的专用 mobject。


例子

示例：十进制表示例

![DecimalTableExample-1.png](../static/DecimalTableExample-1.png)

```py
from manim import *

class DecimalTableExample(Scene):
    def construct(self):
        x_vals = [-2,-1,0,1,2]
        y_vals = np.exp(x_vals)
        t0 = DecimalTable(
            [x_vals, y_vals],
            row_labels=[MathTex("x"), MathTex("f(x)=e^{x}")],
            h_buff=1,
            element_to_mobject_config={"num_decimal_places": 2})
        self.add(t0)
```


的特殊情况[`Table`]()设置`element_to_mobject`为[`DecimalNumber`]()。默认情况下，`num_decimal_places`设置为 1。将根据提供的 舍入/截断小数位`element_to_mobject_config`。

参数

- **table** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _|_ _str_ _\]_ _\]_ ) – 2D 数组或列表的列表。表的内容必须是 的有效输入[`DecimalNumber`]()。
- **element_to_mobject** ( _Callable_ _\[_ _\[_ _float_ _|_ _str_ _\]_ _,_ [_VMobject_]() _\]_ ) –[`Mobject`]()应用于表条目的类。设置为[`DecimalNumber`]().
- **element_to_mobject_config** ( _dict_ ) – 元素到 mobject 配置，此处设置为 {“num_decimal_places”: 1}。
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
