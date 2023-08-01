# 简单函数

简单函数的集合。

功能

二进制搜索（_函数_，_目标_，_下限_，_上限_，_公差= 0.0001_）

通过重复将范围一分为二来搜索范围内的值。

更准确地说，执行数值二分搜索以确定 的输入`function`，在给定的范围内，输出`target` 在范围内`tolerance`（默认为 0.0001）。`None`如果在边界内找不到输入，则返回。

例子

考虑多项式 x2+3x+1 我们搜索的目标值是 11。精确解是 x=2。

> > \> solution = binary_search(lambda x: x**2 + 3\*x + 1, 11, 0, 5)
> > \> abs(solution - 2) < 1e-4
> > True
> > \> solution = binary_search(lambda x: x**2 + 3\*x + 1, 11, 0, 5, tolerance=0.01)
> > \> abs(solution - 2) < 0.01
> > True

Copy to clipboard

在区间内搜索\[0,5\]对于目标值 71 没有产生解决方案：

> > \> binary_search(lambda x: x\**2 + 3*x + 1, 71, 0, 5) is None
> > True

Copy to clipboard

参数

- **函数**(_可调用\_\_\[_ _\[_ _int_ _|_ _float_ _\]_ _,_ _int_ _|_ _float_ _\]_ ) –
- **目标**( _int_ _|_ _float_ ) –
- **lower_bound** ( _int_ _|_ _float_ ) –
- **upper_bound** ( _int_ _|_ _float_ ) –
- **公差**( _int_ _|_ _float_ ) –

返回类型

整数 | 浮动| 没有任何

选择( _n_ , _k_ )

二项式系数 n 选择 k。

(nk)描述了可能的选择的数量 k 一组中的元素 n 元素。

参考

- [https://en.wikipedia.org/wiki/Combination](https://en.wikipedia.org/wiki/Combination)
- [https://docs.scipy.org/doc/scipy/reference/ generated/scipy.special.comb.html](https://docs.scipy.org/doc/scipy/reference/generated/scipy.special.comb.html)

参数

- **n** (_整数_) –
- **k** (_整数_) –

返回类型

整数

剪辑（_a_、 _min_a_、 _max_a_）

剪辑`a`到区间 \[ `min_a`, `max_a`\]。

接受任何可比较的对象（即支持 <、\> 的对象）。`a`如果介于`min_a`和 之间则返回`max_a`。否则，取`min_a`和 中`max_a`最接近的一个。

例子

> > \> clip(15, 11, 20)
> > 15
> > \> clip('a', 'h', 'k')
> > 'h'

Copy to clipboard

获取参数（_函数_）

返回 的参数`function`作为参数名称到其对应对象的有序映射`Parameter`。

例子

> > \> get_parameters(get_parameters)
> > mappingproxy(OrderedDict(\[('function', <Parameter "function: 'Callable'">)\]))

> > \> tuple(get_parameters(choose))
> > ('n', 'k')

Copy to clipboard

参数

**函数**（_可调用_）-

返回类型

MappingProxyType\[str，inspect.Parameter\]

乙状结肠( _x_ )

返回逻辑函数的输出。

逻辑函数（Sigmoid 函数的常见示例）定义为 11+e−x。

参考

- [https://en.wikipedia.org/wiki/Sigmoid_function](https://en.wikipedia.org/wiki/Sigmoid_function)
- [https://en.wikipedia.org/wiki/Logistic_function](https://en.wikipedia.org/wiki/Logistic_function)

参数

**x**（_浮动_）–

返回类型

漂浮
