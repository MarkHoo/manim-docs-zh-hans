# 成长


通过从点增长对象将对象引入场景的动画。

示例：成长

[![视频缩略图]()](https://docs.manim.community/en/stable/reference/Growing-1.mp4)

```py
from manim import *

class Growing(Scene):
    def construct(self):
        square = Square()
        circle = Circle()
        triangle = Triangle()
        arrow = Arrow(LEFT, RIGHT)
        star = Star()

        VGroup(square, circle, triangle).set_x(0).arrange(buff=1.5).set_y(2)
        VGroup(arrow, star).move_to(DOWN).set_x(0).arrange(buff=1.5).set_y(-2)

        self.play(GrowFromPoint(square, ORIGIN))
        self.play(GrowFromCenter(circle))
        self.play(GrowFromEdge(triangle, DOWN))
        self.play(GrowArrow(arrow))
        self.play(SpinInFromNothing(star))
```

Classes

|||
|-|-|
[`GrowArrow`]()|[`Arrow`]()通过从开始向尖端生长来引入。
[`GrowFromCenter`]()|[`Mobject`]()通过从中心生长来引入。
[`GrowFromEdge`]()|[`Mobject`]()通过从其边界框边缘之一增长它来引入。
[`GrowFromPoint`](")|[`Mobject`]()通过从一点增长来引入。
[`SpinInFromNothing`]()|引入[`Mobject`]()旋转并从中心开始生长。

