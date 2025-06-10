# 类: `turquoise::Log`
* 日志管理
* 头文件`turquoise/Log.h`
## 构造
### `Log(const char* dst, const char* type)`
  1. `const char* dst`: 目标日志文件
  2. `const char* type`: 代表日志类型
## 方法
### `void add(const char* info)` 
   * 添加日志
   * `info`: 日志信息
## 测试
```cpp
// 添加一万条信息为try的日志
#include "turquoise/Log.h"
using namespace turquoise;

int main() {
    Log log("test.log", "TEST");
    for (int i = 0; i < 10000; i++) {
        log.add("try");
    }
    return 0;
}
```
### 结果
输出文件`test.log`
```
2025/06/10 20:42:49.515 [TEST] try
2025/06/10 20:42:49.516 [TEST] try
2025/06/10 20:42:49.516 [TEST] try
2025/06/10 20:42:49.516 [TEST] try
2025/06/10 20:42:49.516 [TEST] try
2025/06/10 20:42:49.516 [TEST] try
2025/06/10 20:42:49.516 [TEST] try
2025/06/10 20:42:49.516 [TEST] try
2025/06/10 20:42:49.516 [TEST] try
2025/06/10 20:42:49.516 [TEST] try
...
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try
2025/06/10 20:42:49.526 [TEST] try

```