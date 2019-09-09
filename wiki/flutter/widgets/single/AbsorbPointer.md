# AbsorbPointer 阻止点击事件容器 单子容器

    ```dart
    class MyHomeScreen extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return AbsorbPointer(
          absorbing: false, //屏蔽开关
          ignoringSemantics: false, //屏幕阅读器开关
          child: ABunchOfWidgets();
        );
      }
    }
    ```
