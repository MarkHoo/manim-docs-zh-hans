# 移动相机

合格名称：`manim.camera.moving\_camera.MovingCamera`

```py
class MovingCamera(frame=None, fixed_dimension=0, default_frame_stroke_color='#FFFFFF', default_frame_stroke_width=0, **kwargs)
```

Bases: Camera

与其“框架”（矩形）的高度、宽度和位置保持一致

> 也可以看看

> [`MovingCameraScene`]()

Frame 是一个 Mobject，（几乎肯定是一个矩形）确定相机显示的空间区域

方法

|||
|-|-|
[`auto_zoom`]()|放大到给定的 mobject 数组（或单个 mobject）并自动调整大小以框住所有 mobject。
[`cache_cairo_context`]()|由于帧可以四处移动，因此用于更新的 cairo 上下文应该在每一帧重新生成。
[`capture_mobjects`]()|通过将 mobject 打印在 上来捕获它们`pixel_array`。
[`get_cached_cairo_context`]()|由于帧可以四处移动，因此用于更新的 cairo 上下文应该在每一帧重新生成。
[`get_mobjects_indicating_movement`]()|返回所有其移动意味着相机应将屏幕上的所有其他 mobject 视为移动的 mobject

属性

|||
|-|-|
`background_color`|
`background_opacity`|
[`frame_center`]()|返回笛卡尔坐标系中框架的中心点。
[`frame_height`]()|返回框架的高度。
[`frame_width`]()|返回框架的宽度


```py
auto_zoom(mobjects, margin=0, only_mobjects_in_frame=False, animate=True)
```

放大到给定的 mobject 数组（或单个 mobject）并自动调整大小以框住所有 mobject。

> 笔记

> 此方法仅在考虑 XY 平面中的 2D 对象时才有效，当相机旋转时，该方法将无法正常工作。

参数

- **mobjects** ( _list_ _\[_ [_Mobject_]() _\]_ ) – 相机将聚焦的 mobject 或 mobject 数组。
- **margin** ( _float_ ) – 添加到框架的边距宽度（可选，默认为 0）。
- **only_mobjects_in_frame** ( _bool_ ) – 如果设置为`True`，则仅允许关注已在帧中的 mobject。
- **animate** ( _bool_ ) – 如果设置为`False`，则应用更改而不是返回相应的动画

退货

\_AnimationBuilder 将相机视图缩放到给定的 mobjects 或 ScreenRectangle 列表，并将位置和大小更新为缩放位置。

返回类型

[联合](manim.mobject.geometry.boolean_ops.Union.html#manim.mobject.geometry.boolean_ops.Union "manim.mobject.geometry.boolean_ops.Union")\[\_AnimationBuilder, [ScreenRectangle](manim.mobject.frame.ScreenRectangle.html#manim.mobject.frame.ScreenRectangle "manim.mobject.frame.ScreenRectangle") \]

cache*cairo_context（*像素数组*， \_ctx*）[\[来源\]](../_modules/manim/camera/moving_camera.html#MovingCamera.cache_cairo_context)[#](#manim.camera.moving_camera.MovingCamera.cache_cairo_context "此定义的固定链接")

由于帧可以四处移动，因此用于更新的 cairo 上下文应该在每一帧重新生成。所以没有缓存。

capture*mobjects ( \_mobjects* , _\*\* kwargs_ )[\[来源\]](../_modules/manim/camera/moving_camera.html#MovingCamera.capture_mobjects)[#](#manim.camera.moving_camera.MovingCamera.capture_mobjects "此定义的固定链接")

通过将 mobject 打印在 上来捕获它们`pixel_array`。

这是将场景的内容转换为数组的基本函数，然后将其转换为图像或视频。

参数

- **mobjects** – 要捕获的 Mobjects。
- **kwargs** – 要传递给 的关键字参数`get_mobjects_to_display()`。

笔记

有关当前可以呈现的类的列表，请参阅`display_funcs()`。

_属性_ frame_center [#](#manim.camera.moving_camera.MovingCamera.frame_center "此定义的固定链接")

返回笛卡尔坐标系中框架的中心点。

退货

框架中心的笛卡尔坐标。

返回类型

np.数组

_属性_ frame_height [#](#manim.camera.moving_camera.MovingCamera.frame_height "此定义的固定链接")

返回框架的高度。

退货

框架的高度。

返回类型

漂浮

_属性_ frame_width [#](#manim.camera.moving_camera.MovingCamera.frame_width "此定义的固定链接")

返回框架的宽度

退货

框架的宽度。

返回类型

漂浮

get_cached_cairo*context（*像素数组\_）[\[来源\]](../_modules/manim/camera/moving_camera.html#MovingCamera.get_cached_cairo_context)[#](#manim.camera.moving_camera.MovingCamera.get_cached_cairo_context "此定义的固定链接")

由于帧可以四处移动，因此用于更新的 cairo 上下文应该在每一帧重新生成。所以没有缓存。

get_mobjects_indicating_movement ( )[\[来源\]](../_modules/manim/camera/moving_camera.html#MovingCamera.get_mobjects_indicating_movement)[#](#manim.camera.moving_camera.MovingCamera.get_mobjects_indicating_movement "此定义的固定链接")

返回所有其移动意味着相机应将屏幕上的所有其他 mobject 视为移动的 mobject

返回类型

列表
