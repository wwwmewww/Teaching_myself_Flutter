# Positioned 定位部件

[目录](#toptop) [参考](https://api.flutter.dev/flutter/widgets/Positioned-class.html) 
```
//构建函数
Positioned({
  Key key,
  double left,
  double top,
  double right,
  double bottom,
  double width,
  double height,
  @required Widget child
})

Positioned.directional({
  Key key,
  @required TextDirection textDirection,
  double start,
  double top,
  double end,
  double bottom,
  double width,
  double height,
  @required Widget child
})

Positioned.fill({
  Key key,
  double left: 0.0,
  double top: 0.0,
  double right: 0.0,
  double bottom: 0.0,
  @required Widget child
})

Positioned.fromRect({
  Key key,
  Rect rect,
  @required Widget child
})

Positioned.fromRelativeRect({
  Key key,
  RelativeRect rect,
  @required Widget child
})
```
参数 & 属性
- 子项左边到Stack左边的距离 left → double
- 子项上边到Stack上边的距离 top → double
- 子项右边到Stack右边的距离 right → double
- 子项下边到Stack下边的距离 bottom → double
- 子项的宽 width → double
- 子项的高 height → double
- 子项部件 child → Widget
