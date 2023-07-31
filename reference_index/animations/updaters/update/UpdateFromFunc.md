# 更新自函数[#](#updatefromfunc "此标题的固定链接")

合格名称：`manim.animation.updaters.update.UpdateFromFunc`

_类_ UpdateFromFunc ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/updaters/update.html#UpdateFromFunc)[#](#manim.animation.updaters.update.UpdateFromFunc "此定义的固定链接")

基地：[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")

update_function 形式为 func(mobject)，大概在一个 mobject 的状态依赖于另一个同时动画的 mobject 时使用

方法

[`interpolate_mobject`](#manim.animation.updaters.update.UpdateFromFunc.interpolate_mobject "manim.animation.updaters.update.UpdateFromFunc.interpolate_mobject")

根据 alpha 值对 mobject 进行插值`Animation`。

interpolate*mobject (*阿尔法\_)[\[来源\]](../_modules/manim/animation/updaters/update.html#UpdateFromFunc.interpolate_mobject)[#](#manim.animation.updaters.update.UpdateFromFunc.interpolate_mobject "此定义的固定链接")

根据 alpha 值对 mobject 进行插值`Animation`。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

没有任何
