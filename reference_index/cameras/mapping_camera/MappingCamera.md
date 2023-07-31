# 测绘相机[#](#mappingcamera "此标题的固定链接")

合格名称：`manim.camera.mapping\_camera.MappingCamera`

_类_ MappingCamera（_mapping_func=<function MappingCamera.<lambda>>_， _min_num_curves=50_， _allow_object_intrusion=False_， _\*\*kwargs_）[\[来源\]](../_modules/manim/camera/mapping_camera.html#MappingCamera)[#](#manim.camera.mapping_camera.MappingCamera "此定义的固定链接")

基地：[`Camera`](manim.camera.camera.Camera.html#manim.camera.camera.Camera "manim.camera.camera.Camera")

允许对象之间映射的相机对象。

方法

[`capture_mobjects`](#manim.camera.mapping_camera.MappingCamera.capture_mobjects "manim.camera.mapping_camera.MappingCamera.capture_mobjects")

通过将 mobject 打印在 上来捕获它们`pixel_array`。

`points_to_pixel_coords`

属性

`background_color`

`background_opacity`

capture*mobjects ( \_mobjects* , _\*\* kwargs_ )[\[来源\]](../_modules/manim/camera/mapping_camera.html#MappingCamera.capture_mobjects)[#](#manim.camera.mapping_camera.MappingCamera.capture_mobjects "此定义的固定链接")

通过将 mobject 打印在 上来捕获它们`pixel_array`。

这是将场景的内容转换为数组的基本函数，然后将其转换为图像或视频。

参数

- **mobjects** – 要捕获的 Mobjects。
- **kwargs** – 要传递给 的关键字参数`get_mobjects_to_display()`。

笔记

有关当前可以呈现的类的列表，请参阅`display_funcs()`。
