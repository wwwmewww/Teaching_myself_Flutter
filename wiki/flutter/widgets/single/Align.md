# Align 对齐部件

[参考](https://api.flutter.dev/flutter/widgets/Align-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > RenderObjectWidget > SingleChildRenderObjectWidget > Align

## 构造函数

```dart
Align({
  Key key,
  AlignmentGeometry alignment: Alignment.center,
  double widthFactor,
  double heightFactor,
  Widget child
})
```

## 参数 & 属性

- alignment → AlignmentGeometry  
  *对齐方式*
- widthFactor → double  
  *宽因子, 可大于或小于 1.0, 非负。宽=子项宽*此系数*
- heightFactor → double  
  *高因子, 可大于或小于 1.0, 非负。高=子项高*此系数*
- child → Widget  
  *子部件*

## 举个例子

```dart
Container(
  height: 120.0,
  width: 120.0,
  color: Colors.blue[50],
  child: Align(
    alignment: Alignment.topRight,
    child: FlutterLogo(
      size: 60,
    ),
  ),
)
```
