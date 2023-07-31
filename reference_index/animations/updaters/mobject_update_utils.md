# mobject_update_utils[#](#module-manim.animation.updaters.mobject_update_utils "Permalink to this heading")

用于 mobject 连续动画的实用函数。

Functions

always(_method_, _\*args_, _\*\*kwargs_)[\[source\]](../_modules/manim/animation/updaters/mobject_update_utils.html#always)[#](#manim.animation.updaters.mobject_update_utils.always "Permalink to this definition")

always*redraw(\_func*)[\[source\]](../_modules/manim/animation/updaters/mobject_update_utils.html#always_redraw)[#](#manim.animation.updaters.mobject_update_utils.always_redraw "Permalink to this definition")

always*rotate(\_mobject*, _rate=0.3490658503988659_, _\*\*kwargs_)[\[source\]](../_modules/manim/animation/updaters/mobject_update_utils.html#always_rotate)[#](#manim.animation.updaters.mobject_update_utils.always_rotate "Permalink to this definition")

always*shift(\_mobject*, _direction=array(\[1., 0., 0.\])_, _rate=0.1_)[\[source\]](../_modules/manim/animation/updaters/mobject_update_utils.html#always_shift)[#](#manim.animation.updaters.mobject_update_utils.always_shift "Permalink to this definition")

assert_is_mobject*method(\_method*)[\[source\]](../_modules/manim/animation/updaters/mobject_update_utils.html#assert_is_mobject_method)[#](#manim.animation.updaters.mobject_update_utils.assert_is_mobject_method "Permalink to this definition")

cycle*animation(\_animation*, _\*\*kwargs_)[\[source\]](../_modules/manim/animation/updaters/mobject_update_utils.html#cycle_animation)[#](#manim.animation.updaters.mobject_update_utils.cycle_animation "Permalink to this definition")

f*always(\_method*, _\*arg_generators_, _\*\*kwargs_)[\[source\]](../_modules/manim/animation/updaters/mobject_update_utils.html#f_always)[#](#manim.animation.updaters.mobject_update_utils.f_always "Permalink to this definition")

Always 的更多功能版本，它不接受参数，而是接受输出相关参数的函数。

turn*animation_into*updater(\_animation*, \_cycle=False*, _\*\*kwargs_)[\[source\]](../_modules/manim/animation/updaters/mobject_update_utils.html#turn_animation_into_updater)[#](#manim.animation.updaters.mobject_update_utils.turn_animation_into_updater "Permalink to this definition")

向动画的 mobject 添加更新程序，该更新程序应用动画的插值和更新功能

如果循环为 True，则此过程会一遍又一遍地重复。否则，更新程序将在完成后弹出
