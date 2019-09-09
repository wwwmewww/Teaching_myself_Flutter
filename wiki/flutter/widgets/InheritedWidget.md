# InheritedWidget

    ```dart
    class MyAncestor extends InheritedWidget {
      const MyAncestor(
        this.colorOne,
        this.colorTwo,
        Widget child,
      ) : super(child: child);

      final Color colorOne;
      final Color colorTwo;

      //方法一
      static MyAncestor of(BuildContext context) => context.inheritFromWidgetOfExactType(MyAncestor) as MyAncestor;

      //方法二
      @override
      bool updateShouldNotify(MyAncestor oldWidget) {
        //如果替换了InheritedWidget，return 决定依赖的部件是否 rebuild
        return colorOne != oldWidget.colorOne || colorTwo != oldWidget.colorTwo;
      }
    }

    //子部件
    class ColorOneWidget extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        //方法一
        var ancestor = MyAncestor.of(context);
        //方法二 继承 InheritedWidget 如果属性改变 则会 rebuild 此部件
        final ancestor = context.inheritFromWidgetOfExactType(MyAncestor);
        return Container(
          color: ancestor.colorOne; //访问属性
          height: 50.0,
          width: 50.0,
        );
      }
    }
    ```
