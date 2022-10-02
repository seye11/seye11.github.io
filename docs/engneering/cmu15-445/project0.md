# 实验信息
实验介绍： https://15445.courses.cs.cmu.edu/fall2022/project0/

github: https://github.com/cmu-db/bustub

主要内容: C++实现字典树由单线程->支持并发。

# 遇到的问题
## C++
我对C++的很多语法和工程使用技巧并不熟悉，不知道该如何优雅、快速的实现。

### 显式转换:
用法cast_name<type> (expression)
1. static_cast: 任何具有明确定义的类型转换，只要不包含底层const。
2. const_cast: 主要用来移除变量的const或volatile限定符，去掉/添加对象的底层const属性，该属性为指针所拥有，所以只能转换指针或引用（本质为指针）。
3. dynamic_cast: 用于派生类之间的转换，只能转换指针或引用。相较于static_cast，下行转换时会检查类型是否一致，若不一致转换为空指针，更安全一些。
4. reinterpret_cast: 任意类型强制转换，危险慎用。
