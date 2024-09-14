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



## 类与对象

### 类（Class）

类是一个用户定义的数据类型，用于封装数据和函数。类可以包含属性（成员变量）和行为（成员函数）。

**定义示例**：

```cpp
class Dog {
public:
    // 属性
    std::string name;
    int age;

    // 构造函数
    Dog(std::string n, int a) : name(n), age(a) {}

    // 方法
    void bark() {
        std::cout << name << " says woof!" << std::endl;
    }
};
```

### 对象（Object）

对象是类的实例，通过类的构造函数创建。每个对象都有自己的属性值。

**使用示例**：

```cpp
#include <iostream>
#include <string>

class Dog {
public:
    std::string name;
    int age;

    Dog(std::string n, int a) : name(n), age(a) {}

    void bark() {
        std::cout << name << " says woof!" << std::endl;
    }
};

int main() {
    // 创建对象
    Dog myDog("Buddy", 3);
    
    // 调用对象的方法
    myDog.bark(); // 输出: Buddy says woof!

    return 0;
}
```

### 总结

- **类**是模板，用于定义对象的属性和行为。
- **对象**是类的实例，具有具体的状态和行为。类和对象的结合使得 C++ 支持面向对象编程，便于代码的组织、复用和维护。











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







# string用法



在 C++ 中，`std::string` 本身不是一个栈（stack），但可以像栈一样使用，特别是利用其尾部（末尾）操作。你可以使用 `push_back` 和 `pop_back` 方法来模拟栈的行为。以下是如何用 `std::string` 模拟栈的简单示例：

```cpp
#include <iostream>
#include <string>

using namespace std;

int main() {
    string stack;

    // 入栈
    stack.push_back('A');
    stack.push_back('B');
    stack.push_back('C');

    // 出栈
    while (!stack.empty()) {
        char top = stack.back(); // 获取栈顶元素
        stack.pop_back();        // 出栈
        cout << top << endl;     // 打印栈顶元素
    }

    return 0;
}
```

## 代码解释：

- **入栈**：使用 `push_back` 方法将元素添加到字符串末尾。
- **出栈**：使用 `pop_back` 方法移除末尾元素，并使用 `back` 方法获取栈顶元素（末尾元素）。
- **检查是否为空**：使用 `empty` 方法来检查栈是否为空。

## 注意事项：

- 尽管你可以用 `std::string` 来模拟栈，但对于更复杂的数据结构，建议使用标准库中的 `std::stack`，它提供了更明确的接口和更好的语义清晰性。
- `std::stack` 是一个适配器，通常与其他容器（如 `std::deque` 或 `std::vector`）一起使用，可以更好地满足栈的需求。









