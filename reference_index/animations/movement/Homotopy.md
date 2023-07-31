# 同伦[#](#homotopy "此标题的固定链接")

合格名称：`manim.animation.movement.Homotopy`

_类同_ 伦（_mobject = None_， _\* args_， _use_override = True_， _\*\* kwargs_）[\[来源\]](../_modules/manim/animation/movement.html#Homotopy)[#](#manim.animation.movement.Homotopy "此定义的固定链接")

基地：[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")

同伦。

这是根据指定的变换函数变换 mobject 的点的动画。随着参数 t 在整个动画中从 0 到 1(x,y,z) 描述 mobject 点的坐标，传递给`homotopy`关键字参数的函数应该转换元组(x,y,z,t)到(x′,y′,z′)，原点在某时刻变换到的坐标 t。

参数

- **同伦**——函数映射(x,y,z,t)到(x′,y′,z′)。
- **mobject** – 在给定同伦下变换的 mobject。
- **run_time** – 动画的运行时间。
- **apply_function_kwargs** – 传播到 的关键字参数`Mobject.apply_function()`。
- **kwargs** – 传递给父类的更多关键字参数。

方法

`function_at_time_t`

`interpolate_submobject`
