# Offset
[目录](#toptop) [Shadow](#Shadow)
```dart
//构造函数
Offset(double dx, double dy)
Offset.fromDirection(double direction, [ double distance = 1.0 ])
```
属性
- 偏移弧度,-PI ~ PI之间, direction → double
- 偏移幅度 distance → double
- 偏移幅度的平方 distanceSquared → double
- x偏移值, 正值向左 dx → double
- y偏移值, 正值向下 dy → double

常量
- 最大值 infinite ```const Offset(double.infinity, double.infinity)```
- 零值 zero ```const Offset(0.0, 0.0)```

方法
- 缩放 scale(double scaleX, double scaleY) → Offset
- 转换 translate(double translateX, double translateY) → Offset

静态方法
- 在两个偏移之间进行线性插值 lerp(Offset a, Offset b, double t) → Offset
