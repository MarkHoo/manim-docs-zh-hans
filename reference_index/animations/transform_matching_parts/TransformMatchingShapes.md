# 变换匹配形状[#](#transformmatchingshapes "此标题的固定链接")

合格名称：`manim.animation.transform\_matching\_parts.TransformMatchingShapes`

_类_ TransformMatchingShapes ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform_matching_parts.html#TransformMatchingShapes)[#](#manim.animation.transform_matching_parts.TransformMatchingShapes "此定义的固定链接")

基地：[`TransformMatchingAbstractBase`](manim.animation.transform_matching_parts.TransformMatchingAbstractBase.html#manim.animation.transform_matching_parts.TransformMatchingAbstractBase "manim.animation.transform_matching_parts.TransformMatchingAbstractBase")

试图通过匹配组的子对象的形状来变换组的动画。

如果归一化后（即，平移到原点后，将子对象高度固定为 1 个单位，并将坐标四舍五入到小数点后三位）匹配，则两个子对象匹配。

也可以看看

[`TransformMatchingAbstractBase`](manim.animation.transform_matching_parts.TransformMatchingAbstractBase.html#manim.animation.transform_matching_parts.TransformMatchingAbstractBase "manim.animation.transform_matching_parts.TransformMatchingAbstractBase")

例子

示例：字谜[¶](#anagram)

from manim import \*

class Anagram(Scene):
def construct(self):
src = Text("the morse code")
tar = Text("here come dots")
self.play(Write(src))
self.wait(0.5)
self.play(TransformMatchingShapes(src, tar, path_arc=PI/2))
self.wait(0.5)

Copy to clipboard

方法

`get_mobject_key`

`get_mobject_parts`
