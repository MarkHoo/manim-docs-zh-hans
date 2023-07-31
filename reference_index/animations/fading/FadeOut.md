# 淡出[#](#fadeout "此标题的固定链接")

合格名称：`manim.animation.fading.FadeOut`

_类_ FadeOut ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/fading.html#FadeOut)[#](#manim.animation.fading.FadeOut "此定义的固定链接")

基地：`_Fade`

淡出[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")s.

参数

- **mobjects** – 要淡出的 mobjects。
- **shift** – 对象在淡出时移动的向量。
- **target_position** – mobject 在淡出时移动到的位置。如果另一个 mobject 被指定为目标位置，则使用其中心。
- **缩放**– 对象在淡出时缩放的系数。

例子

示例：淡入示例[¶](#fadeinexample)

from manim import \*

class FadeInExample(Scene):
def construct(self):
dot = Dot(UP * 2 + LEFT)
self.add(dot)
tex = Tex(
"FadeOut with ", "shift ", " or target\\\_position", " and scale"
).scale(1)
animations = \[
FadeOut(tex\[0\]),
FadeOut(tex\[1\], shift=DOWN),
FadeOut(tex\[2\], target_position=dot),
FadeOut(tex\[3\], scale=0.5),
\]
self.play(AnimationGroup(*animations, lag_ratio=0.5))

Copy to clipboard

方法

[`clean_up_from_scene`](#manim.animation.fading.FadeOut.clean_up_from_scene "manim.animation.fading.FadeOut.clean_up_from_scene")

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

`create_target`

属性

`path_arc`

`path_func`

clean_up_from*scene（*场景=无\_）[\[来源\]](../_modules/manim/animation/fading.html#FadeOut.clean_up_from_scene)[#](#manim.animation.fading.FadeOut.clean_up_from_scene "此定义的固定链接")

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

如果动画是移除器，则这包括[`remove()`](manim.scene.scene.Scene.html#manim.scene.scene.Scene.remove "manim.scene.scene.Scene.remove")动画 [`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

参数

**scene** (_可选\_\_\[_ [_Scene_](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景") _\]_ ) – 应清除动画的场景。

返回类型

没有任何
