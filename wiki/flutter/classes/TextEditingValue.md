# TextEditingValue
[目录](#toptop) [textEditingValue](#textEditingValue) [参考](https://api.flutter.dev/flutter/services/TextEditingValue-class.html)
```
//构造函数
TextEditingValue({
  String text: '',
  TextSelection selection: const TextSelection.collapsed(offset: -1),
  TextRange composing: TextRange.empty
})

//从json创建
TextEditingValue.fromJSON(Map<String, dynamic> encoded)
```
参数 & 属性
- 正在编辑的当前文本 text → String
- 当前选择的文字选区 selection → [TextSelection](#TextSelection)
<span id="textRange"></span>
- 正在编写的文本范围 composing → [TextRange](#TextRange)

常量
- empty → const TextEditingValue<br>```const TextEditingValue()```

方法
- 转换成JAON toJSON() → Map<String, dynamic>
- 新建拷贝并覆盖相关的值 copyWith({String text, TextSelection selection, TextRange composing }) → TextEditingValue
