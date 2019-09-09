# CircularProgressIndicator

圆形进度条

[参考](https://api.flutter.dev/flutter/material/CircularProgressIndicator-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > ProgressIndicator > CircularProgressIndicator

## 构造函数

```dart
CircularProgressIndicator({
  Key key,
  double value,
  Color backgroundColor,
  Animation<Color> valueColor, //固定颜色,用 AlwaysStoppedAnimation(Colors color)
  double strokeWidth: 4.0,
  String semanticsLabel,
  String semanticsValue
})
```

## 参数 & 属性

- value → double  
  *进度值(0.0 ~ 1.0)*
- backgroundColor → Color  
  *背景颜色*
- valueColor → Animation\<Color>  
  *进度值颜色*
- strokeWidth → double  
  *进度条宽度*
- semanticsLabel → String  
  *盲文提示*
- semanticsValue → String  
  *盲文值*

## 举个例子

```dart
//进度条显示50%
LinearProgressIndicator(
  backgroundColor: Colors.grey[200],
  valueColor: AlwaysStoppedAnimation(Colors.blue),
  value: .5,
)
```
