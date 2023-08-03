# 抽象图像对象

合格名称：`manim.mobject.types.image\_mobject.AbstractImageMobject`


```py
class AbstractImageMobject(scale_to_resolution, pixel_array_dtype='uint8', resampling_algorithm=Resampling.BICUBIC, **kwargs)
```

Bases: `Mobject`

自动过滤掉黑色像素

参数

**scale_to_resolution** ( _int_ ) – 在此分辨率下，图像将逐像素放置在屏幕上，因此它看起来最清晰、最好。这是 ImageMobject 的自定义参数，因此使用例如或标志来渲染场景以加快渲染速度不会影响图像在屏幕上的位置。` --quality low``--quality medium `


方法

|||
|-|-|
`get_pixel_array`|
[`reset_points`]()|设置`points`为空数组。
[`set_color`]()|条件是接受一个参数 (x, y, z) 的函数。
[`set_resampling_algorithm`]()|设置放大图像的插值方法。


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`depth`|对象的深度。
`height`|mobject 的高度。
`width`|mobject 的宽度。



`reset_points()`

设置`points`为空数组。



`set_color(color, alpha=None, family=True)`

条件是接受一个参数 (x, y, z) 的函数。这里它只是递归到子对象，但是在子类中，这应该基于颜色的内部工作原理进一步实现



`set_resampling_algorithm(resampling_algorithm)`

设置放大图像的插值方法。默认情况下，图像使用双三次算法进行插值。这个方法可以让你改变它。插值是使用 Pillow 在内部完成的，除了描述算法的字符串常量之外，函数还接受 Pillow 整数常量。

参数

**resampling_algorithm**( _int_ ) –

Pillow 库中描述的整数常量，或来自 RESAMPLING_ALGORITHMS 全局字典的整数常量，位于以下键下：

- “bicubic”或“cubic”
- “nearest”或“none”
- 'box'
- “bilinear”或“linear”
- “hamming”
- “lanczos”或“antialias”
