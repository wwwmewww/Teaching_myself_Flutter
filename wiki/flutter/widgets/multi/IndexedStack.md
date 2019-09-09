# IndexedStack 切换堆叠部件 多子容器

    ```dart
    int _widgetIndex = 0;

    IndexedStack(
      index: _widgetIndex,
      children: [
        WidgetOne(),
        WidgetTwo(),
      ],
    )
    //改变 _widgetIndex 后，切换显示顺序
    setState(()=> _widgetIndex = 1);
    ```
