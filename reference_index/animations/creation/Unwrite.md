# 取消写入[#](#unwrite "此标题的固定链接")

合格名称：`manim.animation.creation.Unwrite`

_类_ Unwrite ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/creation.html#Unwrite)[#](#manim.animation.creation.Unwrite "此定义的固定链接")

基地：[`Write`](manim.animation.creation.Write.html#manim.animation.creation.Write "manim.animation.creation.Write")

模拟用手擦除 a[`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")或 a [`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

参数

**相反**– 设置 True 以使动画首先从最后一个子对象开始擦除。

例子

示例：UnwriteReverseTrue [¶](#unwritereversetrue)

from manim import \*

class UnwriteReverseTrue(Scene):
def construct(self):
text = Tex("Alice and Bob").scale(3)
self.add(text)
self.play(Unwrite(text))

Copy to clipboard

示例：UnwriteReverseFalse [¶](#unwritereversefalse)

from manim import \*

class UnwriteReverseFalse(Scene):
def construct(self):
text = Tex("Alice and Bob").scale(3)
self.add(text)
self.play(Unwrite(text, reverse=False))

Copy to clipboard

方法
