# 恢复[#](#restore "此标题的固定链接")

合格名称：`manim.animation.transform.Restore`

_类_ Restore ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#Restore)[#](#manim.animation.transform.Restore "此定义的固定链接")

基地：[`ApplyMethod`](manim.animation.transform.ApplyMethod.html#manim.animation.transform.ApplyMethod "manim.animation.transform.ApplyMethod")

将 mobject 转换为其上次保存的状态。

要保存 mobject 的状态，请使用[`save_state()`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.save_state "manim.mobject.mobject.Mobject.save_state")方法。

例子

示例：恢复示例[¶](#restoreexample)

from manim import \*

class RestoreExample(Scene):
def construct(self):
s = Square()
s.save_state()
self.play(FadeIn(s))
self.play(s.animate.set_color(PURPLE).set_opacity(0.5).shift(2*LEFT).scale(3))
self.play(s.animate.shift(5*DOWN).rotate(PI/4))
self.wait()
self.play(Restore(s), run_time=2)

Copy to clipboard

方法

属性

`path_arc`

`path_func`
