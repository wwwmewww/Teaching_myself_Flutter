# AnimatedPadding 内填充动画 单子容器

    ```dart
    double padValue = 0;

    AnimatedPadding(
      padding: EdgeInsets.all(padValue),
      duration: const Duration(seconds: 1), //动画时间
      curve: Curves.easeInOut, //动画运动曲线
      child: Container(
        color: Colors.blue,
      ),
    )
    //改变 padValue 后，自动执行动画
    setState(()=> padValue = 25);
    ```
