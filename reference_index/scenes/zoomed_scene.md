# 缩放场景[#](#module-manim.scene.zoomed_scene "此标题的固定链接")

支持放大指定区域的场景。

例子

示例：UseZoomedScene [¶](#usezoomedscene)

from manim import \*

class UseZoomedScene(ZoomedScene):
def construct(self):
dot = Dot().set_color(GREEN)
self.add(dot)
self.wait(1)
self.activate_zooming(animate=False)
self.wait(1)
self.play(dot.animate.shift(LEFT))

Copy to clipboard

示例：更改缩放比例[¶](#changingzoomscale)

from manim import \*

class ChangingZoomScale(ZoomedScene):
def \_\_init\_\_(self, **kwargs):
ZoomedScene.\_\_init\_\_(
self,
zoom_factor=0.3,
zoomed_display_height=1,
zoomed_display_width=3,
image_frame_stroke_width=20,
zoomed_camera_config={
"default_frame_stroke_width": 3,
},
**kwargs
)

    def construct(self):
        dot = Dot().set_color(GREEN)
        sq = Circle(fill_opacity=1, radius=0.2).next_to(dot, RIGHT)
        self.add(dot, sq)
        self.wait(1)
        self.activate_zooming(animate=False)
        self.wait(1)
        self.play(dot.animate.shift(LEFT * 0.3))

        self.play(self.zoomed_camera.frame.animate.scale(4))
        self.play(self.zoomed_camera.frame.animate.shift(0.5 * DOWN))

Copy to clipboard

课程

[`ZoomedScene`](manim.scene.zoomed_scene.ZoomedScene.html#manim.scene.zoomed_scene.ZoomedScene "manim.scene.zoomed_scene.ZoomedScene")

这是一个具有特殊配置的场景，适用于必须放大并单独显示场景的特定部分的情况。
