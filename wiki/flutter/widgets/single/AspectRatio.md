# AspectRatio 比例容器 单子容器

    ```dart
    // 如 Expanded 为父级，会强制拉伸 AspectRatio
    // 只需要在 Expanded 和 AspectRatio 之间添加 Align 既可
    // Expanded 会强制拉伸 Align，但是会保持 AspectRatio的宽高比
    AspectRatio(
      aspectRatio: 3 / 2,  // 宽高比为3比2，宽3，高2
      child: MyWidget(),
    )
    ```
