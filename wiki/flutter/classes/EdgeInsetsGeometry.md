# EdgeInsetsGeometry
[目录](#toptop) [edgeInsetsGeometry](#edgeInsetsGeometry) [参考](https://api.flutter.dev/flutter/painting/EdgeInsetsGeometry-class.html)
```
//构造函数
EdgeInsetsGeometry()
```
属性
<span id="edgeInsets"></span>
- EdgeInsets将占用空内部的大小 collapsedSize → [Size](#Size)
- 具有顶部和底部，左侧和右侧，以及开始和结束的翻转 flipped → EdgeInsetsGeometry
- 水平方向上的总偏移量 horizontal → double
- 垂直方向上的总偏移量 vertical → double
- 每个维度是否都是非负的 isNonNegative → bool

方法
- 相加 add(EdgeInsetsGeometry other) → EdgeInsetsGeometry
- 相减 subtract(EdgeInsetsGeometry other) → EdgeInsetsGeometry
<span id="axis"></span>
- 给定方向上的总偏移量 along([Axis](#Axis) axis) → double
- 返回小于给定size的新size，按水平和垂直方向的插入量 deflateSize([Size](#Size) size) → [Size](#Size)
- 返回大于给定size的新size，按水平和垂直方向的插入量 inflateSize([Size](#Size) size) → [Size](#Size)
- 转换 resolve(TextDirection direction) → EdgeInsets
