# SingleChildScrollView

[参考](https://api.flutter.dev/flutter/widgets/SingleChildScrollView-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > SingleChildScrollView

## 构造函数

```dart
SingleChildScrollView({
  Key key,
  Axis scrollDirection: Axis.vertical,
  bool reverse: false,
  EdgeInsetsGeometry padding,
  bool primary,
  ScrollPhysics physics,
  ScrollController controller,
  Widget child,
  DragStartBehavior dragStartBehavior: DragStartBehavior.start
})
```

## 参数 & 属性

- scrollDirection → Axis  
  *滚动视图滚动的轴方向*
- reverse → bool  
  *滚动视图是否沿读取方向滚动*
- padding → EdgeInsetsGeometry  
  *内填充*
- primary → bool  
  *是否与父级 PrimaryScrollController 关联的主滚动视图*
- physics → ScrollPhysics  
  *滚动视图应如何响应用户输入*
- controller → ScrollController  
  *用于控制滑动位置和滑动显示*
- child → Widget  
  *滚动的子部件*
- dragStartBehavior → DragStartBehavior  
  *定义处理拖拽启动行为的方式*

## 举个例子

```dart
Widget build(BuildContext context) {
  return LayoutBuilder(
    builder: (BuildContext context, BoxConstraints viewportConstraints) {
      return SingleChildScrollView(
        child: ConstrainedBox(
          constraints: BoxConstraints(
            minHeight: viewportConstraints.maxHeight,
          ),
          child: Column(
            mainAxisSize: MainAxisSize.min,
            mainAxisAlignment: MainAxisAlignment.spaceAround,
            children: <Widget>[
              Container(
                // A fixed-height child.
                color: const Color(0xff808000), // Yellow
                height: 120.0,
              ),
              Container(
                // Another fixed-height child.
                color: const Color(0xff008000), // Green
                height: 120.0,
              ),
            ],
          ),
        ),
      );
    },
  );
}
```
