+++
title = 'CppVsCode代码快捷模板'
date = 2024-11-15T16:09:30+08:00



categories = ["cpp"]
tags = ["模板" , "cpp"]

+++



# Cpp各类**模板**设置

## 插入代码模板

```json
"nameXXX": {
		"prefix": "XXX操作码",
		"body": [
			"xxxxxx",
			"xxxxxx",
			"yyyyyy",
			"yyyyyy",
			"$0"
		]
	},

```



## 头文件 

```cpp
#pragma GCC optimize("O2")

#include<bits/stdc++.h>
#include <iostream>      // cin/cout
#include <cstdio>        // printf/scanf
#include <algorithm>
#include <vector>        // 容器
#include <string>        // 字符串
#include <stack>         // 栈
#include <queue>         // 队列
#include <unordered_map> // 哈希表
#include <unordered_set> // 哈希表 set
#include <memory>        // 智能指针
#include <functional>
#include <numeric>
#include <ranges>
#include <cstring> 
#include <bitset>
#include <cmath>

using namespace std;

typedef long long ll;       // long long为ll
typedef long double ld;     // long doubleld
typedef pair<int, int> pii; // pair<int, int>pii
typedef pair<ll, ll> pll;   // pair<ll, ll>pll
typedef vector<int> vi;     // vector<int>vi

const long long inf = numeric_limits<long long>::max(); // 无穷大
const int N = 100100; // 100 百 , 100100 十万 , 1100100 一百万 , 100100100 一亿

void Mysolve(){
    
    
}

int main(){
    ios::sync_with_stdio(false);
    cin.tie(NULL);
    cout.tie(NULL);
    //---------优化

    Mysolve();
    return 0;
}
```



> cpp.json 设置

```json
{
	"HEADER": {
		"prefix": "H",
		"body": [
			"#pragma GCC optimize(\"O2\")",
			"",
			"#include<bits/stdc++.h>",
			"#include <iostream>      // cin/cout",
			"#include <cstdio>        // printf/scanf",
			"#include <algorithm>",
			"#include <vector>        // 容器",
			"#include <string>        // 字符串",
			"#include <stack>         // 栈",
			"#include <queue>         // 队列",
			"#include <unordered_map> // 哈希表",
			"#include <unordered_set> // 哈希表 set",
			"#include <memory>        // 智能指针",
			"#include <functional>",
			"#include <numeric>",
			"#include <ranges>",
			"#include <cstring> ",
			"#include <bitset>",
			"#include <cmath>",
			"",
			"using namespace std;",
			"",
			"typedef long long ll;       // long long为ll",
			"typedef long double ld;     // long doubleld",
			"typedef pair<int, int> pii; // pair<int, int>pii",
			"typedef pair<ll, ll> pll;   // pair<ll, ll>pll",
			"typedef vector<int> vi;     // vector<int>vi",
			"",
			"const long long inf = numeric_limits<long long>::max(); // 无穷大",
			"const int N = 100100; //  100100 十万 , 1100100 一百万 , 100100100 一亿",
			"",
			"void Mysolve(){",
			"    ",
			"}",
			"",
			"int main(){",
			"    ios::sync_with_stdio(false);",
			"    cin.tie(NULL);",
			"    cout.tie(NULL);",
			"    //---------优化",
			"",
			"    Mysolve();",
			"    return 0;",
			"}",
			"$0"
		]
	},

}
```



## leetcode模板

```json
	"leetcode": {
		"prefix": "lc",
		"body": [
			"#pragma GCC optimize(\"O2\")",
			"",
			"#include<bits/stdc++.h>",
			"using namespace std;",
			"",
			"const long long inf = numeric_limits<long long>::max();",
			"",
			"$0"
		]
	},
```

---



> 算法模板

## 高精度算法

```json
"ADD_HIGH_PRECISION": { //高精度加法
		"prefix": "hadd",
		"body": [
			"// C = A + B, A >= 0, B >= 0 ",
			"string a, b;",
			"vector<int> A, B;",
			"",
			"// cin >> a >> b;",
			"// for (int i = a.size() - 1; i >= 0; i--)",
			"//     A.push_back(a[i] - '0'); // 倒序存储第一个数",
			"// for (int i = b.size() - 1; i >= 0; i--)",
			"//     B.push_back(b[i] - '0'); // 倒序存储第二个数",
			"// auto C = add(A, B); // 调用加和函数",
			"// for (int i = C.size() - 1; i >= 0; i--)",
			"//     cout << C[i]; // 倒序输出C中的数字",
			"vector<int> add(vector<int> &A, vector<int> &B) {",
			"    if (A.size() < B.size())",
			"        return add(B, A);",
			"",
			"    vector<int> C;",
			"    int t = 0;",
			"    for (int i = 0; i < A.size(); i++) {",
			"        t += A[i];",
			"        if (i < B.size())",
			"            t += B[i];",
			"        C.push_back(t % 10);",
			"        t /= 10;",
			"    }",
			"",
			"    if (t)",
			"        C.push_back(t);",
			"    return C;",
			"}",
			"$0"
		]
	},
	"SUB_LARGE_INTS": { //高精度减hh
		"prefix": "hsub",
		"body": [
			"// C = A - B, 满足A >= B, A >= 0, B >= 0",
			"string a, b;",
			"vector<int> A, B;",
			"",
			"// cin >> a >> b;",
			"// for (int i = a.size() - 1; i >= 0; i--)",
			"//     A.push_back(a[i] - '0');",
			"// for (int i = b.size() - 1; i >= 0; i--)",
			"//     B.push_back(b[i] - '0');",
			"// if (cmp(A, B))",
			"// {",
			"//     auto C = sub(A, B);",
			"//     for (int i = C.size() - 1; i >= 0; i--)",
			"//         printf(\"%d\", C[i]);",
			"//     return 0;",
			"// }",
			"// else",
			"// {",
			"//     auto C = sub(B, A);",
			"//     printf(\"-\");",
			"//     for (int i = C.size() - 1; i >= 0; i--)",
			"//         printf(\"%d\", C[i]);",
			"//     return 0;",
			"// }",
			"",
			"bool cmp(vector<int> &A, vector<int> &B) {",
			"    if (A.size() != B.size())",
			"        return A.size() > B.size(); // 直接返回就不用else",
			"",
			"    for (int i = A.size() - 1; i >= 0; i--)",
			"        if (A[i] != B[i])",
			"            return A[i] > B[i];",
			"",
			"    return true;",
			"}",
			"",
			"vector<int> sub(vector<int> &A, vector<int> &B) {",
			"    vector<int> C;",
			"    int t = 0;",
			"    for (int i = 0; i < A.size(); i++) {",
			"        t = A[i] - t;",
			"        if (i < B.size())",
			"            t -= B[i];",
			"        C.push_back((t + 10) % 10); // 合并为1",
			"        if (t < 0)",
			"            t = 1;",
			"        else",
			"            t = 0;",
			"    }",
			"",
			"    while (C.size() > 1 && C.back() == 0)",
			"        C.pop_back(); // 去掉前导0",
			"",
			"    return C;",
			"}",
			"$0"
		]
	},
	"MUL_LARGE_INTS": { // 高精度乘法
		"prefix": "hmul",
		"body": [
			"// C = a * b , A >= 0, b >= 0",
			"string a, b;",
			"vector<int> A, B;",
			"",
			"// cin >> a >> b;",
			"// for (int i = a.size() - 1; i >= 0; i--)",
			"//     A.push_back(a[i] - '0');",
			"// for (int i = b.size() - 1; i >= 0; i--)",
			"//     B.push_back(b[i] - '0');",
			"",
			"// vector<int> C = mul(A, B);",
			"// for (int i = 0; i < C.size(); i++)",
			"//     cout << C[i];",
			"",
			"vector<int> mul(vector<int> A, vector<int> B) {",
			"    vector<int> C(A.size() + B.size() + 7, 0); // 数组C开大一点没事,可以去前导零的",
			"    for (int i = 0; i < A.size(); i++) {",
			"        for (int j = 0; j < B.size(); j++) {",
			"            C[i + j] += A[i] * B[j];",
			"        }",
			"    }",
			"",
			"    // 处理进位",
			"    for (int i = 0; i + 1 < C.size(); i++) {",
			"        C[i + 1] += C[i] / 10;",
			"        C[i] %= 10;",
			"    }",
			"",
			"    // 处理前导零 '0000' 去掉前导零",
			"    while (C.size() > 1 && C.back() == 0)",
			"        C.pop_back();",
			"",
			"    reverse(C.begin(), C.end());",
			"    return C;",
			"}",
			"$0"
		]
	},
	"DIV_LARGE_INT": { // 高精度除法
		"prefix": "hdiv",
		"body": [
			"// A / b = C ... r, A >= 0, b > 0",
			"string a;",
			"vector<int> A;",
			"int b, c;",
			"",
			"// cin >> a >> b;",
			"// for (int i = a.size() - 1; i >= 0; i--)",
			"//     A.push_back(a[i] - '0');",
			"// auto C = div(A, b, c);",
			"// for (int i = C.size() - 1; i >= 0; i--)",
			"//     cout << C[i];",
			"// cout << \"\\n\"",
			"//      << c << endl;",
			"",
			"vector<int> div(vector<int> &A, int b, int &r) {",
			"    vector<int> C;",
			"    r = 0;",
			"    for (int i = A.size() - 1; i >= 0; i--) {",
			"        r = r * 10 + A[i];",
			"        C.push_back(r / b);",
			"        r %= b;",
			"    }",
			"",
			"    reverse(C.begin(), C.end());",
			"    while (C.size() > 1 && C.back() == 0)",
			"        C.pop_back();",
			"    return C;",
			"}",
			"$0"
		]
	},

```

## cpp 求年月日

```json
int months[13] = {0, 31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};
// int year = date / 10000;
// int month = date % 10000 / 100;
// int day = date % 100;

int is_leap(int year) // 判断闰年
{
    if (year % 4 == 0 && year % 100 || year % 400 == 0)
        return 1;
    return 0;
}

int get_days(int y, int m) // 求当年当月的天数
{
    if (m == 2)
        return 28 + is_leap(y);
    return months[m];
}

int calculateDay(int y, int m, int d) // 计算 00010101 到目标日期的天数
{
    int res = 0;

    for (int i = 1; i < y; i++)
        res += 365 + is_leap(i);
    for (int i = 1; i < m; i++)
        res += get_days(y, i);

    return res + d; // 注意, 如果求2个日期相差几天, 如20110422 - 20110412 的天数 , 结果要+1 , abs(calculateDay(20110422) - calculateDay(20110412)) + 1
}

int calculateDay(int date) // 计算 00010101 到目标日期的天数
{
    int y = date / 10000;       // 年
    int m = date % 10000 / 100; // 月
    int d = date % 100;         // 日

    int res = 0;

    for (int i = 1; i < y; i++)
        res += 365 + is_leap(i);
    for (int i = 1; i < m; i++)
        res += get_days(y, i);

    return res + d; // 注意, 如果求2个日期相差几天, 如20110422 - 20110412 的天数 , 结果要+1 , abs(calculateDay(20110422) - calculateDay(20110412)) + 1
}

bool check_date(int date) // 判断日期是否合法 , 合法形式: 20240201
{
    int year = date / 10000;        // 年
    int month = date % 10000 / 100; // 月
    int day = date % 100;           // 日

    if (!day || month < 0 || month > 12)
        return false;
    if (month != 2 && day > months[month])
        return false;
    if (month == 2)
    {
        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) // 闰年特判
        {
            if (day > 29)
                return false;
        }
        else
        {
            if (day > 28)
                return false;
        }
    }
    return true;
}


```



## 区间合并





## 双指针





## 快速幂

```json
"MODULAR_EXPONENTIATION": { // 快速幂
		"prefix": "qmi",
		"body": [
			"// 求 m^k mod p , 时间复杂度 O(logk)",
			"int qmi(int m, int k, int p) {",
			"    int res = 1 % p, t = m;",
			"    while (k) {",
			"        if (k & 1)",
			"            res = (ll)res * t % p;",
			"        t = (ll)t * t % p;",
			"        k >>= 1;",
			"    }",
			"    return res;",
			"}",
			"",
			"// int qmi(int m, int k) // 不求mod",
			"// {",
			"//     int res = 1, t = m;",
			"//     while (k) {",
			"//         if (k & 1)",
			"//             res = (ll)res * t;",
			"//         t = (ll)t * t;",
			"//         k >>= 1;",
			"//     }",
			"//     return res;",
			"// }",
			"$0"
		]
	},


```





## BFS





## DFS





## 判断素数

```json
// 判断素数 
	"IS_PRIME": {
		"prefix": "prime",
		"body": [
			"// 判断一个数是否是质数",
			"bool is_prime(int n) {",
			"    if (n <= 1)",
			"        return false; // 1 和负数不是质数",
			"    for (int i = 2; i * i <= n; ++i) {",
			"        if (n % i == 0)",
			"            return false;",
			"    }",
			"    return true;",
			"}",
			"$0"
		]
	},
```





## 整数2分



```json
"整数二分": {
		"prefix": "2f",
		"body": [
			"bool check(int x) { /* ... */ } // 检查x是否满足某种性质",
			"",
			"// l l l mid mid+1 r r r   mid 在左边 , l + r >> 1 , 自动取左",
			"",
			"int bsearch_1(int l, int r) {",
			"    while (l < r) {",
			"        int mid = l + r >> 1;",
			"        if (check(mid))",
			"            r = mid; // check()判断mid是否满足性质",
			"        else",
			"            l = mid + 1;",
			"    }",
			"    return l;",
			"}",
			"$0"
		]
	},
```



##

##

##

##

##

##

##

##

##

##

##

##
