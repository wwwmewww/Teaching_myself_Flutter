# TextInputType

[参考](https://api.flutter.dev/flutter/services/TextInputType-class.html)

构造函数

```dart
TextInputType.numberWithOptions({
  bool signed: false,
  bool decimal: false
})
```

参数 & 属性

- decimal → bool  
  *是否是十进制的*
- index → int  
  *枚举值索引*
- signed → bool  
  *该号码已签名，在开始时允许正号或负号*

方法

- toJson() → Map<String, dynamic>
- toString() → String

常量

1. TextInputType.text  
   *文本*
2. TextInputType.multiline  
   *多行*
3. TextInputType.number  
   *数字*
4. TextInputType.phone  
   *电话*
5. TextInputType.datetime  
   *日期*
6. TextInputType.emailAddress  
   *电邮*
7. TextInputType.url  
   *网址*
8. TextInputType.values  
   *返回所有枚举值的列表*
