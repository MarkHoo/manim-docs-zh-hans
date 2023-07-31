# 滞后启动映射[#](#laggedstartmap "此标题的固定链接")

合格名称：`manim.animation.composition.LaggedStartMap`

_类_ LaggedStartMap ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/composition.html#LaggedStartMap)[#](#manim.animation.composition.LaggedStartMap "此定义的固定链接")

基地：[`LaggedStart`](manim.animation.composition.LaggedStart.html#manim.animation.composition.LaggedStart "manim.animation.composition.LaggedStart")

[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")将函数映射到子对象时播放一系列内容。

参数

- **AnimationClass** –[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")应用于 mobject。
- **mobject** –[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")将应用其子对象动画和可选的函数。
- **arg_creator** – 将应用于[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject").
- **run_time** – 动画的持续时间（以秒为单位）。

例子

示例：LaggedStartMapExample [¶](#laggedstartmapexample)

from manim import \*

class LaggedStartMapExample(Scene):
def construct(self):
title = Tex("LaggedStartMap").to*edge(UP, buff=LARGE_BUFF)
dots = VGroup(
\*\[Dot(radius=0.16) for * in range(35)\]
).arrange_in_grid(rows=5, cols=7, buff=MED_LARGE_BUFF)
self.add(dots, title)

        \# Animate yellow ripple effect
        for mob in dots, title:
            self.play(LaggedStartMap(
                ApplyMethod, mob,
                lambda m : (m.set_color, YELLOW),
                lag_ratio = 0.1,
                rate_func = there\_and\_back,
                run_time = 2
            ))

Copy to clipboard

方法
