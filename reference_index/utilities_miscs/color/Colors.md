# 颜色[#](#colors "此标题的固定链接")

合格名称：`manim.utils.color.Colors`

颜色*类别*（_值_）[\[来源\]](../_modules/manim/utils/color.html#Colors)[#](#manim.utils.color.Colors "此定义的固定链接")

基地：`Enum`

预定义颜色的列表。

例子

![../_images/ColorsOverview-1.png](../_images/ColorsOverview-1.png)

使用这些颜色的首选方法是从 manim 导入它们的常量：

> > \> from manim import RED, GREEN, BLUE
> > \> RED
> > '#FC6255'

Copy to clipboard

请注意，这种方式使用大写的颜色名称。

或者，您也可以通过使用 . 直接导入此 Enum 并直接使用其成员`color.value`。请注意，这种方式使用小写的颜色名称。

> > \> from manim.utils.color import Colors
> > \> Colors.red.value
> > '#FC6255'

Copy to clipboard

笔记

“C”类型的颜色有一个别名，等于不带字母的颜色名称，例如 GREEN = GREEN_C

属性

`white`

`gray_a`

`gray_b`

`gray_c`

`gray_d`

`gray_e`

`black`

`lighter_gray`

`light_gray`

`gray`

`dark_gray`

`darker_gray`

`blue_a`

`blue_b`

`blue_c`

`blue_d`

`blue_e`

`pure_blue`

`blue`

`dark_blue`

`teal_a`

`teal_b`

`teal_c`

`teal_d`

`teal_e`

`teal`

`green_a`

`green_b`

`green_c`

`green_d`

`green_e`

`pure_green`

`green`

`yellow_a`

`yellow_b`

`yellow_c`

`yellow_d`

`yellow_e`

`yellow`

`gold_a`

`gold_b`

`gold_c`

`gold_d`

`gold_e`

`gold`

`red_a`

`red_b`

`red_c`

`red_d`

`red_e`

`pure_red`

`red`

`maroon_a`

`maroon_b`

`maroon_c`

`maroon_d`

`maroon_e`

`maroon`

`purple_a`

`purple_b`

`purple_c`

`purple_d`

`purple_e`

`purple`

`pink`

`light_pink`

`orange`

`light_brown`

`dark_brown`

`gray_brown`
