# OverlayEntry

[参考](https://api.flutter.dev/flutter/widgets/OverlayEntry-class.html) 未完待续

## 构建函数

```dart
OverlayEntry({
  @required WidgetBuilder builder,
  bool opaque: false,
  bool maintainState: false
})
```

## 参数 & 属性

- builder → WidgetBuilder  
  *This entry will include the widget built by this builder in the overlay at the entry's position.  
  这个条目将包括这个构建器在条目位置的覆盖中构建的小部件。*
- opaque ↔ bool  
  *Whether this entry occludes the entire overlay.  
  此条目是否覆盖整个覆盖*
- maintainState ↔ bool  
  *Whether this entry must be included in the tree even if there is a fully opaque entry above it.  即使在其上方存在完全不透明的条目，此条目是否必须包含在树中*

## 方法

- markNeedsBuild() → void  
  *Cause this entry to rebuild during the next pipeline flush.  
  导致此条目在下次管道刷新期间重新生成。*
- remove() → void  
  *Remove this entry from the overlay.  
  从遮罩中删除这个 entry*
