# 抽象图像对象

合格名称：`manim.mobject.types.image\_mobject.AbstractImageMobject`

_类_ AbstractImageMobject（_scale_to_resolution_， _pixel_array_dtype = 'uint8'_， _resampling_algorithm = Resampling.BICUBIC_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/types/image_mobject.html#AbstractImageMobject)[#](#manim.mobject.types.image_mobject.AbstractImageMobject "此定义的固定链接")

基地：[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

自动过滤掉黑色像素

参数

**scale_to_resolution** ( _int_ ) – 在此分辨率下，图像将逐像素放置在屏幕上，因此它看起来最清晰、最好。这是 ImageMobject 的自定义参数，因此使用例如或标志来渲染场景以加快渲染速度不会影响图像在屏幕上的位置。` --quality low``--quality medium `

方法

`get_pixel_array`

[`reset_points`](#manim.mobject.types.image_mobject.AbstractImageMobject.reset_points "manim.mobject.types.image_mobject.AbstractImageMobject.reset_points")

设置`points`为空数组。

[`set_color`](#manim.mobject.types.image_mobject.AbstractImageMobject.set_color "manim.mobject.types.image_mobject.AbstractImageMobject.set_color")

条件是接受一个参数 (x, y, z) 的函数。

[`set_resampling_algorithm`](#manim.mobject.types.image_mobject.AbstractImageMobject.set_resampling_algorithm "manim.mobject.types.image_mobject.AbstractImageMobject.set_resampling_algorithm")

设置放大图像的插值方法。

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

重置点( )[\[来源\]](../_modules/manim/mobject/types/image_mobject.html#AbstractImageMobject.reset_points)[#](#manim.mobject.types.image_mobject.AbstractImageMobject.reset_points "此定义的固定链接")

设置`points`为空数组。

set*color (*颜色*, \_alpha = None* , _family = True_ )[\[来源\]](../_modules/manim/mobject/types/image_mobject.html#AbstractImageMobject.set_color)[#](#manim.mobject.types.image_mobject.AbstractImageMobject.set_color "此定义的固定链接")

条件是接受一个参数 (x, y, z) 的函数。这里它只是递归到子对象，但是在子类中，这应该基于颜色的内部工作原理进一步实现

设置重采样算法（_重采样算法_）[\[来源\]](../_modules/manim/mobject/types/image_mobject.html#AbstractImageMobject.set_resampling_algorithm)[#](#manim.mobject.types.image_mobject.AbstractImageMobject.set_resampling_algorithm "此定义的固定链接")

设置放大图像的插值方法。默认情况下，图像使用双三次算法进行插值。这个方法可以让你改变它。插值是使用 Pillow 在内部完成的，除了描述算法的字符串常量之外，函数还接受 Pillow 整数常量。

参数

**重采样算法**( _int_ ) –

Pillow 库中描述的整数常量，或来自 RESAMPLING_ALGORITHMS 全局字典的整数常量，位于以下键下：

- “双三次”或“三次”
- “最近”或“没有”
- '盒子'
- “双线性”或“线性”
- “汉明”
- “lanczos”或“抗锯齿”
