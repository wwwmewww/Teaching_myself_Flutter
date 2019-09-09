# AnimatedSwitcher 部件切换动画

    ```dart
    AnimatedSwitcher(
      duration: const Duration(seconds: 1),
      transitionBuilder: (Widget child, Animation<double> animation) => ScaleTransition( child: child, scale: animation),
      child: _myAnimatedWidget,
    )
    //elsewhere in the code
    //如果类型相同 用 ValueKey 区别
    setState(()=> _myAnimatedWidget = DefferentWidget())
    ```
