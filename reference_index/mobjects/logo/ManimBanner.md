# 马尼姆横幅[#](#manimbanner "此标题的固定链接")

合格名称：`manim.mobject.logo.ManimBanner`

_类_ ManimBanner ( _dark_theme = True_ )[\[来源\]](../_modules/manim/mobject/logo.html#ManimBanner)[#](#manim.mobject.logo.ManimBanner "此定义的固定链接")

基地：[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

代表 Manim 旗帜的便利类。

可以使用自定义方法进行动画处理。

参数

**dark_theme** ( _bool_ ) – 如果`True`（默认），将呈现徽标的深色主题版本（带有浅色文本字体）。否则，如果`False`，则使用浅色主题版本（带有深色文本字体）。

例子

示例：DarkThemeBanner [¶](#darkthemebanner)

from manim import \*

class DarkThemeBanner(Scene):
def construct(self):
banner = ManimBanner()
self.play(banner.create())
self.play(banner.expand())
self.wait()
self.play(Unwrite(banner))

Copy to clipboard

示例：LightThemeBanner [¶](#lightthemebanner)

from manim import \*

class LightThemeBanner(Scene):
def construct(self):
self.camera.background_color = "#ece6e2"
banner = ManimBanner(dark_theme=False)
self.play(banner.create())
self.play(banner.expand())
self.wait()
self.play(Unwrite(banner))

Copy to clipboard

方法

[`create`](#manim.mobject.logo.ManimBanner.create "manim.mobject.logo.ManimBanner.create")

Manim 标志的创作动画。

[`expand`](#manim.mobject.logo.ManimBanner.expand "manim.mobject.logo.ManimBanner.expand")

将 Manim 的徽标扩展到其横幅中的动画。

[`scale`](#manim.mobject.logo.ManimBanner.scale "manim.mobject.logo.ManimBanner.scale")

按指定的比例因子缩放横幅。

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。

创建（_运行时间= 2_）[\[来源\]](../_modules/manim/mobject/logo.html#ManimBanner.create)[#](#manim.mobject.logo.ManimBanner.create "此定义的固定链接")

Manim 标志的创作动画。

参数

**run_time** ( _float_ ) – 动画的运行时间。

退货

通话中使用的动画[`Scene.play()`](manim.scene.scene.Scene.html#manim.scene.scene.Scene.play "manim.场景.场景.场景.play")。

返回类型

[`AnimationGroup`](manim.animation.composition.AnimationGroup.html#manim.animation.composition.AnimationGroup "manim.animation.composition.AnimationGroup")

展开（_运行时间= 1.5_，_方向= '中心'_）[\[来源\]](../_modules/manim/mobject/logo.html#ManimBanner.expand)[#](#manim.mobject.logo.ManimBanner.expand "此定义的固定链接")

将 Manim 的徽标扩展到其横幅中的动画。

返回的动画将横幅从其初始状态（仅代表 Manim 的徽标和图标）转换为展开状态（显示全名和图标）。

有关如何使用它的信息，请参阅类文档。

笔记

在调用此方法之前，文本“anim”不是横幅对象的子对象。扩展后，它被添加为子对象，因此横幅对象的后续动画也适用于文本“anim”。

参数

- **run_time** ( _float_ ) – 动画的运行时间。
- **方向**– 徽标展开的方向。

退货

通话中使用的动画[`Scene.play()`](manim.scene.scene.Scene.html#manim.scene.scene.Scene.play "manim.场景.场景.场景.play")。

返回类型

[`Succession`](manim.animation.composition.Succession.html#manim.animation.composition.Succession "manim.animation.composition.Succession")

例子

示例：展开方向[¶](#expanddirections)

from manim import \*

class ExpandDirections(Scene):
def construct(self):
banners = \[ManimBanner().scale(0.5).shift(UP\*x) for x in \[-2, 0, 2\]\]
self.play(
banners\[0\].expand(direction="right"),
banners\[1\].expand(direction="center"),
banners\[2\].expand(direction="left"),
)

Copy to clipboard

比例（_比例因子_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/logo.html#ManimBanner.scale)[#](#manim.mobject.logo.ManimBanner.scale "此定义的固定链接")

按指定的比例因子缩放横幅。

参数

**scale_factor** ( _float_ ) – 用于缩放横幅的因子。

退货

缩放横幅。

返回类型

[`ManimBanner`](#manim.mobject.logo.ManimBanner "manim.mobject.logo.ManimBanner")
