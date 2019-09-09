# ImageFilter

图片变化(旋转,倾斜,模糊)容器

[参考](https://api.flutter.dev/flutter/dart-ui/ImageFilter-class.html)

## 构造函数

```dart
//高斯模糊
ImageFilter.blur({
  double sigmaX: 0.0,
  double sigmaY: 0.0
})

//矩阵转换
ImageFilter.matrix(
  Float64List matrix4,
  {
    FilterQuality filterQuality: FilterQuality.low
  }
)
```
