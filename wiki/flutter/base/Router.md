# 路由

## 路由表
[目录](#toptop) 
```dart
MaterialApp(
    title: 'Flutter Demo',
    theme: ThemeData(
        primarySwatch: Colors.blue,
    ),
    //默认路由(即 Navigator.defaultRouteName)
    home: MyHomePage(title: 'Flutter Demo Home Page'),
    //路由表
    routes: {
        // Map<String, WidgetBuilder> routes;
        '/': (context) => HomePage(),
        //构造函数传参
        '/room': (context) => RoomPage(roomId: "12"),
    },
);
```
## 路由传参
[目录](#toptop) 
```
//匿名路由
Navigator.push(context, MaterialPageRoute(builder: (context) {
    return NewRoute();//返回Widget
}));
//路由表路由
Navigator.of(context).pushNamed("tip2", arguments: 'txt');
//获取路由传参
ModalRoute.of(context).settings.arguments)
```
## 路由生成钩子
[目录](#toptop) 

MaterialApp有一个onGenerateRoute属性，它在打开命名路由时会可能会被调用，之所以说可能，是因为当调用Navigator.pushNamed(...)打开命名路由时，如果指定的路由名在路由表中已注册，则会调用路由表中的builder函数来生成路由组件；如果路由表中没有注册，才会调用onGenerateRoute来生成路由。onGenerateRoute回调签名如下
```
Route<dynamic> Function(RouteSettings settings)
```
有了onGenerateRoute回调，要实现上面控制页面权限的功能就非常容易：我们放弃使用路由表，取而代之的是提供一个onGenerateRoute回调，然后在该回调中进行统一的权限控制，如：
```
MaterialApp(
  ... //省略无关代码
  onGenerateRoute:(RouteSettings settings){
      return MaterialPageRoute(builder: (context){
           String routeName = settings.name;
       // 如果访问的路由页需要登录，但当前未登录，则直接返回登录页路由，
       // 引导用户登录；其它情况则正常打开路由。
     }
   );
  }
);
```
> 注意，onGenerateRoute只会对命名路由生效。


## Navigator
[目录](#toptop) 

构造函数 & 属性
```
Navigator({
  Key key,
  //初始路由
  String initialRoute,
  //被调用以生成给定RouteSettings的路由
  @required RouteFactory onGenerateRoute,
  //当onGenerateRoute无法生成路由时调用。
  RouteFactory onUnknownRoute,
  //此导航器的观察者列表
  List<NavigatorObserver> observers: const []
})
//常量 The default name for the initialRoute. '/'
defaultRouteName → const String
```
方法
- **canPop**(BuildContext context) → bool<br>判断路由栈中是否还能弹出路由，还有一个时反回false<br>例：```Navigator.canPop(context) ? Navigator.pop(context): null;```
- **maybePop**<T extends Object>(BuildContext context, [ T result ]) → Future<bool><br>能pop时pop，不能pop时不pop<br>例：```Navigator.maybePop(context);```
- **pop**<T extends Object>(BuildContext context, [ T result ]) → bool<br>将栈顶路由弹出，result 为传给上一页面的数据<br>例：```Navigator.pop(context, "我是返回值");```
- **popUntil**(BuildContext context, RoutePredicate predicate) → void<br>跳转到之前的某一页面<br>例：```Navigator.popUntil(context, ModalRoute.withName('/Dashboard'));```
- **popAndPushNamed**<T extends Object, TO extends Object>(BuildContext context, String routeName, { TO result, Object arguments }) → Future<T><br>将栈顶路由弹出，并把新的路由压入栈中<br>例：```Navigator.popAndPushNamed(context, '/newsPage',"我是返回值");```
- **of**(BuildContext context, { bool rootNavigator: false, bool nullOk: false }) → 返回实例的状态上下文<br>例：```Navigator.of(context).pop("我是返回值");```
- **push**<T extends Object>(BuildContext context, Route<T> route) → Future<T><br>将给定的路由入栈（即打开新的页面），返回值是一个Future对象，用以接收新路由出栈（即关闭）时的返回数据<br>例：```Navigator.push(context,  new MaterialPageRoute());```
- **pushNamed**<T extends Object>(BuildContext context, String routeName, { Object arguments }) → Future<T><br>将路由表中的路由入栈，返回值是一个Future对象，用以接收新路由出栈时的返回数据<br>例：```Navigator.pushNamed(context, '/news');```
- **pushAndRemoveUntil**<T extends Object>(BuildContext context, Route<T> newRoute, RoutePredicate predicate) → Future<T><br>将给定的路由入栈，并清空路由栈<br>例：```Navigator.pushAndRemoveUntil(context, '/news');```
- **pushNamedAndRemoveUntil**<T extends Object>(BuildContext context, String newRouteName, RoutePredicate predicate, { Object arguments }) → Future<T><br>将路由表中的路由入栈，并清空路由栈<br>例：```Navigator.pushNamedAndRemoveUntil(context, '/news');```
- **pushReplacement**<T extends Object, TO extends Object>(BuildContext context, Route<T> newRoute, { TO result }) → Future<T><br>用来替代当前栈中栈顶元素<br>例：```Navigator.pushReplacement(context, '/news');```
- **pushReplacementNamed**<T extends Object, TO extends Object>(BuildContext context, String routeName, { TO result, Object arguments }) → Future<T><br>用路由表中的路由来替代当前栈中栈顶元素<br>例：```Navigator.pushReplacementNamed(context, '/news');```
- **removeRoute**(BuildContext context, Route route) → void<br><br>例：```Navigator.removeRoute(context, '/news');```
- **removeRouteBelow**(BuildContext context, Route anchorRoute) → void<br><br>例：```Navigator.removeRouteBelow(context, '/news');```
- **replace**<T extends Object>(BuildContext context, { Route oldRoute, Route<T> newRoute }) → void<br><br>例：```Navigator.replace(context, '/news');```
- **replaceRouteBelow**<T extends Object>(BuildContext context, { Route anchorRoute, Route<T> newRoute }) → void<br><br>例：```Navigator.replaceRouteBelow(context, '/news');```

Navigator是一个路由管理的组件，它提供了打开和退出路由页方法。
Navigator通过一个栈来管理活动路由集合。通常当前屏幕显示的页面就是栈顶的路由。
Navigator提供了一系列方法来管理路由栈，在此我们只介绍其最常用的两个方法：

> Navigator类中第一个参数为context的静态方法都对应一个Navigator的实例方法， 比如Navigator.push(BuildContext context, Route route)等价于Navigator.of(context).push(Route route) ，下面命名路由相关的方法也是一样的。

## MaterialPageRoute
[目录](#toptop) 
```
//导航到新路由
onPressed: () async {
    // 打开`TipRoute`，并等待返回结果
    var result = await Navigator.push(
        context,
        MaterialPageRoute(
            builder: (context) {
                return TipRoute(
                    // 路由参数
                    text: "我是提示xxxx",
                );
            },
        ),
    );
    //输出`TipRoute`路由返回结果
    print("路由返回值: $result");
},
```
构造函数 & 属性
```
MaterialPageRoute({
    //是一个WidgetBuilder类型的回调函数，它的作用是构建路由页面的具体内容，返回值是一个widget。我们通常要实现此回调，返回新路由的实例。
    WidgetBuilder builder,
    //包含路由的配置信息，如路由名称、是否初始路由（首页）。
    RouteSettings settings,
    //默认情况下，当入栈一个新路由时，原来的路由仍然会被保存在内存中，如果想在路由没用的时候释放其所占用的所有资源，可以设置maintainState为false。
    bool maintainState = true,
    //表示新的路由页面是否是一个全屏的模态对话框，在iOS中，如果fullscreenDialog为true，新页面将会从屏幕底部滑入（而不是水平方向）。
    bool fullscreenDialog = false,
})
```
MaterialPageRoute继承自PageRoute类，PageRoute类是一个抽象类，表示占有整个屏幕空间的一个模态路由页面，它还定义了路由构建及切换时过渡动画的相关接口及属性。MaterialPageRoute 是Material组件库提供的组件，它可以针对不同平台，实现与平台页面切换动画风格一致的路由切换动画：
- 对于Android，当打开新页面时，新的页面会从屏幕底部滑动到屏幕顶部；当关闭页面时，当前页面会从屏幕顶部滑动到屏幕底部后消失，同时上一个页面会显示到屏幕上。
- 对于iOS，当打开页面时，新的页面会从屏幕右侧边缘一致滑动到屏幕左边，直到新页面全部显示到屏幕上，而上一个页面则会从当前屏幕滑动到屏幕左侧而消失；当关闭页面时，正好相反，当前页面会从屏幕右侧滑出，同时上一个页面会从屏幕左侧滑入。
> 如果想自定义路由切换动画，可以自己继承PageRoute来实现

## MaterialPageRoute

```dart
MaterialPageRoute({
  @required WidgetBuilder builder,
  RouteSettings settings,
  bool maintainState: true,
  bool fullscreenDialog: false
})
```

参数 & 属性

- builder → WidgetBuilder
- settings → RouteSettings
- maintainState → bool
- fullscreenDialog → bool
- barrierLabel → String
- barrierColor → [Color](/classes/Color)
- barrierDismissible → bool
- transitionDuration → Duration
- animation → Animation\<double>
- controller → AnimationController
- canPop → bool
- popped → Future\<T>
- finishedWhenPopped → bool
- completed → Future\<T>
- currentResult → T
- isActive → bool
- isCurrent → bool
- isFirst → bool
- navigator → NavigatorState
- offstage ↔ bool
- opaque → bool
- overlayEntries → List\<OverlayEntry>
- secondaryAnimation → Animation\<double>
- semanticsDismissible → bool
- subtreeContext → BuildContext
- willHandlePopInternally → bool

方法

- buildPage(BuildContext context, Animation\<double> animation, Animation\<double> secondaryAnimation) → Widget
- buildTransitions(BuildContext context, Animation\<double> animation, Animation\<double> secondaryAnimation, Widget child) → Widget
- canTransitionFrom(TransitionRoute previousRoute) → bool
- canTransitionTo(TransitionRoute nextRoute) → bool

继承方法

- addLocalHistoryEntry(LocalHistoryEntry entry) → void
- addScopedWillPopCallback(WillPopCallback callback) → void
- changedExternalState() → void
- changedInternalState() → void
- createAnimation() → Animation\<double>
- createAnimationController() → AnimationController
- createOverlayEntries() → Iterable\<OverlayEntry>
- didChangeNext(Route nextRoute) → void
- didChangePrevious(Route previousRoute) → void
- didComplete(T result) → void
- didPop(T result) → bool
- didPopNext(Route nextRoute) → void
- didPush() → TickerFuture
- didReplace(Route oldRoute) → void
- dispose() → void
- install(OverlayEntry insertionPoint) → void
- removeLocalHistoryEntry(LocalHistoryEntry entry) → void
- removeScopedWillPopCallback(WillPopCallback callback) → void
- setState(VoidCallback fn) → void
- willPop() → Future\<RoutePopDisposition>
