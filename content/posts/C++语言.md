+++
title = 'C++注意事项'
date = 2024-09-09T21:58:31+08:00

categories = ["语言"] 
tags = ["cpp"]

+++



# 单引号和双引号的区别


>在 C++ 中，单引号 `' '` 用于表示字符字面值（character literals），而双引号 `" "` 用于表示字符串字面值（string literals）。字符字面值只能包含一个字符，例如 `'a'` 或 `'0'`，而字符串字面值可以包含多个字符，例如 `"Hello"`。       

```c
字符字面值只能包含一个字符，例如：    

char singleChar = 'a';  // 单个字符
char digit = '0';       // 数字字符

字符串字面值可以包含多个字符，例如：

const char* greeting = "Hello";  // 一个字符串
const char* message = "12345";    // 字符串中的数字
```



# 指针就是数组

把指针想象成数组          



```c
int yy = 1;
int * xx = & yy; // yy地址: 123

xx ---> 两个内容
      | 
      |--->下标  xx 存的值为 0x123
      |--->数值 *xx 取值为 1 即 yy的值
  
xx:
val    |  1  | ==> *xx
index  |0x123| ==> xx




```





















