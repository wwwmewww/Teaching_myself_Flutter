# TextSpan
[目录](#toptop) [TextStyle](#TextStyle) [参考](https://api.flutter.dev/flutter/painting/TextSpan-class.html)
```dart
//构造函数
TextSpan({
  String text,
  List<InlineSpan> children,
  TextStyle style,
  GestureRecognizer recognizer,
  String semanticsLabel //??
})
//例:
TextSpan(
  text: 'Hello world!',
  style: TextStyle(color: Colors.black),
)
```
参数 & 属性
- 文本 text → String 
- 附加文本列表 children → List<[InlineSpan](#InlineSpan)>
- 文本样式 style → [TextStyle](#TextStyle)
- 手势事件接收器 recognizer → GestureRecognizer
- TextSpan的替代标签 semanticsLabel → String

方法
- build(ParagraphBuilder builder, { double textScaleFactor: 1.0, List<PlaceholderDimensions> dimensions }) → void
- codeUnitAtVisitor(int index, Accumulator offset) → int
- compareTo(InlineSpan other) → RenderComparison
- computeToPlainText(StringBuffer buffer, { bool includeSemanticsLabels: true, bool includePlaceholders: true }) → void
- debugAssertIsValid() → bool
- debugDescribeChildren() → List<DiagnosticsNode>
- debugFillProperties(DiagnosticPropertiesBuilder properties) → void
- describeSemantics(Accumulator offset, List<int> semanticsOffsets, List semanticsElements) → void
- getSpanForPositionVisitor(TextPosition position, Accumulator offset) → InlineSpan
- toStringShort() → String
- visitChildren(InlineSpanVisitor visitor) → bool
