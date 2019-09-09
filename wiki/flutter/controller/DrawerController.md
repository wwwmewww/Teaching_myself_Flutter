# DrawerController

[参考](https://api.flutter.dev/flutter/material/DrawerController-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > DrawerController

## 构造函数

```dart
DrawerController({
  GlobalKey<State<StatefulWidget>> key,
  @required Widget child,
  @required DrawerAlignment alignment,
  DrawerCallback drawerCallback,
  DragStartBehavior dragStartBehavior: DragStartBehavior.start,
  Color scrimColor
})
```

## 参数 & 属性

- child → Widget  
  *子部件*
- alignment → [DrawerAlignment](DrawerAlignment)  
  *抽屉的对齐方式*
- drawerCallback → [DrawerCallback](DrawerCallback)  
  *当抽屉打开或关闭时调用的可选回调*
- dragStartBehavior → [DragStartBehavior](DragStartBehavior)  
  *确定处理拖动启动行为的方式*
- scrimColor → [Color](Color)  
  *用于在抽屉打开时隐藏主要内容的屏幕的颜色*
