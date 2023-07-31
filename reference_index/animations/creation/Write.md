# 写[#](#write "此标题的固定链接")

合格名称：`manim.animation.creation.Write`

_类_ Write ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/creation.html#Write)[#](#manim.animation.creation.Write "此定义的固定链接")

基地：[`DrawBorderThenFill`](manim.animation.creation.DrawBorderThenFill.html#manim.animation.creation.DrawBorderThenFill "manim.animation.creation.DrawBorderThenFill")

模拟手写[`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")或手绘[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

例子

示例：ShowWrite [¶](#showwrite)

from manim import \*

class ShowWrite(Scene):
def construct(self):
self.play(Write(Text("Hello", font_size=144)))

Copy to clipboard

示例：ShowWriteReversed [¶](#showwritereversed)

from manim import \*

class ShowWriteReversed(Scene):
def construct(self):
self.play(Write(Text("Hello", font_size=144), reverse=True, remover=False))

Copy to clipboard

测试

检查创建空[`Write`](#manim.animation.creation.Write "manim.animation.creation.Write")动画是否有效：

> > \> from manim import Write, Text
> > \> Write(Text(''))
> > Write(Text(''))

Copy to clipboard

方法

[`begin`](#manim.animation.creation.Write.begin "manim.animation.creation.Write.begin")

开始动画。

[`finish`](#manim.animation.creation.Write.finish "manim.animation.creation.Write.finish")

完成动画。

`reverse_submobjects`

开始( )[\[来源\]](../_modules/manim/animation/creation.html#Write.begin)[#](#manim.animation.creation.Write.begin "此定义的固定链接")

开始动画。

该方法在动画播放时被调用。尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。

返回类型

没有任何

完成( )[\[来源\]](../_modules/manim/animation/creation.html#Write.finish)[#](#manim.animation.creation.Write.finish "此定义的固定链接")

完成动画。

动画结束时会调用此方法。

返回类型

没有任何
