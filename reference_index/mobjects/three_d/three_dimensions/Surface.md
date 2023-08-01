# 表面

合格名称：`manim.mobject.three\_d.three\_dimensions.Surface`

_类_ Surface ( _func_ , _u_range = \[0, 1\]_ , _v_range = \[0, 1\]_ ,_分辨率= 32_ , _surface_piece_config = {}_ , _fill_color = '#29ABCA'_ , _fill_opacity = 1.0_ , _checkerboard_colors = \['#29ABCA', ' #236B8E'\]_，_笔划颜色= '#BBBBBB'_，_笔划宽度= 0.5_， _should_make_jagged = False_, _pre_function_handle_to_anchor_scale_factor = 1e-05_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Surface)[#](#manim.mobject.three_d.three_dimensions.Surface "此定义的固定链接")

基地：[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

使用棋盘图案创建参数化曲面。

参数

- **func** ( _Callable_ _\[_ _\[_ _float_ _,_ _float_ _\]_ _,_ _np.ndarray_ _\]_ ) – 定义 .ndarray 的函数[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。
- **u_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 变量的范围`u`：。`(u_min, u_max)`
- **v_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 变量的范围`v`：。`(v_min, v_max)`
- **分辨率**( _Sequence_ _\[_ _int_ _\]_ ) – 所采集的样本数[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。元组可用于分别定义`u`和的不同分辨率`v`。
- **fill_color** ( _Color_ ) – 的颜色[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。如果已设置则忽略`checkerboard_colors` 。
- **fill_opacity** ( _float_ ) – 的不透明度[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")，从 0 表示完全透明到 1 表示完全不透明。默认为 1。
- **checkerboard_colors** ( _Sequence_ _\[_ _Color_ _\]_ ) – 各个面交替颜色。覆盖`fill_color`.
- **stroke_color** ( _Color_ ) – 的每个面周围的描边颜色[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。
- **stroke_width** ( _float_ ) – 围绕 的每个面的描边宽度[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。默认为 0.5。
- **should_make_jagged** ( _bool_ ) – 将贝塞尔曲线的锚点模式从平滑更改为锯齿状。默认为`False`.
- **surface_piece_config** (_字典_) –
- **pre_function_handle_to_anchor_scale_factor** ( _float_ ) –

例子

示例：ParaSurface [¶](#parasurface)

![../_images/ParaSurface-1.png](../_images/ParaSurface-1.png)

from manim import \*

class ParaSurface(ThreeDScene):
def func(self, u, v):
return np.array(\[np.cos(u) _ np.cos(v), np.cos(u) _ np.sin(v), u\])

    def construct(self):
        axes = ThreeDAxes(x_range=\[-4,4\], x_length=8)
        surface = Surface(
            lambda u, v: axes.c2p(*self.func(u, v)),
            u_range=\[-PI, PI\],
            v_range=\[0, TAU\],
            resolution=8,
        )
        self.set\_camera\_orientation(theta=70 * DEGREES, phi=75 * DEGREES)
        self.add(axes, surface)

Copy to clipboard

方法

[`func`](#manim.mobject.three_d.three_dimensions.Surface.func "manim.mobject. Three_d. Three_dimensions.Surface.func")

定义所绘制的 z 值[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。

[`set_fill_by_checkerboard`](#manim.mobject.three_d.three_dimensions.Surface.set_fill_by_checkerboard "manim.mobject. Three_d. Three_dimensions.Surface.set_fill_by_checkerboard")

[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")以交替模式设置每个面的 fill_color 。

[`set_fill_by_value`](#manim.mobject.three_d.three_dimensions.Surface.set_fill_by_value "manim.mobject. Three_d. Three_dimensions.Surface.set_fill_by_value")

将参数化曲面的每个 mobject 的颜色设置为相对于其轴值的颜色。

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。

函数（_u_， _v_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Surface.func)[#](#manim.mobject.three_d.three_dimensions.Surface.func "此定义的固定链接")

定义所绘制的 z 值[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。

退货

定义 的 z 值[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。

返回类型

`numpy.array`

参数

- **u**（_浮动_）–
- **v**（_浮动_）–

set_fill_by*checkerboard（*\*颜色*，*不透明度=无\_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Surface.set_fill_by_checkerboard)[#](#manim.mobject.three_d.three_dimensions.Surface.set_fill_by_checkerboard "此定义的固定链接")

[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")以交替模式设置每个面的 fill_color 。

参数

- **颜色**( _Sequence_ _\[_ _Color_ _\]_ ) – 交替图案的颜色列表。
- **opacity** ( _float_ ) – 的 fill_opacity [`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")，从 0 表示完全透明到 1 表示完全不透明。

退货

具有交替图案的参数化曲面。

返回类型

[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")

set*fill_by*value (*轴*, \_colorscale = None* , \_axis = 2* , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Surface.set_fill_by_value)[#](#manim.mobject.three_d.three_dimensions.Surface.set_fill_by_value "此定义的固定链接")

将参数化曲面的每个 mobject 的颜色设置为相对于其轴值的颜色。

参数

- **axis** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 参数化曲面的轴，用于将轴值映射到颜色。
- **colorscale** ( [_Union_](manim.mobject.geometry.boolean_ops.Union.html#manim.mobject.geometry.boolean_ops.Union "manim.mobject.geometry.boolean_ops.Union") _\[_ _Iterable_ _\[_ _Color_ _\]_ _,_ _Color_ _\]_ _|_ _None_ ) – 颜色列表，从较低的轴值到较高的轴值排序。如果传递包含与数字配对的颜色的元组列表，则这些数字将用作主元。
- **axis** ( _int_ ) – 选择用于颜色映射的轴。（0 = x、1 = y、2 = z）

退货

具有按值应用的渐变的参数化曲面。用于链接。

返回类型

[`Surface`](#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")

例子

示例：按值填充示例[¶](#fillbyvalueexample)

![../_images/FillByValueExample-1.png](../_images/FillByValueExample-1.png)

from manim import \*

class FillByValueExample(ThreeDScene):
def construct(self):
resolution*fa = 8
self.set_camera_orientation(phi=75 * DEGREES, theta=-160 \_ DEGREES)
axes = ThreeDAxes(x_range=(0, 5, 1), y_range=(0, 5, 1), z_range=(-1, 1, 0.5))
def param_surface(u, v):
x = u
y = v
z = np.sin(x) \* np.cos(y)
return z
surface_plane = Surface(
lambda u, v: axes.c2p(u, v, param_surface(u, v)),
resolution=(resolution_fa, resolution_fa),
v_range=\[0, 5\],
u_range=\[0, 5\],
)
surface_plane.set_style(fill_opacity=1)
surface_plane.set_fill_by_value(axes=axes, colorscale=\[(RED, -0.5), (YELLOW, 0), (GREEN, 0.5)\], axis=2)
self.add(axes, surface_plane)

Copy to clipboard
