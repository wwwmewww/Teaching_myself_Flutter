# RouteFactory

[参考](https://api.flutter.dev/flutter/widgets/RouteFactory.html)

为给定的路由设置创建路由

```dart
Route RouteFactory (
  RouteSettings settings
)
```

## 参数

- settings → [RouteSettings](/classes/RouteSettings)  
  *路由设置*

## 返回值

- [Route](/classes/Route)  
  *路由*

举例

1. MaterialApp.onGenerateRoute / MaterialApp.onUnknownRoute

    ```dart
    onGenerateRoute: (settings) {
      return 'MyGenerateTitle';
    },
    ```
