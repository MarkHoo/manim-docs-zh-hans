# 贝塞尔曲线

与贝塞尔曲线相关的效用函数。

Functions

`bezier(points)`

贝塞尔曲线的经典实现。

参数

**points**( _np.ndarray_ ) – 定义所需贝塞尔曲线的点。

返回

描述贝塞尔曲线的函数。

返回类型

*`Callable[[float], Union[int, Iterable]]`*


`diag_to_matrix(l_and_u, diag)`

将其行表示矩阵对角线条目的数组转换为矩阵本身。请参阅 scipy.linalg.solve_banded

参数

- **l_and_u** *(tuple[int, int])* –
- **diag**( _np.ndarray_ ) –

返回类型

np.ndarray


`get_quadratic_approximation_of_cubic(a0, h0, h1, a1)`

`get_smooth_cubic_bezier_handle_points(points)`

`get_smooth_handle_points(points)`

给定一些锚点（点），计算手柄，使生成的贝塞尔曲线平滑。

参数

**points**( _np.ndarray_ ) – 锚点。

返回

计算手柄。

返回类型

_Tuple_\[np.ndarray, np.ndarray\]


`integer_interpolate(start, end, alpha)`

Alpha 是 0 到 1 之间的浮点数。这将返回一个介于 start 和 end（含）之间的整数，表示它们之间的适当插值，以及一个“残差”，表示返回的整数与列表中下一个整数之间的新比例。

例如，如果 start=0、end=10、alpha=0.46，则将返回 (4, 0.6)。

参数

- **start**（_float_）–
- **end**（_float_）–
- **alpha**（_float_）–

返回类型

tuple[int, float]


`interpolate(start, end, alpha)`

参数

- **start**（_ndarray_）-
- **end**（_ndarray_）-
- **alpha**（_float_）–

返回类型

_ndarray_


`inverse_interpolate(start, end, value)`

参数

- **start**（_float_）–
- **end**（_float_）–
- **value**（_float_）–

返回类型

_ndarray_


`is_closed(points)`

参数

**points** *(tuple[np.ndarray, np.ndarray])* –

返回类型

bool


`match_interpolate(new_start, new_end, old_start, old_end, old_value)`

参数

- **new_start** (_float_) –
- **new_end** (_float_) –
- **old_start** (_float_) –
- **old_end** (_float_) –
- **old_value**(_float_) –

返回类型

_ndarray_


`mid(start, end)`

参数

- **start**（_float_）–
- **end**（_float_）–

返回类型

float


`partial_bezier_points(points, a, b)`

给定一个定义贝塞尔曲线的点数组和两个数字` 0<=a<b<=1`，返回一个相同大小的数组，该数组描述了原始贝塞尔曲线在区间 \[a, b\] 上的部分。

这个算法非常漂亮，而且非常密集。

参数

- **points**( _ndarray_ ) – 定义贝塞尔曲线的点集。
- **a** ( _float_ ) – 所需部分贝塞尔曲线的下限。
- **b** ( _float_ ) – 所需部分贝塞尔曲线的上限。

返回

定义部分贝塞尔曲线的点集。

返回类型

np.ndarray


`partial_quadratic_bezier_points(points, a, b)`

`point_lies_on_bezier(point, control_points, round_to=1e-06)`

检查给定点是否位于具有给定控制点的贝塞尔曲线上。

这是通过求解以点为常数项的贝塞尔多项式来完成的；如果存在实根，则该点位于贝塞尔曲线上。

参数

- **point** ( _Iterable_ _\[_ _float_ _|_ _int_ _\]_ ) – 要检查的点的笛卡尔坐标。
- **control_points** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _|_ _int_ _\]_ _\]_ ) – 贝塞尔曲线的有序控制点的笛卡尔坐标，该点可能位于也可能不位于其上。
- **round_to** ( _float_ _|_ _int_ _|_ _None_ ) – 一个浮点数，其小数位数所有值（例如点的坐标）都将四舍五入。

返回

该点是否位于曲线上。

返回类型

bool


`proportions_along_bezier_curve_for_point(point, control_points, round_to=1e-06)`

给定贝塞尔曲线的控制点，获取与给定点对应的贝塞尔曲线沿线的比例。

贝塞尔多项式是使用给定点的坐标以及贝塞尔曲线的控制点构建的。在求解每个维度的多项式时，如果每个维度都有共同的根，那么这些根给出了该点所在曲线的比例。如果没有实根，则该点不在曲线上。

参数

- **point** ( _Iterable_ _\[_ _float_ _|_ _int_ _\]_ ) – 应获取参数的点的笛卡尔坐标。
- **control_points** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _|_ _int_ _\]_ _\]_ ) – 贝塞尔曲线的有序控制点的笛卡尔坐标，该点可能位于也可能不位于其上。
- **round_to** ( _float_ _|_ _int_ _|_ _None_ ) – 一个浮点数，其小数位数所有值（例如点的坐标）都将四舍五入。

返回

包含给定贝塞尔曲线上给定点的可能参数（沿贝塞尔曲线的比例）的列表。这通常只包含一个或零个元素，但如果该点位于闭环的开始/结束处，则可能返回一个包含超过 1 个值的列表，对应于循环的开始和结束等。

返回类型

np.ndarray\[float\]

提高

**ValueError** – 当`point`和 控制点具有不同形状时。


`quadratic_bezier_remap(triplets, new_number_of_curves)`

通过分割贝塞尔曲线将曲线数量重新映射到更高的数量

参数

- **Triplets** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _\]_ _\]_ ) – 要重新映射的二次贝塞尔曲线的三元组 shape(n, 3, 3)
- **new_number_of_curves** ( _int_ ) – 输出将包含的曲线数量。这需要高于当前的数字。

返回类型

二次贝塞尔曲线的新三元组。


`split_quadratic_bezier(points, t)`

将参数处的二次贝塞尔曲线拆分`t`为两条二次曲线。

参数

- **points**( _ndarray_ ) – 贝塞尔曲线的控制点具有形状`[a1, h1, b1]`
- **t** ( _float_ ) –`t`分割贝塞尔曲线的值

返回

- _作为元组列表的两条贝塞尔曲线，_
- 有形状`[a1, h1, b1], [a2, h2, b2]`

返回类型

_ndarray_


`subdivide_quadratic_bezier(points, n)`

将二次贝塞尔曲线细分为`n`具有相同形状的子曲线。

曲线分割点位于参数处 t=i/n 为了 i=1,...,n−1。

参数

- **points** ( _Iterable_ _\[_ _float_ _\]_ ) – 形式中贝塞尔曲线的控制点`[a1, h1, b1]`
- **n** ( _int_ ) – 将贝塞尔曲线细分为的曲线数

返回类型

贝塞尔曲线的新点的形式`[a1, h1, b1, a2, h2, b2, ...]`

![bezier_subdivision_example.png](../static/bezier_subdivision_example.png)
