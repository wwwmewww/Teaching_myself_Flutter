# CustomPaint 自定义画板 基础部件

    ```dart
    CustomPaint(
      size: Size(200, 100),
      painter: MyPainter();
    )

    class MyPainter extends CustomPainter {
      // 获取画布
      @override
      void paint(Canvas canvas, Size size) {
        canvas.drawLine(); //线
        canvas.drawRect(); //矩形
        canvas.drawCircle(); //圆形
        canvas.drawArc(); //弧形
        canvas.drawPath(); //路径
        canvas.drawImage(); //图片
        canvas.drawPath(); //点九图片
        canvas.drawParagraph(); //文本段落
      }

      // 重建 CustomPainter 时会 调用 shouldRepaint 方法
      @override
      bool shouldRepaint(CustomPainter old) {
        return old.myParameter != myParameter;
      }
    }
    ```
