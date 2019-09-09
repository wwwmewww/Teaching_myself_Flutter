# Switch

开关按钮

[参考](https://api.flutter.dev/flutter/material/Switch-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > Switch

## 构造函数

```dart
Switch({
  Key key,
  @required bool value,
  @required ValueChanged<bool> onChanged,
  Color activeColor,
  Color activeTrackColor,
  Color inactiveThumbColor,
  Color inactiveTrackColor,
  ImageProvider activeThumbImage,
  ImageProvider inactiveThumbImage,
  MaterialTapTargetSize materialTapTargetSize,
  DragStartBehavior dragStartBehavior: DragStartBehavior.start
})
//CupertinoSwitch
Switch.adaptive({
  Key key,
  @required bool value,
  @required ValueChanged<bool> onChanged,
  Color activeColor,
  Color activeTrackColor,
  Color inactiveThumbColor,
  Color inactiveTrackColor,
  ImageProvider activeThumbImage,
  ImageProvider inactiveThumbImage,
  MaterialTapTargetSize materialTapTargetSize,
  DragStartBehavior dragStartBehavior: DragStartBehavior.start
})
```

## 参数 & 属性

- value → bool  
  *是否打开*
- onChanged → ValueChanged\<bool>  
  *改变事件*
- activeColor → [Color](#Color)  
  *打开时颜色*
- activeTrackColor → [Color](#Color)  
  *打开时轨道颜色*
- inactiveThumbColor → [Color](#Color)  
  *关闭时滑块颜色*
- inactiveTrackColor → [Color](#Color)  
  *关闭时轨道颜色*
- activeThumbImage → ImageProvider  
  *打开时滑块图片*
- inactiveThumbImage → ImageProvider  
  *关闭时滑块图片*
- materialTapTargetSize → [MaterialTapTargetSize](#MaterialTapTargetSize)  
  *配置点击区的最小尺寸*
- dragStartBehavior → [DragStartBehavior](#DragStartBehavior)  
  *确定拖动开始的行为*
