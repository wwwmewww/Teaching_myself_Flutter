# Rect
[目录](#toptop) [centerSlice](#centerSlice) [参考](https://api.flutter.dev/flutter/dart-ui/Rect-class.html)
```dart
//构造函数
Rect.fromCenter({
  Offset center,
  double width,
  double height
})

Rect.fromCircle({
  Offset center,
  double radius
})

Rect.fromLTRB(
  double left,
  double top,
  double right,
  double bottom
)

Rect.fromLTWH(
  double left,
  double top,
  double width,
  double height
)

Rect.fromPoints(
  Offset a,
  Offset b
)
```
属性
- 矩形上边y坐标 **top** → double
- 矩形下边y坐标 **bottom** → double
- 矩形左边x坐标 **left** → double
- 矩形右边x坐标 **right** → double
- 矩形左上角坐标 **topLeft** → Offset
- 矩形上边中点坐标 **topCenter** → Offset
- 矩形右上角坐标 **topRight** → Offset
- 矩形左边中点坐标 **centerLeft** → Offset
- 矩形中心点坐标 **center** → Offset
- 矩形右边中点坐标 **centerRight** → Offset
- 矩形左下角坐标 **bottomLeft** → Offset
- 矩形下边中点坐标 **bottomCenter** → Offset
- 矩形右下角坐标 **bottomRight** → Offset
- 矩形的宽 **width** → double
- 矩形的高 **height** → double
- 矩形的长边距离 **longestSide** → double
- 矩形的短边距离 **shortestSide** → double
- 矩形左上角和右下角之间的距离 **size** → Size
- 矩形的所有坐标是否是有限的 **isFinite** → bool
- 矩形的所有坐标是否是无限的 **isInfinite** → bool
- 是否包含非零区域,负区域为空 **isEmpty** → bool
- 矩形尺寸是否为非数 **hasNaN** → bool

常量
- largest → const Rect<br>```const Rect.fromLTRB(-_giantScalar, -_giantScalar, _giantScalar, _giantScalar)```
- zero → const Rect<br>```const Rect.fromLTRB(0.0, 0.0, 0.0, 0.0)```

方法
- 是否包含此点 contains(Offset offset) → bool
- 缩小成新矩形 deflate(double delta) → Rect
- 组合成新矩形 expandToInclude(Rect other) → Rect
- 扩大成新矩形 inflate(double delta) → Rect
- 重叠成新矩形,未重叠值未负 intersect(Rect other) → Rect
- 是否有非零重叠区域 overlaps(Rect other) → bool
- 偏移成新矩形 shift(Offset offset) → Rect
- 转换成新矩形 translate(double translateX, double translateY) → Rect
- toString() → String

静态方法
- 两个矩形之间的线性差值 lerp(Rect a, Rect b, double t) → Rect ??
