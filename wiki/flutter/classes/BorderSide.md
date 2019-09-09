# BorderSide
[目录](#toptop) [borderSide](#borderSide) [参考](https://api.flutter.dev/flutter/painting/BorderSide-class.html)
```dart
//构造函数
BorderSide({
  Color color: const Color(0xFF000000),
  double width: 1.0,
  BorderStyle style: BorderStyle.solid
})
//例:
BorderSide(width: 16.0, color: Colors.lightBlue.shade50)
```
参数 & 属性
- 边框颜色 color → [Color](#Color)
- 边框宽度 width → double
<span id="borderStyle"></span>
- 边框样式 style → [BorderStyle](#BorderStyle)

常量
- none → const BorderSide<br>```const BorderSide(width: 0.0, style: BorderStyle.none)```

方法
- 新建副本并替换相关属性 copyWith({Color color, double width, BorderStyle style }) → BorderSide
- 新建副本并按t缩放 scale(double t) → BorderSide
- toPaint() → Paint
- toString() → String

静态方法
- 能否合并 canMerge(BorderSide a, BorderSide b) → bool
- 线性插值 lerp(BorderSide a, BorderSide b, double t) → BorderSide
- 合并两个边框属性 merge(BorderSide a, BorderSide b) → BorderSide