
# Offstage

通过一个参数，来控制child是否显示

- 当offstage为true，当前控件不会被绘制在屏幕上，不会响应点击事件，也不会占用空间；
- 当offstage为false，当前控件则跟平常用的控件一样渲染绘制；

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > RenderObjectWidget > SingleChildRenderObjectWidget > Offstage

## 构造函数

```dart
Offstage({
  Key key,
  bool offstage: true,
  Widget child
})
```

### 参数 & 属性

- offstage → bool  
  *是否隐藏子项。这种隐藏是不占用显示空间的，  
  但是并不会停止动画的运行。无论动画是否可见，都会消耗电池和占用cpu  
  如果不在需要了，删除比隐藏更好*  
- child → Widget  
  *子部件*
