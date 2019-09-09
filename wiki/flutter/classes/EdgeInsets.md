# EdgeInsets
[目录](#toptop) [edgeInsets](#edgeInsets) [参考](https://api.flutter.dev/flutter/painting/EdgeInsets-class.html)
```
//构造函数
EdgeInsets.all(double value)
EdgeInsets.fromLTRB(double left, double top, double right, double bottom)
EdgeInsets.fromWindowPadding(WindowPadding padding, double devicePixelRatio)
EdgeInsets.only({double left: 0.0, double top: 0.0, double right: 0.0, double bottom: 0.0 })
EdgeInsets.symmetric({double vertical: 0.0, double horizontal: 0.0 })

//例：
const EdgeInsets.all(8.0)
const EdgeInsets.only(left: 40.0)
const EdgeInsets.symmetric(vertical: 8.0)
```
属性
- 左边偏移量 left → double
- 右边偏移量 right → double
- 上边偏移量 top → double
- 下边偏移量 bottom → double
- 左上偏移量 topLeft → [Offset](#Offset)
- 右上偏移量 topRight → [Offset](#Offset)
- 左下偏移量 bottomLeft → [Offset](#Offset)
- 右下偏移量 bottomRight → [Offset](#Offset)
- 翻转(上下/左右) flipped → EdgeInsets
- 此EdgeInsets将占用空内部的大小 collapsedSize → [Size](#Size)
- 水平方向上的总偏移量 horizontal → double
- 垂直方向上的总偏移量 vertical → double
- 每个维度是否都是非负的 isNonNegative → bool

方法
- 相加 add([EdgeInsetsGeometry](#EdgeInsetsGeometry) other) → [EdgeInsetsGeometry](#EdgeInsetsGeometry)
- 相减 subtract(EdgeInsetsGeometry other) → [EdgeInsetsGeometry](#EdgeInsetsGeometry)
- 新建拷贝并覆盖相关属性 copyWith({double left, double top, double right, double bottom }) → EdgeInsets
- 返回小于给定 rect 的新 rect deflateRect([Rect](#Rect) rect) → Rect
- 返回大于给定 rect 的新 rect inflateRect([Rect](#Rect) rect) → Rect
- 转换 resolve([TextDirection](#TextDirection) direction) → EdgeInsets

常量
- zero → const EdgeInsets<br>```const EdgeInsets.only()```
