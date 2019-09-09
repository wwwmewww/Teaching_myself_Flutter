# SliverGrid 一起使用滚动的列表和网格
    - ListView 分别滚动的列表
    - GridView 分别滚动的网格

    ```dart
    //指定项目数
    SliverGrid.count(
      children: scrollItems,
      //指定纵轴显示4列
      crossAxisCount: 4,
    )
    //指定网格最大项目数
    SliverGrid.extent(
      crossAxisExtent: 90.0,
    )
    ```
