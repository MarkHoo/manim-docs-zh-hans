# 缩放场景[#](#zoomedscene "此标题的固定链接")

合格名称：`manim.scene.zoomed\_scene.ZoomedScene`

_类_ ZoomedScene ( _camera_class=<class 'manim.camera.multi_camera.MultiCamera'>_、 _zoomed_display_height=3_、 _zoomed_display_width=3_、 _zoomed_display_center=None_、 _zoomed_display_corner=array(\[1._、 _1._、 _0.\])_、 _zoomed_display_corner_buff=0.5_、 _Zoomed_camera_config={'background_opacity': 1_ , _'default_frame_lines_width': 2}_ , _Zoomed_camera_image_mobject_config={}_ , _Zoomed_camera_frame_starting_position=array(\[0._ , _0._ , _0.\])_ ,_Zoom_factor=0.15_、 _image_frame_lines_width=3_、 _Zoom_activated=False_、 _\*\*kwargs_）[\[来源\]](../_modules/manim/scene/zoomed_scene.html#ZoomedScene)[#](#manim.scene.zoomed_scene.ZoomedScene "此定义的固定链接")

基地：[`MovingCameraScene`](manim.scene.moving_camera_scene.MovingCameraScene.html#manim.scene.moving_camera_scene.MovingCameraScene "manim.scene.movi​​ng_camera_scene.MovingCameraScene")

这是一个具有特殊配置的场景，适用于必须放大并单独显示场景的特定部分的情况。

方法

[`activate_zooming`](#manim.scene.zoomed_scene.ZoomedScene.activate_zooming "manim.scene.zoomed_scene.ZoomedScene.activate_zooming")

此方法用于激活 Zoomed_camera 的缩放功能。

[`get_zoom_factor`](#manim.scene.zoomed_scene.ZoomedScene.get_zoom_factor "manim.scene.zoomed_scene.ZoomedScene.get_zoom_factor")

返回缩放相机的缩放系数。

[`get_zoom_in_animation`](#manim.scene.zoomed_scene.ZoomedScene.get_zoom_in_animation "manim.scene.zoomed_scene.ZoomedScene.get_zoom_in_animation")

返回相机放大的动画。

[`get_zoomed_display_pop_out_animation`](#manim.scene.zoomed_scene.ZoomedScene.get_zoomed_display_pop_out_animation "manim.scene.zoomed_scene.ZoomedScene.get_zoomed_display_pop_out_animation")

这是迷你显示屏弹出的动画，显示变焦相机的内容。

[`setup`](#manim.scene.zoomed_scene.ZoomedScene.setup "manim.scene.zoomed_scene.ZoomedScene.setup")

Manim 在内部使用此方法来设置场景以供正确使用。

属性

`camera`

activate*zooming (*动画= False\_ )[\[来源\]](../_modules/manim/scene/zoomed_scene.html#ZoomedScene.activate_zooming)[#](#manim.scene.zoomed_scene.ZoomedScene.activate_zooming "此定义的固定链接")

此方法用于激活 Zoomed_camera 的缩放功能。

参数

**animate** ( _bool_ ) – 是否以动画方式激活缩放相机。

获取缩放因子( )[\[来源\]](../_modules/manim/scene/zoomed_scene.html#ZoomedScene.get_zoom_factor)[#](#manim.scene.zoomed_scene.ZoomedScene.get_zoom_factor "此定义的固定链接")

返回缩放相机的缩放系数。定义为变焦相机的高度与变焦迷你显示屏的高度之间的比率。:返回： 缩放系数。:r 类型：浮动

get*zoom_in*animation ( \_run_time = 2* , *\*\* kwargs\_ )[\[来源\]](../_modules/manim/scene/zoomed_scene.html#ZoomedScene.get_zoom_in_animation)[#](#manim.scene.zoomed_scene.ZoomedScene.get_zoom_in_animation "此定义的固定链接")

返回相机放大的动画。

参数

- **run_time** ( _float_ ) – 相机放大动画的运行时间。
- \***\*kwargs** – ApplyMethod() 的任何有效关键字参数

退货

相机放大的动画。

返回类型

[应用方法](manim.animation.transform.ApplyMethod.html#manim.animation.transform.ApplyMethod "manim.animation.transform.ApplyMethod")

get_zoomed_display_pop_out*animation ( *\*\* kwargs\_ )[\[来源\]](../_modules/manim/scene/zoomed_scene.html#ZoomedScene.get_zoomed_display_pop_out_animation)[#](#manim.scene.zoomed_scene.ZoomedScene.get_zoomed_display_pop_out_animation "此定义的固定链接")

这是迷你显示屏弹出的动画，显示变焦相机的内容。

退货

弹出缩放显示的动画。

返回类型

[应用方法](manim.animation.transform.ApplyMethod.html#manim.animation.transform.ApplyMethod "manim.animation.transform.ApplyMethod")

设置( )[\[来源\]](../_modules/manim/scene/zoomed_scene.html#ZoomedScene.setup)[#](#manim.scene.zoomed_scene.ZoomedScene.setup "此定义的固定链接")

Manim 在内部使用此方法来设置场景以供正确使用。
