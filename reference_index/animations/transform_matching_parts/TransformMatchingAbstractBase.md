# TransformMatchingAbstractBase

合格名称：`manim.animation.transform\_matching\_parts.TransformMatchingAbstractBase`

```py
class TransformMatchingAbstractBase(mobject=None, *args, use_override=True, **kwargs)
```

Bases: AnimationGroup

用于跟踪匹配部分的转换的抽象基类。

子类必须实现两个静态方法 `get_mobject_parts()`和 `get_mobject_key()`。

基本上，此转换首先`get_mobject_parts`通过应用该 `get_mobject_key`方法将该方法返回的所有子对象映射到某些键。然后，具有匹配键的子对象相互转换。

参数

- **mobject** – 起始[`Mobject`]().
- **target_mobject** – 目标[`Mobject`]()。
- **transform_mismatches** – 控制没有匹配键的子对象是否使用 相互转换[`Transform`]()。默认值：`False`.
- **fade_transform_mismatches** – 控制没有匹配键的子对象是否使用 相互转换[`FadeTransform`]()。默认值：`False`.
- **key_map** – 可选。将属于某些起始 mobject 的子对象的键（即方法的返回值`get_mobject_key`）映射到属于目标 mobject 的子对象的某些键的字典，尽管键不匹配，但仍应进行转换。
- **kwargs** – 所有其他关键字参数都传递给子对象转换。

笔记

如果 和 均未`transform_mismatches`设置`fade_transform_mismatches` 为`True`，则起始对象中不匹配键的子对象将从目标对象中不匹配的子对象的方向淡出，目标对象中不匹配的子对象将从起始对象中不匹配的子对象的方向淡入对象。

方法

|||
|-|-|
[`clean_up_from_scene`]()|[`Scene`]()完成动画后清理。
`get_mobject_key`|
`get_mobject_parts`|
`get_shape_map`|


clean_up_from*scene（*场景\_）

[`Scene`]()完成动画后清理。

如果动画是移除器，则这包括[`remove()`]()动画 [`Mobject`]()。

参数

**scene** ( [_Scene_]() ) – 应清除动画的场景。

返回类型

没有任何
