# P4
## basic type基本数据类型
bit<n> 大小为n的无符号整型(字节串)
bit 和bit<1>一样
int<n> 大小为n的有符号整型
varbit<n> 变长字节串
## header type标头类型
有顺序的成员集合
Byte-aligned 数据对齐
可以含有bit<n>,int<n>,varbit<n>
可以合法或非法
提供一系列操作来测试或者设置合法的字节如：isValid(),setValid(),setInvalid()

## typedef 类型别名
顾名思义

## standard_metadata 固有元数据
包含了数据包相关的基础信息，已经预定义，可以直接使用。
**ingress_port ：**数据包的入端口，解析之前设置，只读。
**packet_length：**数据包的字节数，当交换机在快速转发模式下，该元数据不能在动作(action)中匹配或引用。只读。
**egress_spec ：**在入端口流水线的匹配-动作过程之后设置，指定数据包出端口，可以是物理端口、逻辑端口或者多播组。
**egress_instance ：**用于区分复制后数据包实例的标识符。只读。
**instance_type：**数据包实例类型：正常(Normal)、入端口复制(ingress clone)、出端口复制(clone)、再循环(recirculated)。
**parser_sratus ：**解析器解析结果，0表示无错误，其实数字代表了对应的错误类型。
**parser_error_location ：**指向P4程序错误发生处。
