# 成长箭头[#](#growarrow "此标题的固定链接")

合格名称：`manim.animation.growing.GrowArrow`

_类_ GrowArrow ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/growing.html#GrowArrow)[#](#manim.animation.growing.GrowArrow "此定义的固定链接")

基地：[`GrowFromPoint`](manim.animation.growing.GrowFromPoint.html#manim.animation.growing.GrowFromPoint "manim.animation.growing.GrowFromPoint")

[`Arrow`](manim.mobject.geometry.line.Arrow.html#manim.mobject.geometry.line.Arrow "manim.mobject.geometry.line.Arrow")通过从开始向尖端生长来引入。

参数

- **arrow** – 要引入的箭头。
- **point_color** – 箭头在增长到完整尺寸之前的初始颜色。留空以匹配箭头的颜色。

例子

示例：GrowArrowExample [¶](#growarrowexample)

from manim import \*

class GrowArrowExample(Scene):
def construct(self):
arrows = \[Arrow(2 _ LEFT, 2 _ RIGHT), Arrow(2 _ DR, 2 _ UL)\]
VGroup(\*arrows).set_x(0).arrange(buff=2)
self.play(GrowArrow(arrows\[0\]))
self.play(GrowArrow(arrows\[1\], point_color=RED))

Copy to clipboard

方法

`create_starting_mobject`

属性

`path_arc`

`path_func`
