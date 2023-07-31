# 弧撑[#](#arcbrace "此标题的固定链接")

合格名称：`manim.mobject.svg.brace.ArcBrace`

_类_ ArcBrace (_弧=弧_,_方向= array(\[1., 0., 0.\])_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/svg/brace.html#ArcBrace)[#](#manim.mobject.svg.brace.ArcBrace "此定义的固定链接")

基地：[`Brace`](manim.mobject.svg.brace.Brace.html#manim.mobject.svg.brace.Brace "manim.mobject.svg.brace.Brace")

创建一个[`Brace`](manim.mobject.svg.brace.Brace.html#manim.mobject.svg.brace.Brace "manim.mobject.svg.brace.Brace")包围[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc").

方向参数允许从圆弧外部或内部应用支撑。

警告

[`ArcBrace`](#manim.mobject.svg.brace.ArcBrace "manim.mobject.svg.brace.ArcBrace")对于半径较小的圆弧，该值较小。

笔记

最初是由 的长度定义的[`ArcBrace`](#manim.mobject.svg.brace.ArcBrace "manim.mobject.svg.brace.ArcBrace")垂直线，但会按比例缩小以匹配起始角度和结束角度。然后根据圆弧半径移动指数函数。[`Brace`](manim.mobject.svg.brace.Brace.html#manim.mobject.svg.brace.Brace "manim.mobject.svg.brace.Brace")[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc")

缩放效果不适用于半径小于 1 的圆弧，以防止过度缩放。

参数

- **arc** ( [_Arc_](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc") ) –[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc")环绕[`Brace`](manim.mobject.svg.brace.Brace.html#manim.mobject.svg.brace.Brace "manim.mobject.svg.brace.Brace")mobject 的。
- **Direction** ( _Sequence_ _\[_ _float_ _\]_ ) – 支撑面向圆弧的方向。 `LEFT`为弧内，`RIGHT`为弧外。

例子

示例：ArcBrace 示例[¶](#arcbraceexample)

![../_images/ArcBraceExample-1.png](../_images/ArcBraceExample-1.png)

from manim import \*

class ArcBraceExample(Scene):
def construct(self):
arc_1 = Arc(radius=1.5,start_angle=0,angle=2\*PI/3).set_color(RED)
brace_1 = ArcBrace(arc_1,LEFT)
group_1 = VGroup(arc_1,brace_1)

        arc_2 = Arc(radius=3,start_angle=0,angle=5*PI/6).set_color(YELLOW)
        brace_2 = ArcBrace(arc_2)
        group_2 = VGroup(arc_2,brace_2)

        arc_3 = Arc(radius=0.5,start_angle=-0,angle=PI).set_color(BLUE)
        brace_3 = ArcBrace(arc_3)
        group_3 = VGroup(arc_3,brace_3)

        arc_4 = Arc(radius=0.2,start_angle=0,angle=3*PI/2).set_color(GREEN)
        brace_4 = ArcBrace(arc_4)
        group_4 = VGroup(arc_4,brace_4)

        arc_group = VGroup(group_1, group_2, group_3, group_4).arrange\_in\_grid(buff=1.5)
        self.add(arc_group.center())

Copy to clipboard

参考：[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc")

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
