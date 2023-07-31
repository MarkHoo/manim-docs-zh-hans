# 路径[#](#module-manim.utils.paths "此标题的固定链接")

确定点集之间的变换路径的函数。

功能

顺时针路径( )[\[来源\]](../_modules/manim/utils/paths.html#clockwise_path)[#](#manim.utils.paths.clockwise_path "此定义的固定链接")

该函数通过顺时针移动半圆来变换每个点。

例子

示例：ClockwisePath 示例[¶](#clockwisepathexample)

from manim import \*

class ClockwisePathExample(Scene):
def construct(self):
colors = \[RED, GREEN, BLUE\]

        starting_points = VGroup(
            *\[
                Dot(LEFT + pos, color=color)
                for pos, color in zip(\[UP, DOWN, LEFT\], colors)
            \]
        )

        finish_points = VGroup(
            *\[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip(\[ORIGIN, UP, DOWN\], colors)
            \]
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

Copy to clipboard

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

逆时针路径( )[\[来源\]](../_modules/manim/utils/paths.html#counterclockwise_path)[#](#manim.utils.paths.counterclockwise_path "此定义的固定链接")

该函数通过逆时针移动半圆来变换每个点。

例子

示例：逆时针路径示例[¶](#counterclockwisepathexample)

from manim import \*

class CounterclockwisePathExample(Scene):
def construct(self):
colors = \[RED, GREEN, BLUE\]

        starting_points = VGroup(
            *\[
                Dot(LEFT + pos, color=color)
                for pos, color in zip(\[UP, DOWN, LEFT\], colors)
            \]
        )

        finish_points = VGroup(
            *\[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip(\[ORIGIN, UP, DOWN\], colors)
            \]
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

Copy to clipboard

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

path*along_arc ( \_arc_angle* , _axis = array(\[0., 0., 1.\])_ )[\[来源\]](../_modules/manim/utils/paths.html#path_along_arc)[#](#manim.utils.paths.path_along_arc "此定义的固定链接")

该函数通过沿圆弧移动每个点来变换每个点。

参数

- **arc_angle** ( _float_ ) – 每个点绕圆弧移动的角度。
- **axis** ( _ndarray_ ) – 旋转轴。

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

例子

示例：PathAlongArcExample [¶](#pathalongarcexample)

from manim import \*

class PathAlongArcExample(Scene):
def construct(self):
colors = \[RED, GREEN, BLUE\]

        starting_points = VGroup(
            *\[
                Dot(LEFT + pos, color=color)
                for pos, color in zip(\[UP, DOWN, LEFT\], colors)
            \]
        )

        finish_points = VGroup(
            *\[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip(\[ORIGIN, UP, DOWN\], colors)
            \]
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
                path_func=utils.paths.path\_along\_arc(TAU * 2 / 3),
                run_time=3,
            )
        )
        self.wait()

Copy to clipboard

path*along_circles ( \_arc_angle* , _Circles_centers_ , _axis = array(\[0., 0., 1.\])_ )[\[来源\]](../_modules/manim/utils/paths.html#path_along_circles)[#](#manim.utils.paths.path_along_circles "此定义的固定链接")

该函数通过沿着圆大致移动每个点来变换每个点，每个点都有自己指定的中心。

该路径可以被视为每个点从起始位置到目的地平滑地改变其轨道。

参数

- **arc_angle** ( _float_ ) – 每个点围绕拟圆穿过的角度。
- **Circles_centers** ( _ndarray_ ) – 每个点旋转的拟圆的中心。
- **axis** ( _ndarray_ ) – 旋转轴。

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

例子

示例：PathAlongCircles 示例[¶](#pathalongcirclesexample)

from manim import \*

class PathAlongCirclesExample(Scene):
def construct(self):
colors = \[RED, GREEN, BLUE\]

        starting_points = VGroup(
            *\[
                Dot(LEFT + pos, color=color)
                for pos, color in zip(\[UP, DOWN, LEFT\], colors)
            \]
        )

        finish_points = VGroup(
            *\[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip(\[ORIGIN, UP, DOWN\], colors)
            \]
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
                path_func=utils.paths.path\_along\_circles(
                    2 * PI, circle_center.get_center()
                ),
                run_time=3,
            )
        )
        self.wait()

Copy to clipboard

螺旋路径(_角度_,_轴= array(\[0., 0., 1.\])_ )[\[来源\]](../_modules/manim/utils/paths.html#spiral_path)[#](#manim.utils.paths.spiral_path "此定义的固定链接")

该函数通过沿着螺旋线移动到目的地来变换每个点。

参数

- **angle** ( _float_ ) – 每个点绕螺旋线移动的角度。
- **axis** ( _ndarray_ ) – 旋转轴。

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

例子

示例：SpiralPathExample [¶](#spiralpathexample)

from manim import \*

class SpiralPathExample(Scene):
def construct(self):
colors = \[RED, GREEN, BLUE\]

        starting_points = VGroup(
            *\[
                Dot(LEFT + pos, color=color)
                for pos, color in zip(\[UP, DOWN, LEFT\], colors)
            \]
        )

        finish_points = VGroup(
            *\[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip(\[ORIGIN, UP, DOWN\], colors)
            \]
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

Copy to clipboard

直路径( _\* args_ )[\[来源\]](../_modules/manim/utils/paths.html#straight_path)[#](#manim.utils.paths.straight_path "此定义的固定链接")

最简单的路径函数。集合中的每个点都沿着一条直线路径到达目的地。

例子

示例：StraightPath 示例[¶](#straightpathexample)

from manim import \*

class StraightPathExample(Scene):
def construct(self):
colors = \[RED, GREEN, BLUE\]

        starting_points = VGroup(
            *\[
                Dot(LEFT + pos, color=color)
                for pos, color in zip(\[UP, DOWN, LEFT\], colors)
            \]
        )

        finish_points = VGroup(
            *\[
                Dot(RIGHT + pos, color=color)
                for pos, color in zip(\[ORIGIN, UP, DOWN\], colors)
            \]
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

Copy to clipboard

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]
