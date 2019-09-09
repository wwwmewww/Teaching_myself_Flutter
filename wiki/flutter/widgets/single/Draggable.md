# Draggable 拖动部件

    ```dart
    //拖动源
    Draggable<Color>(
      data: Color(0x000000ff),
      //要拖动的部件
      child: MyBlueBox(),
      //可选，拖动时的部件，拖动中的部件
      childWhenDragging: MyRoundedBlueBox(),
      //可选，反馈部件，拖动中原位置显示的部件
      feedback: MyGreyBox(),
      //测试目标是否会被接受
      onWillAccept: (value) => value != Colors.black,
      //当着陆时调用
      onAccept: (value) {
        // Update app state with value
      }
      //离开时调用
      onLeave: (value) {
        // Alert the user their value didn't
        // land
      }
      //定义拖动目标的方式，根据拖动到它的值组成
      builder: (context, candidates, rejects) {
        return candidates.length > 0
          ? MyBigColorfulBox(candidates[0])
          : MyDashedOutline();
      }
    )
    ```
