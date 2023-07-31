# VDict

合格名称：`manim.mobject.types.vectorized\_mobject.VDict`

VDict*类*（_mapping_or_iterable = {}_， _show_keys = False_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VDict)[#](#manim.mobject.types.vectorized_mobject.VDict "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

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

from manim import \*

class ShapesWithVDict(Scene):
def construct(self):
square = Square().set_color(RED)
circle = Circle().set_color(YELLOW).next_to(square, UP)

        \# create dict from list of tuples each having key-mobject pair
        pairs = \[("s", square), ("c", circle)\]
        my_dict = VDict(pairs, show_keys=True)

        \# display it just like a VGroup
        self.play(Create(my_dict))
        self.wait()

        text = Tex("Some text").set_color(GREEN).next_to(square, DOWN)

        \# add a key-value pair by wrapping it in a single-element list of tuple
        \# after attrs branch is merged, it will be easier like `.add(t=text)`
        my_dict.add(\[("t", text)\])
        self.wait()

        rect = Rectangle().next_to(text, DOWN)
        \# can also do key assignment like a python dict
        my_dict\["r"\] = rect

        \# access submobjects like a python dict
        my_dict\["t"\].set_color(PURPLE)
        self.play(my_dict\["t"\].animate.scale(3))
        self.wait()

        \# also supports python dict styled reassignment
        my_dict\["t"\] = Tex("Some other text").set_color(BLUE)
        self.wait()

        \# remove submobject by key
        my_dict.remove("t")
        self.wait()

        self.play(Uncreate(my_dict\["s"\]))
        self.wait()

        self.play(FadeOut(my_dict\["c"\]))
        self.wait()

        self.play(FadeOut(my_dict\["r"\], shift=DOWN))
        self.wait()

        \# you can also make a VDict from an existing dict of mobjects
        plain_dict = {
            1: Integer(1).shift(DOWN),
            2: Integer(2).shift(2 * DOWN),
            3: Integer(3).shift(3 * DOWN),
        }

        vdict\_from\_plain_dict = VDict(plain_dict)
        vdict\_from\_plain_dict.shift(1.5 * (UP + LEFT))
        self.play(Create(vdict\_from\_plain_dict))

        \# you can even use zip
        vdict\_using\_zip = VDict(zip(\["s", "c", "r"\], \[Square(), Circle(), Rectangle()\]))
        vdict\_using\_zip.shift(1.5 * RIGHT)
        self.play(Create(vdict\_using\_zip))
        self.wait()

Copy to clipboard

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

square_obj = Square()
self.add_key_value_pair('s', square_obj)

Copy to clipboard

获取所有子对象( )[\[来源\]](../_modules/manim/mobject/types/vectorized_mobject.html#VDict.get_all_submobjects)[#](#manim.mobject.types.vectorized_mobject.VDict.get_all_submobjects "此定义的固定链接")

获取与特定[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")对象关联的所有子对象

退货

[`VDict`](#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")与该对象关联的所有子对象

返回类型

`dict_values`

例子

正常使用：

for submob in my_dict.get_all_submobjects():
self.play(Create(submob))

Copy to clipboard

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

my_dict.remove('square')

Copy to clipboard
