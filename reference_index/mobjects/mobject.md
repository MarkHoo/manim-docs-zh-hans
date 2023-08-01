# 对象

可显示对象的基类。

课程

[`Group`](manim.mobject.mobject.Group.html#manim.mobject.mobject.Group "manim.mobject.mobject.Group")

多个组合在一起[`Mobjects`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

数学对象：可以在屏幕上显示的对象的基类。

功能

override*animate（*方法\_）[\[来源\]](../_modules/manim/mobject/mobject.html#override_animate)[#](#manim.mobject.mobject.override_animate "此定义的固定链接")

用于重写方法动画的装饰器。

这允许指定一个方法（返回），当装饰方法与用于动画方法应用程序的语法[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")一起使用时调用该方法。`.animate`

也可以看看

[`Mobject.animate`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.animate "manim.mobject.mobject.Mobject.animate")

笔记

重写方法不能与使用语法链接的普通方法或其他重写方法组合`.animate`。

例子

示例：AnimationOverrideExample [¶](#animationoverrideexample)

from manim import \*

class CircleWithContent(VGroup):
def \_\_init\_\_(self, content):
super().\_\_init\_\_()
self.circle = Circle()
self.content = content
self.add(self.circle, content)
content.move_to(self.circle.get_center())

    def clear_content(self):
        self.remove(self.content)
        self.content = None

    @override_animate(clear_content)
    def \_clear\_content_animation(self, anim_args=None):
        if anim_args is None:
            anim_args = {}
        anim = Uncreate(self.content, **anim_args)
        self.clear_content()
        return anim

class AnimationOverrideExample(Scene):
def construct(self):
t = Text("hello!")
my_mobject = CircleWithContent(t)
self.play(Create(my_mobject))
self.play(my_mobject.animate.clear_content())
self.wait()

Copy to clipboard
