xC -- A portable C interface
==

"xC" 的主要目的是构建具有 "高度可移植性" 的 C 语言开发接口, 接口包括: 基本类型/操作系统相关 API. 

"xCPI" 是指在 "xC" 的基础上移植的 C 语言开源库, 移植完成的开源库也具有 "高度的可移植性".

    "高度可移植性" 在这里的意思有两个:
    1. "xC" 被设计得容易在不同操作系统平台上重新实现;
    2. "xCPI" 包含的 C 语言开源库, 以及基于 "xC" 开发的 C 语言代码, 不需要任何修改就可以在不同平台上编译使用.

"xC" 命名规范:

1. 文件名: x<模块名> ------ 例如: xfile.h
2. 编译宏: \_<大写文件名>\_<后缀名>\_ ------ 例如: \_XFILE\_H\_
3. 宏定义/枚举值: X<宏定义/枚举值> ------ 例如: XNULL，XOFM_READ
4. 类型名: x<类型>\_t，类型由小写字母组成，如果类型名由多个单词组成，则单词之间使用下划线 ------ 例如: xint16\_t, xfile\_t, xdate\_time\_t
5. 函数名: <文件名(所在头文件名)>\_<功能>，功能由小写字母组成，如果类型名由多个单词组成，则除第一个单词外，其余单词的首字母大写，缩写单词算做一个单词 ------ 例如: xmemory\_alloc, xfile\_open, xtime\_mkTime
6. 函数指针类型(回调函数类型): xfn\_<函数类型名>\_t ------ 例如: xfn\_timer\_event\_t
