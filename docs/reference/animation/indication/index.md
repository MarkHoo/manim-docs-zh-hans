# 指示

动画吸引人们对特定对象的注意。

Classes

示例：适应症

[![视频缩略图]()](https://docs.manim.community/en/stable/reference/Indications-1.mp4)

```py
from manim import *

class Indications(Scene):
    def construct(self):
        indications = [ApplyWave,Circumscribe,Flash,FocusOn,Indicate,ShowPassingFlash,Wiggle]
        names = [Tex(i.__name__).scale(3) for i in indications]

        self.add(names[0])
        for i in range(len(names)):
            if indications[i] is Flash:
                self.play(Flash(UP))
            elif indications[i] is ShowPassingFlash:
                self.play(ShowPassingFlash(Underline(names[i])))
            else:
                self.play(indications[i](names[i]))
            self.play(AnimationGroup(
                FadeOut(names[i], shift=UP*1.5),
                FadeIn(names[(i+1)%len(names)], shift=UP*1.5),
            ))
```

课程

|||
|-|-|
[`ApplyWave`]()|发送一个波穿过 Mobject，使其暂时扭曲。
[`Circumscribe`]()|在对象周围画一条临时线。
[`Flash`]()|向各个方向发出线路。
[`FocusOn`]()|将聚光灯缩小到某个位置。
[`Indicate`]()|通过暂时调整 Mobject 的大小和重新着色来指示它。
[`ShowCreationThenFadeOut`]()|注意 已弃用
[`ShowPassingFlash`]()|每帧仅显示 VMobject 的一小部分。
[`ShowPassingFlashWithThinningStrokeWidth`]()|
[`Wiggle`]()|摆动一个 Mobject。
