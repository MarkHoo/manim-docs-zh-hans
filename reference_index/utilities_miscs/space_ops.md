# 空间操作

二维和三维向量的效用函数。

功能

R3*to_complex（*点\_）

参数

**点**(_序列\_\_\[_ _float_ _\]_ ) –

返回类型

_ndarray_

来自四元数的角度轴（_四元数_）

从四元数获取角度和轴。

参数

**四元数**( _Sequence_ _\[_ _float_ _\]_ ) – 我们从中获取角度和轴的四元数。

退货

给出角度和轴

返回类型

序列\[浮点数\]

向量之间的角度( _v1_ , _v2_ )

返回两个向量之间的角度。这个角度总是在 0 和 pi 之间

参数

- **v1** ( _ndarray_ ) – 第一个向量。
- **v2** ( _ndarray_ ) – 第二个向量。

退货

向量之间的角度。

返回类型

漂浮

向量角度（_向量_）

当向量投影到 xy 平面上时，返回极坐标 theta。

参数

**vector** ( _Sequence_ _\[_ _float_ _\]_ _|_ _np.ndarray_ ) – 要查找角度的向量。

退货

投影矢量的角度。

返回类型

漂浮

笛卡尔到球面( _vec_ )

返回与每个极坐标值（距离、phi、theta）相对应的数字数组。

参数

**vec** ( _Sequence_ _\[_ _float_ _\]_ ) – 一个 numpy 数组。`[x, y, z]`

返回类型

_ndarray_

质量中心（_点_）

获取空间中点的质心。

参数

**点**( _Sequence_ _\[_ _float_ _\]_ ) – 用于查找质心的点。

退货

点的质心。

返回类型

np.ndarray

compass*directions ( \_n = 4* , _start_vect = array(\[1., 0., 0.\])_ )

使用 tau 查找基本方向。

参数

- **n** ( _int_ ) – 要旋转的数量，默认为 4
- **start_vect** ( _ndarray_ ) – 角度起始方向，默认为 RIGHT

退货

已旋转的角度。

返回类型

np.ndarray

complex*func_to_R3_func ( \_complex_func* )

复杂*至\_R3 (*复杂*编号*)

参数

**复杂数**（_复杂_）-

返回类型

_ndarray_

cross2d ( _a_ , _b_ )

Earclip*triangulation（*顶点*， \_ring_ends*）

返回给出多边形三角剖分的索引列表，可能带有孔。

参数

- **verts** ( _ndarray_ ) – verts 是一个 numpy 点数组。
- **ring_ends** ( _list_ ) –ring_ends 是一个索引列表，指示新路径的终点在哪里。

退货

给出多边形三角剖分的索引列表。

返回类型

列表

find*intersection ( \_p0s* , _v0s_ , _p1s_ , _v1s_ ,_阈值= 1e-05_ )

返回沿方向 v0 穿过 p0 的直线与沿方向 v1 穿过 p1 的直线的交点（或此类点/方向数组的交点数组）。对于 3d 值，它返回射线 p0 + v0 _ t 上最接近射线 p1 + v1 _ t 的点

参数

- **p0s** (_序列\_\_\[_ _ndarray_ _\]_ ) –
- **v0s** (_序列\_\_\[_ _ndarray_ _\]_ ) –
- **p1s** (_序列\_\_\[_ _ndarray_ _\]_ ) –
- **v1s** (_序列\_\_\[_ _ndarray_ _\]_ ) –
- **阈值**（_浮动_）–

返回类型

_序列_\[ _ndarray_ \]

get*unit_normal ( \_v1* , _v2_ , _tol = 1e-06_ )

获取向量的单位法线。

参数

- **v1** ( _ndarray_ ) – 第一个向量。
- **v2** ( _ndarray_ ) – 第二个向量
- **tol** ( _float_ ) – \[描述\]，默认为 1e-6

退货

两个向量的法线。

返回类型

np.ndarray

get*winding_number（*点\_）

确定多边形绕原点缠绕的次数。

方向以数学正向测量，即逆时针方向。

参数

**points** ( _Sequence_ _\[_ _ndarray_ _\]_ ) – 正在查询的多边形的顶点。

返回类型

漂浮

例子

> > \> from manim import Square, get_winding_number
> > \> polygon = Square()
> > \> get_winding_number(polygon.get_vertices())
> > 1.0
> > \> polygon.shift(2\*UP)
> > Square
> > \> get_winding_number(polygon.get_vertices())
> > 0.0

Copy to clipboard

线交点(_线 1_ ,_线 2_ )

返回两条线的交点，每条线由线上的一对不同点定义。

参数

- **line1** ( _Sequence_ _\[_ _ndarray_ _\]_ ) – 确定第一条线的两个点的列表。
- **line2** ( _Sequence_ _\[_ _ndarray_ _\]_ ) – 确定第二条线的两个点的列表。

退货

相交的两条线的交点。

返回类型

np.ndarray

提高

**ValueError** – 如果两条线不相交或者坐标不在 xy 平面上，则会产生错误。

中点（_点 1_、_点 2_）

获取两点的中点。

参数

- **point1** ( _Sequence_ _\[_ _float_ _\]_ ) – 第一个点。
- **point2** ( _Sequence_ _\[_ _float_ _\]_ ) – 第二个点。

退货

点的中点

返回类型

[联合]()\[浮点数，np.ndarray\]

范数平方( _v_ )

参数

**v**（_浮动_）–

返回类型

漂浮

标准化（_vect_， _fall_back = None_）

参数

**vect** ( _np.ndarray_ _|**元组**\[_ _float_ _\]_ ) –

返回类型

np.ndarray

Normalize*along_axis（*数组*，\*轴\_）

使用提供的轴标准化数组。

参数

- **array** ( _ndarray_ ) – 必须标准化的数组。
- **axis** ( _ndarray_ ) – 要标准化的轴。

退货

已根据轴标准化的数组。

返回类型

np.ndarray

垂直二分线(_线_,_范数向量=数组(\[0., 0., 1.\])_ )

返回两个点的列表，这些点对应于给定两个点的垂直平分线的端点。

参数

- **line** ( _Sequence_ _\[_ _ndarray_ _\]_ ) – 两个 numpy 数组点的列表（对应于线的末端）。
- **norm_vector** – 垂直于给定直线和垂直平分线的向量。

退货

对应于垂直平分线两端的两个 numpy 数组点的列表

返回类型

列表

四元数共轭（_四元数_）

用于求四元数的共轭

参数

**四元数**( _Sequence_ _\[_ _float_ _\]_ ) – 要查找其共轭的四元数。

退货

四元数的共轭。

返回类型

np.ndarray

quaternion_from_angle*axis (*角度*,*轴*, \_axis_normalized = False* )

从角度和轴获取四元数。欲了解更多信息，请查看[此维基百科页面](https://en.wikipedia.org/wiki/Conversion_between_quaternions_and_Euler_angles)。

参数

- **angle** ( _float_ ) – 四元数的角度。
- **axis** ( _np.ndarray_ ) – 四元数的轴
- **axis_normalized** ( _bool_ ) – 检查轴是否标准化，默认为 False

退货

从角度和轴返回一个四元数

返回类型

列表\[浮动\]

quaternion*mult ( *\\*四元数\_)

获取所提供的四元数的汉密尔顿积。欲了解更多信息，请查看[此维基百科页面](https://en.wikipedia.org/wiki/Quaternion)。

退货

返回两个四元数的乘积列表。

返回类型

[联合]()\[np.ndarray，列表\[[联合]()\[浮点，np.ndarray\]\]\]

参数

**quats** (_序列\_\_\[_ _float_ _\]_ ) –

常规顶点（_n_， _\*_，_半径= 1_，_起始角度=无_）

围绕以原点为圆心的圆生成规则间隔的顶点。

参数

- **n** ( _int_ ) – 顶点数
- **radius** ( _float_ ) – 顶点所在圆的半径。
- **起始角度**（_浮点数**|**无_）–

  顶点开始的角度。

  如果未指定，则将使用偶`n`数值。`0`对于奇`n`数值，使用 90 度。

退货

- **vertices** ( `numpy.ndarray`) – 规则间隔的顶点。
- **start_angle** ( `float`) – 顶点开始的角度。

返回类型

元组\[np.ndarray，浮点数\]

旋转向量(_向量_,_角度_,_轴= array(\[0., 0., 1.\])_ )

旋转向量的函数。

参数

- **vector** ( _ndarray_ ) – 要旋转的向量。
- **angle** ( _float_ ) – 要旋转的角度。
- **axis** ( _ndarray_ ) – 要旋转的轴，默认为 OUT

退货

具有提供的角度和轴的旋转矢量。

返回类型

np.ndarray

提高

**ValueError** – 如果向量的维度不是 2 或 3。

旋转*关于\_z（*角度\_）

返回给定角度的旋转矩阵。

参数

**angle** ( _float_ ) – 旋转矩阵的角度。

退货

返回旋转后的矩阵。

返回类型

np.ndarray

旋转矩阵（_角度_，_轴_，_齐次= False_）

绕指定旋转轴以 R^3 旋转。

参数

- **角度**（_浮动_）–
- **轴**( _ndarray_ ) –
- **同质**( _bool_ ) –

返回类型

_ndarray_

旋转矩阵来自四元数( _quat_ )

参数

**季铵盐**( _ndarray_ ) –

返回类型

_ndarray_

旋转矩阵转置（_角度_，_轴_）

参数

- **角度**（_浮动_）–
- **轴**( _ndarray_ ) –

返回类型

_ndarray_

rotation*matrix_transpose_from_quaternion (*四元数\_)

将四元数 quat 转换为等效的旋转矩阵表示形式。欲了解更多信息，请查看[此页面](https://in.mathworks.com/help/driving/ref/quaternion.rotmat.html)。

参数

**quat** ( _np.ndarray_ ) – 要转换的四元数。

退货

返回旋转矩阵表示形式，以 3×3 矩阵或 3×3×N 多维数组形式返回。

返回类型

列表\[np.ndarray\]

鞋带（_x_y_）

鞋带公式的二维实现。

退货

返回签名区域。

返回类型

`float`

参数

**x_y** ( _ndarray_ ) –

鞋带方向( _x_y_ )

使用鞋带法确定的面积来确定输入点集的方向是顺时针还是逆时针。

退货

要么`"CW"`要么`"CCW"`.

返回类型

`str`

参数

**x_y** ( _ndarray_ ) –

spherical*to_cartesian（*球形\_）

根据给定的球面坐标返回 numpy 数组。`[x, y, z]`

参数

**球形**(_序列\_\_\[_ _float_ _\]_ ) –

三个浮点数的列表，对应于以下内容：

r - 点与原点之间的距离。

theta - 点与 x 轴正方向的方位角。

phi - 点与 z 轴正方向的垂直角度。

返回类型

_ndarray_

厚对角线（_暗淡_，_厚度= 2_）

参数

**暗淡**（_int_） –

返回类型

_ndarray_

z*to_vector（*向量\_）

返回 SO(3) 中的某个矩阵，该矩阵将 z 轴设为作为参数提供的（归一化）向量

参数

**向量**( _ndarray_ ) –

返回类型

_ndarray_
