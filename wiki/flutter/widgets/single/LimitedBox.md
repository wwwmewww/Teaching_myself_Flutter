# LimitedBox 大小限制容器 单子容器

    ```dart
    Container(
      height: 300,
      width: 300,
      //当父部件未约束大小时, 会保持其设定大小
      //当父部件约束大小时, LimitedBox 无效
      //因此当 LimitedBox 作为 ListView 的唯一 item 时，会变得无限大
      child: LimitedBox(
        maxHeight: 150,
        maxWidth: 150,
        child: Container(
          color: Colors.green,
        ),
      ),
    )

    ListView(
      children: <Widget>[
        for(var i=0; i<10; i++){
          LimitedBox(
            maxHeight: 200,
            child: child: Container(
              color: randomColor(),
            ),
          ),
        }
      ]
    )
    ```
