# 焦点[#](#focuson "此标题的固定链接")

合格名称：`manim.animation.indication.FocusOn`

_类_ FocusOn ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/indication.html#FocusOn)[#](#manim.animation.indication.FocusOn "此定义的固定链接")

基地：[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform")

将聚光灯缩小到某个位置。

参数

- **focus_point** – 缩小聚光灯的点。如果是 a，`Mobject`则将使用其中心。
- **不透明度**– 聚光灯的不透明度。
- **颜色**– 聚光灯的颜色。
- **run_time** – 动画的持续时间。
- **kwargs** – 要传递给[`Succession`](manim.animation.composition.Succession.html#manim.animation.composition.Succession "manim.animation.composition.Succession")构造函数的附加参数

例子

示例：使用 FocusOn [¶](#usingfocuson)

from manim import \*

class UsingFocusOn(Scene):
def construct(self):
dot = Dot(color=YELLOW).shift(DOWN)
self.add(Tex("Focusing on the dot below:"), dot)
self.play(FocusOn(dot))
self.wait()

Copy to clipboard

方法

`create_target`

属性

`path_arc`

`path_func`
