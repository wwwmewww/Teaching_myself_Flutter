# TextRange
[目录](#toptop) [textRange](#textRange) [参考](https://api.flutter.dev/flutter/services/TextRange-class.html)
```
//构造函数
TextRange({@required int start, @required int end })

//以偏移量开始和结束的文本范围创建
TextRange.collapsed(int offset)
```
参数 & 属性
- 文本范围的起始索引 start → int 
- 文本范围的结束后下一个索引 end → int
- 是否是有效的范围 isValid → bool
- 是否是空的 isCollapsed → bool
- 是否开始在结束之前 isNormalized → bool

常量
- empty → const TextRange<br>```const TextRange(start: -1, end: -1)```

方法
- 范围之后的文本 textAfter(String text) → String
- 范围之前的文本 textBefore(String text) → String
- 范围之内的文本 textInside(String text) → String
