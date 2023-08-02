# VDict

合格名称：`manim.mobject.types.vectorized\_mobject.VDict`


```py

```

类似 VGroup 的类，还提供通过键访问子对象的功能，如 python 字典

参数

- **mapping_or_iterable** ( _Mapping_ _\[_ _Hashable_ _,_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _|_ _Iterable_ _\[_ _tuple_ _\[_ _Hashable_ _,_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _\]_ ) – 指定键和 mobject 的键值映射的参数。
- **show_keys** ( _bool_ ) – 是否还显示与 mobject 关联的键。这在调试时可能很有用，特别是当 [`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict"). 默认为 False。
- **kwargs** – 要传递给 Mobject 的其他参数。

显示键[#](#manim.mobject.types.vectorized_mobject.VDict.show_keys "此定义的固定链接")

是否还显示与 mobject 关联的键。这在调试时可能很有用，特别是当 [`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict"). 显示时，关键点位于对象的左侧。默认为 False。

类型

`bool`

submob_dict [#](#manim.mobject.types.vectorized_mobject.VDict.submob_dict "此定义的固定链接")

是用于将键绑定到 mobject 的实际 Python 字典。

类型

`dict`

例子

示例：ShapesWithVDict [¶](#shapeswithvdict)

```py

```


方法

[`add`](#manim.mobject.types.vectorized_mobject.VDict.add "manim.mobject.types.vectorized_mobject.VDict.add")

将键值对添加到[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")对象。

[`add_key_value_pair`](#manim.mobject.types.vectorized_mobject.VDict.add_key_value_pair "manim.mobject.types.vectorized_mobject.VDict.add_key_value_pair")

[`add()`](#manim.mobject.types.vectorized_mobject.VDict.add "manim.mobject.types.vectorized_mobject.VDict.add")用于将键值对添加到 的实用程序函数[`submob_dict`](#manim.mobject.types.vectorized_mobject.VDict.submob_dict "manim.mobject.types.vectorized_mobject.VDict.submob_dict")。

[`get_all_submobjects`](#manim.mobject.types.vectorized_mobject.VDict.get_all_submobjects "manim.mobject.types.vectorized_mobject.VDict.get_all_submobjects")

获取与特定[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")对象关联的所有子对象

[`remove`](#manim.mobject.types.vectorized_mobject.VDict.remove "manim.mobject.types.vectorized_mobject.VDict.remove")

[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")从具有 key key 的对象中删除 mobject

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

添加（_映射或可迭代_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VDict.add)[#](#manim.mobject.types.vectorized_mobject.VDict.add "此定义的固定链接")

将键值对添加到[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")对象。

此外，它在内部将值添加到 的子对象 中，该子对象负责实际的屏幕显示。`list`[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

参数

**mapping_or_iterable** ( _Mapping_ _\[_ _Hashable_ _,_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _|_ _Iterable_ _\[_ _tuple_ _\[_ _Hashable_ _,_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _\]_ ) – 指定键和 mobject 的键值映射的参数。

退货

返回[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")调用此方法的对象。

返回类型

[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")

例子

正常使用：

square_obj = Square()
my_dict.add(\[('s', square_obj)\])

Copy to clipboard

添加键值对（_键_，_值_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VDict.add_key_value_pair)[#](#manim.mobject.types.vectorized_mobject.VDict.add_key_value_pair "此定义的固定链接")

[`add()`](#manim.mobject.types.vectorized_mobject.VDict.add "manim.mobject.types.vectorized_mobject.VDict.add")用于将键值对添加到 的实用程序函数[`submob_dict`](#manim.mobject.types.vectorized_mobject.VDict.submob_dict "manim.mobject.types.vectorized_mobject.VDict.submob_dict")。并不是真正要在外部使用。

参数

- **key** ( _Hashable_ ) – 要添加的子对象的键。
- **value** ( [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) – 与键关联的 mobject

返回类型

没有任何

提高

**TypeError** – 如果值不是 VMobject 的实例

例子

正常使用：


```py

```


获取所有子对象( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VDict.get_all_submobjects)[#](#manim.mobject.types.vectorized_mobject.VDict.get_all_submobjects "此定义的固定链接")

获取与特定[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")对象关联的所有子对象

退货

[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")与该对象关联的所有子对象

返回类型

`dict_values`

例子

正常使用：


```py

```

删除（_键_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VDict.remove)[#](#manim.mobject.types.vectorized_mobject.VDict.remove "此定义的固定链接")

[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")从具有 key key 的对象中删除 mobject

此外，它在内部从的子对象 中删除该对象（负责将其从屏幕上删除）`list`[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

参数

**key** ( _Hashable_ ) – 要删除的子对象的键。

退货

返回[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")调用此方法的对象。

返回类型

[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")

例子

正常使用：


```py

```
