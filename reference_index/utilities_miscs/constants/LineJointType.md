# 线连接类型[#](#linejointtype "此标题的固定链接")

合格名称：`manim.constants.LineJointType`

LineJointType*类*（_值_）[\[来源\]](../_modules/manim/constants.html#LineJointType)[#](#manim.constants.LineJointType "此定义的固定链接")

基地：`Enum`

可用线接头类型的集合。

请参阅下面的示例，了解不同接头类型的直观说明。

例子

示例：LineJointVariants [¶](#linejointvariants)

![../_images/LineJointVariants-1.png](../_images/LineJointVariants-1.png)

from manim import \*

class LineJointVariants(Scene):
def construct(self):
mob = VMobject(stroke*width=20, color=GREEN).set_points_as_corners(\[
np.array(\[-2, 0, 0\]),
np.array(\[0, 0, 0\]),
np.array(\[-2, 1, 0\]),
\])
lines = VGroup(\*\[mob.copy() for * in range(len(LineJointType))\])
for line, joint_type in zip(lines, LineJointType):
line.joint_type = joint_type

        lines.arrange(RIGHT, buff=1)
        self.add(lines)
        for line in lines:
            label = Text(line.joint_type.name).next_to(line, DOWN)
            self.add(label)

Copy to clipboard

属性

`AUTO`

`ROUND`

`BEVEL`

`MITER`
