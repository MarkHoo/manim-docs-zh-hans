# 旧多相机

合格名称：`manim.camera.mapping\_camera.OldMultiCamera`

```py
class OldMultiCamera(*cameras_with_start_positions, **kwargs)
```

Bases: Camera

方法

[`capture_mobjects`]()|通过将 mobject 打印在 上来捕获它们`pixel_array`。
[`init_background`]()|初始化背景。
[`set_background`]()|转换为有效的 RGB 值后，将背景设置为传递的 Pixel_array。
[`set_pixel_array`]()|将相机的像素数组设置为传递的像素数组。

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

初始化背景（）

初始化背景。如果 self.background_image 是图像的路径，则图像被设置为背景；否则，默认背景颜色填充背景。

设置背景（_像素数组_， _\*\* kwargs_）

转换为有效的 RGB 值后，将背景设置为传递的 Pixel_array。

参数

- **Pixel_array** – 要设置背景的像素数组。
- **Convert_from_floats** – 是否将浮点值转换为正确的 RGB 有效值，默认为 False

set*pixel_array ( \_Pixel_array* , _\*\* kwargs_ )

将相机的像素数组设置为传递的像素数组。

参数

- **Pixel_array** – 要转换的像素数组，然后设置为相机的像素数组。
- **Convert_from_floats** – 是否将浮点值转换为正确的 RGB 值，默认为 False
