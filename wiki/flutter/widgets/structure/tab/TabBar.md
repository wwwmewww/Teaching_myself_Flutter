# TabBar

[参考](https://api.flutter.dev/flutter/material/TabBar-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > TabBar

## 构造函数

```dart
TabBar({
  Key key,
  @required List<Widget> tabs,
  TabController controller,
  bool isScrollable: false,
  Color indicatorColor,
  double indicatorWeight: 2.0,
  EdgeInsetsGeometry indicatorPadding: EdgeInsets.zero,
  Decoration indicator,
  TabBarIndicatorSize indicatorSize,
  Color labelColor,
  TextStyle labelStyle,
  EdgeInsetsGeometry labelPadding,
  Color unselectedLabelColor,
  TextStyle unselectedLabelStyle,
  DragStartBehavior dragStartBehavior: DragStartBehavior.start,
  ValueChanged<int> onTap
})
```

## 参数 & 属性

- tabs → List\<Widget>  
  *通常是两个或多个 Tab 部件的列表*
- controller → [TabController](TabController)  
  *tabbar部件的选择和动画状态控制器*
- isScrollable → bool  
  *是否水平滚动*
- indicatorColor → [Color](Color)  
  *显示在所选 tab 下边线的颜色*
- indicatorWeight → double  
  *显示在所选 tab 下边线的粗细*
- indicatorPadding → [EdgeInsetsGeometry](EdgeInsetsGeometry)  
  *所选 tab 下边线的水平内填充*
- indicator → [Decoration](Decoration)  
  *定义所选 tab 的外观*
- indicatorSize → [TabBarIndicatorSize](TabBarIndicatorSize)  
  *定义如何计算所选 tab 的 size*
- labelColor → [Color](Color)  
  *所选 tab 的 labbe 的颜色*
- labelStyle → [TextStyle](TextStyle)  
  *所选 tab 的 labbe 的样式*
- labelPadding → EdgeInsetsGeometry  
  *添加到每个 tab 的 label 的内填充*
- unselectedLabelColor → [Color](Color)  
  *未选 tab 的 labels 的颜色*
- unselectedLabelStyle → [TextStyle](TextStyle)  
  *未选 tab 的 labbe 的样式*
- dragStartBehavior → [DragStartBehavior](DragStartBehavior)  
  *确定处理拖动启动行为的方式*
- onTap → ValueChanged\<int>  
  *点击 tab 时调用的可选回调*
- preferredSize → [Size](Size)  
  *其 size 的高度取决于 tab 是否同时拥有 icon 和 text 的 size*
