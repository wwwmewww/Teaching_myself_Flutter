# ScrollPhysics ？？
[目录](#toptop) [scrollPhysics](#scrollPhysics) [参考](https://api.flutter.dev/flutter/widgets/ScrollPhysics-class.html)
```
//构造函数
ScrollPhysics({ScrollPhysics parent })
```
参数 & 属性
- 如果为非null，则确定每个方法的默认行为 parent → ScrollPhysics
- 是否允许视口在响应对RenderObject.showOnScreen的调用时隐式更改其滚动位置 allowImplicitScrolling → bool
- 像素距离拖动的最小量必须移动以在第一次开始运动时或在每次拖动运动停止之后开始运动 dragStartDistanceMotionThreshold → double
- 滚动速度幅度将被钳制到该值 maxFlingVelocity → double
- 输入指针拖动必须移动到的最小距离才被视为滚动拖动手势 minFlingDistance → double
- 输入指针拖动的最小速度被视为滚动拖动 minFlingVelocity → double
- 用于弹道模拟的弹簧 spring → SpringDescription
- 用于弹道模拟的容差 tolerance → Tolerance

方法
- applyBoundaryConditions(ScrollMetrics position, double value) → double
- applyPhysicsToUserOffset(ScrollMetrics position, double offset) → double
- applyTo(ScrollPhysics ancestor) → ScrollPhysics
- buildParent(ScrollPhysics ancestor) → ScrollPhysics
- carriedMomentum(double existingVelocity) → double
- createBallisticSimulation(ScrollMetrics position, double velocity) → Simulation
- shouldAcceptUserOffset(ScrollMetrics position) → bool

