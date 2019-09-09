# LayoutBuilder 布局建造器 在构建之前知道部件大小

    ```dart
    class HomeScreen extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        return LayoutBuilder(
          builder: (context, constraints) {
            if(constraints.maxWidth < 600) {
              return MyOneColumnLayout();
            } else {
              return MyTwoColumnLayout();
            }
          },
        );
      }
    }
    ```
