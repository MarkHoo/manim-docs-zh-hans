# 下划线

合格名称：`manim.mobject.geometry.shape\_matchers.Underline`

_类_ 下划线（_mobject_， _buff = 0.1_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/shape_matchers.html#Underline)[#](#manim.mobject.geometry.shape_matchers.Underline "此定义的固定链接")

基地：[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")

创建下划线。

例子

示例：下划线[¶](#underline)

![../_images/UnderLine-1.png](../_images/UnderLine-1.png)

from manim import \*

class UnderLine(Scene):
def construct(self):
man = Tex("Manim") \# Full Word
ul = Underline(man) \# Underlining the word
self.add(man, ul)

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
