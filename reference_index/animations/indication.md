# 指示

动画吸引人们对特定对象的注意。

例子

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
[`ApplyWave`](manim.animation.indication.ApplyWave.html#manim.animation.indication.ApplyWave "manim.animation.indication.ApplyWave")|发送一个波穿过 Mobject，使其暂时扭曲。
[`Circumscribe`](manim.animation.indication.Circumscribe.html#manim.animation.indication.Circumscribe "manim.animation.indication.Circumscribe")|在对象周围画一条临时线。
[`Flash`](manim.animation.indication.Flash.html#manim.animation.indication.Flash "动画.指示.Flash")|向各个方向发出线路。
[`FocusOn`](manim.animation.indication.FocusOn.html#manim.animation.indication.FocusOn "manim.animation.indication.FocusOn")|将聚光灯缩小到某个位置。
[`Indicate`](manim.animation.indication.Indicate.html#manim.animation.indication.Indicate "manim.animation.indication.Indicate")|通过暂时调整 Mobject 的大小和重新着色来指示它。
[`ShowCreationThenFadeOut`](manim.animation.indication.ShowCreationThenFadeOut.html#manim.animation.indication.ShowCreationThenFadeOut "manim.animation.inspiration.ShowCreationThenFadeOut")|注意 已弃用
[`ShowPassingFlash`](manim.animation.indication.ShowPassingFlash.html#manim.animation.indication.ShowPassingFlash "manim.animation.inspiration.ShowPassingFlash")|每帧仅显示 VMobject 的一小部分。
[`ShowPassingFlashWithThinningStrokeWidth`](manim.animation.indication.ShowPassingFlashWithThinningStrokeWidth.html#manim.animation.indication.ShowPassingFlashWithThinningStrokeWidth "manim.animation.inspiration.ShowPassingFlashWithThinningStrokeWidth")|
[`Wiggle`](manim.animation.indication.Wiggle.html#manim.animation.indication.Wiggle "manim.animation.indication.Wiggle")|摆动一个 Mobject。
