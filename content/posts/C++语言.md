+++
title = 'C++注意事项'
date = 2024-09-09T21:58:31+08:00

categories = ["语言"] 
tags = ["cpp"]

+++

# cpp基础

## 编译

![](../img/231213.png)



## 内联函数

内联函数（inline function）是 C++ 中的一种特殊函数，通过在函数调用处直接插入其代码来提高程序的执行效率。内联函数的主要优点是减少函数调用的开销。

### 特点：

1. **定义方式**：
   使用 `inline` 关键字定义内联函数：

   ```cpp
   inline int add(int a, int b) {
       return a + b;
   }
   ```

2. **调用开销减少**：
   由于编译器在每个调用点替换函数体，避免了栈操作和跳转，增强了性能。

3. **适合小函数**：
   内联函数通常适用于简单、短小的函数，过大的函数可能导致代码膨胀。

4. **编译期决策**：
   编译器可以选择是否将某个函数作为内联函数处理，并不总是强制内联。

### 示例：

```cpp
#include <iostream>

inline int square(int x) {
    return x * x;
}

int main() {
    std::cout << "Square of 5: " << square(5) << std::endl;
    return 0;
}
```

在上述示例中，调用 `square(5)` 时，编译器会在调用处替换为 `5 * 5`，从而减少函数调用的开销。



## 指针

![](../img/屏幕截图2024-09-11001210.png)











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





















