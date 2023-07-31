# 注明[#](#indicate "此标题的固定链接")

合格名称：`manim.animation.indication.Indicate`

_类_ 指示( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/indication.html#Indicate)[#](#manim.animation.indication.Indicate "此定义的固定链接")

基地：[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform")

通过暂时调整 Mobject 的大小和重新着色来指示它。

参数

- **mobject** – 要指示的 mobject。
- **scale_factor** – 对象临时缩放的因子
- **color** – 对象暂时采用的颜色。
- **rate_func** – 定义每个时间点的动画进度的函数。
- **kwargs** – 要传递给[`Succession`](manim.animation.composition.Succession.html#manim.animation.composition.Succession "manim.animation.composition.Succession")构造函数的附加参数

例子

示例：使用指示[¶](#usingindicate)

from manim import \*

class UsingIndicate(Scene):
def construct(self):
tex = Tex("Indicate").scale(3)
self.play(Indicate(tex))
self.wait()

Copy to clipboard

方法

`create_target`

属性

`path_arc`

`path_func`
