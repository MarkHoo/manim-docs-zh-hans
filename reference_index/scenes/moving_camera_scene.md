# 移动相机场景[#](#module-manim.scene.moving_camera_scene "此标题的固定链接")

摄像机可以移动的场景。

也可以看看

[`moving_camera`](manim.camera.moving_camera.html#module-manim.camera.moving_camera "manim.camera.movi​​ng_camera")

例子

示例：更改相机宽度并恢复[¶](#changingcamerawidthandrestore)

from manim import \*

class ChangingCameraWidthAndRestore(MovingCameraScene):
def construct(self):
text = Text("Hello World").set_color(BLUE)
self.add(text)
self.camera.frame.save_state()
self.play(self.camera.frame.animate.set(width=text.width \* 1.2))
self.wait(0.3)
self.play(Restore(self.camera.frame))

Copy to clipboard

示例：移动相机中心[¶](#movingcameracenter)

from manim import \*

class MovingCameraCenter(MovingCameraScene):
def construct(self):
s = Square(color=RED, fill*opacity=0.5).move_to(2 * LEFT)
t = Triangle(color=GREEN, fill*opacity=0.5).move_to(2 * RIGHT)
self.wait(0.3)
self.add(s, t)
self.play(self.camera.frame.animate.move_to(s))
self.wait(0.3)
self.play(self.camera.frame.animate.move_to(t))

Copy to clipboard

示例：MovingAndZoomingCamera [¶](#movingandzoomingcamera)

from manim import \*

class MovingAndZoomingCamera(MovingCameraScene):
def construct(self):
s = Square(color=BLUE, fill*opacity=0.5).move_to(2 * LEFT)
t = Triangle(color=YELLOW, fill*opacity=0.5).move_to(2 * RIGHT)
self.add(s, t)
self.play(self.camera.frame.animate.move_to(s).set(width=s.width*2))
self.wait(0.3)
self.play(self.camera.frame.animate.move_to(t).set(width=t.width*2))

        self.play(self.camera.frame.animate.move_to(ORIGIN).set(width=14))

Copy to clipboard

示例：MovingCameraOnGraph [¶](#movingcameraongraph)

from manim import \*

class MovingCameraOnGraph(MovingCameraScene):
def construct(self):
self.camera.frame.save_state()

        ax = Axes(x_range=\[-1, 10\], y_range=\[-1, 10\])
        graph = ax.plot(lambda x: np.sin(x), color=WHITE, x_range=\[0, 3 * PI\])

        dot_1 = Dot(ax.i2gp(graph.t_min, graph))
        dot_2 = Dot(ax.i2gp(graph.t_max, graph))
        self.add(ax, graph, dot_1, dot_2)

        self.play(self.camera.frame.animate.scale(0.5).move_to(dot_1))
        self.play(self.camera.frame.animate.move_to(dot_2))
        self.play(Restore(self.camera.frame))
        self.wait()

Copy to clipboard

课程

[`MovingCameraScene`](manim.scene.moving_camera_scene.MovingCameraScene.html#manim.scene.moving_camera_scene.MovingCameraScene "manim.scene.movi​​ng_camera_scene.MovingCameraScene")

这是一个场景，具有特殊的配置和属性，使其适合相机必须四处移动的情况。
