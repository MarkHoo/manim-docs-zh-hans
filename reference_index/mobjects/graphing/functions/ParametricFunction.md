# 参数函数

合格名称：`manim.mobject.graphing.functions.ParametricFunction`


```py

```

参数曲线。

参数

- **function** ( _Callable_ _\[_ _\[_ _float_ _,_ _float_ _\]_ _,_ _float_ _\]_ ) – 以以下形式绘制的函数`(lambda x: x**2)`
- **t_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 确定函数跨越的长度。默认情况下`[0, 1]`
- **scaling** ( \__ScaleBase_ ) – 应用于函数点的缩放类。默认为[`LinearBase`]().
- **use_smoothing** ( _bool_ ) – 创建函数后是否在函数点之间进行插值。（分数较低时会出现奇怪的行为）
- **use_vectorized** ( _bool_ ) – 是否将生成的 t 值数组传递给函数 as 。仅当您的函数支持时才使用它。输出应该是形状的 numpy 数组，但如果轴是二维的，也可以为 0` [t_0, t_1, ...]``[[x_0, x_1, ...], [y_0, y_1, ...], [z_0, z_1, ...]]``z `
- **discontinuities** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 函数经历不连续性时的 t 值。
- **dt** ( _float_ ) – 不连续性的左右容差。

例子

示例：绘图参数函数

![PlotParametricFunction-1.png](../_images/PlotParametricFunction-1.png)

```py

```

示例：ThreeDParametricSpring 

![ThreeDParametricSpring-1.png](../_images/ThreeDParametricSpring-1.png)

```py

```


注意力

如果您的函数存在不连续性，则必须手动指定不连续性的位置。请参阅以下示例以获取指导。

示例：不连续示例

![DiscontinuousExample-1.png](../_images/DiscontinuousExample-1.png)

```py

```

方法

[`generate_points`]()

初始化`points`并因此初始化形状。

`get_function`

`get_point_from_function`

[`init_points`]()

初始化`points`并因此初始化形状。

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

生成点( )

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

初始化点（）

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。
