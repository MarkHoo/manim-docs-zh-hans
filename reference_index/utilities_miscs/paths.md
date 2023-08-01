# 路径

确定点集之间的变换路径的函数。

功能

顺时针路径( )

该函数通过顺时针移动半圆来变换每个点。

例子

示例：ClockwisePath 示例

```py

```

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

逆时针路径( )

该函数通过逆时针移动半圆来变换每个点。

例子

示例：逆时针路径示例

```py

```

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

path*along_arc ( \_arc_angle* , _axis = array(\[0., 0., 1.\])_ )

该函数通过沿圆弧移动每个点来变换每个点。

参数

- **arc_angle** ( _float_ ) – 每个点绕圆弧移动的角度。
- **axis** ( _ndarray_ ) – 旋转轴。

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

例子

示例：PathAlongArcExample 

```py

```

path*along_circles ( \_arc_angle* , _Circles_centers_ , _axis = array(\[0., 0., 1.\])_ )

该函数通过沿着圆大致移动每个点来变换每个点，每个点都有自己指定的中心。

该路径可以被视为每个点从起始位置到目的地平滑地改变其轨道。

参数

- **arc_angle** ( _float_ ) – 每个点围绕拟圆穿过的角度。
- **Circles_centers** ( _ndarray_ ) – 每个点旋转的拟圆的中心。
- **axis** ( _ndarray_ ) – 旋转轴。

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

例子

示例：PathAlongCircles 示例

```py

```

螺旋路径(_角度_,_轴= array(\[0., 0., 1.\])_ )

该函数通过沿着螺旋线移动到目的地来变换每个点。

参数

- **angle** ( _float_ ) – 每个点绕螺旋线移动的角度。
- **axis** ( _ndarray_ ) – 旋转轴。

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]

例子

示例：SpiralPathExample 

```py

```


直路径( _\* args_ )

最简单的路径函数。集合中的每个点都沿着一条直线路径到达目的地。

例子

示例：StraightPath 示例

```py

```

返回类型

_可调用_\[\[ _ndarray_ , _ndarray_ , float\], _ndarray_ \]
