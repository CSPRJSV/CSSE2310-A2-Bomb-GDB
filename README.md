# CSSE2310-A2-Bomb-GDB
# CSSE2310-A2-Bomb-GDB 专业1v1远程辅导助攻、讲题和VIP定制服务 保证原创 严厉拒绝一份多售
# 源头导师 科班出身 可全英文听说读写流畅丝滑 非中介甩单！
# 支持 零散答疑 lecture同步辅导 assignment专题辅导 test prep 等多种灵活辅导方式
# VX: csprojhelp 备注：github

【重点解析：】

1. 考验 GDB 使用能力的炸弹拆除游戏。每个童鞋获得一份定制的 bomb 可执行文件，并要求使用特制的 2310gdb 来跟踪运行。每个 phase 5 分一共 50 分，同一 phase 在第一次尝试失败后开始降低得分上限，也就是说盲目地去猜是有代价的。学校还提供了部分 bomb 程序的源代码文件可供参考。

2. bomb 与 2310gdb 只能在 moss 上运行，并且每一步操作都会被联网记录以供后续审计

3. 整体思路框架如下：

4. 首先通过 phases.c 熟悉当前待拆除  phase 的运行逻辑，并识别出 key expression。key expression 的定义是对最终 secret 字符串内容有影响的值。

5. 然后在 2310gdb 内的合适地点（行数）与时机（条件）打好断点。运行程序在断点停下来后，通过 print expression 的形式得到 key expression 的值并自己另外找地方记录下来。重复以上过程直到得到所有 key  expressions

6. 最后得到所有 key  expressions 的值后，可通过多种方式把原来含有未知值的 phase 函数变成全明文的 phase 函数，模拟运行该 phase 函数即可得出答案 secret string。

【避坑Tips：】

1. 某些表面人畜无害的函数调用比如 append_to_secret_string() 实际上会改变程序状态，从而间接影响 key  expressions。

2. 某靠后 phase 的解开过程竟然意外地直观与简单，让不少在前面 phases 被炸出心理阴影的童鞋一着被蛇咬十年怕井绳，拿着答案却不敢确认。其实这就是出题者的恶趣味。

3. 注意 mute() 与 flipmute() 函数对 secret string 的影响，许多童鞋就是因为忽略了这俩函数捣的鬼

4. 某些 phase 需要一定的位运算分析推理化简能力才能找到简洁可操作的规律。

==============================================

有需要 辅导 or VIP服务 的童鞋欢迎浏览个人主页传送与滴滴 ~

![1](https://github.com/CSPRJSV/CSSE2010-7201-AVR-Project-Battleship/blob/main/ad-1.png)
![3](https://github.com/CSPRJSV/CSSE2010-7201-AVR-Project-Battleship/blob/main/ad-3.jpg)
![4](https://github.com/CSPRJSV/CSSE2010-7201-AVR-Project-Battleship/blob/main/ad-4.jpg)
![2](https://github.com/CSPRJSV/CSSE2010-7201-AVR-Project-Battleship/blob/main/ad-2.png)


