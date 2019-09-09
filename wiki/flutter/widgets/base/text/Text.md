# Text

## 构造函数

```dart
Text(
  String data, //要显示的文本
  {
    Key key, //key
    TextStyle style, //文本样式
    StrutStyle strutStyle, //支撑样式
    TextAlign textAlign, //水平对齐方式
    TextDirection textDirection, //文本的方向
    Locale locale, //区域设置
    bool softWrap, //是否自动换行
    TextOverflow overflow, //文本溢出如何显示
    double textScaleFactor, //字体显示的倍率
    int maxLines, //文本显示的最大行数
    String semanticsLabel, //此文本的替代语义标签。
    TextWidthBasis textWidthBasis //null
  }
)
//富文本1
Text.rich(
  InlineSpan textSpan,
  {
    Key key,
    TextStyle style,
    StrutStyle strutStyle,
    TextAlign textAlign,
    TextDirection textDirection,
    Locale locale,
    bool softWrap,
    TextOverflow overflow,
    double textScaleFactor,
    int maxLines,
    String semanticsLabel,
    TextWidthBasis textWidthBasis
  }
)
//富文本2
RichText({
  Key key,
  @required InlineSpan text,
  TextAlign textAlign: TextAlign.start,
  TextDirection textDirection,
  bool softWrap: true,
  TextOverflow overflow: TextOverflow.clip,
  double textScaleFactor: 1.0,
  int maxLines,
  Locale locale,
  StrutStyle strutStyle,
  TextWidthBasis textWidthBasis: TextWidthBasis.parent
})
```

例:

```dart
Text("测试"*6,  //字符串重复六次,
  style: TextStyle(
    color: Colors.red,
    backgroundColor: Colors.green,
  ),
  softWrap: true,
)

Text.rich(

)

RichText(
  text: TextSpan(
    text: 'Hello ',
    style: DefaultTextStyle.of(context).style,
    children: <TextSpan>[
      TextSpan(text: 'bold', style: TextStyle(fontWeight: FontWeight.bold)),
      TextSpan(text: ' world!'),
    ],
  ),
)
```

## 参数 & 属性

- style → [TextStyle](/classes/TextStyle)  
  *文本样式*
- strutStyle → [StrutStyle](/classes/StrutStyle)  
  *结构样式* ??
- textAlign → [TextAlign](#TextAlign)  
  *水平对齐*
- textDirection → [TextDirection](#TextDirection)  
  *文字方向*
- overflow → [TextOverflow](#TextOverflow)  
  *溢出方式*
- textWidthBasis → [TextWidthBasis](#TextWidthBasis)
- locale → [Locale](#Locale)  
  *语言设置*
- softWrap → bool  
  *自动换行*
- textScaleFactor → double
  *放大倍数*
- maxLines → int  
  *最大行数*
- semanticsLabel → String  
  *盲文提示*
