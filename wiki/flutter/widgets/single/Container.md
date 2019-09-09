# Container

[参考](https://api.flutter.dev/flutter/widgets/Container-class.html) 未完待续

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > Container

## 构造函数

```dart
Container({
  Key key,
  AlignmentGeometry alignment,
  EdgeInsetsGeometry padding,
  Color color,
  Decoration decoration,
  Decoration foregroundDecoration,
  double width,
  double height,
  BoxConstraints constraints,
  EdgeInsetsGeometry margin,
  Matrix4 transform,
  Widget child
})
```

## 参数 & 属性

- alignment → [AlignmentGeometry](/classes/AlignmentGeometry)
- decoration → [Decoration](/classes/Decoration)  
  *背景装饰*
- foregroundDecoration → [Decoration](/classes/Decoration)  
  *前景装饰*
- constraints → [BoxConstraints]()  
  *子部件的限制*
- margin → [EdgeInsetsGeometry]()  
  *外填充*
- padding → [EdgeInsetsGeometry]()  
  *内填充*
- transform → [Matrix4]()  
  *在绘制自身之前的矩阵转换*
- child → [Widget]()  
  *子部件*

## 方法

- build(BuildContext context) → Widget  
  *描述此部件UI部分*
- debugFillProperties(DiagnosticPropertiesBuilder properties) → void  
  *添加与节点关联的其他属性*
