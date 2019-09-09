# BorderRadius
[目录](#toptop) [borderRadius](#borderRadius) [参考](https://api.flutter.dev/flutter/painting/BorderRadius-class.html)
```
//构造函数
//所有边框半径为半径
BorderRadius.all(Radius radius)
//所有边框半径为Radius.circular(radius)
BorderRadius.circular(double radius)
//水平对称的半径
BorderRadius.horizontal({
  Radius left: Radius.zero,
  Radius right: Radius.zero
})
//设置四角边框半径
BorderRadius.only({
  Radius topLeft: Radius.zero,
  Radius topRight: Radius.zero,
  Radius bottomLeft: Radius.zero,
  Radius bottomRight: Radius.zero
})
//上下对称的半径
BorderRadius.vertical({
  Radius top: Radius.zero,
  Radius bottom: Radius.zero
})
```
参数 & 属性
<span id="radius"></span>
- 半径实例值 radius → [Radius](#Radius)
- 半径 radius → double
- 左边半径 left → [Radius](#Radius)
- 右边半径 right → [Radius](#Radius)
- 上边半径 top → [Radius](#Radius)
- 下班半径 bottom → [Radius](#Radius)
- 左上半径 topLeft → [Radius](#Radius)
- 右上半径 topRight → [Radius](#Radius)
- 左下半径 bottomLeft → [Radius](#Radius)
- 右下半径 bottomRight → [Radius](#Radius)

常量
- zero → const BorderRadius<br>```const BorderRadius.all(Radius.zero)```

方法
- add(BorderRadiusGeometry other) → BorderRadiusGeometry
- resolve(TextDirection direction) → BorderRadiu
- subtract(BorderRadiusGeometry other) → BorderRadiusGeometry
- toRRect(Rect rect) → RRect

静态方法
- lerp(BorderRadius a, BorderRadius b, double t) → BorderRadius
