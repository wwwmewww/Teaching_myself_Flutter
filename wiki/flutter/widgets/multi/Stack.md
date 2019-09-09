# Stack

[参考](https://api.flutter.dev/flutter/widgets/Stack-class.html) 

## 继承关系

## 构造函数

```dart
Stack({
  Key key,
  AlignmentGeometry alignment: AlignmentDirectional.topStart,
  TextDirection textDirection,
  StackFit fit: StackFit.loose,
  Overflow overflow: Overflow.clip,
  List<Widget> children: const []
})
```

## 参数 & 属性

- alignment → [AlignmentGeometry](#alignment)([AlignmentDirectional](#AlignmentDirectional))  
  *对齐方式*
- textDirection → [TextDirection](#TextDirection)  
  *排序方向*
- fit → [StackFit](#StackFit)  
  *设置未定位子项的size*
- overflow → [Overflow](#Overflow)  
  *溢出处理*
- children → List\<Widget>  
  *子部件列表*
