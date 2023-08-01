# 外接


合格名称：`manim.animation.indication.Circumscribe`


```py
class Circumscribe(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Succession

在对象周围画一条临时线。

参数

*   **mobject** – 要限制的 mobject。
    
*   **shape** – 包围给定对象的形状。应该是 [`Rectangle`]()或者[`Circle`]()
    
*   **fade_in** – 是否使周围的形状淡入。否则将绘制它。
    
*   **fade_out** – 是否使周围的形状淡出。否则它将被取消绘制。
    
*   **time_width** – 绘制和取消绘制的时间宽度。如果fade_in或fade_out为True ，则被忽略。
    
*   **buff** – 周围形状与给定对象之间的距离。
    
*   **color**– 周围形状的颜色。
    
*   **run_time** – 整个动画的持续时间。
    
*   **kwargs** – 要传递给[`Succession`]()构造函数的附加参数
    

例子

示例：使用Circumscribe 

```py
from manim import *

class UsingCircumscribe(Scene):
    def construct(self):
        lbl = Tex(r"Circum-\\scribe").scale(2)
        self.add(lbl)
        self.play(Circumscribe(lbl))
        self.play(Circumscribe(lbl, Circle))
        self.play(Circumscribe(lbl, fade_out=True))
        self.play(Circumscribe(lbl, time_width=2))
        self.play(Circumscribe(lbl, Circle, True))
```

方法