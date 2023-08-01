# 环带

合格名称：`manim.mobject.geometry.arc.Annulus`

环形*类*（_内部半径= 1_，_外部半径= 2_，_填充不透明度= 1_，_描边宽度= 0_，_颜色= '#FFFFFF'_，_标记路径闭合=假_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Annulus)[#](#manim.mobject.geometry.arc.Annulus "此定义的固定链接")

基地：[`Circle`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")

两个同心圆之间的区域[`Circles`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")。

参数

- **inner_radius** ( _float_ _|_ _None_ ) – 内部的半径[`Circle`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")。
- **outer_radius** ( _float_ _|_ _None_ ) – 外部的半径[`Circle`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")。
- **kwargs** – 要传递给的附加参数[`Annulus`](#manim.mobject.geometry.arc.Annulus "manim.mobject.geometry.arc.Annulus")

例子

示例： Annulus 示例[¶](#annulusexample)

![../_images/AnnulusExample-1.png](../_images/AnnulusExample-1.png)

from manim import \*

class AnnulusExample(Scene):
def construct(self):
annulus_1 = Annulus(inner_radius=0.5, outer_radius=1).shift(UP)
annulus_2 = Annulus(inner_radius=0.3, outer_radius=0.6, color=RED).next_to(annulus_1, DOWN)
self.add(annulus_1, annulus_2)

Copy to clipboard

方法

[`generate_points`](#manim.mobject.geometry.arc.Annulus.generate_points "manim.mobject.geometry.arc.Annulus.generate_points")

初始化`points`并因此初始化形状。

[`init_points`](#manim.mobject.geometry.arc.Annulus.init_points "manim.mobject.geometry.arc.Annulus.init_points")

初始化`points`并因此初始化形状。

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

生成点( )[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Annulus.generate_points)[#](#manim.mobject.geometry.arc.Annulus.generate_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

初始化点（）[#](#manim.mobject.geometry.arc.Annulus.init_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。
