# ScrollController
[目录](#toptop) [scrollController](#scrollController) [参考](https://api.flutter.dev/flutter/widgets/ScrollController-class.html)
```
//构造函数
ScrollController({
  double initialScrollOffset: 0.0,
  bool keepScrollOffset: true,
  String debugLabel,
})
```
参数 & 属性
- 偏移的初始值 initialScrollOffset → double
- 每次滚动完成时，使用PageStorage保存当前滚动偏移量，并在重新创建此控制器的可滚动时恢复它 keepScrollOffset → bool
- toString()输出的文字,调试用 debugLabel → String
- 是否有任何ScrollPosition对象使用attach方法将自己附加到ScrollController hasClients → bool
- 可滚动窗口小部件的当前滚动偏移量 offset → double
- 返回附加的ScrollPosition，可以从中获取ScrollView的实际滚动偏移量 position → ScrollPosition
<span id="scrollPosition"></span>
- 当前添加的位置 positions → Iterable<[ScrollPosition](#ScrollPosition)>
- 是否注册事件 hasListeners → bool

方法
- 动画到指定位置 animateTo(double offset, { Duration duration, Curve curve }) → Future<void>
- 使用此控制器注册给定位置 attach([ScrollPosition](#ScrollPosition) position) → void
- 使用此控制器取消注册给定位置 detach([ScrollPosition](#ScrollPosition) position) → void
- 丢弃对象使用的所有资源 dispose() → void
- 将滚动位置从其当前值跳转到给定值，不进行动画，也不检查新值是否在范围内 jumpTo(double value) → void
- 注册事件 addListener(VoidCallback listener) → void
- 注销事件 removeListener(VoidCallback listener) → void
