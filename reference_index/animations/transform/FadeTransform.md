# 淡入淡出变换[#](#fadetransform "此标题的固定链接")

合格名称：`manim.animation.transform.FadeTransform`

_类_ FadeTransform ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#FadeTransform)[#](#manim.animation.transform.FadeTransform "此定义的固定链接")

基地：[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform")

将一个对象淡入另一个对象。

参数

- **mobject** – 起始[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject").
- **target_mobject** – 目标[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。
- **拉伸**– 控制目标[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")在动画过程中是否拉伸。默认值：`True`.
- **dim_to_match**[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") – 如果目标 mobject 没有自动拉伸，则可以在移入时调整目标的初始比例。分别将其设置为 0、1 和 2，使目标的长度与目标的长度相匹配[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")分别从 x、y 和 z 方向开始 。
- **kwargs** – 更多关键字参数传递给父类。

例子

示例：不同的淡入淡出变换[¶](#differentfadetransforms)

from manim import \*

class DifferentFadeTransforms(Scene):
def construct(self):
starts = \[Rectangle(width=4, height=1) for _ in range(3)\]
VGroup(*starts).arrange(DOWN, buff=1).shift(3*LEFT)
targets = \[Circle(fill_opacity=1).scale(0.25) for _ in range(3)\]
VGroup(*targets).arrange(DOWN, buff=1).shift(3*RIGHT)

        self.play(*\[FadeIn(s) for s in starts\])
        self.play(
            FadeTransform(starts\[0\], targets\[0\], stretch=True),
            FadeTransform(starts\[1\], targets\[1\], stretch=False, dim\_to\_match=0),
            FadeTransform(starts\[2\], targets\[2\], stretch=False, dim\_to\_match=1)
        )

        self.play(*\[FadeOut(mobj) for mobj in self.mobjects\])

Copy to clipboard

方法

[`begin`](#manim.animation.transform.FadeTransform.begin "manim.animation.transform.FadeTransform.begin")

动画的初始设置。

[`clean_up_from_scene`](#manim.animation.transform.FadeTransform.clean_up_from_scene "manim.animation.transform.FadeTransform.clean_up_from_scene")

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

`get_all_families_zipped`

[`get_all_mobjects`](#manim.animation.transform.FadeTransform.get_all_mobjects "manim.animation.transform.FadeTransform.get_all_mobjects")

获取动画中涉及的所有 mobject。

[`ghost_to`](#manim.animation.transform.FadeTransform.ghost_to "manim.animation.transform.FadeTransform.ghost_to")

将源替换为目标并将不透明度设置为 0。

属性

`path_arc`

`path_func`

开始( )[\[来源\]](../_modules/manim/animation/transform.html#FadeTransform.begin)[#](#manim.animation.transform.FadeTransform.begin "此定义的固定链接")

动画的初始设置。

该动画绑定到的 mobject 是由起始 mobject 和结束 mobject 组成的组。开始时，结束 mobject 取代起始 mobject（并且完全褪色）。最终，事情注定会适得其反。

clean_up_from*scene（*场景\_）[\[来源\]](../_modules/manim/animation/transform.html#FadeTransform.clean_up_from_scene)[#](#manim.animation.transform.FadeTransform.clean_up_from_scene "此定义的固定链接")

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

如果动画是移除器，则这包括[`remove()`](manim.scene.scene.Scene.html#manim.scene.scene.Scene.remove "manim.scene.scene.Scene.remove")动画 [`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

参数

**scene** – 应该清除动画的场景。

获取所有对象( )[\[来源\]](../_modules/manim/animation/transform.html#FadeTransform.get_all_mobjects)[#](#manim.animation.transform.FadeTransform.get_all_mobjects "此定义的固定链接")

获取动画中涉及的所有 mobject。

顺序必须与 interpolate_submobject 的参数顺序匹配

退货

mobject 的序列。

返回类型

序列\[ [Mobject](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") \]

Ghost*to（*源*，*目标\_）[\[来源\]](../_modules/manim/animation/transform.html#FadeTransform.ghost_to)[#](#manim.animation.transform.FadeTransform.ghost_to "此定义的固定链接")

将源替换为目标并将不透明度设置为 0。

如果提供的目标没有点，因此位置为 \[0, 0, 0\]，源将简单地淡出其当前所在位置。
