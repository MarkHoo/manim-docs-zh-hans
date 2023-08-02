# 背景 ColoredVMobjectDisplayer

合格名称：`manim.camera.camera.BackgroundColoredVMobjectDisplayer`

```py
class BackgroundColoredVMobjectDisplayer(camera)
```

Bases: object

参数

**相机**( [_Camera_]() ) – 要使用的相机对象。

方法

|||
|||
[`display`]()|显示彩色 VMobject。
[`get_background_array`]()|获取具有传递的 file_name 的背景数组。
`reset_pixel_array`|
[`resize_background_array`]()|调整代表背景的像素阵列的大小。
[`resize_background_array_to_match`]()|调整背景数组的大小以匹配传递的像素数组。


显示（_\* cvmobjects_）

显示彩色 VMobject。

参数

**\*cvmobjects** ( [_VMobject_]() ) – VMobjects

退货

显示 cvmobjects 的像素数组。

返回类型

np.数组

获取背景数组（_图像_）

获取具有传递的 file_name 的背景数组。

参数

**image** ( _Image.Image_ _|_ _pathlib.Path_ _|_ _str_ ) – 背景图像或其文件名。

退货

图像的像素阵列。

返回类型

np.ndarray

调整背景数组大小（_背景数组_、_新宽度_、_新高度_、_模式= 'RGBA'_）

调整代表背景的像素阵列的大小。

参数

- **background_array** ( _ndarray_ ) – 像素
- **new_width** ( _float_ ) – 背景的新宽度
- **new_height** ( _float_ ) – 背景的新高度
- **mode** ( _str_ ) – PIL 图像模式，默认为“RGBA”

退货

调整大小背景的 numpy 像素数组。

返回类型

np.数组

resize\*background_array_to_match（*背景数组*，\*像素数组\_）

调整背景数组的大小以匹配传递的像素数组。

参数

- **background_array** ( _ndarray_ ) – 预期像素数组。
- **Pixel_array** ( _ndarray_ ) – 宽度和高度应匹配的像素数组。

退货

调整大小的背景数组。

返回类型

np.数组
