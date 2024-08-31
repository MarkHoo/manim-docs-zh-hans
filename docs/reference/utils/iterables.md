# 可迭代

对可迭代对象的操作。

Functions

`adjacent_n_tuples(objects, n)`

返回循环分割成 n 个长度元组的 Sequence 对象。

> 也可以看看

> [`adjacent_pairs`]()

> 		alias with n=2

例子

正常使用：


```py
list(adjacent_n_tuples([1, 2, 3, 4], 2))
# returns [(1, 2), (2, 3), (3, 4), (4, 1)]

list(adjacent_n_tuples([1, 2, 3, 4], 3))
# returns [(1, 2, 3), (2, 3, 4), (3, 4, 1), (4, 1, 2)]
```


参数

- **objects**（_Sequence_）-
- **n** (_int_) –

返回类型

zip


`adjacent_pairs(objects)`

别名为`adjacent_n_tuples(objects, 2)`

> 也可以看看

> [`adjacent_n_tuples`]()

例子

正常使用：

```py
list(adjacent_pairs([1, 2, 3, 4]))
# returns [(1, 2), (2, 3), (3, 4), (4, 1)]
```

参数

**objects**（_Sequence_）-

返回类型

zip


`all_elements_are_instances(iterable, Class)`

`True`如果 iterable 的所有元素都是 Class 的实例，则返回。否则为假。

参数

**iterable**（_Iterable_）–

返回类型

bool


`batch_by_property(items, property_func)`

接受一个序列，并返回一个元组列表，(batch, prop)，这样当放入 Callable property_func 时，批次中的所有项目都具有相同的输出，并且将所有这些批次链接在一起将给出原始序列（即顺序被保留）。

例子

正常使用：


```py
batch_by_property([(1, 2), (3, 4), (5, 6, 7), (8, 9)], len)
# returns [([(1, 2), (3, 4)], 2), ([(5, 6, 7)], 3), ([(8, 9)], 2)]
```


参数

- **items**（_Sequence_）–
- **property_func**（_Callable_）–

返回类型

list[tuple[list, Any]]


`concatenate_lists(*list_of_lists)`

将作为参数提供的 Iterables 合并到一个列表中。

例子

正常使用：

```py
concatenate_lists([1, 2], [3, 4], [5])
# returns [1, 2, 3, 4, 5]
```

参数

**list_of_lists** (_Iterable_) –

返回类型

list


`hash_obj(obj)`

确定哈希值，甚至是潜在可变对象的哈希值。

参数

**obj**（_object_）–

返回类型

int


`list_difference_update(l1, l2)`

返回一个列表，其中包含 l1 中不在 l2 中的所有元素。

例子

正常使用：

```py
list_difference_update([1, 2, 3, 4], [2, 4])
# returns [1, 3]
```


参数

- **l1**（_Iterable_）–
- **l2**（_Iterable_）–

返回类型

list


`list_update(l1, l2)`

用来代替`set.update()`维持秩序，

确保从 l1 而非 l2 中删除重复项。删除 l1 和 l2 的重叠，然后将 l2 保持不变连接。

例子

正常使用：

```py
list_update([1, 2, 3], [2, 4, 4])
# returns [1, 3, 2, 4, 4]
```


参数

- **l1**（_Iterable_）–
- **l2**（_Iterable_）–

返回类型

list


`listify(obj)`

智能地将 obj 转换为列表。

例子

正常使用：

```py
listify('str')   # ['str']
listify((1, 2))  # [1, 2]
listify(len)     # [<built-in function len>]
```


返回类型

list


`make_even(iterable_1, iterable_2)`

扩展具有重复值的两个迭代中较短的一个，直到其

长度等于较长的可迭代对象（有利于较早的元素）。

> 也可以看看

> [`make_even_by_cycling`]()

> 	循环元素而不是偏爱较早的元素

例子

正常使用：

```py
make_even([1, 2], [3, 4, 5, 6])
([1, 1, 2, 2], [3, 4, 5, 6])

make_even([1, 2], [3, 4, 5, 6, 7])
# ([1, 1, 1, 2, 2], [3, 4, 5, 6, 7])
```

参数

- **iterable_1** (_Iterable_) –
- **iterable_2** (_Iterable_) –

返回类型

tuple[list, list]


`make_even_by_cycling(iterable_1, iterable_2)`

扩展具有重复值的两个迭代中较短的一个，直到其

长度等于较长的迭代（在较短的迭代上循环）。

> 也可以看看

> [`make_even`]()

> 	偏爱较早的元素而不是循环它们


例子

正常使用：

```py
make_even_by_cycling([1, 2], [3, 4, 5, 6])
([1, 2, 1, 2], [3, 4, 5, 6])

make_even_by_cycling([1, 2], [3, 4, 5, 6, 7])
# ([1, 2, 1, 2, 1], [3, 4, 5, 6, 7])
```


参数

- **iterable_1**（_Collection_）-
- **iterable_2**（_Collection_）-

返回类型

tuple[list, list]


`remove_list_redundancies(lst)`

用于代替`list(set(l))`维持秩序。保留每个元素的最后一次出现。

参数

**lst**（_Reversible_）–

返回类型

list


`remove_nones(sequence)`

删除 bool(x) 计算结果为 False 的元素。

例子

正常使用：

```py
remove_nones(['m', '', 'l', 0, 42, False, True])
# ['m', 'l', 42, True]
```

参数

**sequence**（_Iterable_）–

返回类型

list


`resize_array(nparray, length)`

扩展/截断 nparray 以便.`len(result) == length`

循环 nparray 的元素以达到所需的长度。

> 也可以看看

> [`resize_preserving_order`]()

> 	偏爱较早的元素而不是循环它们

> [`make_even_by_cycling`]()

>	平衡 2 个迭代的类似循环行为

例子

正常使用：

```py
points = np.array([[1, 2], [3, 4]])
resize_array(points, 1)
array([[1, 2]])
resize_array(points, 3)
array([[1, 2],
       [3, 4],
       [1, 2]])
resize_array(points, 2)
array([[1, 2],
       [3, 4]])
```


参数

- **nparray** ( _ndarray_ ) –
- **length**( _int_ ) –

返回类型

_ndarray_


`resize_preserving_order(nparray, length)`

扩展/截断 nparray 以便.`len(result) == length`

复制 nparray 的元素以达到所需的长度（有利于较早的元素）。

如果 nparray 为空，则构造一个长度为零的数组。

> 也可以看看

> [`resize_array`]()

> 循环元素而不是偏爱较早的元素

> [`make_even`]()

> 平衡 2 个迭代的类似早期偏好行为


例子

正常使用：

```py
resize_preserving_order(np.array([]), 5)
# np.array([0., 0., 0., 0., 0.])

nparray = np.array([[1, 2],
                    [3, 4]])

resize_preserving_order(nparray, 1)
# np.array([[1, 2]])

resize_preserving_order(nparray, 3)
# np.array([[1, 2],
#           [1, 2],
#           [3, 4]])
```


参数

- **nparray** ( _ndarray_ ) –
- **length**( _int_ ) –

返回类型

_ndarray_


`resize_with_interpolation(nparray, length)`

扩展/截断 nparray 以便.`len(result) == length`

插入新元素以达到所需的长度。

请注意，如果 nparray 的长度发生变化，其数据类型也可能发生变化（例如 int -> float：请参阅示例）

> 也可以看看

> [`resize_array`]()

> 循环元素而不是插值

> [`resize_preserving_order`]()

> 倾向于较早的元素而不是插值

例子

正常使用：

```py
nparray = np.array([[1, 2],
                    [3, 4]])

resize_with_interpolation(nparray, 1)
# np.array([[1., 2.]])

resize_with_interpolation(nparray, 4)
# np.array([[1.        , 2.        ],
#           [1.66666667, 2.66666667],
#           [2.33333333, 3.33333333],
#           [3.        , 4.        ]])

nparray = np.array([[[1, 2],[3, 4]]])
resize_with_interpolation(nparray, 3)
# np.array([[[1., 2.], [3., 4.]],
#           [[1., 2.], [3., 4.]],
#           [[1., 2.], [3., 4.]]])

nparray = np.array([[1, 2], [3, 4], [5, 6]])
resize_with_interpolation(nparray, 4)
# np.array([[1.        , 2.        ],
#           [2.33333333, 3.33333333],
#           [3.66666667, 4.66666667],
#           [5.        , 6.        ]])

nparray = np.array([[1, 2], [3, 4], [1, 2]])
resize_with_interpolation(nparray, 4)
# np.array([[1.        , 2.        ],
#           [2.33333333, 3.33333333],
#           [2.33333333, 3.33333333],
#           [1.        , 2.        ]])
```


参数

- **nparray** ( _ndarray_ ) –
- **length**( _int_ ) –

返回类型

_ndarray_


`stretch_array_to_length(nparray, length)`

参数

- **nparray** ( _ndarray_ ) –
- **length**( _int_ ) –

返回类型

_ndarray_


`tuplify(obj)`

智能地将 obj 转换为元组。

例子

正常使用：

```py
tuplify('str')   # ('str',)
tuplify([1, 2])  # (1, 2)
tuplify(len)     # (<built-in function len>,)
```

返回类型

tuple


`uniq_chain(*args)`

返回一个生成器，生成 Iterables 的所有唯一元素

按提供的顺序通过 args 提供。

例子

正常使用：

```py
uniq_chain([1, 2], [2, 3], [1, 4, 4])
# yields 1, 2, 3, 4
```


参数

**args**（_Iterable_）-

返回类型

_Generator_
