# 虚线

合格名称：`manim.mobject.geometry.line.DashedLine`

```py
class DashedLine(*args, dash_length=0.05, dashed_ratio=0.5, **kwargs)
```

Bases: Line

一个虚线[`Line`]()。

参数

- **args** ( _Any_ ) – 要传递给的参数[`Line`]()
- **dash_length** ( _float_ ) – 线条中每个单独虚线的长度。
- **dashed_ratio** ( _float_ ) – 虚线空间与空白空间的比率。范围为 0-1。
- **kwargs** – 要传递给的附加参数[`Line`]()

> 也可以看看

> [`DashedVMobject`]()

例子

示例：虚线示例

![DashedLineExample-1.png](../static/DashedLineExample-1.png)

```py
from manim import *

class DashedLineExample(Scene):
    def construct(self):
        # dash_length increased
        dashed_1 = DashedLine(config.left_side, config.right_side, dash_length=2.0).shift(UP*2)
        # normal
        dashed_2 = DashedLine(config.left_side, config.right_side)
        # dashed_ratio decreased
        dashed_3 = DashedLine(config.left_side, config.right_side, dashed_ratio=0.1).shift(DOWN*2)
        self.add(dashed_1, dashed_2, dashed_3)
```

方法

|||
|-|-|
[`get_end`])|返回线的终点。
[`get_first_handle`]()|返回第一个句柄的点。
[`get_last_handle`]()|返回最后一个句柄的点。
[`get_start`]()|返回线的起点。


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


`get_end()`

返回线的终点。

例子

```sh
>>> DashedLine().get_end()
array([1., 0., 0.])
```

返回类型

_ndarray_

`get_first_handle()`

返回第一个句柄的点。

例子

```sh
>>> DashedLine().get_first_handle()
array([-0.98333333,  0.        ,  0.        ])
```

返回类型

_ndarray_

`get_last_handle()`

返回最后一个句柄的点。

例子

```sh
>>> DashedLine().get_last_handle()
array([0.98333333, 0.        , 0.        ])
```

返回类型

_ndarray_

`get_start()`

返回线的起点。

例子

```sh
>>> DashedLine().get_start()
array([-1.,  0.,  0.])
```

返回类型

_ndarray_
