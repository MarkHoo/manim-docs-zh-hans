# ManimBanner

合格名称：`manim.mobject.logo.ManimBanner`


```py
class ManimBanner(dark_theme=True)
```

Bases: `VGroup`

代表 Manim 旗帜的便利类。

可以使用自定义方法进行动画处理。

参数

**dark_theme** ( _bool_ ) – 如果`True`（默认），将呈现徽标的深色主题版本（带有浅色文本字体）。否则，如果`False`，则使用浅色主题版本（带有深色文本字体）。

例子

示例：DarkThemeBanner

```py
from manim import *

class DarkThemeBanner(Scene):
    def construct(self):
        banner = ManimBanner()
        self.play(banner.create())
        self.play(banner.expand())
        self.wait()
        self.play(Unwrite(banner))
```


示例：LightThemeBanner 

```py
from manim import *

class LightThemeBanner(Scene):
    def construct(self):
        self.camera.background_color = "#ece6e2"
        banner = ManimBanner(dark_theme=False)
        self.play(banner.create())
        self.play(banner.expand())
        self.wait()
        self.play(Unwrite(banner))
```


方法

|||
|-|-|
[`create`]()|Manim 标志的创作动画。
[`expand`]()|将 Manim 的徽标扩展到其banner中的动画。
[`scale`]()|按指定的比例因子缩放banner。


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


`_original__init__(dark_theme=True)`

初始化自身。请参阅 help(type(self)) 以获取准确的签名。

参数
**dark_theme** (bool) –


`create(run_time=2)`

Manim 标志的创作动画。

参数

**run_time** ( _float_ ) – 动画的运行时间。

返回

通话中使用的动画[`Scene.play()`]()。

返回类型

[`AnimationGroup`]()



`expand(run_time=1.5, direction='center')`

将 Manim 的徽标扩展到其banner中的动画。

返回的动画将banner从其初始状态（仅代表 Manim 的徽标和图标）转换为展开状态（显示全名和图标）。

有关如何使用它的信息，请参阅类文档。

> 提示：
> 在调用此方法之前，文本“anim”不是banner对象的子对象。扩展后，它被添加为子对象，因此banner对象的后续动画也适用于文本“anim”。

参数

- **run_time** ( _float_ ) – 动画的运行时间。
- **direction**– 徽标展开的方向。

返回

通话中使用的动画[`Scene.play()`]()。

返回类型

[`Succession`]()


例子

示例：展开方向

```py
from manim import *

class ExpandDirections(Scene):
    def construct(self):
        banners = [ManimBanner().scale(0.5).shift(UP*x) for x in [-2, 0, 2]]
        self.play(
            banners[0].expand(direction="right"),
            banners[1].expand(direction="center"),
            banners[2].expand(direction="left"),
        )
```


`scale(scale_factor, **kwargs)`

按指定的比例因子缩放banner。

参数

**scale_factor** ( _float_ ) – 用于缩放banner的因子。

返回

缩放banner。

返回类型

[`ManimBanner`]()
