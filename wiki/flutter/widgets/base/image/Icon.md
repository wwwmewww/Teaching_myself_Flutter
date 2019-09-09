# Icon

[参考](https://api.flutter.dev/flutter/widgets/Icon-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > Icon

## 构造函数

```dart
//构造函数
Icon(
  IconData icon,
  {
    Key key,
    double size,
    Color color,
    String semanticLabel,
    TextDirection textDirection
})
```

## 参数 & 属性

- icon → [IconData](IconData)  
  *要显示的图标*
- size → double  
  *图标大小*
- color → [Color](Color)  
  *绘制图标时的颜色*
- semanticLabel → String  
  *icon 的 semanticLabel*
- textDirection → [TextDirection](TextDirection)  
  *渲染图标的方向*

## 举个例子

```dart
Icon(
  Icons.add,
  color: Colors.pink,
  size: 30.0,
)
```
