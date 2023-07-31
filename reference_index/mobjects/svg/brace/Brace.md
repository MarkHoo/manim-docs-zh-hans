# 大括号[#](#brace "此标题的固定链接")

合格名称：`manim.mobject.svg.brace.Brace`

_类_ Brace ( _mobject_ ,_方向= array(\[0., \- 1., 0.\])_ , _buff = 0.2_ ,_锐度= 2_ ,_描边宽度= 0_ ,_填充不透明度= 1.0_ ,_背景描边宽度= 0_ ,_描边颜色= '#000000'_ , _\* \*夸格斯_）[\[来源\]](../_modules/manim/mobject/svg/brace.html#Brace)[#](#manim.mobject.svg.brace.Brace "此定义的固定链接")

基地：[`VMobjectFromSVGPath`](manim.mobject.svg.svg_mobject.VMobjectFromSVGPath.html#manim.mobject.svg.svg_mobject.VMobjectFromSVGPath "manim.mobject.svg.svg_mobject.VMobjectFromSVGPath")

获取一个 mobject 并在其旁边绘制一个大括号。

传递方向向量确定绘制支撑的方向。默认情况下，它是从下面绘制的。

参数

- **mobject** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 与大括号相邻的 mobject。
- **Direction** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 支撑面向 mobject 的方向。

也可以看看

[`BraceBetweenPoints`](manim.mobject.svg.brace.BraceBetweenPoints.html#manim.mobject.svg.brace.BraceBetweenPoints "manim.mobject.svg.brace.BraceBetweenPoints")

例子

示例：大括号示例[¶](#braceexample)

![../_images/BraceExample-1.png](../_images/BraceExample-1.png)

from manim import \*

class BraceExample(Scene):
def construct(self):
s = Square()
self.add(s)
for i in np.linspace(0.1,1.0,4):
br = Brace(s, sharpness=i)
t = Text(f"sharpness= {i}").next_to(br, RIGHT)
self.add(t)
self.add(br)
VGroup(\*self.mobjects).arrange(DOWN, buff=0.2)

Copy to clipboard

方法

[`get_direction`](#manim.mobject.svg.brace.Brace.get_direction "manim.mobject.svg.brace.Brace.get_direction")

用于[`shoelace_direction()`](manim.utils.space_ops.html#manim.utils.space_ops.shoelace_direction "manim.utils.space_ops.shoelac_direction")计算方向。

`get_tex`

`get_text`

`get_tip`

`put_at_tip`

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

获取方向( )[\[来源\]](../_modules/manim/mobject/svg/brace.html#Brace.get_direction)[#](#manim.mobject.svg.brace.Brace.get_direction "此定义的固定链接")

用于[`shoelace_direction()`](manim.utils.space_ops.html#manim.utils.space_ops.shoelace_direction "manim.utils.space_ops.shoelac_direction")计算方向。点的方向决定了绘制对象的方向，顺时针还是逆时针。

例子

a 的默认方向[`Circle`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")是逆时针：

> > \> from manim import Circle
> > \> Circle().get_direction()
> > 'CCW'

Copy to clipboard

退货

要么`"CW"`要么`"CCW"`.

返回类型

`str`
