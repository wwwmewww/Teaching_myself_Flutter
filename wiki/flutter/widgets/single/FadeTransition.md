# FadeTransition 淡入淡出动画 单子容器

   ```dart
   // 包装在  StatefulWidget 中
   class MyFadeIn extends StatefulWidget {
     final Widget child;
     MyFadeIn({@required this.child});

     @override
     _MyFadeInState createState() => _MyFadeInState();
   }
   // 要在 状态类中 with SingleTickerProviderStateMixin
   class _MyFadeInState extends State<MyFadeIn> with SingleTickerProviderStateMixin {
     // 1. 创建动画控制器
     AnimationController _controller;
     // 2. 创建动画变化数值
     Animation _animation;
     // 3. 初始化 控制器 和 变化数值
     @override
     void initState() {
       _controller = AnimationController(
         vsync: this,
         duration: Duration(seconds: 2),
       );
       _animation = Tween(
         begin: 0.0,
         end: 1.0,
       ).animate(controller);
     }
     // 4. 释放 控制器
     @override
     dispose() {
       _controller.dispose();
       super.dispose();
     }
     @override
     Widget build(BuildContext context) {
       // 5. 启动动画
       _controller.forward();
       // 6. 执行动画的容器
       return FadeTransition( //淡入淡出动画容器
         opacity: _animation, //透明度
         child: widget.child,
       );
     }
   }
   ```
