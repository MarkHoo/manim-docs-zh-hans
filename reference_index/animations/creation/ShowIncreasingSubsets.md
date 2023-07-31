# 显示增加子集[#](#showincreasingsubsets "此标题的固定链接")

合格名称：`manim.animation.creation.ShowIncreasingSubsets`

_类_ ShowIncreasingSubsets ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/creation.html#ShowIncreasingSubsets)[#](#manim.animation.creation.ShowIncreasingSubsets "此定义的固定链接")

基地：[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")

一次显示一个子对象，使所有先前的子对象显示在屏幕上。

例子

示例：显示 IncreasingSubsetsScene [¶](#showincreasingsubsetsscene)

from manim import \*

class ShowIncreasingSubsetsScene(Scene):
def construct(self):
p = VGroup(Dot(), Square(), Triangle())
self.add(p)
self.play(ShowIncreasingSubsets(p))
self.wait()

Copy to clipboard

方法

[`interpolate_mobject`](#manim.animation.creation.ShowIncreasingSubsets.interpolate_mobject "manim.animation.creation.ShowIncreasingSubsets.interpolate_mobject")

根据 alpha 值对 mobject 进行插值`Animation`。

`update_submobject_list`

interpolate*mobject (*阿尔法\_)[\[来源\]](../_modules/manim/animation/creation.html#ShowIncreasingSubsets.interpolate_mobject)[#](#manim.animation.creation.ShowIncreasingSubsets.interpolate_mobject "此定义的固定链接")

根据 alpha 值对 mobject 进行插值`Animation`。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

没有任何
