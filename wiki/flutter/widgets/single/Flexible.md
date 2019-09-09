# Flexible 宽高适应父容器 单子容器

    ```dart
    Column(children:<Widget>[
      Flexible(
        flex: 2,//弹性比例值
        fit: FlexFit.tight, //紧凑 or 松散(loose)
        child:Container(color:Colors.cyan)
      ),
      Flexible(child:Container(color:Colors.cyan)),
      Flexible(child:Container(color:Colors.cyan)),
    ]);
    ```
