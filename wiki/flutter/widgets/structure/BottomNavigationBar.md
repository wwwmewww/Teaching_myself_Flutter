# BottomNavigationBar 底部导航栏

[参考](https://api.flutter.dev/flutter/material/BottomNavigationBar-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > BottomNavigationBar

## 构造函数

```dart
BottomNavigationBar({
  Key key,
  @required List<BottomNavigationBarItem> items,
  ValueChanged<int> onTap,
  int currentIndex: 0,
  double elevation: 8.0,
  BottomNavigationBarType type,
  Color fixedColor,
  Color backgroundColor,
  double iconSize: 24.0,
  Color selectedItemColor,
  Color unselectedItemColor,
  IconThemeData selectedIconTheme: const IconThemeData(),
  IconThemeData unselectedIconTheme: const IconThemeData(),
  double selectedFontSize: 14.0,
  double unselectedFontSize: 12.0,
  TextStyle selectedLabelStyle,
  TextStyle unselectedLabelStyle,
  bool showSelectedLabels: true,
  bool showUnselectedLabels
})
```

## 参数 & 属性

- items → List\<BottomNavigationBarItem>  
  *定义在底部导航栏中排列的按钮项*
- onTap → ValueChanged\<int>
  *被选中项的点击事件*
- currentIndex → int
  *被选中项的索引*
- elevation → double  
  *z 坐标*
- type → BottomNavigationBarType  
  *定义 BottomNavigationBar 的布局和行为*
- fixedColor → [Color](/classes/Color)  
  *被选中项的颜色*
- backgroundColor → [Color](/classes/Color)  
  *背景颜色*
- iconSize → double  
  *所有 item 项的图标大小*
- selectedFontSize → double
  *被选中 item 项的 label 字体大小*
- selectedItemColor → Color
  *被选中项的 BottomNavigationBarItem.icon 和 BottomNavigationBarItem.label 的颜色*
- unselectedItemColor → [Color](/classes/Color)  
  *未被选中的 BottomNavigationBarItem.icon 和 BottomNavigationBarItem.labels 的颜色*
- selectedIconTheme → IconThemeData
  *被选中项的 icon 主题(size,opacity,color)*
- unselectedIconTheme → IconThemeData  
  *未被选中的 BottomNavigationBarItem.icons 的主题(size,opacity,color)*
- unselectedFontSize → double  
  *未被选中的 BottomNavigationBarItem 的 labels 的字体大小*
- selectedLabelStyle → TextStyle
  *当被选中时，BottomNavigationBarItem 的 labels 的 TextStyle*
- unselectedLabelStyle → TextStyle  
  *未被选中时，BottomNavigationBarItem 的 labels 的 TextStyle*
- showSelectedLabels → bool
  *是否显示 未被选中的 BottomNavigationBarItems的 Labels*
- showUnselectedLabels → bool  
  *是否 显示 被选中的 BottomNavigationBarItem 的 labels*

## 举个例子

```dart
// Flutter code sample for material.BottomNavigationBar.1

// This example shows a [BottomNavigationBar] as it is used within a [Scaffold]
// widget. The [BottomNavigationBar] has three [BottomNavigationBarItem]
// widgets and the [currentIndex] is set to index 0. The selected item is
// amber. The `_onItemTapped` function changes the selected item's index
// and displays a corresponding message in the center of the [Scaffold].
//
// ![A scaffold with a bottom navigation bar containing three bottom navigation
// bar items. The first one is selected.](https://flutter.github.io/assets-for-api-docs/assets/material/bottom_navigation_bar.png)

import 'package:flutter/material.dart';

void main() => runApp(MyApp());

/// This Widget is the main application widget.
class MyApp extends StatelessWidget {
  static const String _title = 'Flutter Code Sample';

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: _title,
      home: MyStatefulWidget(),
    );
  }
}

class MyStatefulWidget extends StatefulWidget {
  MyStatefulWidget({Key key}) : super(key: key);

  @override
  _MyStatefulWidgetState createState() => _MyStatefulWidgetState();
}

class _MyStatefulWidgetState extends State<MyStatefulWidget> {
  int _selectedIndex = 0;
  static const TextStyle optionStyle =
      TextStyle(fontSize: 30, fontWeight: FontWeight.bold);
  static const List<Widget> _widgetOptions = <Widget>[
    Text(
      'Index 0: Home',
      style: optionStyle,
    ),
    Text(
      'Index 1: Business',
      style: optionStyle,
    ),
    Text(
      'Index 2: School',
      style: optionStyle,
    ),
  ];

  void _onItemTapped(int index) {
    setState(() {
      _selectedIndex = index;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('BottomNavigationBar Sample'),
      ),
      body: Center(
        child: _widgetOptions.elementAt(_selectedIndex),
      ),
      bottomNavigationBar: BottomNavigationBar(
        items: const <BottomNavigationBarItem>[
          BottomNavigationBarItem(
            icon: Icon(Icons.home),
            title: Text('Home'),
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.business),
            title: Text('Business'),
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.school),
            title: Text('School'),
          ),
        ],
        currentIndex: _selectedIndex,
        selectedItemColor: Colors.amber[800],
        onTap: _onItemTapped,
      ),
    );
  }
}

//例2
import 'package:flutter/material.dart';
import '../widgets/main_page/match_screen.dart';
import '../widgets/main_page/news_screen.dart';
import '../widgets/main_page/live_screen.dart';
import '../widgets/main_page/shop_screen.dart';

class MainPage extends StatefulWidget {
  MainPage({Key key}) : super(key: key);

  @override
  _MainPageState createState() => _MainPageState();
}

class _MainPageState extends State<MainPage> {
  final _bottomNavigationColor = Colors.blue;
  int _currentIndex = 0;
  var _controller = PageController(initialPage: 0);
  List<Widget> list = List();

  // @override
  // void initState() {
  //   super.initState();
  // }

  @override
  void dispose() {
    super.dispose();
    _controller.dispose();
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: PageView(
        controller: _controller,
        children: <Widget>[
          MatchScreen(),
          NewsScreen(),
          LiveScreen(),
          ShopScreen()
        ],
        physics: NeverScrollableScrollPhysics(),
      ),
      bottomNavigationBar: BottomNavigationBar(
        items: [
          BottomNavigationBarItem(
              icon: Icon(Icons.home, color: _bottomNavigationColor),
              title:
                  Text("比赛", style: TextStyle(color: _bottomNavigationColor))),
          BottomNavigationBarItem(
              icon: Icon(Icons.home, color: _bottomNavigationColor),
              title:
                  Text("新闻", style: TextStyle(color: _bottomNavigationColor))),
          BottomNavigationBarItem(
              icon: Icon(Icons.home, color: _bottomNavigationColor),
              title:
                  Text("直播", style: TextStyle(color: _bottomNavigationColor))),
          BottomNavigationBarItem(
              icon: Icon(Icons.home, color: _bottomNavigationColor),
              title:
                  Text("商城", style: TextStyle(color: _bottomNavigationColor))),
        ],
        currentIndex: _currentIndex,
        onTap: (index) {
          // _controller.jumpToPage(index);
          _controller.animateToPage(index, duration: Duration(milliseconds: 500), curve: Curves.fastOutSlowIn);
          setState(() {
            _currentIndex = index;
          });
        },
        type: BottomNavigationBarType.fixed,
      ),
    );
  }
}

```
