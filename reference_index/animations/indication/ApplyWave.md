# 应用波[#](#applywave "此标题的固定链接")

合格名称：`manim.animation.indication.ApplyWave`

_类_ ApplyWave ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/indication.html#ApplyWave)[#](#manim.animation.indication.ApplyWave "此定义的固定链接")

基地：[`Homotopy`](manim.animation.movement.Homotopy.html#manim.animation.movement.Homotopy "动画.运动.同伦")

发送一个波穿过 Mobject，使其暂时扭曲。

参数

- **mobject** – 要扭曲的 mobject。
- **方向**– 波浪推动形状点的方向
- **振幅**– 形状的距离点发生移动
- **wave_func** – 定义一个波侧面形状的函数。
- **time_width** – 波的长度相对于对象的宽度。
- **波纹**\- 波的波纹数
- **run_time** – 动画的持续时间。

例子

示例：应用 Waves [¶](#applyingwaves)

from manim import \*

class ApplyingWaves(Scene):
def construct(self):
tex = Tex("WaveWaveWaveWaveWave").scale(2)
self.play(ApplyWave(tex))
self.play(ApplyWave(
tex,
direction=RIGHT,
time_width=0.5,
amplitude=0.3
))
self.play(ApplyWave(
tex,
rate_func=linear,
ripples=4
))

Copy to clipboard

方法
