# mobject_update_utils

用于 mobject 连续动画的实用函数。

Functions

`always(method, *args, **kwargs)`

`always_redraw(func)`

`always_rotate(mobject, rate=0.3490658503988659, **kwargs)`

`always_shift(mobject, direction=array([1., 0., 0.]), rate=0.1)`

`assert_is_mobject_method(method)`

`cycle_animation(animation, **kwargs)`


`f_always(method, *arg_generators, **kwargs)`

Always 的更多功能版本，它不接受参数，而是接受输出相关参数的函数。


`turn_animation_into_updater(animation, cycle=False, **kwargs)`

向动画的 mobject 添加更新程序，该更新程序应用动画的插值和更新功能

如果循环为 True，则此过程会一遍又一遍地重复。否则，更新程序将在完成后弹出
