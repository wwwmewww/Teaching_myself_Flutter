# Semantics 描述 UI，用于屏幕阅读器和搜索引擎，其它语义分析工具 单子容器

    ```dart
    Semantics(
      label: 'An image of $name.', //文本描述
      enabled: true, //是否启用或关闭部件
      readOnly: true, //仅限只读或时输入
      child: FaceImage(
        file: '$name.png',
      ),
    )
    ```
