网络结构：
（以二级为例）
图片A1
进一级自编码器得到C1
A1和C1求差
图片B1
变换
图片A2
进二级自编码器得到C2
A2和C2求差
图片B2

生成时
白噪音B2a
与二级自编码器生成图像C2a求和
图片A2a
逆变换
图片B1a
与一级自编码器生成图像C1a求和
图片A1a

结构一：
自编码器取普通自编码器
多级自编码器尺度一致
变换取恒等（不需要训练）
共三级自编码器
训练方法一：
一个batch
进100张图
直接全局反传做总loss
训练方法二：
各级自编码器按各级目标做分loss
