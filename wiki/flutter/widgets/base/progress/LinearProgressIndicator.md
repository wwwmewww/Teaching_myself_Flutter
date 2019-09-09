# LinearProgressIndicator

直线进度条

[参考](https://api.flutter.dev/flutter/material/LinearProgressIndicator-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > ProgressIndicator > LinearProgressIndicator

## 构造函数

```dart
LinearProgressIndicator({
  Key key,
  double value, //不传值，会播放一个循环的动画
  Color backgroundColor,
  Animation<Color> valueColor, //固定颜色 用 AlwaysStoppedAnimation(Colors color)
  String semanticsLabel,
  String semanticsValue
})
```

## 参数 & 属性

- 进度值(0.0 ~ 1.0) value → double
- 背景颜色 backgroundColor → Color
- 进度值颜色 valueColor → Animation<Color> ？？<br>```ColorTween(begin: Colors.grey, end: Colors.blue).animate(_animationController), // 从灰色变成蓝色```
- 盲文提示 semanticsLabel → String
- 盲文值 semanticsValue → String

> 自定义进度指示器样式
> 定制进度指示器风格样式，可以通过CustomPainter Widget 来自定义绘制逻辑，实际上LinearProgressIndicator和CircularProgressIndicator也正是通过CustomPainter来实现外观绘制的。

## 举个例子

```dart
//进度条显示50%
LinearProgressIndicator(
  backgroundColor: Colors.grey[200],
  valueColor: AlwaysStoppedAnimation(Colors.blue),
  value: .5,
)

//绘制
AnimationController _animationController;
//initState 动画执行时间3秒  
_animationController = new AnimationController(vsync: this, duration: Duration(seconds: 3));
_animationController.forward();
_animationController.addListener(() => setState(() => {}));
//dispose
_animationController.dispose();
//build
ColorTween(begin: Colors.grey, end: Colors.blue).animate(_animationController)
```
