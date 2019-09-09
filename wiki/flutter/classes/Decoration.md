# Decoration

[参考](https://api.flutter.dev/flutter/painting/Decoration-class.html)

对装饰盒子的装饰(应用于矩形的装饰)

这个类为所有装饰提供抽象接口。具体示例请参见 BoxDecoration

要实际绘制装饰，请使用 createBoxPainter 方法获取 BoxPainter。装饰对象可以在盒子之间共享；BoxPainter对象可以缓存资源，以使更快地在特定表面上的绘制。

## 继承关系

> Object > Diagnosticable > Decoration

## 构造函数

```dart
Decoration()
```

## 属性

- isComplex → bool  
  *装饰是否复杂。可以从缓存它绘制获益*
- padding → EdgeInsetsGeometry  
  *返回 在包含内容的盒子上正在使用装饰，以便插入的内容不会遮挡装饰的边缘*

## 方法

- createBoxPainter([VoidCallback onChanged ]) → BoxPainter
  *返回将绘制此装饰的BoxPainter*
- debugAssertIsValid() → bool
  *在检查模式下，如果对象不在有效配置中，则引发异常。否则，返回true*
- hitTest(Size size, Offset position, { TextDirection textDirection }) → bool
  *测试给定大小的矩形上的给定点是否会被视为击中装饰。例如，如果装饰仅绘制一个圆，则如果点位于圆内，则此函数可能返回true，否则返回false*
- lerpFrom(Decoration a, double t) → Decoration
  *从另一个装饰（可能属于不同的类别）线性插值到这个*
- lerpTo(Decoration b, double t) → Decoration
  *从这个线性插值到另一个装饰（可能属于不同的类别）*
- toStringShort() → String

## 静态方法

- lerp(Decoration a, Decoration b, double t) → Decoration  
  *线性插值*
