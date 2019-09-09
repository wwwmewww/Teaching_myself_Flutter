# RouteSettings

[参考](https://api.flutter.dev/flutter/widgets/RouteSettings-class.html)

## 构造函数

```dart
RouteSettings({
  String name,
  bool isInitialRoute: false,
  Object arguments
})
```

## 参数 & 属性

- name → String  
  *路由的名字(例："/settings")*
- isInitialRoute → bool  
  *此路由是否是第一条推到 Navigator 上的路由*
- arguments → Object  
  *传递给路由的参数*

## 方法

- copyWith({String name, bool isInitialRoute, Object arguments }) → RouteSettings  
  *创建此路由设置对象的副本，并将给定字段替换为新值。*
