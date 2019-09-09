# Wrap 多子容器

# Wrap 流式
[目录](#toptop) [Wrap](https://api.flutter.dev/flutter/widgets/Wrap-class.html) 
```
//构建函数
Wrap({
  Key key,
  Axis direction: Axis.horizontal,
  WrapAlignment alignment: WrapAlignment.start,
  double spacing: 0.0,
  WrapAlignment runAlignment: WrapAlignment.start,
  double runSpacing: 0.0,
  WrapCrossAlignment crossAxisAlignment: WrapCrossAlignment.start,
  TextDirection textDirection,
  VerticalDirection verticalDirection: VerticalDirection.down,
  List<Widget> children: const []
})
```
参数 & 属性
- 主轴方向 direction → [Axis](#Axis)
<span id="wrapAlignment"></span>
- 主轴对齐 alignment → [WrapAlignment](#WrapAlignment)
- 主轴方向的间距 spacing → double
- 纵轴方向的间距 runSpacing → double
- 纵轴方向的对齐方式 runAlignment → [WrapAlignment](#WrapAlignment)
<span id="wrapCrossAlignment"></span>
- 纵轴对齐 crossAxisAlignment → [WrapCrossAlignment](#WrapCrossAlignment)
- 水平排序 textDirection → [TextDirection](#TextDirection)
- 垂直排序 verticalDirection → [VerticalDirection](#VerticalDirection)
- 子部件列表 children → List<Widget>
