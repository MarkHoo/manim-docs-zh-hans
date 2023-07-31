# 弃用[#](#module-manim.utils.deprecation "此标题的固定链接")

用于弃用类、函数和函数参数的装饰器。

功能

已弃用（_func = None_、 _since = None_、 _until = None_、 _replacement = None_、 _message = ''_）[\[来源\]](../_modules/manim/utils/deprecation.html#deprecated)[#](#manim.utils.deprecation.deprecated "此定义的固定链接")

将可调用标记为已弃用的装饰器。

装饰后的可调用对象在使用时会引发警告。已弃用的可调用对象的文档字符串经过调整以指示该可调用对象已弃用。

参数

- **func** ( _Callable_ ) – 要装饰的函数。不应由用户设置。
- **since** ( _str_ _|_ _None_ ) – 自弃用以来的版本或日期。
- **直到**( _str_ _|_ _None_ ) – 删除已弃用的可调用函数之前的版本或日期。
- **replacement** ( _str_ _|_ _None_ ) – 替换已弃用的可调用函数的标识符。
- **message** ( _str_ _|_ _None_ ) – 可调用对象已被弃用的原因。

退货

装饰后的可调用。

返回类型

可调用

例子

基本用法：

from manim.utils.deprecation import deprecated

@deprecated
def foo(\*\*kwargs):
pass

@deprecated
class Bar:
def \_\_init\_\_(self):
pass

    @deprecated
    def baz(self):
        pass

foo()
\# WARNING The function foo has been deprecated and may be removed in a later version.

a = Bar()
\# WARNING The class Bar has been deprecated and may be removed in a later version.

a.baz()
\# WARNING The method Bar.baz has been deprecated and may be removed in a later version.

Copy to clipboard

您可以指定附加信息以获得更精确的警告：

from manim.utils.deprecation import deprecated

@deprecated(
since="v0.2",
until="v0.4",
replacement="bar",
message="It is cooler."
)
def foo():
pass

foo()
\# WARNING The function foo has been deprecated since v0.2 and is expected to be removed after v0.4. Use bar instead. It is cooler.

Copy to clipboard

您还可以使用日期而不是版本：

from manim.utils.deprecation import deprecated

@deprecated(since="05/01/2021", until="06/01/2021")
def foo():
pass

foo()
\# WARNING The function foo has been deprecated since 05/01/2021 and is expected to be removed after 06/01/2021.

Copy to clipboard

deprecated*pa​​rams（\_params = None*， _since = None_， _until = None_， _message = ''_，_重定向= None_）[\[来源\]](../_modules/manim/utils/deprecation.html#deprecated_params)[#](#manim.utils.deprecation.deprecated_params "此定义的固定链接")

将可调用参数标记为已弃用的装饰器。

它还可用于自动将已弃用的参数值重定向到其替换值。

参数

- **params** ( _str_ _|_ _Iterable_ _\[_ _str_ _\]_ _|_ _None_ ) –

  要弃用的参数。可以包括：

  - 字符串的可迭代对象，每个元素代表一个要弃用的参数
  - 单个字符串，参数名称以逗号或空格分隔。

- **since** ( _str_ _|_ _None_ ) – 自弃用以来的版本或日期。
- **直到**( _str_ _|_ _None_ ) – 删除已弃用的可调用函数之前的版本或日期。
- **message** ( _str_ _|_ _None_ ) – 可调用对象已被弃用的原因。
- **重定向**( _None_ _|_ _Iterable_ _\[_ _tuple_ _\[_ _str_ _,_ _str_ _\]_ _|_ _Callable_ _\[_ _..._ _,_ _dict_ _\[_ _str_ _,_ _Any_ _\]_ _\]_ _\]_ ) –

  参数重定向列表。每个重定向可以是以下之一：

  - 两个字符串的元组。第一个字符串定义不推荐使用的参数的名称；第二个字符串定义在尝试使用第一个字符串时要重定向到的参数的名称。
  - 执行映射操作的函数。函数的参数名称决定将哪些参数用作输入。该函数必须返回一个包含重定向参数的字典。

  重定向参数也被隐式弃用。

退货

装饰后的可调用。

返回类型

可调用

提高

- **ValueError** – 如果未定义任何参数（无论是显式还是隐式）。
- **ValueError** – 如果定义的参数是无效的 python 标识符。

例子

基本用法：

from manim.utils.deprecation import deprecated_params

@deprecated_params(params="a, b, c")
def foo(\*\*kwargs):
pass

foo(x=2, y=3, z=4)
\# No warning

foo(a=2, b=3, z=4)
\# WARNING The parameters a and b of method foo have been deprecated and may be removed in a later version.

Copy to clipboard

您还可以指定附加信息以获得更精确的警告：

from manim.utils.deprecation import deprecated_params

@deprecated_params(
params="a, b, c",
since="v0.2",
until="v0.4",
message="The letters x, y, z are cooler."
)
def foo(\*\*kwargs):
pass

foo(a=2)
\# WARNING The parameter a of method foo has been deprecated since v0.2 and is expected to be removed after v0.4. The letters x, y, z are cooler.

Copy to clipboard

基本参数重定向：

from manim.utils.deprecation import deprecated_params

@deprecated_params(redirections=\[
\# Two ways to redirect one parameter to another:
("old_param", "new_param"),
lambda old_param2: {"new_param22": old_param2}
\])
def foo(\*\*kwargs):
return kwargs

foo(x=1, old_param=2)
\# WARNING The parameter old_param of method foo has been deprecated and may be removed in a later version.
\# returns {"x": 1, "new_param": 2}

Copy to clipboard

使用计算值重定向：

from manim.utils.deprecation import deprecated_params

@deprecated_params(redirections=\[
lambda runtime_in_ms: {"run_time": runtime_in_ms / 1000}
\])
def foo(\*\*kwargs):
return kwargs

foo(runtime_in_ms=500)
\# WARNING The parameter runtime_in_ms of method foo has been deprecated and may be removed in a later version.
\# returns {"run_time": 0.5}

Copy to clipboard

将多个参数值重定向为一个：

from manim.utils.deprecation import deprecated_params

@deprecated_params(redirections=\[
lambda buff_x=1, buff_y=1: {"buff": (buff_x, buff_y)}
\])
def foo(\*\*kwargs):
return kwargs

foo(buff_x=2)
\# WARNING The parameter buff_x of method foo has been deprecated and may be removed in a later version.
\# returns {"buff": (2, 1)}

Copy to clipboard

将一个参数重定向为多个：

from manim.utils.deprecation import deprecated_params

@deprecated_params(redirections=\[
lambda buff=1: {"buff_x": buff\[0\], "buff_y": buff\[1\]} if isinstance(buff, tuple)
else {"buff_x": buff, "buff_y": buff}
\])
def foo(\*\*kwargs):
return kwargs

foo(buff=0)
\# WARNING The parameter buff of method foo has been deprecated and may be removed in a later version.
\# returns {"buff_x": 0, buff_y: 0}

foo(buff=(1,2))
\# WARNING The parameter buff of method foo has been deprecated and may be removed in a later version.
\# returns {"buff_x": 1, buff_y: 2}

Copy to clipboard
