# 多机位

合格名称：`manim.camera.multi\_camera.MultiCamera`

```py
class MultiCamera(image_mobjects_from_cameras=None, allow_cameras_to_capture_their_own_display=False, **kwargs)
```

Bases: `MovingCamera`

允许多个视角的相机对象。

初始化多相机

参数

- **image_mobjects_from_cameras** ( [_ImageMobject_]() _|\_\_None_) –
- **kwargs** – MovingCamera 的任何有效关键字参数。


方法

|||
|-|-|
[`add_image_mobject_from_camera`]()|将从相机获取的 ImageMobject 添加到列表中`self.image_mobject_from_cameras`
[`capture_mobjects`]()|通过将 mobject 打印在 上来捕获它们`pixel_array`。
[`get_mobjects_indicating_movement`]()|返回所有其移动意味着相机应将屏幕上的所有其他 mobject 视为移动的 mobject
[`reset`]()|重置多摄像机。
[`update_sub_cameras`]()|重塑子相机像素数组


属性

|||
|-|-|
`background_color`|
`background_opacity`|
`frame_center`|返回笛卡尔坐标系中框架的中心点。
`frame_height`|返回框架的高度。
`frame_width`|返回框架的宽度


```py
add_image_mobject_from_camera(image_mobject_from_camera)
```

将从相机获取的 ImageMobject 添加到列表中`self.image_mobject_from_cameras`

参数

**image_mobject_from_camera** ( [_ImageMobject_]() ) – 要添加到 self.image_mobject_from_cameras 的 ImageMobject



`capture_mobjects(mobjects, **kwargs)`

通过将 mobject 打印在 上来捕获它们`pixel_array`。

这是将场景的内容转换为数组的基本函数，然后将其转换为图像或视频。

参数

- **mobjects** – 要捕获的 Mobjects。
- **kwargs** – 要传递给 的关键字参数`get_mobjects_to_display()`。

笔记

有关当前可以呈现的类的列表，请参阅`display_funcs()`。


`get_mobjects_indicating_movement()`

返回所有其移动意味着相机应将屏幕上的所有其他 mobject 视为移动的 mobject

返回类型

list



`reset()`

重置多摄像机。

返回

重置多摄像头

返回类型

[MultiCamera]()



`update_sub_cameras()`

重塑子相机像素数组
