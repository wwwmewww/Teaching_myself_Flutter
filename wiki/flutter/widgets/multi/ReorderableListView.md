# ReorderableListView 可拖动子项的 listView 多子容器

    ```dart
    ReorderableListView(
      children: [
        for(final item in myItems)
          ListTile(
            key: ValueKey(item),
            title: Text("Item #$item"),
          ),
      ],
      header: Text("This is the header!"),
      //重新排序列表时的回调
      onReorder: (oldIndex, newIndex) {
        setState(() {
          _updateMyItems(oldIndex, newIndex);
        });
      }
    )
    ```
