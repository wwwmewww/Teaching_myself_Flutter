# TabController

[参考](https://api.flutter.dev/flutter/material/TabController-class.html)

在 Tabbar 和 TabbarView 之间协调tab选择

## 继承关系

> Object > ChangeNotifier > TabController

## 构造函数

```dart
TabController({
  int initialIndex: 0, //初始化时已选 tab 的索引
  @required int length,
  @required TickerProvider vsync
})
```

## 参数 & 属性

- length → int  
  *tab 的总数*
- animation → [Animation](Animation)\<double>  
  *选择 tab 时播放的动画*
- index ↔ int  
  *所选 tab 的索引*
- indexIsChanging → bool  
  *当调用 animateTo 从 previousIndex 到 index 进行动画调换 index*
- offset ↔ double  
  *动画值与 index 之间的偏移量*
- previousIndex → int  
  *前一个选择的 tab 的索引*

## 方法

- animateTo(int value, { [Duration](Duration) duration: kTabScrollDuration, [Curve](Curve) curve: Curves.ease }) → void  
  *设置 index 和 previousIndex,然后播放动画到当前 index 值*
- dispose() → void  
  *释放资源*

## 举个例子

```dart
class MyTabbedPage extends StatefulWidget {
  const MyTabbedPage({ Key key }) : super(key: key);
  @override
  _MyTabbedPageState createState() => _MyTabbedPageState();
}

class _MyTabbedPageState extends State<MyTabbedPage> with SingleTickerProviderStateMixin {
  final List<Tab> myTabs = <Tab>[
    Tab(text: 'LEFT'),
    Tab(text: 'RIGHT'),
  ];

  TabController _tabController;

  @override
  void initState() {
    super.initState();
    _tabController = TabController(vsync: this, length: myTabs.length);
  }

 @override
 void dispose() {
   _tabController.dispose();
   super.dispose();
 }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        bottom: TabBar(
          controller: _tabController,
          tabs: myTabs,
        ),
      ),
      body: TabBarView(
        controller: _tabController,
        children: myTabs.map((Tab tab) {
          final String label = tab.text.toLowerCase();
          return Center(
            child: Text(
              'This is the $label tab',
              style: const TextStyle(fontSize: 36),
            ),
          );
        }).toList(),
      ),
    );
  }
}
```
