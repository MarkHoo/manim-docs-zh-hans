# 配置操作[#](#module-manim.utils.config_ops "此标题的固定链接")

可能对配置字典有用的实用程序。

课程

[`DictAsObject`](manim.utils.config_ops.DictAsObject.html#manim.utils.config_ops.DictAsObject "manim.utils.config_ops.DictAsObject")

功能

merge_dicts_recursively ( _\*字典_)[\[来源\]](../_modules/manim/utils/config_ops.html#merge_dicts_recursively)[#](#manim.utils.config_ops.merge_dicts_recursively "此定义的固定链接")

创建一个字典，其键集是所有输入字典的并集。每个键的值基于列表中具有该键的第一个字典。

列表中后面的字典具有更高的优先级

当值是字典时，会递归应用

update_dict_recursively ( _current_dict_ , _\* other_ )[\[来源\]](../_modules/manim/utils/config_ops.html#update_dict_recursively)[#](#manim.utils.config_ops.update_dict_recursively "此定义的固定链接")
