# 应用方法[#](#applymethod "此标题的固定链接")

合格名称：`manim.animation.transform.ApplyMethod`

_类_ ApplyMethod ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#ApplyMethod)[#](#manim.animation.transform.ApplyMethod "此定义的固定链接")

基地：[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform")

通过应用方法对 mobject 进行动画处理。

注意，这个动画只需要传递方法，不需要传递相应的 mobject。此外，该动画类仅在该方法返回修改后的 mobject 时才起作用。

参数

- **method** – 将在动画中应用的方法。
- **args** – 应用该方法时要传递的任何位置参数。
- **kwargs** – 传递给[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform").

方法

`check_validity_of_input`

`create_target`

属性

`path_arc`

`path_func`
