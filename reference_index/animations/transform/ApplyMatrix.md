# 应用矩阵

合格名称：`manim.animation.transform.ApplyMatrix`

```py
class ApplyMatrix(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `ApplyPointwiseFunction`

对 mobject 应用矩阵变换。

参数

- **matrix**——变换矩阵。
- **mobject**– [`Mobject`]().
- **about_point** – 变换的原点。默认为`ORIGIN`.
- **kwargs** – 传递给 的更多关键字参数[`ApplyPointwiseFunction`]()。


例子

示例：ApplyMatrixExample

```py
from manim import *

class ApplyMatrixExample(Scene):
    def construct(self):
        matrix = [[1, 1], [0, 2/3]]
        self.play(ApplyMatrix(matrix, Text("Hello World!")), ApplyMatrix(matrix, NumberPlane()))
```


方法

`initialize_matrix`


属性

`path_arc`
`path_func`
