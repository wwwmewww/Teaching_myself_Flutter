# InkWell 溅墨效果 
[目录](#toptop) [参考](https://api.flutter.dev/flutter/material/InkWell-class.html)
```
//构造函数
InkWell({
  Key key,
  Widget child,
  GestureTapCallback onTap,
  GestureTapCallback onDoubleTap,
  GestureLongPressCallback onLongPress,
  GestureTapDownCallback onTapDown,
  GestureTapCancelCallback onTapCancel,
  ValueChanged<bool> onHighlightChanged,
  ValueChanged<bool> onHover,
  Color focusColor,
  Color hoverColor,
  Color highlightColor,
  Color splashColor,
  InteractiveInkFeatureFactory splashFactory,
  double radius,
  BorderRadius borderRadius,
  ShapeBorder customBorder,
  bool enableFeedback: true,
  bool excludeFromSemantics: false
})
//例
double sideLength = 50;
Widget build(BuildContext context) {
  return Center(
    child: AnimatedContainer(
      height: sideLength,
      width: sideLength,
      duration: Duration(seconds: 2),
      curve: Curves.easeIn,
      child: Material(
        color: Colors.yellow,
        child: InkWell(
          onTap: () {
            setState(() {
              sideLength == 50 ? sideLength = 100 : sideLength = 50;
            });
          },
        ),
      ),
    ),
  );
}
```
参数 & 属性
<span id="borderRadius"></span>
- 子部件 child → Widget
- 点击回调 onTap → GestureTapCallback
- 双击回调 onDoubleTap → GestureTapCallback
- 长按回调 onLongPress → GestureLongPressCallback
- 点下回调 onTapDown → GestureTapDownCallback
- 点击取消回到 onTapCancel → GestureTapCallback
- 溅满回调 onHighlightChanged → ValueChanged<bool>
- 进入/退出溅墨响应区回调 onHover → ValueChanged<bool>
- 聚焦时颜色 focusColor → [Color](#Color)
- 悬停时颜色 hoverColor → [Color](#Color)
- 高亮时颜色 highlightColor → [Color](#Color)
- 溅墨颜色 splashColor → [Color](#Color)
<span id="splashFactory"></span>
- 溅墨外观 splashFactory → [InteractiveInkFeatureFactory](#InteractiveInkFeatureFactory)
- 溅墨半径 radius → double
- 剪裁半径,customBorder为null时有效 borderRadius → [BorderRadius](#BorderRadius)
- 自定义边框 customBorder → [ShapeBorder](#ShapeBorder)
- 是否提供手势声音/触觉反馈 enableFeedback → bool
- 是否从盲文提示中去除 excludeFromSemantics → bool
- 按下/悬停/聚焦时高光形状 highlightShape → BoxShape
- 是否被裁剪限制 containedInkWell → bool
