# 对象表

合格名称：`manim.mobject.table.MobjectTable`


```py

```

[`Table`](manim.mobject.table.Table.html#manim.mobject.table.Table "manim.mobject.table.Table")与 一起使用的专用对象[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

例子

示例：MobjectTableExample 

![../_images/MobjectTableExample-1.png](../_images/MobjectTableExample-1.png)

```py

```


[`Table`](manim.mobject.table.Table.html#manim.mobject.table.Table "manim.mobject.table.Table")with`element_to_mobject`设置为恒等函数的特殊情况。在这里， 中的每一项都`table`必须已经是类型[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

参数

- **table** ( _Iterable_ _\[_ _Iterable_ _\[_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _\]_ ) – 2D 数组或列表列表。表的内容必须是类型[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。
- **element_to_mobject** ( _Callable_ _\[_ _\[_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ _,_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ ) –[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")应用于表条目的类。设置为返回自身。`lambda m : m`
- **kwargs** – 要传递给 的附加参数[`Table`](manim.mobject.table.Table.html#manim.mobject.table.Table "manim.mobject.table.Table")。

方法

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
