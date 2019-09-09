# InheritedModel 深度嵌套的部件 访问顶部附近的数据

    ```dart
    class MyAncestor extends InheritedModel {
      const MyAncestor(
        this.colorOne,
        this.colorTwo,
        Widget child,
      ) : super(child: child);

      final Color colorOne;
      final Color colorTwo;

      @override
      bool updateShouldNotify(MyAncestor oldWidget) {
        //如果替换了InheritedWidget，return 决定依赖的部件是否 rebuild
        return colorOne != oldWidget.colorOne || colorTwo != oldWidget.colorTwo;
      }

      @override
      bool updateShouldNotifyDependent(MyAncestor oldWidget, Set<String> dependencies) {
        if(dependencies.contains('one') && colorOne != oldWidget.colorOne) {
          return true;
        }
        if(dependencies.contains('two') && colorTwo != oldWidget.colorTwo) {
          return true;
        }
        return false;
      }
    }

    //子部件
    class ColorOneWidget extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        //继承 InheritedModel 中某个属性，当此属性变化时，此部件会 rebuild
        final ancestor = InheritedModel.inheritFrom<MyAncestor>(context, aspect:'one');
        return Container(
          color: ancestor.colorOne; //访问属性
          height: 50.0,
          width: 50.0,
        );
      }
    }
    ```
