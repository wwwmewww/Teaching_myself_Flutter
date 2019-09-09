# Dismissible 侧滑控件容器 单子容器 stateful使用

    ```dart
    ListView.builder(
      itemCount: items.length;
      itemBuilder: (context, i){
        //侧滑控件
        return Dismissible(
          key: ValueKey(myString),
          child: ListTile(
            title: Text(myString),
          ),
          //滑动方向
          direction: DismissDirection.vertical,
          //左滑动显示的背景
          background: Container(
            color: Colors.green,
            child: Icon(Icons.check),
          ),
          //右滑动显示的背景
          secondaryBackground: Container(
            color: Colors.red,
            child: Icon(Icons.cancel),
          ),
          //滑动后的操作
          onDismissed: (direction) {
            setState((){
              items.removeAt(i); //从列表中删除此项
            });
          }
        )
      }
    )
    ```
