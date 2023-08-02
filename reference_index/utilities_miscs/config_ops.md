# 配置操作

可能对配置字典有用的实用程序。

Classes

[`DictAsObject`]()


Functions

`merge_dicts_recursively(*dicts)`

创建一个字典，其键集是所有输入字典的并集。每个键的值基于列表中具有该键的第一个字典。

列表中后面的字典具有更高的优先级

当值是字典时，会递归应用


`update_dict_recursively(current_dict, *others)`
