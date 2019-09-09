# TextEditingController
[目录](#toptop) [controller](#controller) [参考](https://api.flutter.dev/flutter/widgets/TextEditingController-class.html)
```
//构造函数
TextEditingController({String text })
TextEditingController.fromValue(TextEditingValue value)
//例：
final _controller = TextEditingController();
```
参数 & 属性
<span id="textSelection"></span>
- 当前选定的文字 selection ↔ [TextSelection](#TextSelection)
- 正在编辑的文字 text ↔ String
<span id="textEditingValue"></span>
- 当前存储的值 value ↔ [TextEditingValue](#TextEditingValue)

方法
- 清空value值 clear() → void
- 清空构成区域 clearComposing() → void
- 注册事件 addListener(VoidCallback listener) → void
- 注销事件 removeListener(VoidCallback listener) → void
- 销毁当前实例 dispose() → void
