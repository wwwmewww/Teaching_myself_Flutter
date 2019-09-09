# AnimatedList 动画列表 用作列表中添加删除等动画

    ```dart
    AnimatedList(
      key: _myListKey,
      initialItemCount: _myItems.length,
      itemBuilder: (context, index, animation) {
        //普通构建
        return MyListItem(_myItems[index]);
        //动画构建
        return SlideTransition(
          position:animation.drive(MyTween()),
          child: MyListItem(_myItems[index]),
        );
      },
    )

    //在列表项目内部调用添加删除方法
    AnimatedList.of(context).insertItem(index); //动画在 itemBuilder 定义
    AnimatedList.of(context).removeItem(index, (context, animation) => ...);
    //在列表项目外的任何地方调用添加删除方法，使用GlobalKey
    final _myListKey = GlobalKey<AnimatedListState>();
    _myListKey.currentState.insertItem(index); //动画在 itemBuilder 定义
    _myListKey.currentState.removeItem(index, (context, animation) => ...);
    //添加和删除时，也要更新基础数据
    _myItems.insert(index, element);
    var removedItem = _myItems.removeAt(index);
    ```
