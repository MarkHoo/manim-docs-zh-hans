# 点云点[#](#pointclouddot "此标题的固定链接")

合格名称：`manim.mobject.types.point\_cloud\_mobject.PointCloudDot`

_类_ PointCloudDot (_中心= array(\[0., 0., 0.\])_ ,_半径= 2.0_ ,_描边宽度= 2_ ,_密度= 10_ ,_颜色= '#FFFF00'_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PointCloudDot)[#](#manim.mobject.types.point_cloud_mobject.PointCloudDot "此定义的固定链接")

基地：[`Mobject1D`](manim.mobject.types.point_cloud_mobject.Mobject1D.html#manim.mobject.types.point_cloud_mobject.Mobject1D "manim.mobject.types.point_cloud_mobject.Mobject1D")

由点云组成的圆盘 .. 标题:: 示例

示例：PointCloudDotExample [¶](#pointclouddotexample)

![../_images/PointCloudDotExample-1.png](../_images/PointCloudDotExample-1.png)

from manim import \*

class PointCloudDotExample(Scene):
def construct(self):
cloud_1 = PointCloudDot(color=RED)
cloud_2 = PointCloudDot(stroke_width=4, radius=1)
cloud_3 = PointCloudDot(density=15)

        group = Group(cloud_1, cloud_2, cloud_3).arrange()
        self.add(group)

Copy to clipboard

示例：PointCloudDotExample2 [¶](#pointclouddotexample2)

from manim import \*

class PointCloudDotExample2(Scene):
def construct(self):
plane = ComplexPlane()
cloud = PointCloudDot(color=RED)
self.add(
plane, cloud
)
self.wait()
self.play(
cloud.animate.apply_complex_function(lambda z: np.exp(z))
)

Copy to clipboard

方法

[`generate_points`](#manim.mobject.types.point_cloud_mobject.PointCloudDot.generate_points "manim.mobject.types.point_cloud_mobject.PointCloudDot.generate_points")

初始化`points`并因此初始化形状。

`init_points`

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`depth`

对象的深度。

`height`

mobject 的高度。

`width`

mobject 的宽度。

生成点( )[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PointCloudDot.generate_points)[#](#manim.mobject.types.point_cloud_mobject.PointCloudDot.generate_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。
