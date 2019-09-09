# Color 颜色

[参考](https://api.flutter.dev/flutter/dart-ui/Color-class.html)

## 构造函数

```dart
Color c = const Color(0xFF42A5F5);
Color c = const Color.fromARGB(0xFF, 0x42, 0xA5, 0xF5);
Color c = const Color.fromARGB(255, 66, 165, 245);
Color c = const Color.fromRGBO(66, 165, 245, 1.0);
Color c1 = const Color(0xFFFFFF); // 完全透明的白色 (隐藏)
Color c2 = const Color(0xFFFFFFFF); // 全不透明白色 (显示)
```

## 参数

- value → int  
  *十六进制颜色，颜色循序为 ARGB*
- a → int  
  *alpha 值 0(透明) ~ 255(不透明)*
- r → int  
  *红色 0 ~ 255*
- g → int  
  *绿色 0 ~ 255*
- b → int  
  *蓝色 0 ~ 255*
- opacity → double  
  *透明度 0.0 ~ 1.0*

## 属性

- Color.alpha  
  *8 bit value*
- Color.red  
  *8 bit value*
- Color.green  
  *8 bit value*
- Color.blue  
  *8 bit value*
- Color.opacity  
  *double 0.0 ~ 1.0*
- Color.value  
  *32bit value*

## 方法

- withAlpha(int a) → Color  
  *返回一个新颜色，并用参数 a 值替换 Alpha 值 0 ~ 255*
- withRed(int r) → Color  
  *返回一个新颜色，并用参数 r 值替换 红色 值 0 ~ 255*
- withGreen(int g) → Color  
  *返回一个新颜色，并用参数 g 值替换 绿色 值 0 ~ 255*
- withBlue(int b) → Color  
  *返回一个新颜色，并用参数 b 值替换 蓝色 值 0 ~ 255*
- withOpacity(double o) → Color  
  *返回一个新颜色，并用参数 o 值替换 opacity 值 0.0 ~ 1.0*
- computeLuminance() → double  
  *返回亮度值 0.0(暗) ~ 1.0(亮)*
