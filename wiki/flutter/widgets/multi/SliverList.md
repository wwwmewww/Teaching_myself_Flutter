# SliverList & SliverGrid 一起使用滚动的列表和网格
    - ListView 分别滚动的列表
    - GridView 分别滚动的网格

    ```dart
    SliverList(
      //提供列表中的项目
      delegate: SliverChildListDelegate([
        widget,
        anotherWidget,
        yetAnotherWidget,
      ]),
      //或者用builder构建它们
      delegate: SliverChildBuilderDelegate((BuildContext context, int index) {
        return aWidget;
      }),
    );
    ```
