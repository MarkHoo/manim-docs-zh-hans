# 显示传递 Flash [#](#showpassingflash "此标题的固定链接")

合格名称：`manim.animation.indication.ShowPassingFlash`

_类_ ShowPassingFlash ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/indication.html#ShowPassingFlash)[#](#manim.animation.indication.ShowPassingFlash "此定义的固定链接")

基地：[`ShowPartial`](manim.animation.creation.ShowPartial.html#manim.animation.creation.ShowPartial "manim.animation.creation.ShowPartial")

每帧仅显示 VMobject 的一小部分。

参数

- **mobject** – 其笔划具有动画效果的 mobject。
- **time_width** – 条子的长度相对于笔划的长度。

例子

示例：时间宽度值[¶](#timewidthvalues)

from manim import \*

class TimeWidthValues(Scene):
def construct(self):
p = RegularPolygon(5, color=DARK_GRAY, stroke_width=6).scale(3)
lbl = VMobject()
self.add(p, lbl)
p = p.copy().set_color(BLUE)
for time_width in \[0.2, 0.5, 1, 2\]:
lbl.become(Tex(r"\\texttt{time\\\_width={{%.1f}}}"%time_width))
self.play(ShowPassingFlash(
p.copy().set_color(BLUE),
run_time=2,
time_width=time_width
))

Copy to clipboard

也可以看看

[`Create`](manim.animation.creation.Create.html#manim.animation.creation.Create "manim.animation.creation.Create")

方法

[`clean_up_from_scene`](#manim.animation.indication.ShowPassingFlash.clean_up_from_scene "manim.animation.indicate.ShowPassingFlash.clean_up_from_scene")

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

clean_up_from*scene（*场景\_）[\[来源\]](../_modules/manim/animation/indication.html#ShowPassingFlash.clean_up_from_scene)[#](#manim.animation.indication.ShowPassingFlash.clean_up_from_scene "此定义的固定链接")

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

如果动画是移除器，则这包括[`remove()`](manim.scene.scene.Scene.html#manim.scene.scene.Scene.remove "manim.scene.scene.Scene.remove")动画 [`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

参数

**scene** ( [_Scene_](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景") ) – 应清除动画的场景。

返回类型

没有任何
