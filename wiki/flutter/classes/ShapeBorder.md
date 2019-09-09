# ShapeBorder
[目录](#toptop) [ShapeBorder](#ShapeBorder) [参考](https://api.flutter.dev/flutter/painting/ShapeBorder-class.html)
```
//构造函数
ShapeBorder()
```
属性
- 此边框两侧的宽度表示为EdgeInsets **dimensions** → EdgeInsetsGeometry

方法
- 相加 add(ShapeBorder other, { bool reversed: false }) → ShapeBorder
- 获取内路径 getInnerPath(Rect rect, { TextDirection textDirection }) → Path
- 获取外路径 getOuterPath(Rect rect, { TextDirection textDirection }) → Path
- lerpFrom(ShapeBorder a, double t) → ShapeBorder
- lerpTo(ShapeBorder b, double t) → ShapeBorder
- paint(Canvas canvas, Rect rect, { TextDirection textDirection }) → void
- 缩放 scale(double t) → ShapeBorder
