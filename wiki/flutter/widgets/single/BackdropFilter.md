# BackdropFilter

[参考](https://api.flutter.dev/flutter/widgets/BackdropFilter-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > RenderObjectWidget > SingleChildRenderObjectWidget > BackdropFilter

## 构造函数

```dart
BackdropFilter({
  Key key,
  @required ImageFilter filter,
  Widget child
})
```

## 参数 & 属性

- filter → ImageFilter  
  *图片过滤器*
- child → Widget  
  *子部件的子部件将被过滤*

## 举个例子

```dart
Stack(children: <Widget>[
  DashWidget,
  //覆盖部分
  Positioned(top: 100, bottom: 150, left: 200, right: 100,//完全覆盖
  //Positioned.fill(
    child: BackdropFilter(
      filter: ImageFilter.blur(
        sigmaX: 5,
        sigmaY: 5,
      ),
      //child 不受影响,child 的 child 才有效果
      child: Container(
        color: Colors.black.withOpacity(0),
      ),
    )
  ),
])
```
