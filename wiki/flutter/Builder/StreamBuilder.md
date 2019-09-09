# StreamBuilder 串流Builder

    ```dart
    //串流
    Stream<int> count() async* {
      int i = 1;
      while(true){
        yield i++;
      }
    }
    //可以用在 Firebase的数据
    //可以用在传感器事件
    //可以用在网络连接状况
    StreamBuilder<int>(
      stream: _myStream, //串流
      initialData: 42, //初始数据，可以展示
      builder: (BuildContext context, snapshot) {
        //确认是否有错误
        if(snapshot.hasError) {
          return UhOh(snapshot.error);
        }
        //确认是否有数据
        if(!snapshot.hasData) {
          return CircularProgressIndicator();
        }
        //更多状态
        switch(snapshot.connectionState) {
          case ConnectionState.waiting:
          case ConnectionState.none:
            return LinearProgressIndicator();
          case ConnectionState.active:
            return MyWidget(snapshot.data);
          case ConnectionState.done:
            return MyFinalWidget(snapshot.data);
        }
      },
    )
    ```
