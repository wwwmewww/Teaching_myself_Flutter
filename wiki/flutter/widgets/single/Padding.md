# padding 内填充
[目录](#toptop) [参考](https://api.flutter.dev/flutter/widgets/Padding-class.html) 
```
//构建函数
Padding({
  Key key,
  @required EdgeInsetsGeometry padding,
  Widget child
})
//例：
Padding(
  //上下左右各添加16像素补白
  padding: EdgeInsets.all(16.0),
  child: Text('title'),
)
```
参数 & 属性
<span id="aligment"></span>
- 内填充 padding → EdgeInsetsGeometry([EdgeInsets](#EdgeInsets))
- 子项部件 child → Widget
