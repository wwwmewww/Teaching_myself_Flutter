# TextSelection 文字选区
[目录](#toptop) [textSelection](#textSelection) [参考](https://api.flutter.dev/flutter/services/TextSelection-class.html)
```
//构造函数
TextSelection({
  @required int baseOffset, //起点
  @required int extentOffset, //终点
  TextAffinity affinity: TextAffinity.downstream,
  bool isDirectional: false 
})
//例：
TextSelection(baseOffset: text.length, extentOffset: text.length),

//从给定偏移量处创建
TextSelection.collapsed({
  @required int offset, //偏移量
  TextAffinity affinity: TextAffinity.downstream
})

//从指定位置创建
TextSelection.fromPosition(TextPosition position)
```
参数 & 属性
<span id="textAffinity"></span>
- 插入符位置 affinity → [TextAffinity](#TextAffinity)
<span id="textPosition"></span>
- 选择的起始位置 base → [TextPosition](#TextPosition)
- 选择终止的位置 extent → [TextPosition](#TextPosition)
- 选择的起始偏移量 baseOffset → int
- 选择终止的偏移量 extentOffset → int
- 范围中第一个字符的索引 start → int
- 在字符范围后的下个索引 end → int
- 是否选择 isDirectional → bool ？？
- 是否为空 isCollapsed → bool ？？
- 该范围的开始是否在结束之前 isNormalized → bool ？？
- 此范围是否代表文本中的有效位置 isValid → bool ？？

方法
- 选区之前的文本 textBefore(String text) → String
- 选区之后的文本 textAfter(String text) → String
- 选区内的文本 textInside(String text) → String

```
//新建选区
copyWith({
  int baseOffset,
  int extentOffset,
  TextAffinity affinity,
  bool isDirectional
}) → TextSelection
```
方法参数
- 起点偏移量 baseOffset → int
- 终点偏移量 extentOffset → int
- 插入符位置 affinity → [TextAffinity](#TextAffinity)
- 是否选择 isDirectional → bool ？？
