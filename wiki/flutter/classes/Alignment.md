# Alignment

[参考](https://api.flutter.dev/flutter/painting/Alignment-class.html)

## 继承关系

> Object > AlignmentGeometry > Alignment

## 构造函数

```dart
Alignment(double x, double y)
```

## 参数 & 属性

- x → double  
  *水平方向的距离。-1.0 值为左边缘，1.0 值为右边缘；超出边缘的值表示在范围之外的位置*
- y → double  
  *垂直方向的距离。-1.0 值为上边缘，1.0 值为下边缘；超出边缘的值表示在范围之外的位置*

## 常量

- bottomCenter  
  *下居中*  
  ```const Alignment(0.0, 1.0)```
- bottomLeft  
  *下居左*  
  ```const Alignment(-1.0, 1.0)```
- bottomRight  
  *下居右*  
  ```const Alignment(1.0, 1.0)```
- center  
  *居中*  
  ```const Alignment(0.0, 0.0)```
- centerLeft  
  *中居左*  
  ```const Alignment(-1.0, 0.0)```
- centerRight  
  *中居右*  
  ```const Alignment(1.0, 0.0)```
- topCenter  
  *上居中*  
  ```const Alignment(0.0, -1.0)```
- topLeft  
  *上居左*  
  ```const Alignment(-1.0, -1.0)```
- topRight  
  *上居右*  
  ```const Alignment(1.0, -1.0)```

## 方法

- add(AlignmentGeometry other) → AlignmentGeometry  
  *相加*
- alongOffset(Offset other) → Offset  
  *返回该分数在给定偏移量方向上的偏移量*
- alongSize(Size other) → Offset  
  *返回此分数在给定大小(size)内的偏移量*
- inscribe(Size size, Rect rect) → Rect  
  *返回给定大小(size)的矩形，按此对齐方式在给定矩形内对齐*
- resolve(TextDirection direction) → Alignment  
  *转换成 Alignment*
- withinRect(Rect rect) → Offset  
  *返回给定矩形内此分数的点*
- toString() → String

## 静态方法

- lerp(Alignment a, Alignment b, double t) → Alignment  
  *线性插值*
