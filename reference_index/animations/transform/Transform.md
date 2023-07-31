# 变换[#](#transform "此标题的固定链接")

合格名称：`manim.animation.transform.Transform`

_类_ Transform ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#Transform)[#](#manim.animation.transform.Transform "此定义的固定链接")

基地：[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")

Transform 将 Mobject 转换为目标 Mobject。

参数

- **mobject** –[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")要转换的对象。它将变异成为`target_mobject`.
- **target_mobject** – 转换的目标。
- **path_func** – 定义 的点沿其`mobject`移动直到与 的点匹配的路径的函数`target_mobject`，请参阅[`utils.paths`](manim.utils.paths.html#module-manim.utils.paths "manim.utils.paths")。
- **path_arc** – 如果使用圆形路径弧，则 的点将`mobject`遵循的弧角（以弧度为单位）到达目标点，请参阅`path_arc_centers`。另请参阅[`manim.utils.paths.path_along_arc()`](manim.utils.paths.html#manim.utils.paths.path_along_arc "manim.utils.paths.path_along_arc")。
- **path_arc_axis** – 如果使用圆形路径弧，则沿其旋转的轴，请参阅`path_arc_centers`。
- **路径弧中心**–

  圆弧的中心， 的点`mobject`通过变换移动。

  如果设置和`path_func`未设置，则将`path_along_circles`使用`path_arc`参数生成路径并存储在`path_func`. 如果`path_func`设置了 ，则该字段和其他`path_arc`字段将被设置为属性，但`path_func`不会从中生成 a 。

- **Replace_mobject_with_target_in_scene** –

  控制转换完成后替换哪个对象。

  如果设置为 True，`mobject`将从场景中删除并`target_mobject`替换它。否则，`target_mobject`永远不会被添加，`mobject`只会形成其形状。

例子

示例：TransformPathArc [¶](#transformpatharc)

from manim import \*

class TransformPathArc(Scene):
def construct(self):
def make_arc_path(start, end, arc_angle):
points = \[\]
p_fn = path_along_arc(arc_angle)
\# alpha animates between 0.0 and 1.0, where 0.0
\# is the beginning of the animation and 1.0 is the end.
for alpha in range(0, 11):
points.append(p_fn(start, end, alpha / 10.0))
path = VMobject(stroke_color=YELLOW)
path.set_points_smoothly(points)
return path

        left = Circle(stroke_color=BLUE_E, fill_opacity=1.0, radius=0.5).move_to(LEFT * 2)
        colors = \[TEAL_A, TEAL_B, TEAL_C, TEAL_D, TEAL_E, GREEN_A\]
        \# Positive angles move counter-clockwise, negative angles move clockwise.
        examples = \[-90, 0, 30, 90, 180, 270\]
        anims = \[\]
        for idx, angle in enumerate(examples):
            left_c = left.copy().shift((3 - idx) * UP)
            left_c.fill_color = colors\[idx\]
            right_c = left_c.copy().shift(4 * RIGHT)
            path_arc = make\_arc\_path(left_c.get_center(), right_c.get_center(),
                                     arc_angle=angle * DEGREES)
            desc = Text('%d°' % examples\[idx\]).next_to(left_c, LEFT)
            \# Make the circles in front of the text in front of the arcs.
            self.add(
                path_arc.set\_z\_index(1),
                desc.set\_z\_index(2),
                left_c.set\_z\_index(3),
            )
            anims.append(Transform(left_c, right_c, path_arc=angle * DEGREES))

        self.play(*anims, run_time=2)
        self.wait()

Copy to clipboard

方法

[`begin`](#manim.animation.transform.Transform.begin "manim.animation.transform.Transform.begin")

开始动画。

[`clean_up_from_scene`](#manim.animation.transform.Transform.clean_up_from_scene "manim.animation.transform.Transform.clean_up_from_scene")

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

`create_target`

`get_all_families_zipped`

[`get_all_mobjects`](#manim.animation.transform.Transform.get_all_mobjects "manim.animation.transform.Transform.get_all_mobjects")

获取动画中涉及的所有 mobject。

`interpolate_submobject`

属性

`path_arc`

`path_func`

开始( )[\[来源\]](../_modules/manim/animation/transform.html#Transform.begin)[#](#manim.animation.transform.Transform.begin "此定义的固定链接")

开始动画。

该方法在动画播放时被调用。尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。

返回类型

没有任何

clean_up_from*scene（*场景\_）[\[来源\]](../_modules/manim/animation/transform.html#Transform.clean_up_from_scene)[#](#manim.animation.transform.Transform.clean_up_from_scene "此定义的固定链接")

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

如果动画是移除器，则这包括[`remove()`](manim.scene.scene.Scene.html#manim.scene.scene.Scene.remove "manim.scene.scene.Scene.remove")动画 [`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

参数

**scene** ( [_Scene_](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景") ) – 应清除动画的场景。

返回类型

没有任何

获取所有对象( )[\[来源\]](../_modules/manim/animation/transform.html#Transform.get_all_mobjects)[#](#manim.animation.transform.Transform.get_all_mobjects "此定义的固定链接")

获取动画中涉及的所有 mobject。

顺序必须与 interpolate_submobject 的参数顺序匹配

退货

mobject 的序列。

返回类型

序列\[ [Mobject](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") \]
