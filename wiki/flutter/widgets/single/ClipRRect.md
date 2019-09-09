# ClipRRect 切圆角矩形 单子容器 RenderObject

    ```dart
    // ClipOval 圆形剪切容器
    // ClipPath 路径剪切器
    ClipRRect(
      //圆角半径
      borderRadius: BorderRadius.circular(15.0),
      //剪切行为 是否启用抗锯齿
      clipBehavior: Clip.hardEdge,
      child: MyDashPicWidget(),
    );
    ```
