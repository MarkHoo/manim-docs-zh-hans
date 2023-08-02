# mobject_update_utils

用于 mobject 连续动画的实用函数。

Functions

always(_method_, _\*args_, _\*\*kwargs_)[\[source\]]()

always*redraw(\_func*)

always*rotate(\_mobject*, _rate=0.3490658503988659_, _\*\*kwargs_)

always*shift(\_mobject*, _direction=array(\[1., 0., 0.\])_, _rate=0.1_)

assert_is_mobject*method(\_method*)

cycle*animation(\_animation*, _\*\*kwargs_)

f*always(\_method*, _\*arg_generators_, _\*\*kwargs_)

Always 的更多功能版本，它不接受参数，而是接受输出相关参数的函数。

turn*animation_into*updater(\_animation*, \_cycle=False*, _\*\*kwargs_)

向动画的 mobject 添加更新程序，该更新程序应用动画的插值和更新功能

如果循环为 True，则此过程会一遍又一遍地重复。否则，更新程序将在完成后弹出
