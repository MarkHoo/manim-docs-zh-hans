# 渐显渐隐

淡入淡出视野。

示例：渐显渐隐

[![视频缩略图]()](https://docs.manim.community/en/stable/reference/Fading-1.mp4)

```py
from manim import *

class Fading(Scene):
    def construct(self):
        tex_in = Tex("Fade", "In").scale(3)
        tex_out = Tex("Fade", "Out").scale(3)
        self.play(FadeIn(tex_in, shift=DOWN, scale=0.66))
        self.play(ReplacementTransform(tex_in, tex_out))
        self.play(FadeOut(tex_out, shift=DOWN * 2, scale=1.5))
```

Classes

|||
|-|-|
[`FadeIn`]()|淡入[`Mobject`]()s。
[`FadeOut`]()|淡出[`Mobject`]()s.
