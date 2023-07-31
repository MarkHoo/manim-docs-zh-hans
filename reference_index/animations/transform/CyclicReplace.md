# 循环替换[#](#cyclicreplace "此标题的固定链接")

合格名称：`manim.animation.transform.CyclicReplace`

_类_ CyclicReplace ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#CyclicReplace)[#](#manim.animation.transform.CyclicReplace "此定义的固定链接")

基地：[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform")

循环移动对象的动画。

具体来说，这意味着：第一个 mobject 取代第二个 mobject，第二个 mobject 取代第三个 mobject，依此类推。最后一个 mobject 取代了第一个 mobject。

参数

- **mobjects** – 要转换的 mobject 列表。
- **path_arc** – mobjects 到达目标所遵循的弧线角度（以弧度为单位）。
- **kwargs** – 传递给 的更多关键字参数[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform")。

例子

示例：循环替换示例[¶](#cyclicreplaceexample)

from manim import \*

class CyclicReplaceExample(Scene):
def construct(self):
group = VGroup(Square(), Circle(), Triangle(), Star())
group.arrange(RIGHT)
self.add(group)

        for _ in range(4):
            self.play(CyclicReplace(*group))

Copy to clipboard

方法

`create_target`

属性

`path_arc`

`path_func`
