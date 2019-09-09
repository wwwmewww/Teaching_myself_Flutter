# RaisedButton

漂浮按钮，默认带有阴影和灰色背景；按下后，阴影会变大

[参考](https://api.flutter.dev/flutter/material/RaisedButton-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > MaterialButton > RaisedButton

## 构造参数

```dart
RaisedButton({
  Key key,
  @required VoidCallback onPressed,
  ValueChanged<bool> onHighlightChanged,
  ButtonTextTheme textTheme,
  Color textColor,
  Color disabledTextColor,
  Color color,
  Color disabledColor,
  Color focusColor,
  Color hoverColor,
  Color highlightColor,
  Color splashColor,
  Brightness colorBrightness,
  double elevation,
  double focusElevation,
  double hoverElevation,
  double highlightElevation,
  double disabledElevation,
  EdgeInsetsGeometry padding,
  ShapeBorder shape,
  Clip clipBehavior,
  FocusNode focusNode,
  MaterialTapTargetSize materialTapTargetSize,
  Duration animationDuration,
  Widget child
})
//带图标
RaisedButton.icon({
  Key key,
  @required VoidCallback onPressed,
  ValueChanged<bool> onHighlightChanged,
  ButtonTextTheme textTheme,
  Color textColor,
  Color disabledTextColor,
  Color color,
  Color disabledColor,
  Color focusColor,
  Color hoverColor,
  Color highlightColor,
  Color splashColor,
  Brightness colorBrightness,
  double elevation,
  double highlightElevation,
  double disabledElevation,
  ShapeBorder shape,
  Clip clipBehavior,
  FocusNode focusNode,
  MaterialTapTargetSize materialTapTargetSize,
  Duration animationDuration,
  @required Widget icon,
  @required Widget label
})
```

## 参数 & 属性

- onPressed → VoidCallback  
  *点击事件*
- onHighlightChanged → ValueChanged\<bool>  
  *由下层lnkWell.onHighlightChanged调用*
- textTheme → [ButtonTextTheme](#ButtonTextTheme)  
  *文字主题*
- textColor → [Color](#Color)  
  *文字颜色*
- disabledTextColor → [Color](#Color)  
  *禁用时文本颜色*
- color → [Color](#Color)  
  *启用时填充颜色*
- disabledColor → [Color](#Color)  
  *禁用时填充颜色*
- focusColor → [Color](#Color)  
  *有焦点时填充颜色*
- hoverColor → [Color](#Color)  
  *悬停时填充颜色*
- highlightColor → [Color](#Color)  
  *InkWell高亮颜色*
- splashColor → [Color](#Color)  
  *InkWell溅墨颜色*
- colorBrightness → [Brightness](#Brightness)
  *主题亮度*
- elevation → double  
  *相对于父级的z坐标,默认2,非负*
- focusElevation → double  
  *有焦点时相对于父级的z坐标,默认4.0,非负*
- hoverElevation → double  
  *悬停时相对于父级的z坐标,默认4.0,非负*
- highlightElevation → double  
  *按下时相对于父级的z坐标,默认8.0,非负*
- disabledElevation → double  
  *禁用时相对于父级的z坐标,默认0.0,非负*
- shape → [ShapeBorder](#ShapeBorder)  
  *图形边框*
- clipBehavior → [Clip](#Clip)  
  *溢出裁剪*
- focusNode → [FocusNode](https://api.flutter.dev/flutter/widgets/FocusNode-class.html)  
  *获取焦点的节点*
- materialTapTargetSize → [MaterialTapTargetSize](#MaterialTapTargetSize)  
  *配置点击区的最小尺寸*
- animationDuration → [Duration](#Duration)  
  *图像和高度的动画持续时间*
- child → Widget  
  *子部件*
- icon → Widget  
  *图标*
- label → Widget  
  *文本*
- enabled → bool  
  *是否启用按钮*
- height → double  
  *高*
- minWidth → double  
  *最小宽度*
