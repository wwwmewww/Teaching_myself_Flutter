# FloatingActionButtonLocation

构造函数

```dart
FloatingActionButtonLocation()
```

方法

- **getOffset**(ScaffoldPrelayoutGeometry scaffoldGeometry) → Offset<br>根据 Scaffold 的布局放置 FloatingActionButton

常量

- **FloatingActionButtonLocation.centerDocked**<br>中心对齐的 FloatingActionButton,浮动在 Scaffold.bottomNavigationBar 上,<br>以便 FloatingActionButton 的中心与 bottomNavigationBar 的上方对齐
- FloatingActionButtonLocation.centerFloat<br>居中的 FloatingActionButton,浮动在屏幕的下方  
- **FloatingActionButtonLocation.endDocked**<br>末端对齐的 FloatingActionButton,浮动在 Scaffold.bottomNavigationBar 上,<br>以便 FloatingActionButton 的中心与 bottomNavigationBar 的上方对齐
- **FloatingActionButtonLocation.endFloat**<br>末端对齐的 FloatingActionButton,浮动在屏幕的下方
- **FloatingActionButtonLocation.endTopt**<br>末端对齐的 FloatingActionButton,浮动在 Scaffold.appBar 和 the Scaffold.body 之间的过渡(transition)上
- **FloatingActionButtonLocation.miniStartTop**<br>始端对齐的 FloatingActionButton,浮动在 scaffold.appbar 和 scaffold.body 之间的过渡(transition)上,优化为迷你 FloatingActionButton
- **FloatingActionButtonLocation.startTop**<br>始端对齐的 FloatingActionButton,浮动在 scaffold.appbar 和 scaffold.body 之间的过渡(transition)上