# 测绘相机

合格名称：`manim.camera.mapping\_camera.MappingCamera`

```py
class MappingCamera(mapping_func=<function MappingCamera.<lambda>>, min_num_curves=50, allow_object_intrusion=False, **kwargs)
```

Bases: Camera

允许对象之间映射的相机对象。

方法

|||
|-|-|
[`capture_mobjects`]()|通过将 mobject 打印在 上来捕获它们`pixel_array`。
`points_to_pixel_coords`|


属性

`background_color`

`background_opacity`

capture*mobjects ( \_mobjects* , _\*\* kwargs_ )

通过将 mobject 打印在 上来捕获它们`pixel_array`。

这是将场景的内容转换为数组的基本函数，然后将其转换为图像或视频。

参数

- **mobjects** – 要捕获的 Mobjects。
- **kwargs** – 要传递给 的关键字参数`get_mobjects_to_display()`。

笔记

有关当前可以呈现的类的列表，请参阅`display_funcs()`。
