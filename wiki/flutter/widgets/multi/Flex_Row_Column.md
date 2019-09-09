# Flex & Row & Column
[目录](#toptop) [Flex](https://api.flutter.dev/flutter/widgets/Flex-class.html) [Row](https://api.flutter.dev/flutter/widgets/Row-class.html) [Column](https://api.flutter.dev/flutter/widgets/Column-class.html)
```
//构建函数
Flex({
  Key key,
  @required Axis direction,
  MainAxisAlignment mainAxisAlignment: MainAxisAlignment.start,
  MainAxisSize mainAxisSize: MainAxisSize.max,
  CrossAxisAlignment crossAxisAlignment: CrossAxisAlignment.center,
  TextDirection textDirection,
  VerticalDirection verticalDirection: VerticalDirection.down,
  TextBaseline textBaseline,
  List<Widget> children: const []
})

Row({
  Key key,
  MainAxisAlignment mainAxisAlignment: MainAxisAlignment.start,
  MainAxisSize mainAxisSize: MainAxisSize.max,
  CrossAxisAlignment crossAxisAlignment: CrossAxisAlignment.center,
  TextDirection textDirection,
  VerticalDirection verticalDirection: VerticalDirection.down,
  TextBaseline textBaseline,
  List<Widget> children: const []
})

Column({
  Key key,
  MainAxisAlignment mainAxisAlignment: MainAxisAlignment.start,
  MainAxisSize mainAxisSize: MainAxisSize.max,
  CrossAxisAlignment crossAxisAlignment: CrossAxisAlignment.center,
  TextDirection textDirection,
  VerticalDirection verticalDirection: VerticalDirection.down,
  TextBaseline textBaseline,
  List<Widget> children: const []
})
```
参数 & 属性
- 主轴方向 direction → [Axis](#Axis)
<span id="mainAxisAlignment"></span>
- 主轴对齐 mainAxisAlignment → [MainAxisAlignment](#MainAxisAlignment)
<span id="mainAxisSize"></span>
- 主轴size mainAxisSize → [MainAxisSize](#MainAxisSize)
<span id="crossAxisAlignment"></span>
- 纵轴对齐 crossAxisAlignment → [CrossAxisAlignment](#CrossAxisAlignment)
- 水平排列顺序 textDirection → [TextDirection](#TextDirection)
<span id="verticalDirection"></span>
- 纵向排列顺序 verticalDirection → [VerticalDirection](#VerticalDirection)
<span id="textBaseline"></span>
- 基线对齐 textBaseline → [TextBaseline](#TextBaseline)
- 子部件列表 children → List<Widget>
