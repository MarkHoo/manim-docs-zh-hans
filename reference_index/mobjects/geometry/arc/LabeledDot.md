# 标记点

合格名称：`manim.mobject.geometry.arc.LabeledDot`

```py
class LabeledDot(label, radius=None, **kwargs)
```

Bases: `Dot`

A[`Dot`]()的中心包含一个标签。

参数

- **label** ( _str_ _|_ [_SingleStringMathTex_]() _|_ [_Text_]() _|_ [_Tex_]() ) – 的标签[`Dot`]()。这是[`MathTex`]() 默认渲染的（即，当传递 a 时`str`），但也 可以传递表示渲染字符串的其他类，例如[`Text`]()或。[`Tex`]()
- **radius** ( _float_ _|_ _None_ ) – 的半径[`Dot`]()。如果`None`（默认），则根据 的大小计算半径`label`。

例子

示例：几个 LabeledDots 

![SeveralLabeledDots-1.png](../static/SeveralLabeledDots-1.png)

```py
from manim import *

class SeveralLabeledDots(Scene):
    def construct(self):
        sq = Square(fill_color=RED, fill_opacity=1)
        self.add(sq)
        dot1 = LabeledDot(Tex("42", color=RED))
        dot2 = LabeledDot(MathTex("a", color=GREEN))
        dot3 = LabeledDot(Text("ii", color=BLUE))
        dot4 = LabeledDot("3")
        dot1.next_to(sq, UL)
        dot2.next_to(sq, UR)
        dot3.next_to(sq, DL)
        dot4.next_to(sq, DR)
        self.add(dot1, dot2, dot3, dot4)
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
