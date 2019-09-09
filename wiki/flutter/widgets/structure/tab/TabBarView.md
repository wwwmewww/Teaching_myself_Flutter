# TabBarView

[参考](https://api.flutter.dev/flutter/material/TabBarView-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > TabBarView

## 构造函数

```dart
TabBarView({
  Key key,
  @required List<Widget> children,
  TabController controller,
  ScrollPhysics physics,
  DragStartBehavior dragStartBehavior: DragStartBehavior.start
})
```

## 参数 & 属性

- children → List\<Widget>  
  *每个 tab 对应一个 Widget*
- controller → [TabController](TabController)
  *tabbar部件的选择和动画状态控制器*
- physics → [ScrollPhysics](ScrollPhysics)  
  *页面视图应如何相应用户输入*
- dragStartBehavior → [DragStartBehavior](DragStartBehavior)  
  *确定处理拖动启动行为的方式*
