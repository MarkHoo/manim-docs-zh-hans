# 继承[#](#succession "此标题的固定链接")

合格名称：`manim.animation.composition.Succession`

_类_ 继承（_mobject = None_， _\* args_， _use_override = True_， _\*\* kwargs_）[\[来源\]](../_modules/manim/animation/composition.html#Succession)[#](#manim.animation.composition.Succession "此定义的固定链接")

基地：[`AnimationGroup`](manim.animation.composition.AnimationGroup.html#manim.animation.composition.AnimationGroup "manim.animation.composition.AnimationGroup")

连续播放一系列动画。

参数

- **动画**[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")–要播放的对象序列。
- **滞后比率**–

  定义动画应用于子对象之前的延迟。lag_ratio `n.nn`表示当前动画播放完毕后将播放`nnn%`下一个动画。默认为 1.0，这意味着下一个动画将在当前动画播放 100% 时开始。

  这不会影响动画的总运行时间。相反，会调整各个动画的运行时间，以便完整的动画具有定义的运行时间。

例子

示例：继承示例[¶](#successionexample)

from manim import \*

class SuccessionExample(Scene):
def construct(self):
dot1 = Dot(point=LEFT _ 2 + UP _ 2, radius=0.16, color=BLUE)
dot2 = Dot(point=LEFT _ 2 + DOWN _ 2, radius=0.16, color=MAROON)
dot3 = Dot(point=RIGHT _ 2 + DOWN _ 2, radius=0.16, color=GREEN)
dot4 = Dot(point=RIGHT _ 2 + UP _ 2, radius=0.16, color=YELLOW)
self.add(dot1, dot2, dot3, dot4)

        self.play(Succession(
            dot1.animate.move_to(dot2),
            dot2.animate.move_to(dot3),
            dot3.animate.move_to(dot4),
            dot4.animate.move_to(dot1)
        ))

Copy to clipboard

方法

[`begin`](#manim.animation.composition.Succession.begin "manim.animation.composition.Succession.begin")

开始动画。

[`finish`](#manim.animation.composition.Succession.finish "manim.animation.composition.Succession.finish")

完成动画。

[`interpolate`](#manim.animation.composition.Succession.interpolate "manim.animation.composition.Succession.interpolate")

设置动画进度。

[`next_animation`](#manim.animation.composition.Succession.next_animation "manim.animation.composition.Succession.next_animation")

继续下一个动画。

`update_active_animation`

[`update_mobjects`](#manim.animation.composition.Succession.update_mobjects "manim.animation.composition.Succession.update_mobjects")

更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。

开始( )[\[来源\]](../_modules/manim/animation/composition.html#Succession.begin)[#](#manim.animation.composition.Succession.begin "此定义的固定链接")

开始动画。

该方法在动画播放时被调用。尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。

返回类型

没有任何

完成( )[\[来源\]](../_modules/manim/animation/composition.html#Succession.finish)[#](#manim.animation.composition.Succession.finish "此定义的固定链接")

完成动画。

动画结束时会调用此方法。

返回类型

没有任何

插值(_阿尔法_)[\[来源\]](../_modules/manim/animation/composition.html#Succession.interpolate)[#](#manim.animation.composition.Succession.interpolate "此定义的固定链接")

设置动画进度。

动画期间的每一帧都会调用此方法。

参数

**alpha** ( _float_ ) – 设置动画的相对时间，0 表示开始，1 表示结束。

返回类型

没有任何

下一个动画( )[\[来源\]](../_modules/manim/animation/composition.html#Succession.next_animation)[#](#manim.animation.composition.Succession.next_animation "此定义的固定链接")

继续下一个动画。

当活动动画结束时立即调用此方法。

返回类型

没有任何

update*mobjects ( \_dt* )[\[来源\]](../_modules/manim/animation/composition.html#Succession.update_mobjects)[#](#manim.animation.composition.Succession.update_mobjects "此定义的固定链接")

更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。请注意，由于通常（总是？） self.mobject 会在动画期间暂停其更新，因此这对 self.mobject 没有任何作用。

参数

**dt**（_浮动_）–

返回类型

没有任何
