# 调试

调试实用程序。

功能

index*labels（\_mobject*， _label_height = 0.15_， _background_lines_width = 5_， _background_lines_color = '＃000000'_， _\*\* kwargs_）

返回 mobjects[`VGroup`]()的一个[`Integer`]()，显示每个子对象的索引。

对于处理复杂对象的部分很有用。

参数

- **mobject** ( [_Mobject_]() ) – 将为其子对象添加标签的 mobject。
- **label_height** ( _float_ ) – 标签的高度，默认为 0.15。
- **background_lines_width** – 标签轮廓的描边宽度，默认为 5。
- **background_lines_color** – 标签轮廓的描边颜色。
- **kwargs** – 要传递到用于构造标签的 :class`~.Integer` mobject 中的附加参数。

例子

示例：IndexLabelsExample 

![../_images/IndexLabelsExample-1.png](../_images/IndexLabelsExample-1.png)

```py

```


print*family ( \_mobject* , _n_tabs = 0_ )

用于调试目的
