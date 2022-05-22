# For Designers

{% hint style="info" %}
**Good to know:** depending on the product you're building, it can be useful to explicitly document use cases. Got a product that can be used by a bunch of people in different ways? Maybe consider splitting it out!
{% endhint %}



#### C++17 的 19 个新特性

1. 使 static\_assert 的文本信息可选
2. 删除 trigraphs
3. 在模板参数中允许使用 typename（作为替代类）
4. 来自 braced-init-list 的新规则用于自动推导
5. 嵌套命名空间的定义，例如：使用 namespace X::Y { … } 代替 namespace X { namespace Y { … \}}
6. 允许命名空间和枚举器的属性
7. 新的标准属性：\[\[fallthrough]], \[\[maybe\_unused]] 和 \[\[nodiscard]]
8. UTF-8 字符文字
9. 对所有非类型模板参数进行常量评估
10. Fold 表达式，用于可变的模板
11. A compile-time static if with the form if constexpr(expression)
12. 结构化的绑定声明，现在允许 auto \[a, b] = getTwoReturnValues();
13. &#x20;if 和 switch 语句中的初始化器
14. 在某些情况下，确保通过编译器进行 copy elision（Guaranteed copy elision by compilers in some cases）
15. &#x20;一些用于对齐内存分配的扩展
16. 构造函数的模板推导，允许使用 std::pair(5.0, false) 代替 std::pair\<double,bool>(5.0, false)
17. 内联变量，允许在头文件中定义变量
18. \_\_has\_include，允许由预处理程序指令检查头文件的可用性
