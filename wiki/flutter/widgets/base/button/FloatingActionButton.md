# FloatingActionButton

浮动按钮

[参考](https://api.flutter.dev/flutter/material/FloatingActionButton-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > FloatingActionButton

## 构造函数

```dart
FloatingActionButton({
  Key key,
  Widget child,
  String tooltip,
  Color foregroundColor,
  Color backgroundColor,
  Color focusColor,
  Color hoverColor,
  Object heroTag: const _DefaultHeroTag(),
  double elevation,
  double focusElevation,
  double hoverElevation,
  double highlightElevation,
  double disabledElevation,
  @required VoidCallback onPressed,
  bool mini: false,
  ShapeBorder shape,
  Clip clipBehavior: Clip.none,
  FocusNode focusNode,
  MaterialTapTargetSize materialTapTargetSize,
  bool isExtended: false
})

FloatingActionButton.extended({
  Key key,
  String tooltip,
  Color foregroundColor,
  Color backgroundColor,
  Color focusColor,
  Color hoverColor,
  Object heroTag: const _DefaultHeroTag(),
  double elevation,
  double focusElevation,
  double hoverElevation,
  double highlightElevation,
  double disabledElevation,
  @required VoidCallback onPressed,
  ShapeBorder shape,
  bool isExtended: true,
  MaterialTapTargetSize materialTapTargetSize,
  Clip clipBehavior: Clip.none,
  FocusNode focusNode,
  Widget icon,
  @required Widget label
})
```

## 参数 & 属性

- child → Widget  
  *子部件*
- tooltip → String  
  *按下时的提示*
- foregroundColor → [Color](#Color)  
- *图标和文字的颜色*
- backgroundColor → [Color](#Color)  
  *按钮背景填充颜色*
- focusColor → [Color](#Color)  
  *焦点按钮填充颜色*
- hoverColor → [Color](#Color)  
  *悬停按钮填充颜色*
- heroTag → Object  
  *Hero部件的标记*
- elevation → double  
  *相对于父级的z坐标,默认6,非负*
- focusElevation → double  
  *聚焦时相对于父级的z坐标,默认8,非负*
- hoverElevation → double  
  *悬停时相对于父级的z坐标,默认8,非负*
- highlightElevation → double  
  *按下时相对于父级的z坐标,默认12,非负*
- disabledElevation → double  
  *禁用时相对于父级的z坐标,默认6,非负*
- onPressed → VoidCallback  
  *点击事件*
- mini → bool  
  *控制按钮的大小*
- shape → [ShapeBorder](#ShapeBorder)  
  *图形边框*
- isExtended → bool  
  *是extended创建的为true*
- materialTapTargetSize → [MaterialTapTargetSize](#MaterialTapTargetSize)  
  *配置点击区的最小尺寸*
- clipBehavior → [Clip](#Clip)  
  *溢出裁剪*
- focusNode → [FocusNode](https://api.flutter.dev/flutter/widgets/FocusNode-class.html)  
  *获取焦点的节点*
- icon → Widget  
  *图标*
- label → Widget  
  *文本*

## 举个例子

```dart
Widget build(BuildContext context) {
  return Scaffold(
    appBar: AppBar(title: Text('Floating Action Button Sample')),
    body: Center(child: Text('Press the extended button below!')),
    floatingActionButton: FloatingActionButton.extended(
      onPressed: () {},
      label: Text('Approve'),
      icon: Icon(Icons.thumb_up),
      backgroundColor: Colors.pink,
    ),
    bottomNavigationBar: BottomNavigationBar(
      color: Colors.yellow,
      child Container(height: 50.0),
      // 在 BottomNavigationBar 中嵌入
      // FloatingActionButtonLocation.centerDocked 中间
      // FloatingActionButtonLocation.endDocked 末端
      floatingActionButtonLocation: FloatingActionButtonLocation.endDocked,
    )
  );
}
```
