# InputBorder
[目录](#toptop) [inputBorder](#inputBorder) [参考](https://api.flutter.dev/flutter/material/InputBorder-class.html)
```
//构造函数
InputBorder({BorderSide borderSide: BorderSide.none })
```
参数 & 属性
- borderSide → [BorderSide](#BorderSide)
- isOutline → bool
- dimensions → [EdgeInsetsGeometry](#EdgeInsetsGeometry)

常量
- none → const InputBorder<br>```const _NoInputBorder()```

方法
- copyWith({[BorderSide](#BorderSide) borderSide }) → [InputBorder](#InputBorder)
- paint(Canvas canvas, Rect rect, { double gapStart, double gapExtent: 0.0, double gapPercentage: 0.0, [TextDirection](#TextDirection) textDirection }) → void
- add([ShapeBorder](#ShapeBorder) other, { bool reversed: false }) → [ShapeBorder](#ShapeBorder)
- getInnerPath(Rect rect, { [TextDirection](#TextDirection) textDirection }) → Path
- getOuterPath(Rect rect, { [TextDirection](#TextDirection) textDirection }) → Path
- lerpFrom([ShapeBorder](#ShapeBorder) a, double t) → [ShapeBorder](#ShapeBorder)
- lerpTo([ShapeBorder](#ShapeBorder) b, double t) → [ShapeBorder](#ShapeBorder)
- scale(double t) → [ShapeBorder](#ShapeBorder)
