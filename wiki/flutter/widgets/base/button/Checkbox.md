# Checkbox

选择框

[参考](https://api.flutter.dev/flutter/material/Checkbox-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > Checkbox

## 构造函数

```dart
Checkbox({
  Key key,
  @required bool value,
  bool tristate: false,
  @required ValueChanged<bool> onChanged,
  Color activeColor,
  Color checkColor,
  MaterialTapTargetSize materialTapTargetSize
})
```

## 参数 & 属性

- value → bool  
  *是否被选中*
- tristate → bool  
  *是否为三态(true,false,null)*
- onChanged → ValueChanged\<bool>  
  *更改回调*
- activeColor → [Color](#Color)  
  *选中颜色*
- checkColor → Color  
  *选中图标颜色*
- materialTapTargetSize → [MaterialTapTargetSize](#MaterialTapTargetSize)  
  *配置点击区的最小尺寸*

## 常量

- width → const double  
  *宽度* ```18.0```
