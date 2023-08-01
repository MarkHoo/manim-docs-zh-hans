# 散列

用于场景缓存的实用程序。

功能

get*hash_from_play_call（*场景对象*、*相机对象*、*动画列表*、\*当前对象列表\_）

获取动画列表和 mobject 列表并输出它们的哈希值。这适用于 scene.play 函数。

参数

- **scene_object** ( [_Scene_]() ) – 场景对象。
- **camera_object** ( [_Camera_]() ) – 场景中使用的相机对象。
- **animations_list** ( _Iterable_ _\[_ [_Animation_]() _\]_ ) – 动画列表。
- **current_mobjects_list** ( _Iterable_ _\[_ [_Mobject_]() _\]_ ) – mobject 列表。

退货

camera*object、animations_list 和 current_mobjects_list 各自哈希值的字符串串联，以*分隔。

返回类型

`str`

获取 json (_对象_)

使用类递归地将对象序列化为 JSON `CustomEncoder`。

参数

**obj** ( _dict_ ) – 要展平的 dict

退货

被压扁的物体

返回类型

`str`
