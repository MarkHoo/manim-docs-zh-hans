# 应用波

合格名称：`manim.animation.indication.ApplyWave`

```py
class ApplyWave(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Homotopy

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

示例：应用 Waves 

```py
from manim import *

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
```

方法
