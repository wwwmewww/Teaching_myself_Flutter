# FittedBox 适应/对齐父级的容器 单子容器

    ```dart
    MyBlueRect( //父部件
      child: FittedBox(
        fit: BoxFit.contain, //适应
        alignment: Alignment.centerLeft, //对齐
        child: MyDashPic(), //子部件
      ),
    )
    ```
