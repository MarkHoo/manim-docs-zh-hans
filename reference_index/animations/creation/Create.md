# 创建[#](#create "此标题的固定链接")

合格名称：`manim.animation.creation.Create`

_类_ 创建（_mobject = None_， _\* args_， _use_override = True_， _\*\* kwargs_）[\[来源\]](../_modules/manim/animation/creation.html#Create)[#](#manim.animation.creation.Create "此定义的固定链接")

基地：[`ShowPartial`](manim.animation.creation.ShowPartial.html#manim.animation.creation.ShowPartial "manim.animation.creation.ShowPartial")

增量显示 VMobject。

参数

**mobject** – 要设置动画的 VMobject。

提高

**TypeError** – 如果`mobject`不是 的实例[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

例子

示例：创建场景[¶](#createscene)

from manim import \*

class CreateScene(Scene):
def construct(self):
self.play(Create(Square()))

Copy to clipboard

也可以看看

[`ShowPassingFlash`](manim.animation.indication.ShowPassingFlash.html#manim.animation.indication.ShowPassingFlash "manim.animation.inspiration.ShowPassingFlash")

方法
