# AlignmentGeometry

[参考](https://api.flutter.dev/flutter/painting/AlignmentGeometry-class.html)

[Alignment](Alignment) 的基类，允许 text-direction 解决问题.

此类型的属性或参数 接受使用 new [Alignment](Alignment) 及其变体 或 new [AlignmentDirectional](AlignmentDirectional)

要将不确定类型的 AlignmentGeometry 对象转换为 [Alignment](Alignment) 对象，请使用 resolve 方法

## 构造函数

```dart
AlignmentGeometry()
```

## 方法

- add(AlignmentGeometry other) → AlignmentGeometry  
  *相加*
- resolve(TextDirection direction) → Alignment  
  *转换成 Alignment*
- toString() → String  
  *返回一个表示此对象的字符串*

## 静态方法

- lerp(AlignmentGeometry a, AlignmentGeometry b, double t) → AlignmentGeometry  
  *线性插值*
