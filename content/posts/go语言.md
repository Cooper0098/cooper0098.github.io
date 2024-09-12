+++
title = 'Go语言'
date = 2024-09-09T21:55:24+08:00

categories = ["语言"] 
tags = ["go"]

+++



# 变量声明

- **第一种，指定变量类型，如果没有初始化，则变量默认为零值**。

例如：

```go

var a int   // 声明一个整型变量 a，默认为 0
var b float64 // 声明一个浮点型变量 b，默认为 0.0
```

- **第二种，根据值自行判定变量类型。**

例如：

```go

var c = "Hello" // 声明变量 c，类型为 string
var d = 42      // 声明变量 d，类型为 int
```



- **第三种，如果变量已经使用 var 声明过了，再使用 := 声明变量，就产生编译错误**

例如：

```go

var e int = 10  // 使用 var 声明
// e := 20      // 编译错误：e 已经被声明过
```



# go语言常量

**常量**是一个简单值的标识符，在程序运行时，不会被修改的量。

常量中的数据类型只可以是布尔型、数字型（整数型、浮点型和复数）和字符串型。

常量的定义格式：

```go
const identifier [type] = value
```

你可以省略类型说明符 [type]，因为编译器可以根据变量的值来推断其类型。

- 显式类型定义： `const b string = "abc"`
- 隐式类型定义： `const b = "abc"`

多个相同类型的声明可以简写为：

```go
const c_name1, c_name2 = value1, value2
```
---

**iota**，特殊常量，可以认为是一个可以被编译器修改的常量。

iota 在 const关键字出现时将被重置为 0(const 内部的第一行之前)，const 中每新增一行常量声明将使 iota 计数一次(iota 可理解为 const 语句块中的行索引)。

iota 可以被用作枚举值：

```go
const (
    a = iota
    b = iota
    c = iota
)
```

第一个 iota 等于 0，每当 iota 在新的一行被使用时，它的值都会自动加 1；所以 a=0, b=1, c=2 可以简写为如下形式：

```go
const (
    a = iota
    b
    c
)
```

### iota 用法

## 实例

```go
package main

import "fmt"

func main() {
    const (
            a = iota   //0
            b          //1
            c          //2
            d = "ha"   //独立值，iota += 1
            e          //"ha"   iota += 1
            f = 100    //iota +=1
            g          //100  iota +=1
            h = iota   //7,恢复计数
            i          //8
    )
    fmt.Println(a,b,c,d,e,f,g,h,i)
}

```



以上实例运行结果为：

```go
0 1 2 ha ha 100 100 7 8
```





