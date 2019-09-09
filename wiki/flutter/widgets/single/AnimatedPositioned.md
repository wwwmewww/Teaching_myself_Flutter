# AnimatedPositioned 部件定位动画 单子容器

    ```dart
    bool showMessage = false;

    Stack(
      children: [
        Positioned(
          bottom: 10,
          right: 10,
          child: MessageWidget(widget.message),
        ),
        AnimatedPositioned(
          duration: Duration(milliseconds: 500),
          bottom: showMessage ? 70 : 10,
          right: 10,
          child: BlockerWidget(),
        ),
      ],
    )
    //改变 showMessage 后，自动执行动画
    setState(()=> showMessage = true);
    ```
