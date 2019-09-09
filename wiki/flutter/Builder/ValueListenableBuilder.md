# ValueListenableBuilder 监听值构建器 使用这个修改状态可以不用setState; 跟 15. InheritedWidget & InheritedModel 很像

    ```dart
    //简单数据
    ValueNotifier('Hello');
    ValueListenableBuilder<String>(
      valueListenable: value,
      builder: (context, value, _) {
        return Text('$value');
      }
    )
    //复杂数据
    class MyNotifier extends ValueNotifier<MyDataClass> {
      MyNotifier(MyDataClass value) : super(value);
      void changeMyData(int i) {
        value.myInt = i;
        notifyListeners();
      }
    }
    ValueListenableBuilder(
      valueListenable: myAnimation,
      child: Container(
        width:100,
        height:100,
        color:Colors.green
      ),
      builder: (context, value, child) {
        return Transform.rotate(
          angle:myAnimation.value * 2.0 * math.pi,
          child: child,
        );
      }
    )
    ```
