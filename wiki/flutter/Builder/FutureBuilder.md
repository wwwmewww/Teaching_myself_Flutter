# FutureBuilder 涉及Future时构建Widget 可以知道future的当前状态

    ```dart
    FutureBuilder(
      future: http.get('http://awesome.data'),
      builder: (centext, snapshot){
        if(snapshot.connectionState == ConnectionState.done) {
          // ConnectionState.none
          // ConnectionState.waiting
          // ConnectionState.active
          // ConnectionState.done
          if(snapshot.hasError) {
            return SomethingWentWrong();
          }
          return AwesomeData(snapshot.data);
        } else {
          return CircularProgressIndicator();
        }
      },
    )
    ```
