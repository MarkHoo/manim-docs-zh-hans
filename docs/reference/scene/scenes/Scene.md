# 场景

合格名称：`manim.scene.scene.Scene`

```py
class Scene(renderer=None, camera_class=<class 'manim.camera.camera.Camera'>, always_update_mobjects=False, random_seed=None, skip_animations=False)
```

Bases: `object`

场景是动画的画布。

主要作用[`Scene`]()是为用户提供管理对象和动画的工具。一般来说，manim 脚本由一个派生类组成，该类的[`Scene`]()方法[`Scene.construct()`]()被用户的代码覆盖。

Mobjects 通过调用显示在屏幕上[`Scene.add()`]()，并通过调用从屏幕上删除[`Scene.remove()`]()。当前屏幕上的所有 mobject 都保存在`Scene.mobjects`. 动画是通过调用来播放的[`Scene.play()`]()。

A[`Scene`]()通过调用在内部呈现[`Scene.render()`]()。这依次按顺序调用[`Scene.setup()`]()、[`Scene.construct()`]()、 和 [`Scene.tear_down()`]()。

不建议`__init__`在用户场景中重写该方法。对于应该在渲染场景之前运行的代码，请改用[`Scene.setup()`]()。


例子

用您的代码覆盖该[`Scene.construct()`]()方法。

```py
class MyScene(Scene):
    def construct(self):
        self.play(Write(Text("Hello World!")))
```


方法

|||
|-|-|
[`add`]()|Mobject 将按照添加顺序从背景到前景显示。
[`add_foreground_mobject`]()|将单个 mobject 添加到前台，并在内部添加到列表 foreground_mobjects 和 mobjects。
[`add_foreground_mobjects`]()|将 mobject 添加到前台，并在内部添加到列表 foreground_mobjects 和 mobjects。
`add_mobjects_from_animations`|
[`add_sound`]()|该方法用于为动画添加声音。
[`add_subcaption`]()|在当前时间戳的相应子字幕文件中添加一个条目。
[`add_updater`]()|为场景添加更新功能。
[`begin_animations`]()|启动场景的动画。
[`bring_to_back`]()|从场景中移除 mobject 并将其添加到场景的后面。
[`bring_to_front`]()|将传递的对象再次添加到场景中，将它们推到场景的前面。
`check_interactive_embed_is_valid`|
[`clear`]()|从场景中移除 self.mobjects 和 self.foreground_mobjects 中存在的所有 mobject。
[`compile_animation_data`]()|给定动画列表，编译相应的静态和移动对象，并收集动画持续时间。
[`compile_animations`]()|从任何 \_AnimationBuilders 创建 \_MethodAnimations 并使用传递给 play() 的 kwargs 更新动画 kwargs。
[`construct`]()|将内容添加到场景中。
`embed`|
[`get_attrs`]()|给定属性的标识符/名称，获取场景的属性。
[`get_mobject_family_members`]()|返回场景中所有对象的家庭成员列表。
`get_moving_and_static_mobjects`|
[`get_moving_mobjects`]()|获取传递的动画中的所有移动对象。
[`get_restructured_mobject_list`]()|给定一个 mobject 列表和一个要删除的 mobject 列表，这会从 mobject 列表中过滤掉可删除的 mobject。
[`get_run_time`]()|获取动画列表的总运行时间。
[`get_time_progression`]()|当你制作自己的动画时，你几乎不会使用它。
[`get_top_level_mobjects`]()|返回所有不是子对象的对象。
`interact`|
[`interactive_embed`]()|与 embed() 类似，但允许屏幕交互。
[`is_current_animation_frozen_frame`]()|返回当前动画是否产生静态帧（通常是 Wait）。
`mouse_drag_orbit_controls`|
`mouse_scroll_orbit_controls`|
[`next_section`]()|在这里创建分离；最后一部分完成并创建一个新部分。
`on_key_press`|
`on_key_release`|
`on_mouse_drag`|
`on_mouse_motion`|
`on_mouse_press`|
`on_mouse_scroll`|
[`pause`]()|暂停场景（即显示冻结的帧）。
[`play`]()|在此场景中播放动画。
[`play_internal`]()|此方法用于准备要渲染的动画、应用动画所需的参数和参数、渲染它们并将它们写入视频文件。
[`remove`]()|通过从“mobjects”和“foreground_mobjects”中删除 mobjects，从场景和前景中删除传递的 mobjects 列表中的 mobjects
[`remove_foreground_mobject`]()|从前台删除单个 mobject，并在内部从 foreground_mobjects 列表中删除。
[`remove_foreground_mobjects`]()|从前台删除 mobject，并在内部从 foreground_mobjects 列表中删除。
[`remove_updater`]()|从场景中删除更新功能。
[`render`]()|渲染此场景。
[`replace`]()|将场景中的一个 mobject 替换为另一个 mobject，保留绘制顺序。
[`restructure_mobjects`]()|TL:WR
`set_key_function`|
[`setup`]()|这意味着由通常子类化的任何场景来实现，并且在调用构造方法之前涉及一些常见的设置。
[`should_update_mobjects`]()|如果该场景的 mobject 应该更新，则返回 True。
[`tear_down`]()|这意味着由通常子类化的任何场景来实现，并且在场景结束之前具有要调用的一些通用方法。
`update_meshes`|
[`update_mobjects`]()|开始更新场景中的所有 mobject。
[`update_self`]()|运行所有场景更新程序功能。`update_to_time`|
[`wait`]()|播放“无操作”动画。
[`wait_until`]()|等待直到满足条件，直至达到给定的最大持续时间。


属性

`camera`



`add(*mobjects)`

Mobject 将按照添加顺序从背景到前景显示。

参数

**\*mobjects** ( [_Mobject_]() ) – 要添加的 Mobjects。

返回

添加 Mobjects 后的相同场景。

返回类型

[Scene]()


`add_foreground_mobject(mobject)`

将单个 mobject 添加到前台，并在内部添加到列表 foreground_mobjects 和 mobjects。

参数

**mobject** ( [_Mobject_]() ) – 要添加到前台的 Mobject。

返回

添加了前景 mobject 的场景。

返回类型

[Scene]()


`add_foreground_mobjects(*mobjects)`

将 mobject 添加到前台，并在内部添加到列表 foreground_mobjects 和 mobjects。

参数

**\*mobjects** ( [_Mobject_]() ) – 要添加到前台的 Mobject。

返回

添加了前景对象的场景。

返回类型

[Scene]()


`add_sound(sound_file, time_offset=0, gain=None, **kwargs)`

该方法用于为动画添加声音。

参数

- **sound_file** ( _str_ ) – 声音文件的路径。
- **time_offset** ( _float_ ) – 声音文件中的偏移量，在此之后可以播放声音。
- **gain**( _float_ _|_ _None_ ) – 声音的放大。


例子

示例：声音示例

```py
from manim import *

class SoundExample(Scene):
    # Source of sound under Creative Commons 0 License. https://freesound.org/people/Druminfected/sounds/250551/
    def construct(self):
        dot = Dot().set_color(GREEN)
        self.add_sound("click.wav")
        self.add(dot)
        self.wait()
        self.add_sound("click.wav")
        dot.set_color(BLUE)
        self.wait()
        self.add_sound("click.wav")
        dot.set_color(RED)
        self.wait()
```

[在此处](https://github.com/ManimCommunity/manim/blob/main/docs/source/_static/click.wav)下载上一个示例的资源。



`add_subcaption(content, duration=1, offset=0)`

在当前时间戳的相应子字幕文件中添加一个条目。

当前时间戳是从 获得的`Scene.renderer.time`。

参数

- **content** ( _str_ ) – 子标题内容。
- **duration**( _float_ ) – 显示子标题的持续时间（以秒为单位）。
- **offset** ( _float_ ) – 此偏移量（以秒为单位）将添加到子标题的开始时间戳中。

返回类型

None


例子

此示例说明了向动画添加子标题的两种可能性：

```py
class SubcaptionExample(Scene):
    def construct(self):
        square = Square()
        circle = Circle()

        # first option: via the add_subcaption method
        self.add_subcaption("Hello square!", duration=1)
        self.play(Create(square))

        # second option: within the call to Scene.play
        self.play(
            Transform(square, circle),
            subcaption="The square transforms."
        )
```


`add_updater(func)`

为场景添加更新功能。

场景更新器函数每帧运行，它们是最后运行的更新器类型。

> 警告

> 使用 Cairo 渲染器时，不会以与 mobject 更新程序相同的方式检测修改 mobject 的场景更新程序。更具体地说，仅通过场景更新器修改的移动对象不一定会添加到*移动移动对象*列表中，因此可能不会每帧都更新。

TL;DR：使用 mobject 更新程序来更新 mobject。

参数

**func** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _None_ _\]_ ) – 更新函数。它需要一个浮点数，即自上次更新以来的时间差（通常等于帧速率）。

返回类型

None

> 也可以看看

> [`Scene.remove_updater()`](),[`Scene.update_self()`]()


`begin_animations()`

启动场景的动画。

返回类型

None


`bring_to_back(*mobjects)`

从场景中移除 mobject 并将其添加到场景的后面。

参数

**\*mobjects** ( [_Mobject_]() ) – 要推到场景后面的 mobject。

返回

场景，mobject 被推到场景的后面。

返回类型

[Scene]()


`bring_to_front(*mobjects)`

将传递的对象再次添加到场景中，将它们推到场景的前面。

参数

**\*mobjects** ( [_Mobject_]() ) – 带到场景前面的 mobject。

返回

场景，mobjects 被带到场景的前面。

返回类型

[Scene]()


`clear()`

从场景中移除 self.mobjects 和 self.foreground_mobjects 中存在的所有 mobject。

返回

场景，已删除 self.mobjects 和 self.foreground_mobjects 中的所有 mobject。

返回类型

[Scene]()


`compile_animation_data(*animations, **play_kwargs)`

给定动画列表，编译相应的静态和移动对象，并收集动画持续时间。

这也开始动画。

参数

- **animations**( [_Animation_]() ) – 带有 mobject 方法和参数的动画或 mobject
- **play_kwargs** – 影响传入内容的命名参数`animations`，例如`run_time`，`lag_ratio`等等。

返回

如果没有什么可玩的，则无，否则为 self。

返回类型

self, None



`compile_animations(*args, **kwargs)`

从任何 \_AnimationBuilders 创建 \_MethodAnimations 并使用传递给 play() 的 kwargs 更新动画 kwargs。

参数

- **\*args** ( [_Animation_]() ) – 要播放的动画。
- \***\*kwargs** – 调用 play() 的配置。

返回

要播放的动画。

返回类型

Tuple\[ `Animation`\]



`construct()`

将内容添加到场景中。

从内部[`Scene.construct()`]()，通过调用在屏幕上显示 mobjects [`Scene.add()`]()，并通过调用将它们从屏幕上删除[`Scene.remove()`]()。当前屏幕上的所有 mobject 都保存在`Scene.mobjects`. 通过调用 来播放动画[`Scene.play()`]()。

笔记

初始化代码应该放在[`Scene.setup()`](). 终止代码应输入[`Scene.tear_down()`]().


例子

典型的 manim 脚本包含一个派生自[`Scene`]()重写`Scene.contruct()`方法的类：

```py
class MyScene(Scene):
    def construct(self):
        self.play(Write(Text("Hello World!")))
```


> 也可以看看

> [`Scene.setup()`](), [`Scene.render()`](),[`Scene.tear_down()`]()


`get_attrs(*keys)`

给定属性的标识符/名称，获取场景的属性。

参数

**\*keys** ( _str_ ) – 要返回其属性的参数的名称。

返回

传递的标识符的属性列表。

返回类型

list


`get_mobject_family_members()`

返回场景中所有对象的家庭成员列表。如果添加了 Circle() 和 VGroup(Rectangle(),Triangle())，则它不仅返回 Circle()、Rectangle() 和 Triangle()，还返回 VGroup() 对象。

返回

mobject 家族成员列表。

返回类型

list


`get_moving_mobjects(*animations)`

获取传递的动画中的所有移动对象。

参数

**\*animations** ( [_Animation_]() ) – 检查移动对象的动画。

返回

可以在动画中移动的 mobject 列表

返回类型

list


`get_restructured_mobject_list(mobjects, to_remove)`

给定一个 mobject 列表和一个要删除的 mobject 列表，这会从 mobject 列表中过滤掉可删除的 mobject。

参数

- **mobjects** ( _list_ ) – 要检查的 Mobjects。
- **to_remove** ( _list_ ) – 要删除的 mobject 列表。

返回

包含要删除的 mobject 的 mobject 列表已删除。

返回类型

list


`get_run_time(animations)`

获取动画列表的总运行时间。

参数

**animations** ( _list_ _\[_ [_Animation_]() _\]_`run_time` ) –要计算总数的动画列表 。

返回

`run_time`列表中所有动画的总数。

返回类型

float


```py
get_time_progression(run_time, description, n_iterations=None, override_skip_animations=False)
```

当你制作自己的动画时，你几乎不会使用它。该方法供 Manim 内部使用。

返回一个 CommandLine ProgressBar，其`fill_time` 依赖于`run_time`动画的、在该动画中执行的迭代以及指示是否考虑跳过的动画的布尔值。

参数

- **run_time** ( _float_ ) –`run_time`动画的时间。
- **n_iterations** ( _int_ _|_ _None_ ) – 动画中的迭代次数。
- **override_skip_animations** ( _bool_ ) – 是否在进度栏中显示跳过的动画。

返回

命令行进度条。

返回类型

time_progression


`get_top_level_mobjects()`

返回所有不是子对象的对象。

返回

顶级 mobject 列表。

返回类型

list


`interactive_embed()`

与 embed() 类似，但允许屏幕交互。



`is_current_animation_frozen_frame()`

返回当前动画是否产生静态帧（通常是 Wait）。

返回类型

bool


```py
next_section(name='unnamed', type=DefaultSectionType.NORMAL, skip_animations=False)
```

在这里创建分离；最后一部分完成并创建一个新部分。 `skip_animations`跳过本节中所有动画的渲染。请参阅有关如何使用部分的[文档。]()

参数

- **name**( _str_ ) –
- **type**( _str_ ) –
- **skip_animations**( _bool_ ) –

返回类型

None


`pause(duration=1.0)`

暂停场景（即显示冻结的帧）。

[`wait()`]()这是 with `frozen_frame` set to 的别名`True`。

参数

**duration**( _float_ ) – 暂停的持续时间。

> 也可以看看

> [`wait()`](),[`Wait`]()



```py
play(*args, subcaption=None, subcaption_duration=None, subcaption_offset=0, **kwargs)
```

在此场景中播放动画。

参数

- **args** – 要播放的动画。
- **subcaption** – 应在动画期间添加的外部子标题的内容。
- **subcaption_duration** – 添加指定子标题的持续时间。如果`None`（默认），则采用动画的运行时间。
- **subcaption_offset** – 添加的子标题的开始时间的偏移量（以秒为单位）。
- **kwargs** – 所有其他关键字都会传递给渲染器。


`play_internal(skip_rendering=False)`

此方法用于准备要渲染的动画、应用动画所需的参数和参数、渲染它们并将它们写入视频文件。

参数

**Skip_rendering** ( _bool_ ) – 是否应该跳过渲染，默认为 False


`remove(*mobjects)`

通过从“mobjects”和“foreground_mobjects”中删除 mobjects，从场景和前景中删除传递的 mobjects 列表中的 mobjects

参数

**\*mobjects** ( [_Mobject_]() ) – 要删除的 mobject。



`remove_foreground_mobject(mobject)`

从前台删除单个 mobject，并在内部从 foreground_mobjects 列表中删除。

参数

**mobject** ( [_Mobject_]() ) – 要从前台删除的 mobject。

返回

场景，删除了前景对象。

返回类型

[Scene]()



`remove_foreground_mobjects(*to_remove)`

从前台删除 mobject，并在内部从 foreground_mobjects 列表中删除。

参数

**\*to_remove** ( [_Mobject_]() ) – 要从前台删除的 mobject。

返回

场景，前景对象被移除。

返回类型

[Scene]()



`remove_updater(func)`

从场景中删除更新功能。

参数

**func** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _None_ _\]_ ) – 要删除的更新函数。

返回类型

None

> 也可以看看

> [`Scene.add_updater()`](),[`Scene.update_self()`]()


`render(preview=False)`

渲染此场景。

参数

**Preview** ( _bool_ ) – 如果为 true，则在文件查看器中打开场景。



`replace(old_mobject, new_mobject)`

将场景中的一个 mobject 替换为另一个 mobject，保留绘制顺序。

如果`old_mobject`是某个其他 Mobject（例如 a [`Group`]()）的子对象，则 new_mobject 将在组内替换它，而不更改父对象。

参数

- **old_mobject** ( [_Mobject_]() ) – 要替换的 mobject。必须出现在场景中。
- **new_mobject** ( [_Mobject_]() ) – 场景中尚未存在的 mobject。

返回类型

None


```py
restructure_mobjects(to_remove, mobject_list_name='mobjects', extract_families=True)
```

TL:WR

如果您的场景有一个 Group()，并且您从 Group 中删除了一个 mobject，则会解散该组并将其余 mobject 直接放入 self.mobjects 或 self.foreground_mobjects 中。

如果场景包含一个组，例如 Group(m1, m2, m3)，但其中一个子对象被删除，例如 scene.remove(m1)，则 mobject 列表将被编辑为包含其他子对象，但不包含 m1 ，例如，它现在会将 m2 和 m3 插入到该组曾经所在的位置。

参数

- **to_remove** ( [_Mobject_]() ) – 要删除的 Mobject。
- **mobject_list_name** ( _str_ ) – 要从中删除的 mobject（“mobjects”、“foreground_mobjects”等）列表。
- **extract_families** ( _bool_ ) – 是否应递归提取 mobject 的族。

返回

具有重构 Mobject 的场景 mobject。

返回类型

[Scene]()



`setup()`

这意味着由通常子类化的任何场景来实现，并且在调用构造方法之前涉及一些常见的设置。



`should_update_mobjects()`

如果该场景的 mobject 应该更新，则返回 True。

特别是，这会检查是否

- 的`always_update_mobjects`属性[`Scene`]() 设置为`True`,
- 它[`Scene`]()本身附加了基于时间的更新程序，
- 其中的任何对象都[`Scene`]()附加了基于时间的更新程序。

仅当播放单个等待动画时才会调用此函数。

返回类型

bool



`tear_down()`

这意味着由通常子类化的任何场景来实现，并且在场景结束之前具有要调用的一些通用方法。


`update_mobjects(dt)`

开始更新场景中的所有 mobject。

参数

**dt** ( _float_ ) – 更新之间的时间变化。默认（大部分）为 1/frames_per_second


`update_self(dt)`

运行所有场景更新程序功能。

在所有类型的更新函数（对象更新器、网格更新器、场景更新器）中，场景更新函数是最后调用的。

参数

**dt** ( _float_ ) – 自上次更新以来的场景时间。

> 也可以看看

> [`Scene.add_updater()`](),[`Scene.remove_updater()`]()


`wait(duration=1.0, stop_condition=None, frozen_frame=None)`

播放“无操作”动画。

参数

- **duration**( _float_ ) – 动画的运行时间。
- **stop_condition** ( _Callable_ _\[_ _\[_ _\]_ _,_ _bool_ _\]_ _|_ _None_ ) – 没有位置参数的函数，每次渲染帧时都会评估该函数。仅当函数的返回值为 true 或经过指定的时间时动画才会停止`duration` 。
- **freeze_frame** ( _bool_ _|_ _None_ ) – 如果为 True，则不评估更新程序函数，并且动画输出冻结帧。如果为 False，则调用更新程序函数并照常渲染帧。如果“无”（默认值），则场景会尝试确定帧是否自行冻结。

> 也可以看看

> [`Wait`](),`should_mobjects_update()`


`wait_until(stop_condition, max_time=60)`

等待直到满足条件，直至达到给定的最大持续时间。

参数

- **stop_condition** ( _Callable_ _\[_ _\[_ _\]_ _,_ _bool_ _\]_ ) – 一个不带参数的函数，用于确定场景是否应该继续等待。
- **max_time** ( _float_ ) – 最大等待时间（以秒为单位）。
