# FlatButton

扁平按钮。默认背景透明并不带阴影。按下后，会有背景色

[参考](https://api.flutter.dev/flutter/material/FlatButton-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > MaterialButton > FlatButton

## 构造函数

```dart
FlatButton({
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
  EdgeInsetsGeometry padding,
  ShapeBorder shape,
  Clip clipBehavior,
  FocusNode focusNode,
  MaterialTapTargetSize materialTapTargetSize,
  @required Widget child
})
//带图标
FlatButton.icon({
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
  EdgeInsetsGeometry padding,
  ShapeBorder shape,
  Clip clipBehavior,
  FocusNode focusNode,
  MaterialTapTargetSize materialTapTargetSize,
  @required Widget icon,
  @required Widget label
})
```

## 参数 & 属性

- **onPressed** → VoidCallback  
  *点击事件*
- **onHighlightChanged** → ValueChanged\<bool>  
  *由下层lnkWell.onHighlightChanged调用*
- textTheme → [ButtonTextTheme](#ButtonTextTheme)  
  *文字主题*
- textColor → [Color](#Color)  
  *文字颜色*
- disabledTextColor → [Color](#Color)  
  *禁用按钮文本颜色*
- color → [Color](#Color)  
  *按钮填充颜色*
- disabledColor → [Color](#Color)  
  *禁用按钮填充颜色*
- focusColor → [Color](#Color)  
  *焦点按钮填充颜色*
- hoverColor → [Color](#Color)  
  *悬停按钮填充颜色*
- highlightColor → [Color](#Color)  
  *InkWell高亮颜色*
- splashColor → [Color](#Color)  
  *InkWell溅墨颜色*
- colorBrightness → [Brightness](#Brightness)  
  *主题亮度*
- padding → [EdgeInsetsGeometry](#EdgeInsetsGeometry)  
  *内部填充*
- shape → [ShapeBorder](#ShapeBorder)  
  *图形边框*
- clipBehavior → [Clip](#Clip)  
  *溢出裁剪*
- focusNode → [FocusNode](https://api.flutter.dev/flutter/widgets/FocusNode-class.html)
  *获取焦点的节点*
- materialTapTargetSize → [MaterialTapTargetSize](#MaterialTapTargetSize)  
  *配置点击区的最小尺寸*
- child → Widget  
  *按钮的文本*
- icon → Widget  
  *按钮的图标*
- label → Widget  
  *按钮的文本*
