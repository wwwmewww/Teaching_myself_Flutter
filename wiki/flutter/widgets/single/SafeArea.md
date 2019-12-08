# SafeArea 屏幕安全区 单子容器

[参考](https://api.flutter.dev/flutter/widgets/SafeArea-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > SafeArea

## 构造函数

```dart
SafeArea({
  Key key,
  bool left: true,
  bool top: true,
  bool right: true,
  bool bottom: true,
  EdgeInsets minimum: EdgeInsets.zero,
  bool maintainBottomViewPadding: false,
  @required Widget child
})
```

## 参数 & 属性

- left → bool  
  *左部安全* 
- top → bool  
  *顶部安全*
- right → bool  
  *右部安全*
- bottom → bool  
  *底部安全*
- minimum → EdgeInsets
  *要应用的最小填充。*
- maintainBottomViewPadding → bool
  *指定当当前上下文的MediaQuery的viewinset使用时，SafeArea是否应保留viewPadding而不是padding，默认值为false。*
- child → Widget  
  *子部件*

## 举个例子

```dart
@override
Widget build(BuildContext context) {
  return Scaffold()
    body: SafeArea(
      top: true,
      bottom: true,
      left: false,
      right: false,
      child: ListView(
        children:List.generate(100,() => Text('This is some text')),
      ),
    ),
  ;
}
```
