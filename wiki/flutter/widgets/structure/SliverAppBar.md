# SliverAppBar 动画标题 与 CustomScrollView 一起使用

    ```dart
    CustomScrollView(
      slivers: <Widget>[
        SliverAppBar(
          title: Text("SliverAppBar"),
          //设置展开高度
          expandedHeight: 200.0,
          //设置外观
          //flexibleSpace 与 expandedHeight 一起使用
          flexibleSpace: FlexibleSpaceBar(
            background: _expandedImage,
          )
        ),
        _oneSliver,
        _antherSliver,
        _yetAnotherSliver,
      ],
    )
    ```
