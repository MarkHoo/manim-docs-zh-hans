# 路径

确定点集之间的变换路径的函数。

Functions

`clockwise_path()`

该函数通过顺时针移动半圆来变换每个点。

例子

示例：ClockwisePath 示例

```py
from manim import *

class ClockwisePathExample(Scene):
    def construct(self):
        colors = [RED, GREEN, BLUE]

        starting_points = VGroup(
            *[
                Dot(LEFT + pos, color=color)
                for pos, color in zip([UP, DOWN, LEFT], colors)
            ]
        )

        finish_points = VGroup(
            *[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip([ORIGIN, UP, DOWN], colors)
            ]
        )

        self.add(starting_points)
        self.add(finish_points)
        for dot in starting_points:
            self.add(TracedPath(dot.get_center, stroke_color=dot.get_color()))

        self.wait()
        self.play(
            Transform(
                starting_points,
                finish_points,
                path_func=utils.paths.clockwise_path(),
                run_time=2,
            )
        )
        self.wait()
```

返回类型

*Callable[[ndarray, ndarray, float], ndarray]*


`counterclockwise_path()`

该函数通过逆时针移动半圆来变换每个点。

例子

示例：逆时针路径示例

```py
from manim import *

class CounterclockwisePathExample(Scene):
    def construct(self):
        colors = [RED, GREEN, BLUE]

        starting_points = VGroup(
            *[
                Dot(LEFT + pos, color=color)
                for pos, color in zip([UP, DOWN, LEFT], colors)
            ]
        )

        finish_points = VGroup(
            *[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip([ORIGIN, UP, DOWN], colors)
            ]
        )

        self.add(starting_points)
        self.add(finish_points)
        for dot in starting_points:
            self.add(TracedPath(dot.get_center, stroke_color=dot.get_color()))

        self.wait()
        self.play(
            Transform(
                starting_points,
                finish_points,
                path_func=utils.paths.counterclockwise_path(),
                run_time=2,
            )
        )
        self.wait()
```

返回类型

*Callable[[ndarray, ndarray, float], ndarray]*


`path_along_arc(arc_angle, axis=array([0., 0., 1.]))`

该函数通过沿圆弧移动每个点来变换每个点。

参数

- **arc_angle** ( _float_ ) – 每个点绕圆弧移动的角度。
- **axis** ( _ndarray_ ) – 旋转轴。

返回类型

*Callable[[ndarray, ndarray, float], ndarray]*

例子

示例：PathAlongArcExample 

```py
from manim import *

class PathAlongArcExample(Scene):
    def construct(self):
        colors = [RED, GREEN, BLUE]

        starting_points = VGroup(
            *[
                Dot(LEFT + pos, color=color)
                for pos, color in zip([UP, DOWN, LEFT], colors)
            ]
        )

        finish_points = VGroup(
            *[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip([ORIGIN, UP, DOWN], colors)
            ]
        )

        self.add(starting_points)
        self.add(finish_points)
        for dot in starting_points:
            self.add(TracedPath(dot.get_center, stroke_color=dot.get_color()))

        self.wait()
        self.play(
            Transform(
                starting_points,
                finish_points,
                path_func=utils.paths.path_along_arc(TAU * 2 / 3),
                run_time=3,
            )
        )
        self.wait()
```


`path_along_circles(arc_angle, circles_centers, axis=array([0., 0., 1.]))`

该函数通过沿着圆大致移动每个点来变换每个点，每个点都有自己指定的中心。

该路径可以被视为每个点从起始位置到目的地平滑地改变其轨道。

参数

- **arc_angle** ( _float_ ) – 每个点围绕拟圆穿过的角度。
- **Circles_centers** ( _ndarray_ ) – 每个点旋转的拟圆的中心。
- **axis** ( _ndarray_ ) – 旋转轴。

返回类型

*Callable[[ndarray, ndarray, float], ndarray]*

例子

示例：PathAlongCircles 示例

```py
from manim import *

class PathAlongCirclesExample(Scene):
    def construct(self):
        colors = [RED, GREEN, BLUE]

        starting_points = VGroup(
            *[
                Dot(LEFT + pos, color=color)
                for pos, color in zip([UP, DOWN, LEFT], colors)
            ]
        )

        finish_points = VGroup(
            *[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip([ORIGIN, UP, DOWN], colors)
            ]
        )

        self.add(starting_points)
        self.add(finish_points)
        for dot in starting_points:
            self.add(TracedPath(dot.get_center, stroke_color=dot.get_color()))

        circle_center = Dot(3 * LEFT)
        self.add(circle_center)

        self.wait()
        self.play(
            Transform(
                starting_points,
                finish_points,
                path_func=utils.paths.path_along_circles(
                    2 * PI, circle_center.get_center()
                ),
                run_time=3,
            )
        )
        self.wait()
```


`spiral_path(angle, axis=array([0., 0., 1.]))`

该函数通过沿着螺旋线移动到目的地来变换每个点。

参数

- **angle** ( _float_ ) – 每个点绕螺旋线移动的角度。
- **axis** ( _ndarray_ ) – 旋转轴。

返回类型

*Callable[[ndarray, ndarray, float], ndarray]*

例子

示例：SpiralPathExample 

```py
from manim import *

class SpiralPathExample(Scene):
    def construct(self):
        colors = [RED, GREEN, BLUE]

        starting_points = VGroup(
            *[
                Dot(LEFT + pos, color=color)
                for pos, color in zip([UP, DOWN, LEFT], colors)
            ]
        )

        finish_points = VGroup(
            *[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip([ORIGIN, UP, DOWN], colors)
            ]
        )

        self.add(starting_points)
        self.add(finish_points)
        for dot in starting_points:
            self.add(TracedPath(dot.get_center, stroke_color=dot.get_color()))

        self.wait()
        self.play(
            Transform(
                starting_points,
                finish_points,
                path_func=utils.paths.spiral_path(2 * TAU),
                run_time=5,
            )
        )
        self.wait()
```


`straight_path(*args)`

最简单的路径函数。集合中的每个点都沿着一条直线路径到达目的地。

例子

示例：StraightPath 示例

```py
from manim import *

class StraightPathExample(Scene):
    def construct(self):
        colors = [RED, GREEN, BLUE]

        starting_points = VGroup(
            *[
                Dot(LEFT + pos, color=color)
                for pos, color in zip([UP, DOWN, LEFT], colors)
            ]
        )

        finish_points = VGroup(
            *[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip([ORIGIN, UP, DOWN], colors)
            ]
        )

        self.add(starting_points)
        self.add(finish_points)
        for dot in starting_points:
            self.add(TracedPath(dot.get_center, stroke_color=dot.get_color()))

        self.wait()
        self.play(
            Transform(
                starting_points,
                finish_points,
                path_func=utils.paths.straight_path(),
                run_time=2,
            )
        )
        self.wait()
```

返回类型

*Callable[[ndarray, ndarray, float], ndarray]*
