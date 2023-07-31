# 可迭代[#](#module-manim.utils.iterables "此标题的固定链接")

对可迭代对象的操作。

功能

相邻\_n\_元组（_对象_， _n_）[\[来源\]](../_modules/manim/utils/iterables.html#adjacent_n_tuples)[#](#manim.utils.iterables.adjacent_n_tuples "此定义的固定链接")

返回循环分割成 n 个长度元组的 Sequence 对象。

也可以看看

[`adjacent_pairs`](#manim.utils.iterables.adjacent_pairs "manim.utils.iterables.adjacent_pairs")

n=2 的别名

例子

正常使用：

list(adjacent_n_tuples(\[1, 2, 3, 4\], 2))
\# returns \[(1, 2), (2, 3), (3, 4), (4, 1)\]

list(adjacent_n_tuples(\[1, 2, 3, 4\], 3))
\# returns \[(1, 2, 3), (2, 3, 4), (3, 4, 1), (4, 1, 2)\]

Copy to clipboard

参数

- **对象**（_序列_）-
- **n** (_整数_) –

返回类型

压缩

相邻对（_对象_）[\[来源\]](../_modules/manim/utils/iterables.html#adjacent_pairs)[#](#manim.utils.iterables.adjacent_pairs "此定义的固定链接")

别名为.`adjacent_n_tuples(objects, 2)`

也可以看看

[`adjacent_n_tuples`](#manim.utils.iterables.adjacent_n_tuples "manim.utils.iterables.adjacent_n_tuples")

例子

正常使用：

list(adjacent_pairs(\[1, 2, 3, 4\]))
\# returns \[(1, 2), (2, 3), (3, 4), (4, 1)\]

Copy to clipboard

参数

**对象**（_序列_）-

返回类型

压缩

all_elements_are*instances（*可迭代*，*类\_）[\[来源\]](../_modules/manim/utils/iterables.html#all_elements_are_instances)[#](#manim.utils.iterables.all_elements_are_instances "此定义的固定链接")

`True`如果 iterable 的所有元素都是 Class 的实例，则返回。否则为假。

参数

**可迭代**（_可迭代_）–

返回类型

布尔值

按属性批量（_项目_，_属性函数_）[\[来源\]](../_modules/manim/utils/iterables.html#batch_by_property)[#](#manim.utils.iterables.batch_by_property "此定义的固定链接")

接受一个序列，并返回一个元组列表，(batch, prop)，这样当放入 Callable property_func 时，批次中的所有项目都具有相同的输出，并且将所有这些批次链接在一起将给出原始序列（即顺序被保留）。

例子

正常使用：

batch_by_property(\[(1, 2), (3, 4), (5, 6, 7), (8, 9)\], len)
\# returns \[(\[(1, 2), (3, 4)\], 2), (\[(5, 6, 7)\], 3), (\[(8, 9)\], 2)\]

Copy to clipboard

参数

- **项目**（_序列_）–
- **property_func**（_可调用_）–

返回类型

列表\[元组\[列表，任意\]\]

concatenate*lists ( *\* list_of_lists\_ )[\[来源\]](../_modules/manim/utils/iterables.html#concatenate_lists)[#](#manim.utils.iterables.concatenate_lists "此定义的固定链接")

将作为参数提供的 Iterables 合并到一个列表中。

例子

正常使用：

concatenate_lists(\[1, 2\], \[3, 4\], \[5\])
\# returns \[1, 2, 3, 4, 5\]

Copy to clipboard

参数

**list_of_lists** (_可迭代_) –

返回类型

列表

hash*obj ( \_obj* )[\[来源\]](../_modules/manim/utils/iterables.html#hash_obj)[#](#manim.utils.iterables.hash_obj "此定义的固定链接")

确定哈希值，甚至是潜在可变对象的哈希值。

参数

**obj**（_对象_）–

返回类型

整数

列表差异更新（_l1_， _l2_）[\[来源\]](../_modules/manim/utils/iterables.html#list_difference_update)[#](#manim.utils.iterables.list_difference_update "此定义的固定链接")

返回一个列表，其中包含 l1 中不在 l2 中的所有元素。

例子

正常使用：

list_difference_update(\[1, 2, 3, 4\], \[2, 4\])
\# returns \[1, 3\]

Copy to clipboard

参数

- **l1**（_可迭代_）–
- **l2**（_可迭代_）–

返回类型

列表

列表更新（_l1_， _l2_）[\[来源\]](../_modules/manim/utils/iterables.html#list_update)[#](#manim.utils.iterables.list_update "此定义的固定链接")

用来代替`set.update()`维持秩序，

确保从 l1 而非 l2 中删除重复项。删除 l1 和 l2 的重叠，然后将 l2 保持不变连接。

例子

正常使用：

list_update(\[1, 2, 3\], \[2, 4, 4\])
\# returns \[1, 3, 2, 4, 4\]

Copy to clipboard

参数

- **l1**（_可迭代_）–
- **l2**（_可迭代_）–

返回类型

列表

列出( _obj_ )[\[来源\]](../_modules/manim/utils/iterables.html#listify)[#](#manim.utils.iterables.listify "此定义的固定链接")

智能地将 obj 转换为列表。

例子

正常使用：

listify('str') \# \['str'\]
listify((1, 2)) \# \[1, 2\]
listify(len) \# \[<built-in function len>\]

Copy to clipboard

返回类型

列表

make*even（*可迭代 1*，*可迭代 2\_）[\[来源\]](../_modules/manim/utils/iterables.html#make_even)[#](#manim.utils.iterables.make_even "此定义的固定链接")

扩展具有重复值的两个迭代中较短的一个，直到其

长度等于较长的可迭代对象（有利于较早的元素）。

也可以看看

[`make_even_by_cycling`](#manim.utils.iterables.make_even_by_cycling "manim.utils.iterables.make_even_by_cycling")

循环元素而不是偏爱较早的元素

例子

正常使用：

make_even(\[1, 2\], \[3, 4, 5, 6\])
(\[1, 1, 2, 2\], \[3, 4, 5, 6\])

make_even(\[1, 2\], \[3, 4, 5, 6, 7\])
\# (\[1, 1, 1, 2, 2\], \[3, 4, 5, 6, 7\])

Copy to clipboard

参数

- **iterable_1** (_可迭代_) –
- **iterable_2** (_可迭代_) –

返回类型

元组\[列表，列表\]

make*even_by*cycling ( \_iterable_1* , \_iterable_2* )[\[来源\]](../_modules/manim/utils/iterables.html#make_even_by_cycling)[#](#manim.utils.iterables.make_even_by_cycling "此定义的固定链接")

扩展具有重复值的两个迭代中较短的一个，直到其

长度等于较长的迭代（在较短的迭代上循环）。

也可以看看

[`make_even`](#manim.utils.iterables.make_even "manim.utils.iterables.make_even")

偏爱较早的元素而不是循环它们

例子

正常使用：

make_even_by_cycling(\[1, 2\], \[3, 4, 5, 6\])
(\[1, 2, 1, 2\], \[3, 4, 5, 6\])

make_even_by_cycling(\[1, 2\], \[3, 4, 5, 6, 7\])
\# (\[1, 2, 1, 2, 1\], \[3, 4, 5, 6, 7\])

Copy to clipboard

参数

- **iterable_1**（_集合_）-
- **iterable_2**（_集合_）-

返回类型

元组\[列表，列表\]

删除列表冗余（_lst_）[\[来源\]](../_modules/manim/utils/iterables.html#remove_list_redundancies)[#](#manim.utils.iterables.remove_list_redundancies "此定义的固定链接")

用于代替`list(set(l))`维持秩序。保留每个元素的最后一次出现。

参数

**lst**（_可逆_）–

返回类型

列表

删除*nones（*序列\_）[\[来源\]](../_modules/manim/utils/iterables.html#remove_nones)[#](#manim.utils.iterables.remove_nones "此定义的固定链接")

删除 bool(x) 计算结果为 False 的元素。

例子

正常使用：

remove_nones(\['m', '', 'l', 0, 42, False, True\])
\# \['m', 'l', 42, True\]

Copy to clipboard

参数

**序列**（_可迭代_）–

返回类型

列表

调整数组大小（_nparray_，_长度_）[\[来源\]](../_modules/manim/utils/iterables.html#resize_array)[#](#manim.utils.iterables.resize_array "此定义的固定链接")

扩展/截断 nparray 以便.`len(result) == length`

循环 nparray 的元素以达到所需的长度。

也可以看看

[`resize_preserving_order`](#manim.utils.iterables.resize_preserving_order "manim.utils.iterables.resize_preserving_order")

偏爱较早的元素而不是循环它们

[`make_even_by_cycling`](#manim.utils.iterables.make_even_by_cycling "manim.utils.iterables.make_even_by_cycling")

平衡 2 个迭代的类似循环行为

例子

正常使用：

> > \> points = np.array(\[\[1, 2\], \[3, 4\]\])
> > \> resize_array(points, 1)
> > array(\[\[1, 2\]\])
> > \> resize_array(points, 3)
> > array(\[\[1, 2\],
> > \[3, 4\],
> > \[1, 2\]\])
> > \> resize_array(points, 2)
> > array(\[\[1, 2\],
> > \[3, 4\]\])

Copy to clipboard

参数

- **nparray** ( _ndarray_ ) –
- **长度**( _int_ ) –

返回类型

_ndarray_

resize*preserving_order（\_nparray*，_长度_）[\[来源\]](../_modules/manim/utils/iterables.html#resize_preserving_order)[#](#manim.utils.iterables.resize_preserving_order "此定义的固定链接")

扩展/截断 nparray 以便.`len(result) == length`

复制 nparray 的元素以达到所需的长度（有利于较早的元素）。

如果 nparray 为空，则构造一个长度为零的数组。

也可以看看

[`resize_array`](#manim.utils.iterables.resize_array "manim.utils.iterables.resize_array")

循环元素而不是偏爱较早的元素

[`make_even`](#manim.utils.iterables.make_even "manim.utils.iterables.make_even")

平衡 2 个迭代的类似早期偏好行为

例子

正常使用：

resize_preserving_order(np.array(\[\]), 5)
\# np.array(\[0., 0., 0., 0., 0.\])

nparray = np.array(\[\[1, 2\],
\[3, 4\]\])

resize_preserving_order(nparray, 1)
\# np.array(\[\[1, 2\]\])

resize_preserving_order(nparray, 3)
\# np.array(\[\[1, 2\],
\# \[1, 2\],
\# \[3, 4\]\])

Copy to clipboard

参数

- **nparray** ( _ndarray_ ) –
- **长度**( _int_ ) –

返回类型

_ndarray_

resize*with_interpolation（\_nparray*，_长度_）[\[来源\]](../_modules/manim/utils/iterables.html#resize_with_interpolation)[#](#manim.utils.iterables.resize_with_interpolation "此定义的固定链接")

扩展/截断 nparray 以便.`len(result) == length`

插入新元素以达到所需的长度。

请注意，如果 nparray 的长度发生变化，其数据类型也可能发生变化（例如 int -> float：请参阅示例）

也可以看看

[`resize_array`](#manim.utils.iterables.resize_array "manim.utils.iterables.resize_array")

循环元素而不是插值

[`resize_preserving_order`](#manim.utils.iterables.resize_preserving_order "manim.utils.iterables.resize_preserving_order")

倾向于较早的元素而不是插值

例子

正常使用：

nparray = np.array(\[\[1, 2\],
\[3, 4\]\])

resize_with_interpolation(nparray, 1)
\# np.array(\[\[1., 2.\]\])

resize_with_interpolation(nparray, 4)
\# np.array(\[\[1. , 2. \],
\# \[1.66666667, 2.66666667\],
\# \[2.33333333, 3.33333333\],
\# \[3\. , 4. \]\])

nparray = np.array(\[\[\[1, 2\],\[3, 4\]\]\])
resize_with_interpolation(nparray, 3)
\# np.array(\[\[\[1., 2.\], \[3., 4.\]\],
\# \[\[1., 2.\], \[3., 4.\]\],
\# \[\[1., 2.\], \[3., 4.\]\]\])

nparray = np.array(\[\[1, 2\], \[3, 4\], \[5, 6\]\])
resize_with_interpolation(nparray, 4)
\# np.array(\[\[1. , 2. \],
\# \[2.33333333, 3.33333333\],
\# \[3.66666667, 4.66666667\],
\# \[5\. , 6. \]\])

nparray = np.array(\[\[1, 2\], \[3, 4\], \[1, 2\]\])
resize_with_interpolation(nparray, 4)
\# np.array(\[\[1. , 2. \],
\# \[2.33333333, 3.33333333\],
\# \[2.33333333, 3.33333333\],
\# \[1\. , 2. \]\])

Copy to clipboard

参数

- **nparray** ( _ndarray_ ) –
- **长度**( _int_ ) –

返回类型

_ndarray_

拉伸数组到长度（_nparray_，_长度_）[\[来源\]](../_modules/manim/utils/iterables.html#stretch_array_to_length)[#](#manim.utils.iterables.stretch_array_to_length "此定义的固定链接")

参数

- **nparray** ( _ndarray_ ) –
- **长度**( _int_ ) –

返回类型

_ndarray_

元组化( _obj_ )[\[来源\]](../_modules/manim/utils/iterables.html#tuplify)[#](#manim.utils.iterables.tuplify "此定义的固定链接")

智能地将 obj 转换为元组。

例子

正常使用：

tuplify('str') \# ('str',)
tuplify(\[1, 2\]) \# (1, 2)
tuplify(len) \# (<built-in function len>,)

Copy to clipboard

返回类型

元组

uniq*chain ( *\*参数\_)[\[来源\]](../_modules/manim/utils/iterables.html#uniq_chain)[#](#manim.utils.iterables.uniq_chain "此定义的固定链接")

返回一个生成器，生成 Iterables 的所有唯一元素

按提供的顺序通过 args 提供。

例子

正常使用：

uniq_chain(\[1, 2\], \[2, 3\], \[1, 4, 4\])
\# yields 1, 2, 3, 4

Copy to clipboard

参数

**args**（_可迭代_）-

返回类型

_发电机_
