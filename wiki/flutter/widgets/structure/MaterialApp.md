# MaterialApp

[参考](https://api.flutter.dev/flutter/material/MaterialApp-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > MaterialApp

## 构造函数

```dart
MaterialApp({
    Key key,
    String title: '',
    GenerateAppTitle onGenerateTitle,
    Color color,
    ThemeData theme,
    ThemeData darkTheme,
    Widget home,
    Map<String, WidgetBuilder> routes: const {},
    String initialRoute,
    RouteFactory onGenerateRoute,
    RouteFactory onUnknownRoute,
    GlobalKey<NavigatorState> navigatorKey,
    List<NavigatorObserver> navigatorObservers: const [],
    TransitionBuilder builder,
    Locale locale,
    Iterable<LocalizationsDelegate> localizationsDelegates,
    LocaleListResolutionCallback localeListResolutionCallback,
    LocaleResolutionCallback localeResolutionCallback,
    Iterable<Locale> supportedLocales: const [Locale('en', 'US')],
    bool debugShowMaterialGrid: false,
    bool showPerformanceOverlay: false,
    bool checkerboardRasterCacheImages: false,
    bool checkerboardOffscreenLayers: false,
    bool showSemanticsDebugger: false,
    bool debugShowCheckedModeBanner: true
});
```

## 参数 & 属性

- title → String  
  *一行用于设备识别用户app的描述*
- onGenerateTitle → [GenerateAppTitle](/typedef/GenerateAppTitle)  
  *如果非null，则调用此回调函数以生成 app 的 title，否则使用title*
- color → [Color](/classes/Color)  
  *在os界面中用于app的主要颜色*
- theme → [ThemeData](/classes/ThemeData)  
  *默认主题，包含颜色、字体、形状等*
- darkTheme → [ThemeData](/classes/ThemeData)  
  *当平台专门请求黑暗主题UI时使用的 ThemeData*
- routes → Map<String, WidgetBuilder>  
  *app 的顶级路由表*
- home → Widget  
  *app 默认路径的Widget(即Navigator.defaultRouteName)*
- initialRoute → String  
  *如果构建了导航，则显示第一条路由的名称*
- onGenerateRoute → [RouteFactory](/typedef/RouteFactory)  
  *app 导航到路由时路由生成器回调*
- onUnknownRoute → [RouteFactory](/typedef/RouteFactory)  
  *当onGenerateRoute无法生成路由时调用，initialRoute除外*
- navigatorKey → GlobalKey\<[NavigatorState](/classes/NavigatorState)>  
  *创建导航(Navigator)时使用的key*
- navigatorObservers → List\<[NavigatorObserver]()>  
  *为app创建的导航(Navigator)的观察者列表*
- builder → [TransitionBuilder]()  
  *在导航上面和在其它Widget下面 创建或替换导航的Widget的构建器*
- locale → [Locale]()  
  *设置 app 的(语言)区域(Localizations Widget基于此值)*
- localizationsDelegates → Iterable\<[LocalizationsDelegate]()>  
  *app 的本地化Widget的代理*
- localeListResolutionCallback → LocaleListResolutionCallback  
  *当启动app时及用户改变设备区域时，选择 app 区域设置的回调函数*
- localeResolutionCallback → LocaleResolutionCallback  
  *null*
- supportedLocales → Iterable\<Locale>  
  *本地化的区域列表*
- debugShowMaterialGrid → bool  
  *是否显示基线网格*
- showPerformanceOverlay → bool  
  *是否显示性能面板*
- checkerboardRasterCacheImages → bool  
  *是否打开光栅缓存图像的检查板*
- checkerboardOffscreenLayers → bool  
  *是否打开渲染到屏幕外位图的图层检查板*
- showSemanticsDebugger → bool  
  *是否显示框架可访问性信息的遮罩层*
- debugShowCheckedModeBanner → bool  
  *是否在右上角显示 DEBUG*
