# 类： `turquoise::Str`
* > 记录特定数据类型的一组串
* > 位于`turquoise/Str.hpp`
## 模板参数: `<class T, class Allocator = std::allocator<T>>`
* > `class T`: 特定数据类型
* > `Allocator`: (可选): 满足c++标准的allocator， 默认使用std::allocator
## 构造
* > `Str(const T*)`: 用常值数据构造, 最后一位是NULL
* > `Str(int)`： 用长度构造
## 方法
* > `int length()`： 获取长度
* > `T* data`: 获取原始指针
* > `加法运算符`：返回两者拼接结果，按先后顺序
* > `[]`: 获取指定下标位置的元素引用
## 示例
```cpp
#include "turquoise/Str.hpp"
#include <iostream>
using namespace turquoise;

int main() {
    Str<char> string1("Hello");
    Str<char> string2("world");
    Str<char> string3 = string1 + " " + string2 + "!";

    for (int i = 0; i < string3.length(); i++) {
        std::cout << string3[i];
    }

    return 0;
}
```
### 输出
```
Hello world!
```