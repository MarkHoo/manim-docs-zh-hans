# 按字母添加文本

合格名称：`manim.animation.creation.AddTextLetterByLetter`

```py
class AddTextLetterByLetter(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `ShowIncreasingSubsets`

[`Text`]()在现场逐个字母地展示。

参数

- **time_per_char** – 字母出现的频率。
- **Tip::** ( _.._ ) – 目前仅适用于类：~.Text，不适用于类：~.MathTex
- **text** (Text) –
- **suspend_mobject_updating** (bool) –
- **int_func** (Callable[[np.ndarray], np.ndarray]) –
- **rate_func** (Callable[[float], float]) –
- **run_time** (float | None) –


方法
