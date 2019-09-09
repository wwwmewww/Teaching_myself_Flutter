# IconButton

[参考](https://api.flutter.dev/flutter/material/IconButton-class.html)

是一个可点击的Icon，不包括文字，默认没有背景，点击后会出现背景

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > IconButton

## 构建函数

```dart
IconButton({
  Key key,
  double iconSize: 24.0,
  EdgeInsetsGeometry padding: const EdgeInsets.all(8.0),
  AlignmentGeometry alignment: Alignment.center,
  @required Widget icon,
  Color color,
  Color focusColor,
  Color hoverColor,
  Color highlightColor,
  Color splashColor,
  Color disabledColor,
  @required VoidCallback onPressed,
  FocusNode focusNode,
  String tooltip
})
```

## 参数 & 属性

- iconSize → double  
  *按钮内图标大小*
- padding → [EdgeInsetsGeometry](https://api.flutter.dev/flutter/painting/EdgeInsetsGeometry-class.html)  
  *内部填充*
- alignment → [AlignmentGeometry](#AlignmentGeometry)  
  *对齐图像; 左上角(-1.0,-1.0) 右下角(1.0,1.0)*
- icon → Widget  
  *按钮的图标*
- color → [Color](#Color)  
  *按钮填充颜色*
- focusColor → [Color](#Color)  
  *焦点按钮填充颜色*
- hoverColor → [Color](#Color)  
  *悬停按钮填充颜色*
- highlightColor → [Color](#Color)  
  *按钮的InkWell高亮颜色*
- splashColor → [Color](#Color)  
  *按钮的InkWell溅墨颜色*
- disabledColor → [Color](#Color)  
  *禁用按钮填充颜色*
- onPressed → VoidCallback  
  *点击事件*
- focusNode → [FocusNode](https://api.flutter.dev/flutter/widgets/FocusNode-class.html)  
  *获取焦点的节点*
- tooltip → String  
  *提示按下按钮时的文本*

## 举个例子

```dart
IconButton(
  icon: Icon(Icons.android),
  color: Colors.white,
  onPressed: () {
    print("filled background");
  },
)
```
