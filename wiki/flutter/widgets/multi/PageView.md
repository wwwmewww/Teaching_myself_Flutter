# PageView 页面展示 多子容器

    ```dart
    final controller = PageControoler(
      initialPage: 1, //设定初始页面
    );
    final pageView = PageView(
      controller: controller, //设置 控制器
      scrollDirection: Axis.vertical, //设置 滑动方向
      children: <Widget>[
        MyPage1Widget(),
        MyPage2Widget(),
        MyPage3Widget(),
      ],
    ),
    ```
