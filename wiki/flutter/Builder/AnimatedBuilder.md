# AnimatedBuilder 动画构建器

    ```dart
    //先创建个动画 参考 7. FadeTransition
    final animation = Tween(
      begin: 0,
      end: 2 * pi
    ).animate(controller);

    AnimatedBuilder(
      animation: animation,
      child: FlutterLogo(),
      builder: (context, child) {
        return Transform.rotate(
          angle: animation.value,
          child: Container(),
        );
      }
    )
    ```
