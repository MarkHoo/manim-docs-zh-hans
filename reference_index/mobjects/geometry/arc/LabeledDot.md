# 标记点

合格名称：`manim.mobject.geometry.arc.LabeledDot`

_类_ LabeledDot (_标签_,_半径=无_, _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/arc.html#LabeledDot)[#](#manim.mobject.geometry.arc.LabeledDot "此定义的固定链接")

基地：[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")

A[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")的中心包含一个标签。

参数

- **label** ( _str_ _|_ [_SingleStringMathTex_](manim.mobject.text.tex_mobject.SingleStringMathTex.html#manim.mobject.text.tex_mobject.SingleStringMathTex "manim.mobject.text.tex_mobject.SingleStringMathTex") _|_ [_Text_](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text") _|_ [_Tex_](manim.mobject.text.tex_mobject.Tex.html#manim.mobject.text.tex_mobject.Tex "manim.mobject.text.tex_mobject.Tex") ) – 的标签[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")。这是[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex") 默认渲染的（即，当传递 a 时`str`），但也 可以传递表示渲染字符串的其他类，例如[`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")或。[`Tex`](manim.mobject.text.tex_mobject.Tex.html#manim.mobject.text.tex_mobject.Tex "manim.mobject.text.tex_mobject.Tex")
- **radius** ( _float_ _|_ _None_ ) – 的半径[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")。如果`None`（默认），则根据 的大小计算半径`label`。

例子

示例：几个 LabeledDots [¶](#severallabeleddots)

![../_images/SeveralLabeledDots-1.png](../_images/SeveralLabeledDots-1.png)

from manim import \*

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
