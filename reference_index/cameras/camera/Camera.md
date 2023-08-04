# 相机

合格名称：`manim.camera.camera.Camera`

```py
class Camera(background_image=None, frame_center=array([0., 0., 0.]), image_mode='RGBA', n_channels=4, pixel_array_dtype='uint8', cairo_line_width_multiple=0.01, use_z_index=True, background=None, pixel_height=None, pixel_width=None, frame_height=None, frame_width=None, frame_rate=None, **kwargs)
```

Bases: `object`

基础相机类。

该对象负责在任何给定时刻在屏幕上准确显示的内容。

参数

- **background_image** ( _str_ _|_ _None_ ) – 应作为背景图像的图像的路径。如果未设置，则背景填充为`self.background_color`
- **background**( _np.ndarray_ _|_ _None_ ) –`background`设置的内容。默认情况下，`None`.
- **Pixel_height** ( _int_ _|_ _None_ ) – 场景的高度（以像素为单位）。
- **Pixel_width** ( _int_ _|_ _None_ ) – 场景的宽度（以像素为单位）。
- **kwargs** – 要设置的附加参数 ( `background_color`, )。`background_opacity`
- **frame_center** ( _np.ndarray_ ) –
- **image_mode**( _str_ ) –
- **n_channels** ( _int_ ) –
- **Pixel_array_dtype** ( _str_ ) –
- **cairo_line_width_multiple** (_float_) –
- **use_z_index** (_bool_) –
- **frame_height**（_float**|**None_）–
- **frame_width**（_float**|**None_）–
- **frame_rate**（_float**|**None_）–


方法

|||
|-|-|
[`adjust_out_of_range_points`]()|如果传递的数组中的任何点超出了可行范围，则对其进行适当调整。
[`adjusted_thickness`]()|参数厚度
[`apply_fill`]()|填充开罗上下文
[`apply_stroke`]()|对 cairo 上下文中的 VMobject 应用描边。
[`cache_cairo_context`]()|将传递的像素数组缓存到开罗上下文中
[`capture_mobject`]()|通过将其存储在 中来捕获 mobject `pixel_array`。
[`capture_mobjects`]()|通过将 mobject 打印在 上来捕获它们`pixel_array`。
[`convert_pixel_array`]()|将像素数组从包含浮点数的值转换为正确的 RGB 值。
[`display_image_mobject`]()|通过适当更改 Pixel_array 显示 ImageMobject。
[`display_multiple_background_colored_vmobjects`]()|显示多个与背景颜色相同的 vmobject。
[`display_multiple_image_mobjects`]()|通过修改传递的 pixel_array 来显示多个图像 mobject。
[`display_multiple_non_background_colored_vmobjects`]()|在 cairo 上下文中显示多个 VMobject，只要它们没有背景色。
[`display_multiple_point_cloud_mobjects`]()|通过修改传递的像素数组来显示多个 PMobject。
[`display_multiple_vectorized_mobjects`]()|显示 pixel_array 中的多个 VMobject
[`display_point_cloud`]()|通过适当修改像素数组来显示 PMobject。
[`display_vectorized`]()|在 cairo 上下文中显示 VMobject
[`get_background_colored_vmobject_displayer`]()|如果存在则返回 background_colored_vmobject_displayer，或者创建一个，如果不存在则返回它。
[`get_cached_cairo_context`]()|如果传递的像素数组存在，则返回已缓存的 cairo 上下文；如果不存在，则返回 None。
[`get_cairo_context`]()|将像素数组缓存到 self.pixel_array_to_cairo_context 后返回该像素数组的 cairo 上下文。如果该数组已被缓存，则返回缓存的版本。
[`get_coords_of_all_pixels`]()|返回每个像素的笛卡尔坐标。
[`get_fill_rgbas`]()|返回传入的 VMobject 的填充的 RGBA 数组
[`get_image`]()|从传递的像素数组返回图像，如果传递的像素数组为空，则从当前帧返回图像。
[`get_mobjects_to_display`]()|用于获取要通过相机显示的对象列表。
[`get_stroke_rgbas`]()|获取传递的 VMobject 笔画的 RGBA 数组。
[`get_thickening_nudges`]()|参数厚度
[`init_background`]()|初始化背景。
[`is_in_frame`]()|检查传递的 mobject 是否在框架中。
[`make_background_from_func`]()|通过使用 coords_to_colors_func 确定每个像素的颜色，为背景创建像素数组。
[`on_screen_pixels`]()|从给定的像素坐标数组返回屏幕上的像素数组
[`overlay_PIL_image`]()|将 PIL 图像叠加在传递的像素阵列上。
[`overlay_rgba_array`]()|将 RGBA 数组叠加在给定的 Pixel 数组之上。
`points_to_pixel_coords`|
[`reset`]()|将相机的像素阵列重置为背景的像素阵列
[`reset_pixel_shape`]()|该方法将单个像素的高度和宽度重置为传递的 new_height 和 new_width。
[`resize_frame_shape`]()|更改 frame_shape 以匹配像素的宽高比，其中 fixed_dimension 确定 frame_height 或 frame_width 是否保持固定，而其他则相应变化。
[`set_background`]()|转换为有效的 RGB 值后，将背景设置为传递的 Pixel_array。
[`set_background_from_func`]()|使用 coords_to_colors_func 将背景设置为像素数组以确定每个像素的颜色。
[`set_cairo_context_color`]()|设置开罗上下文的颜色
[`set_cairo_context_path`]()|设置 cairo 上下文的路径并传递 vmobject
`set_frame_to_background`|
[`set_pixel_array`]()|将相机的像素数组设置为传递的像素数组。
[`thickened_coordinates`]()|返回传递的像素坐标数组的加厚坐标以及要加厚的厚度。
`transform_points_pre_display`|
[`type_or_raise`]()|如果 mobject 是可渲染的类型，则返回该类型。



属性

`background_color`

`background_opacity`



`adjust_out_of_range_points(points)`

如果传递的数组中的任何点超出了可行范围，则对其进行适当调整。

参数

**points**( _ndarray_ ) – 要调整的点

返回

调整后的点。

返回类型

np.array


`adjusted_thickness(thickness)`

参数

**thickness**（_float_）–

返回类型

float


`apply_fill(ctx, vmobject)`

填充开罗上下文

参数

- **ctx** ( _Context_ ) – 开罗上下文
- **vmobject** ( [_VMobject_]() ) – VMobject

返回

相机对象。

返回类型

[Camera]()



`apply_stroke(ctx, vmobject, background=False)`

对 cairo 上下文中的 VMobject 应用描边。

参数

- **ctx** ( _Context_ ) – 开罗上下文
- **vmobject** ( [_VMobject_]() ) – VMobject
- **background** ( _bool_ ) – 应用此描边宽度时是否考虑背景，默认为 False

返回

应用了描边的相机对象。

返回类型

[Camera]()



`cache_cairo_context(pixel_array, ctx)`

将传递的像素数组缓存到开罗上下文中

参数

- **Pixel_array** ( _ndarray_ ) – 要缓存的像素数组
- **ctx** ( _Context_ ) – 将其缓存到的上下文。



`capture_mobject(mobject, **kwargs)`

通过将其存储在 中来捕获 mobject `pixel_array`。

这是 的单对象版本[`capture_mobjects()`]()。

参数

- **mobject** ( [_Mobject_]() ) – 要捕获的 Mobject。
- **kwargs** ( _Any_ ) – 要传递给的关键字参数[`get_mobjects_to_display()`]()。



`capture_mobjects(mobjects, **kwargs)`

通过将 mobject 打印在 上来捕获它们`pixel_array`。

这是将场景的内容转换为数组的基本函数，然后将其转换为图像或视频。

参数

- **mobjects** ( _Iterable_ _\[_ [_Mobject_]() _\]_ ) – 要捕获的 Mobjects。
- **kwargs** – 要传递给 的关键字参数[`get_mobjects_to_display()`]()。

笔记

有关当前可以呈现的类的列表，请参阅`display_funcs()`。


`convert_pixel_array(pixel_array, convert_from_floats=False)`

将像素数组从包含浮点数的值转换为正确的 RGB 值。

参数

- **Pixel_array** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要转换的像素数组。
- **Convert_from_floats** ( _bool_ ) – 是否将浮点值转换为整数，默认为 False

返回

新的、转换后的像素阵列。

返回类型

np.array



`display_image_mobject(image_mobject, pixel_array)`

通过适当更改 Pixel_array 显示 ImageMobject。

参数

- **image_mobject** ( [_AbstractImageMobject_]() ) – 要显示的 imageMobject
- **Pixel_array** ( _ndarray_ ) – 放置图像对象的像素数组。



`display_multiple_background_colored_vmobjects(cvmobjects, pixel_array)`

显示多个与背景颜色相同的 vmobject。

参数

- **cvmobjects** ( _list_ ) – 彩色 VMobject 列表
- **Pixel_array** ( _ndarray_ ) – 像素数组。

返回

相机对象。

返回类型

[Camera]()



`display_multiple_image_mobjects(image_mobjects, pixel_array)`

通过修改传递的 pixel_array 来显示多个图像 mobject。

参数

- **image_mobjects** ( _list_ ) – ImageMobjects 列表
- **Pixel_array** ( _ndarray_ ) – 要修改的像素数组。



`display_multiple_non_background_colored_vmobjects(vmobjects, pixel_array)`

在 cairo 上下文中显示多个 VMobject，只要它们没有背景色。

参数

- **vmobjects** ( _list_ ) – VMobjects 列表
- **Pixel_array** ( _ndarray_ ) – 要添加 VMobject 的像素数组。


`display_multiple_point_cloud_mobjects(pmobjects, pixel_array)`

通过修改传递的像素数组来显示多个 PMobject。

参数

- **pmobjects** ( _list_ ) – PMobjects 列表
- **Pixel_array** ( _ndarray_ ) – 要修改的像素数组。


`display_multiple_vectorized_mobjects(vmobjects, pixel_array)`

显示 pixel_array 中的多个 VMobject

参数

- **vmobjects** ( _list_ ) – 要显示的 VMobject 列表
- **Pixel_array** ( _ndarray_ ) – 像素数组


`display_point_cloud(pmobject, points, rgbas, thickness, pixel_array)`

通过适当修改像素数组来显示 PMobject。 TODO：为 rgbas 参数编写描述。:param pmobject: 点云 Mobject :parampoints: 在点云 mobject 中显示的点 :param rgbas: :param Thickness: PMobject 每个点的厚度 :param Pixel_array: 要修改的像素数组。

参数

- **pmobject** ( [_PMobject_]() ) –
- **points**（_list_）-
- **rgbas** ( _ndarray_ ) –
- **thickness**（_float_）–
- **pixel_array**( _ndarray_ ) –


`display_vectorized(vmobject, ctx)`

在 cairo 上下文中显示 VMobject

参数

- **vmobject** ( [_VMobject_]() ) – 要显示的矢量化 Mobject
- **ctx** ( _Context_ ) – 要使用的 cairo 上下文。

返回

相机对象

返回类型

[Camera]()



`get_background_colored_vmobject_displayer()`

如果存在则返回 background_colored_vmobject_displayer，或者创建一个，如果不存在则返回它。

返回

显示与背景颜色相同的 VMobject 的对象。

返回类型

BackGroundColoredVMobjectDisplayer


`get_cached_cairo_context(pixel_array)`

如果传递的像素数组存在，则返回已缓存的 cairo 上下文；如果不存在，则返回 None。

参数

**Pixel_array** ( _ndarray_ ) – 要检查的像素数组。

返回

缓存的开罗上下文。

返回类型

cairo.Context


`get_cairo_context(pixel_array)`

将像素数组缓存到 self.pixel_array_to_cairo_context 后返回该像素数组的 cairo 上下文。如果该数组已被缓存，则返回缓存的版本。

参数

**Pixel_array** ( _ndarray_ ) – 要获取 cairo 上下文的像素数组。

返回

像素数组的 cairo 上下文。

返回类型

cairo.Context



`get_coords_of_all_pixels()`

返回每个像素的笛卡尔坐标。

返回

笛卡尔坐标数组。

返回类型

np.ndarray


`get_fill_rgbas(vmobject)`

返回传入的 VMobject 的填充的 RGBA 数组

参数

**vmobject** ( [_VMobject_]() ) – VMobject

返回

VMobject 填充的 RGBA 数组

返回类型

np.array


`get_image(pixel_array=None)`

从传递的像素数组返回图像，如果传递的像素数组为空，则从当前帧返回图像。

参数

**Pixel_array** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ _|_ _None_ ) – 从中获取图像的像素数组，默认为 None

返回

阵列的 PIL 图像。

返回类型

PIL.Image



`get_mobjects_to_display(mobjects, include_submobjects=True, excluded_mobjects=None)`

用于获取要通过相机显示的对象列表。

参数

- **mobjects** ( _Iterable_ _\[_ [_Mobject_]() _\]_ ) – Mobjects
- **include_submobjects** ( _bool_ ) – 是否包含 mobjects 的子对象，默认 True
- **excepted_mobjects** ( _list_ _|_ _None_ ) – 要排除的任何 mobjects，默认为 None

返回

对象列表

返回类型

list


`get_stroke_rgbas(vmobject, background=False)`

获取传递的 VMobject 笔画的 RGBA 数组。

参数

- **vmobject** ( [_VMobject_]() ) – VMobject
- **background** ( _bool_ ) – 获取描边 RGBAs 时是否考虑背景，默认 False

返回

笔画的 RGBA 数组。

返回类型

np.ndarray


`get_thickening_nudges(thickness)`

参数

**thickness**（_float_）–

返回类型

np.array


`init_background()`

初始化背景。如果 self.background_image 是图像的路径，则图像被设置为背景；否则，默认背景颜色填充背景。


`is_in_frame(mobject)`

检查传递的 mobject 是否在框架中。

参数

**mobject** ( [_Mobject_]() ) – 需要进行检查的 mobject。

返回

如果在框架内则为 True，否则为 False。

返回类型

bool


`make_background_from_func(coords_to_colors_func)`

通过使用 coords_to_colors_func 确定每个像素的颜色，为背景创建像素数组。每个输入像素的颜色。coords_to_colors_func 的每个输入都是空间中的 (x, y) 对（在普通空间坐标中；不是像素坐标），并且每个输出预计是 4 个浮点数的 RGBA 数组。

参数

**coords_to_colors_func** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 输入是 (x,y) 坐标对且返回值必须是该点的颜色的函数

返回

然后可以将像素数组传递给 set_background。

返回类型

np.array


`on_screen_pixels(pixel_coords)`


从给定的像素坐标数组返回屏幕上的像素数组

参数

**Pixel_coords** ( _ndarray_ ) – 要检查的像素坐标。

返回

屏幕上的像素坐标。

返回类型

np.array


`overlay_PIL_image(pixel_array, image)`

将 PIL 图像叠加在传递的像素阵列上。

参数

- **Pixel_array** ( _np.ndarray_ ) – 像素数组
- **image** ( _Image_ ) – 要叠加的图像。



`overlay_rgba_array(pixel_array, new_array)`

将 RGBA 数组叠加在给定的 Pixel 数组之上。

参数

- **Pixel_array** ( _ndarray_ ) – 要修改的原始像素数组。
- **new_array** ( _ndarray_ ) – 要覆盖的新像素数组。


`reset()`

将相机的像素阵列重置为背景的像素阵列

返回

设置像素数组后的相机对象。

返回类型

[Camera]()


`reset_pixel_shape(new_height, new_width)`

该方法将单个像素的高度和宽度重置为传递的 new_height 和 new_width。

参数

- **new_height** ( _float_ ) – 整个场景的新高度（以像素为单位）
- **new_width** ( _float_ ) – 整个场景的新宽度（以像素为单位）


`resize_frame_shape(fixed_dimension=0)`

更改 frame_shape 以匹配像素的宽高比，其中 fixed_dimension 确定 frame_height 或 frame_width 是否保持固定，而其他则相应变化。

参数

**fixed_dimension** ( _int_ ) – 如果为 0，则高度相对于宽度缩放，否则宽度相对于高度缩放。


`set_background(pixel_array, convert_from_floats=False)`

转换为有效的 RGB 值后，将背景设置为传递的 Pixel_array。

参数

- **Pixel_array** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要设置背景的像素数组。
- **Convert_from_floats** ( _bool_ ) – 是否将浮点值转换为正确的 RGB 有效值，默认为 False


`set_background_from_func(coords_to_colors_func)`

使用 coords_to_colors_func 将背景设置为像素数组以确定每个像素的颜色。每个输入像素的颜色。coords_to_colors_func 的每个输入都是空间中的 (x, y) 对（在普通空间坐标中；不是像素坐标），并且每个输出预计是 4 个浮点数的 RGBA 数组。

参数

**coords_to_colors_func** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 输入是 (x,y) 坐标对且返回值必须是该点的颜色的函数


`set_cairo_context_color(ctx, rgbas, vmobject)`

设置开罗上下文的颜色

参数

- **ctx** ( _Context_ ) – 开罗上下文
- **rgbas** ( _ndarray_ ) – 用于为上下文着色的 RGBA 数组。
- **vmobject** ( [_VMobject_]() ) – 用于设置颜色的 VMobject。

返回

相机对象

返回类型

[Camera]()


`set_cairo_context_path(ctx, vmobject)`

设置 cairo 上下文的路径并传递 vmobject

参数

- **ctx** ( _Context_ ) – 开罗上下文
- **vmobject** ( [_VMobject_]() ) – VMobject

返回

设置 cairo_context_path 后的相机对象

返回类型

[Camera]()


`set_pixel_array(pixel_array, convert_from_floats=False)`

将相机的像素数组设置为传递的像素数组。

参数

- **Pixel_array** ( _np.ndarray_ _|_ _list_ _|_ _tuple_ ) – 要转换的像素数组，然后设置为相机的像素数组。
- **Convert_from_floats** ( _bool_ ) – 是否将浮点值转换为正确的 RGB 值，默认为 False



`thickened_coordinates(pixel_coords, thickness)`

返回传递的像素坐标数组的加厚坐标以及要加厚的厚度。

参数

- **Pixel_coords** ( _ndarray_ ) – 像素坐标
- **thickness**( _float_ ) – 厚度

返回

加厚像素坐标数组。

返回类型

np.array


`type_or_raise(mobject)`

如果 mobject 是可渲染的类型，则返回该类型。

如果 mobject 是继承自可呈现类的类的实例，则返回超类。例如，Square 的实例也是 VMobject 的实例，并且可以渲染它们。因此，type_or_raise(Square())返回 True。

参数

**mobject** ( [_Mobject_]() ) – 要采用其类型的对象。

笔记

有关当前可以呈现的类的列表，请参阅`display_funcs()`。

返回

mobject 的类型（如果可以渲染）。

返回类型

Type\[ [`Mobject`]()\]

提高

**TypeError** – 当 mobject 不是可呈现的类的实例时。

参数

**mobject** ( [_Mobject_]() ) –
