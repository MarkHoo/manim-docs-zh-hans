# 贝塞尔曲线[#](#module-manim.utils.bezier "此标题的固定链接")

与贝塞尔曲线相关的效用函数。

功能

贝塞尔曲线（_点_）[\[来源\]](../_modules/manim/utils/bezier.html#bezier)[#](#manim.utils.bezier.bezier "此定义的固定链接")

贝塞尔曲线的经典实现。

参数

**点**( _np.ndarray_ ) – 定义所需贝塞尔曲线的点。

退货

描述贝塞尔曲线的函数。

返回类型

_可调用_\[\[float\]、_Union_ \[int、_Iterable_ \]\]

diag*to_matrix（\_l_and_u*， _diag_）[\[来源\]](../_modules/manim/utils/bezier.html#diag_to_matrix)[#](#manim.utils.bezier.diag_to_matrix "此定义的固定链接")

将其行表示矩阵对角线条目的数组转换为矩阵本身。请参阅 scipy.linalg.solve_banded

参数

- **l_and_u** (_元组\_\_\[_ _int_ _,_ _int_ _\]_ ) –
- **诊断**( _np.ndarray_ ) –

返回类型

np.ndarray

get*quadratic_approximation_of_cubic ( \_a0* , _h0_ , _h1_ , _a1_ )[\[来源\]](../_modules/manim/utils/bezier.html#get_quadratic_approximation_of_cubic)[#](#manim.utils.bezier.get_quadratic_approximation_of_cubic "此定义的固定链接")

get_smooth_cubic_bezier_handle*points（*点\_）[\[来源\]](../_modules/manim/utils/bezier.html#get_smooth_cubic_bezier_handle_points)[#](#manim.utils.bezier.get_smooth_cubic_bezier_handle_points "此定义的固定链接")

get_smooth_handle*points (*点\_)[\[来源\]](../_modules/manim/utils/bezier.html#get_smooth_handle_points)[#](#manim.utils.bezier.get_smooth_handle_points "此定义的固定链接")

给定一些锚点（点），计算手柄，使生成的贝塞尔曲线平滑。

参数

**点**( _np.ndarray_ ) – 锚点。

退货

计算手柄。

返回类型

_元组_\[np.ndarray, np.ndarray\]

整数插值（_开始_、_结束_、_阿尔法_）[\[来源\]](../_modules/manim/utils/bezier.html#integer_interpolate)[#](#manim.utils.bezier.integer_interpolate "此定义的固定链接")

Alpha 是 0 到 1 之间的浮点数。这将返回一个介于 start 和 end（含）之间的整数，表示它们之间的适当插值，以及一个“残差”，表示返回的整数与列表中下一个整数之间的新比例。

例如，如果 start=0、end=10、alpha=0.46，则将返回 (4, 0.6)。

参数

- **开始**（_浮动_）–
- **结束**（_浮动_）–
- **阿尔法**（_浮动_）–

返回类型

元组\[整数，浮点数\]

插值（_开始_、_结束_、 _alpha_）[\[来源\]](../_modules/manim/utils/bezier.html#interpolate)[#](#manim.utils.bezier.interpolate "此定义的固定链接")

参数

- **开始**（_ndarray_）-
- **结束**（_ndarray_）-
- **阿尔法**（_浮动_）–

返回类型

_ndarray_

inverse*interpolate（*开始*、*结束*、*值\_）[\[来源\]](../_modules/manim/utils/bezier.html#inverse_interpolate)[#](#manim.utils.bezier.inverse_interpolate "此定义的固定链接")

参数

- **开始**（_浮动_）–
- **结束**（_浮动_）–
- **值**（_浮点数_）–

返回类型

_ndarray_

is*close (*点\_)[\[来源\]](../_modules/manim/utils/bezier.html#is_closed)[#](#manim.utils.bezier.is_closed "此定义的固定链接")

参数

**点**(_元组\_\_\[_ _np.ndarray_ _,_ _np.ndarray_ _\]_ ) –

返回类型

布尔值

match*interpolate (*新开始*,*新结束*,*旧开始*,*旧结束*,*旧值\_)[\[来源\]](../_modules/manim/utils/bezier.html#match_interpolate)[#](#manim.utils.bezier.match_interpolate "此定义的固定链接")

参数

- **new_start** (_浮点数_) –
- **new_end** (_浮点数_) –
- **old_start** (_浮点数_) –
- **old_end** (_浮点数_) –
- **旧值**(_浮点_) –

返回类型

_ndarray_

中（_开始_、_结束_）[\[来源\]](../_modules/manim/utils/bezier.html#mid)[#](#manim.utils.bezier.mid "此定义的固定链接")

参数

- **开始**（_浮动_）–
- **结束**（_浮动_）–

返回类型

漂浮

部分贝塞尔曲线点(_点_, _a_ , _b_ )[\[来源\]](../_modules/manim/utils/bezier.html#partial_bezier_points)[#](#manim.utils.bezier.partial_bezier_points "此定义的固定链接")

给定一个定义贝塞尔曲线的点数组和两个数字 0<=a<b<=1，返回一个相同大小的数组，该数组描述了原始贝塞尔曲线在区间 \[a, b\] 上的部分。

这个算法非常漂亮，而且非常密集。

参数

- **点**( _ndarray_ ) – 定义贝塞尔曲线的点集。
- **a** ( _float_ ) – 所需部分贝塞尔曲线的下限。
- **b** ( _float_ ) – 所需部分贝塞尔曲线的上限。

退货

定义部分贝塞尔曲线的点集。

返回类型

np.ndarray

partial*quadratic_bezier*points (_点_, \_a* , \_b* )[\[来源\]](../_modules/manim/utils/bezier.html#partial_quadratic_bezier_points)[#](#manim.utils.bezier.partial_quadratic_bezier_points "此定义的固定链接")

point*lies_on*bezier (_点_, \_control_points* , \_round_to = 1e-06* )[\[来源\]](../_modules/manim/utils/bezier.html#point_lies_on_bezier)[#](#manim.utils.bezier.point_lies_on_bezier "此定义的固定链接")

检查给定点是否位于具有给定控制点的贝塞尔曲线上。

这是通过求解以点为常数项的贝塞尔多项式来完成的；如果存在实根，则该点位于贝塞尔曲线上。

参数

- **point** ( _Iterable_ _\[_ _float_ _|_ _int_ _\]_ ) – 要检查的点的笛卡尔坐标。
- **control_points** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _|_ _int_ _\]_ _\]_ ) – 贝塞尔曲线的有序控制点的笛卡尔坐标，该点可能位于也可能不位于其上。
- **round_to** ( _float_ _|_ _int_ _|_ _None_ ) – 一个浮点数，其小数位数所有值（例如点的坐标）都将四舍五入。

退货

该点是否位于曲线上。

返回类型

布尔值

比例*沿*贝塞尔曲线\_for*point （*点*，*控制点*， \_round_to = 1e-06*）[\[来源\]](../_modules/manim/utils/bezier.html#proportions_along_bezier_curve_for_point)[#](#manim.utils.bezier.proportions_along_bezier_curve_for_point "此定义的固定链接")

给定贝塞尔曲线的控制点，获取与给定点对应的贝塞尔曲线沿线的比例。

贝塞尔多项式是使用给定点的坐标以及贝塞尔曲线的控制点构建的。在求解每个维度的多项式时，如果每个维度都有共同的根，那么这些根给出了该点所在曲线的比例。如果没有实根，则该点不在曲线上。

参数

- **point** ( _Iterable_ _\[_ _float_ _|_ _int_ _\]_ ) – 应获取参数的点的笛卡尔坐标。
- **control_points** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _|_ _int_ _\]_ _\]_ ) – 贝塞尔曲线的有序控制点的笛卡尔坐标，该点可能位于也可能不位于其上。
- **round_to** ( _float_ _|_ _int_ _|_ _None_ ) – 一个浮点数，其小数位数所有值（例如点的坐标）都将四舍五入。

退货

包含给定贝塞尔曲线上给定点的可能参数（沿贝塞尔曲线的比例）的列表。这通常只包含一个或零个元素，但如果该点位于闭环的开始/结束处，则可能返回一个包含超过 1 个值的列表，对应于循环的开始和结束等。

返回类型

np.ndarray\[浮点数\]

提高

**ValueError** – 当`point`和 控制点具有不同形状时。

Quadratic*bezier_remap (*三元组*, \_new_number_of_curves* )[\[来源\]](../_modules/manim/utils/bezier.html#quadratic_bezier_remap)[#](#manim.utils.bezier.quadratic_bezier_remap "此定义的固定链接")

通过分割贝塞尔曲线将曲线数量重新映射到更高的数量

参数

- **Triplets** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _\]_ _\]_ ) – 要重新映射的二次贝塞尔曲线的三元组 shape(n, 3, 3)
- **new_number_of_curves** ( _int_ ) – 输出将包含的曲线数量。这需要高于当前的数字。

返回类型

二次贝塞尔曲线的新三元组。

split*quadratic_bezier (*点*, \_t* )[\[来源\]](../_modules/manim/utils/bezier.html#split_quadratic_bezier)[#](#manim.utils.bezier.split_quadratic_bezier "此定义的固定链接")

将参数处的二次贝塞尔曲线拆分`t`为两条二次曲线。

参数

- **点**( _ndarray_ ) – 贝塞尔曲线的控制点具有形状`[a1, h1, b1]`
- **t** ( _float_ ) –`t`分割贝塞尔曲线的值

退货

- _作为元组列表的两条贝塞尔曲线，_
- 有形状`[a1, h1, b1], [a2, h2, b2]`

返回类型

_ndarray_

subdivide*quadratic_bezier (*点*, \_n* )[\[来源\]](../_modules/manim/utils/bezier.html#subdivide_quadratic_bezier)[#](#manim.utils.bezier.subdivide_quadratic_bezier "此定义的固定链接")

将二次贝塞尔曲线细分为`n`具有相同形状的子曲线。

曲线分割点位于参数处 t=i/n 为了 i=1,...,n−1。

参数

- **points** ( _Iterable_ _\[_ _float_ _\]_ ) – 形式中贝塞尔曲线的控制点`[a1, h1, b1]`
- **n** ( _int_ ) – 将贝塞尔曲线细分为的曲线数

返回类型

贝塞尔曲线的新点的形式`[a1, h1, b1, a2, h2, b2, ...]`

![../_images/bezier_subdivision_example.png](../_images/bezier_subdivision_example.png)