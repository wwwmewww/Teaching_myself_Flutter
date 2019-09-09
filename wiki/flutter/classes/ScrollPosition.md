# ScrollPosition ？？
[目录](#toptop) [scrollPosition](#scrollPosition) [参考](https://api.flutter.dev/flutter/widgets/ScrollPosition-class.html)
```
//构造函数
ScrollPosition({
  @required ScrollPhysics physics,
  @required ScrollContext context,
  bool keepScrollOffset: true,
  ScrollPosition oldPosition,
  String debugLabel
})
```
参数 & 属性
- 滚动位置应如何响应用户输入 physics → ScrollPhysics
- 滚动发生的地方 context → ScrollContext
- 使用PageStorage保存当前滚动偏移量，并在重新创建此滚动位置的可滚动时恢复它 keepScrollOffset → bool
- 目前有效的ScrollActivity activity → ScrollActivity
- 是否允许视口隐式更改像素以响应对RenderObject.showOnScreen的调用 allowImplicitScrolling → bool
- toString()输出的文字 debugLabel → String
- haveDimensions → bool
- 如果滚动正在进行，则通知程序的值为true;如果滚动位置为空闲，则为false isScrollingNotifier → ValueNotifier<bool>
- 像素的最大范围内值 maxScrollExtent → double
- 像素的最小范围内值 minScrollExtent → double
- 在轴方向的相反方向上偏移子项的像素数 pixels → double
- 沿axisDirection的视口范围 viewportDimension → double
- 像素值是否恰好位于minScrollExtent或maxScrollExtent atEdge → bool
- 滚动视图滚动的轴 axis → Axis
- 滚动视图滚动的方向 axisDirection → AxisDirection
- extentAfter → double
- extentBefore → double
- extentInside → double
- hasListeners → bool
- outOfRange → bool
- userScrollDirection → ScrollDirection

方法
- applyNewDimensions() → void
- applyViewportDimension(double viewportDimension) → bool
- beginActivity(ScrollActivity newActivity) → void
- correctBy(double correction) → void
- correctPixels(double value) → void
- didEndScroll() → void
- didOverscrollBy(double value) → void
- didStartScroll() → void
- didUpdateScrollDirection(ScrollDirection direction) → void
- didUpdateScrollPositionBy(double delta) → void
- dispose() → void
- drag(DragStartDetails details, VoidCallback dragCancelCallback) → Drag
- ensureVisible(RenderObject object, { double alignment: 0.0, Duration duration: Duration.zero, Curve curve: Curves.ease }) → Future<void>
- forcePixels(double value) → void
- hold(VoidCallback holdCancelCallback) → ScrollHoldController
- jumpTo(double value) → void
- moveTo(double to, { Duration duration, Curve curve, bool clamp: true }) → Future<void>
- notifyListeners() → void
- restoreScrollOffset() → void
- saveScrollOffset() → void
- setPixels(double newPixels) → double
- copyWith({double minScrollExtent, double maxScrollExtent, double pixels, double viewportDimension, AxisDirection axisDirection }) → ScrollMetrics
- removeListener(VoidCallback listener) → void
