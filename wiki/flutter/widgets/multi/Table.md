# Table 不滑动的网格部件 多子容器

    ```dart
    Table(
      //设置垂直对齐方式
      //TableCellVerticalAlignment.top
      //TableCellVerticalAlignment.middle
      //TableCellVerticalAlignment.bottom
      defaultVerticalAlignment: TableCellVerticalAlignment.top,
      //水平列的相对宽度
      //IntrinsicColumnWidth()
      defaultColumnWidth: FlexColumnWidth(1.0),
      //为各个列设置特定行为
      columnWidths: {1:FractionColumnWidth(.2)},
      //设置边框
      border: TableBorder.all(),
      children: <Widget>[
        TableRow(children: <Widget>[
            WideWidget(),
            MediumWidget(),
            MediumWidget(),
        ]),
        TableRow(children: <Widget>[
            WideWidget(),
            MediumWidget(),
            MediumWidget(),
        ]),
      ],
    ),
    ```
