# AlignmentDirectional

[参考](https://api.flutter.dev/flutter/painting/AlignmentDirectional-class.html)

## 继承关系

> Object > AlignmentGeometry > AlignmentDirectional

## 构造函数

```dart
AlignmentDirectional(double start, double y)
```

## 参数 & 属性

- start → double  
  *水平方向上的距离。-1.0 值为起始端(即 TextDirection.ltr 的左侧边缘,TextDirection.rtl 的右侧边缘)，1.0 值为末端边缘。超出边缘的值表示在范围之外的位置*
- y → double  
  *垂直方向上的距离。-1.0 值为上边缘，1.0 值为下边缘。超出边缘的值表示在范围之外的位置*

## 常量

- bottomCenter  
  *下边的中心点*  
  ```const AlignmentDirectional(0.0, 1.0)```
- bottomEnd  
  *末端的底角*  
  ```const AlignmentDirectional(1.0, 1.0)```
- bottomStart  
  *起始端的底角*  
```const AlignmentDirectional(-1.0, 1.0)```
- center  
  *垂直和水平的中心点*  
  ```const AlignmentDirectional(0.0, 0.0)```
- centerEnd  
  *末端的中心点*  
  ```const AlignmentDirectional(1.0, 0.0)```
- centerStart  
  *起始段的中心点*  
  ```const AlignmentDirectional(-1.0, 0.0)```
- topCenter  
  *上边的中心点*  
  ```const AlignmentDirectional(0.0, -1.0)```
- topEnd  
  *末端的顶角*  
  ```const AlignmentDirectional(1.0, -1.0)```
- topStart  
  *起始端的顶角*  
  ```const AlignmentDirectional(-1.0, -1.0)```

## 方法

- add(AlignmentGeometry other) → AlignmentGeometry  
  *相加*
- resolve(TextDirection direction) → Alignment  
  *转换成 Alignment*
- toString() → String  
  *返回一个表示此对象的字符串*

## 静态方法

- lerp(AlignmentDirectional a, AlignmentDirectional b, double t) → AlignmentDirectional  
  *线性插值*
