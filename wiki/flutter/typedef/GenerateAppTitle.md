# GenerateAppTitle

[参考](https://api.flutter.dev/flutter/widgets/GenerateAppTitle.html)

用于设置 App 的全局值：Title.title。设备使用该值为用户标识 app。

参数 context 包含了 app 的 Localizations 部件，因此可以使用此方法生成本地化标题(localized title).

此函数不能返回null

```dart
String GenerateAppTitle (
  BuildContext context
)
```

举例

1. MaterialApp.onGenerateTitle

    ```dart
    onGenerateTitle: (context) {
      return 'MyGenerateTitle';
    },
    ```
