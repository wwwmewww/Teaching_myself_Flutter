# Scaffold 页面模板

[参考](https://api.flutter.dev/flutter/material/Scaffold-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > Scaffold

## 构造函数

```dart
Scaffold({
  Key key,
  PreferredSizeWidget appBar,
  Widget body,
  Widget floatingActionButton,
  FloatingActionButtonLocation floatingActionButtonLocation,
  FloatingActionButtonAnimator floatingActionButtonAnimator,
  List<Widget> persistentFooterButtons,
  Widget drawer,
  Widget endDrawer,
  Widget bottomNavigationBar,
  Widget bottomSheet,
  Color backgroundColor,
  bool resizeToAvoidBottomPadding,
  bool resizeToAvoidBottomInset,
  bool primary: true,
  DragStartBehavior drawerDragStartBehavior: DragStartBehavior.start,
  bool extendBody: false,
  Color drawerScrimColor
})
```

## 参数 & 属性

- appBar → [PreferredSizeWidget](/classes/PreferredSizeWidget)  
  *显示在scaffold上方的应用栏*
- body → Widget  
  *scaffold的主要内容*
- floatingActionButton → Widget  
  *在 body 的右下角上，显示一个浮动按钮*
- floatingActionButtonLocation → [FloatingActionButtonLocation](/classes/FloatingActionButtonLocation)  
  *负责确定 floatingActionButton 的位置*
- floatingActionButtonAnimator → FloatingActionButtonAnimator  
  *Animator 将 floatingActionButton 移动到 新的 FloatingActionButtonLocation*
- persistentFooterButtons → List\<Widget>  
  *一组显示在scaffold底部的按钮*
- drawer → Widget  
  *显示在 body 侧面的面板,通常隐藏在移动设备上。从左向右(TextDirection.ltr)或从右向左(TextDirection.rtl)滑动出来*
- endDrawer → Widget  
  *显示在 body 侧面的面板,通常隐藏在移动设备上。从右向左(TextDirection.ltr)或从左向右(TextDirection.rtl)滑动出来*
- bottomNavigationBar → Widget  
  *显示在scaffold底部的底部导航栏*
- bottomSheet → Widget  
  *显示持久性底板* ??
- backgroundColor → [Color](/classes/Color)  
  *整个 scaffold 背景颜色*
- ~~resizeToAvoidBottomPadding~~ → bool  
  *弃用，请用resizeToAvoidBottomInset 代替*
- resizeToAvoidBottomInset → bool  
  *如为真，当屏幕上弹出键盘时，body 和 浮动小部件 会自行调整size*
- primary → bool  
  *是否将scaffold显示在屏幕的顶层*
- drawerDragStartBehavior → [DragStartBehavior](/enums/DragStartBehavior)  
  *确定拖动启动行为的方式的句柄*
- extendBody → bool  
  *如为真，且指定了 bottomNavigationBar 或 persistentFooterButtons，则 body 将延申到 Scaffold 的下方，而不是它们的顶部*
- drawerScrimColor → [Color](/classes/Color)  
  *用于在 drawer 打开时隐藏(模糊)主要内容的屏幕颜色*

## 静态方法

- geometryOf(BuildContext context) → ValueListenable\<ScaffoldGeometry>
- hasDrawer(BuildContext context, { bool registerForUpdates: true }) → bool
- of(BuildContext context, { bool nullOk: false }) → ScaffoldState

## 举个例子

```dart
int _count = 0;

Widget build(BuildContext context) {
  return Scaffold(
    appBar: AppBar(
      title: Text('Sample Code'),
    ),
    body: Center(
      child: Text('You have pressed the button $_count times.'),
    ),
    bottomNavigationBar: BottomAppBar(
      child: Container(height: 50.0,),
    ),
    floatingActionButton: FloatingActionButton(
      onPressed: () => setState(() {
        _count++;
      }),
      tooltip: 'Increment Counter',
      child: Icon(Icons.add),
    ),
    floatingActionButtonLocation: FloatingActionButtonLocation.centerDocked,
  );
}
```
