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