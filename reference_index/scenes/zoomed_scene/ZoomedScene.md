# 缩放场景

合格名称：`manim.scene.zoomed\_scene.ZoomedScene`

```py
class ZoomedScene(camera_class=<class 'manim.camera.multi_camera.MultiCamera'>, zoomed_display_height=3, zoomed_display_width=3, zoomed_display_center=None, zoomed_display_corner=array([1., 1., 0.]), zoomed_display_corner_buff=0.5, zoomed_camera_config={'background_opacity': 1, 'default_frame_stroke_width': 2}, zoomed_camera_image_mobject_config={}, zoomed_camera_frame_starting_position=array([0., 0., 0.]), zoom_factor=0.15, image_frame_stroke_width=3, zoom_activated=False, **kwargs)
```

Bases: `MovingCameraScene`

这是一个具有特殊配置的场景，适用于必须放大并单独显示场景的特定部分的情况。


方法

|||
|-|-|
[`activate_zooming`]()|此方法用于激活 Zoomed_camera 的缩放功能。
[`get_zoom_factor`]()|返回缩放相机的缩放系数。
[`get_zoom_in_animation`]()|返回相机放大的动画。
[`get_zoomed_display_pop_out_animation`]()|这是迷你显示屏弹出的动画，显示变焦相机的内容。
[`setup`]()|Manim 在内部使用此方法来设置场景以供正确使用。



属性

`camera`



`activate_zooming(animate=False)`

此方法用于激活 Zoomed_camera 的缩放功能。

参数

**animate** ( _bool_ ) – 是否以动画方式激活缩放相机。


`get_zoom_factor()`

返回缩放相机的缩放系数。定义为变焦相机的高度与变焦迷你显示屏的高度之间的比率。:返回： 缩放系数。:r 类型：浮动



`get_zoom_in_animation(run_time=2, **kwargs)`

返回相机放大的动画。

参数

- **run_time** ( _float_ ) – 相机放大动画的运行时间。
- \***\*kwargs** – ApplyMethod() 的任何有效关键字参数

返回

相机放大的动画。

返回类型

[ApplyMethod]()



`get_zoomed_display_pop_out_animation(**kwargs)`

这是迷你显示屏弹出的动画，显示变焦相机的内容。

返回

弹出缩放显示的动画。

返回类型

[ApplyMethod]()



`setup()`

Manim 在内部使用此方法来设置场景以供正确使用。
