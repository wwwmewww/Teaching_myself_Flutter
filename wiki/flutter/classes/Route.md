# Route

[参考](https://api.flutter.dev/flutter/widgets/Route-class.html)

## 构造函数

```dart
Route({RouteSettings settings })
```

## 参数 && 属性

- settings → [RouteSettings](/classes/RouteSettings)  
  *路由设置*
- currentResult → T  
  *当此路由被弹出(见 Navigator.pop)时，如果没有指定结果或结果为空，那么将使用这个值*
- isActive → bool  
  *此路由是否在 navigator 上*
- isCurrent → bool  
  *此路由是否是 navigator 中最上面(当前的)的路由*
- isFirst → bool  
  *此路由是否是 navigator 中最下面(第一个)的路由*
- navigator → [NavigatorState](/classes/NavigatorState)  
  *路由所在的 navigator*
- overlayEntries → List\<[OverlayEntry](/classes/OverlayEntry)>  
  *此路由的遮罩层*
- popped → Future\<T>  
  *future 在 路由从 navigator 中弹出来后完成*
- willHandlePopInternally → bool  
  *当正在调用 didPop 时，返回 false*

## 方法

- changedExternalState() → void  
  *每当 Navigator 重建其小部件时调用，以表面路由可能也希望重建*
- changedInternalState() → void  
  *每当路由的内部状态更改时调用*
- didChangeNext(Route nextRoute) → void  
  *此路由的下一个路由已改为指定的新路由。当下一个路由因任何原因发生更改时，只要它在历史记录中，包括第一次将路由添加到导航器时（例如，通过navigator.push），就会在该路由上调用该调用，但调用 didPopNext 的情况除外。如果没有下一条路线，nextRoute 将为空*
- didChangePrevious(Route previousRoute) → void  
  *此路由的前一个路由已经改为指定的新路由。只要以前的路由出于任何原因发生更改，只要它在历史记录中，就在该路由上调用它。如果没有以前的路由，则 previousRoute 将为空*
- didComplete(T result) → void  
  *路由被弹出或以其它方式被优雅的删除了*
- didPop(T result) → bool  
  *请求弹出此路由，如果路由可以在内部处理它(例：因为它有自己的内部状态栈)，那么返回 false，否则返回 true(通过return 返回调用的 super.didpop 的值)。反会 false 将阻止 NavigatorState.pop 的默认行为*
- didPopNext(Route nextRoute) → void  
  *指定路由，从 avigator 弹出它上面的路由*
- didPush() → TickerFuture  
  *当路由被推倒 navigator 上时，在 install 后调用*
- didReplace(Route oldRoute) → void  
  *当路由替换 navigator 中另一个路由时，在 install 后调用*
- dispose() → void  
  *路由应该删除遮罩层和释放任何其它资源*
- install(OverlayEntry insertionPoint) → void  
  *当路由插入到 navigator 时调用*
- willPop() → Future\<RoutePopDisposition>  
  *如果此路由要不执行 Navigator.pop,返回 false；此方法由 Navigator.maybePop 调用*
