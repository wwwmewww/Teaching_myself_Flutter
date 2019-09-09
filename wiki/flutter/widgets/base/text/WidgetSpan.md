# InlineSpan
[目录](#toptop) [TextSpan](#TextSpan) [参考](https://api.flutter.dev/flutter/painting/InlineSpan-class.html)
```dart
//构造函数
InlineSpan({TextStyle style })
//例:
Text.rich(
  TextSpan(
    text: 'My name is ',
    style: TextStyle(color: Colors.black),
    children: <InlineSpan>[
      WidgetSpan(
        alignment: PlaceholderAlignment.baseline,
        baseline: TextBaseline.alphabetic,
        child: ConstrainedBox(
          constraints: BoxConstraints(maxWidth: 100),
          child: TextField(),
        )
      ),
      TextSpan(
        text: '.',
      ),
    ],
  ),
)
```
参数 & 属性
- span中的文本 text → String 
- span包含的子项 children → List<InlineSpan>
- 文本样式 style → [TextStyle](#TextStyle)
- 手势事件接收器 recognizer → GestureRecognizer
- TextSpan的替代标签 semanticsLabel → String

方法
- build(ParagraphBuilder builder, { double textScaleFactor: 1.0, List<PlaceholderDimensions> dimensions }) → void
- codeUnitAt(int index) → int
- codeUnitAtVisitor(int index, Accumulator offset) → int
- compareTo(InlineSpan other) → RenderComparison
- computeToPlainText(StringBuffer buffer, { bool includeSemanticsLabels: true, bool includePlaceholders: true }) → void
- debugAssertIsValid() → bool
- debugFillProperties(DiagnosticPropertiesBuilder properties) → void
- describeSemantics(Accumulator offset, List<int> semanticsOffsets, List semanticsElements) → void
- getSpanForPosition(TextPosition position) → InlineSpan
- getSpanForPositionVisitor(TextPosition position, Accumulator offset) → InlineSpan
- toPlainText({bool includeSemanticsLabels: true, bool includePlaceholders: true }) → String
- visitChildren(InlineSpanVisitor visitor) → bool


# WidgetSpan
[目录](#toptop) [TextStyle](#InlineSpan) [参考](https://api.flutter.dev/flutter/widgets/WidgetSpan-class.html)
```
//构造函数
WidgetSpan({
  @required Widget child,
  PlaceholderAlignment alignment: ui.PlaceholderAlignment.bottom,
  TextBaseline baseline,
  TextStyle style
})
//例
Text.rich(
  TextSpan(
    children: <InlineSpan>[
      TextSpan(text: 'Flutter is'),
      WidgetSpan(
        child: SizedBox(
          width: 120,
          height: 50,
          child: Card(
            child: Center(
              child: Text('Hello World!')
            )
          ),
        )
      ),
      TextSpan(text: 'the best!'),
    ],
  )
)
```
参数 & 属性
- 子项 child → Widget
- 占位符垂直对齐方式 alignment → [PlaceholderAlignment](#PlaceholderAlignment)
- 基线对齐方式 baseline → [TextBaseline](#TextBaseline)
- 文本样式 style → [TextStyle](#TextStyle)
