# OutlineButton

边框按钮。默认有一个边框，不带阴影且背景透明。按下后，边框颜色会变亮、同时出现背景和阴影(较弱)

[参考](https://api.flutter.dev/flutter/material/OutlineButton-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > MaterialButton > OutlineButton

## 构造函数

```dart
OutlineButton({
  Key key,
  @required VoidCallback onPressed,
  ButtonTextTheme textTheme,
  Color textColor,
  Color disabledTextColor,
  Color color,
  Color focusColor,
  Color hoverColor,
  Color highlightColor,
  Color splashColor,
  double highlightElevation,
  BorderSide borderSide,
  Color disabledBorderColor,
  Color highlightedBorderColor,
  EdgeInsetsGeometry padding,
  ShapeBorder shape,
  Clip clipBehavior,
  FocusNode focusNode,
  Widget child
})
//带图标
OutlineButton.icon({
  Key key,
  @required VoidCallback onPressed,
  ButtonTextTheme textTheme,
  Color textColor,
  Color disabledTextColor,
  Color color,
  Color focusColor,
  Color hoverColor,
  Color highlightColor,
  Color splashColor,
  double highlightElevation,
  Color highlightedBorderColor,
  Color disabledBorderColor,
  BorderSide borderSide,
  EdgeInsetsGeometry padding,
  ShapeBorder shape,
  Clip clipBehavior,
  FocusNode focusNode,
  @required Widget icon,
  @required Widget label
})
```

## 参数 & 属性

- **onPressed** → VoidCallback  
  *点击事件*
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
  *按钮的InkWell高亮颜色*
- splashColor → [Color](#Color)  
  *按钮的InkWell溅墨颜色*
- highlightElevation → double  
  *按钮按下时相对于父级的z坐标*
- borderSide → [BorderSide](#BorderSide)  
  *未按下时边框颜色,宽度,样式*
- highlightedBorderColor → [Color](#Color)  
  *按下按钮时边框颜色*
- disabledBorderColor → [Color](#Color)  
  *禁用按钮时边框颜色*
- padding → [EdgeInsetsGeometry](https://api.flutter.dev/flutter/painting/EdgeInsetsGeometry-class.html)
  *内部填充*
- shape → [ShapeBorder](https://api.flutter.dev/flutter/painting/ShapeBorder-class.html)  
  *图形边框*
- clipBehavior → [Clip](#Clip)  
  *溢出裁剪*
- focusNode → [FocusNode](https://api.flutter.dev/flutter/widgets/FocusNode-class.html)  
  *获取焦点的节点*
- child → Widget  
  *按钮的文本*
- icon → Widget  
  *按钮的图标*
- label → Widget  
  *按钮的文本*
