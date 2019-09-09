# Flutter

## [库包](Package)

## [资源](Assets)

## [路由](Router)

## [状态](Provider)

## [部件](Widgets)

## 搭配环境
[目录](#toptop) 

1. 安装git [Git官网](https://git-scm.com/download/)
2. 获取Flutter [Flutter](https://flutter.dev/docs/development/tools/sdk/releases#windows)
3. 解压并运行flutter/flutter_console.bat
4. 添加环境变量Path:xxx/flutter/bin
5. 命令行运行 flutter doctor
6. IDE设置查看[Flutter中文网](https://flutterchina.club/setup-windows/)
7. 创建项目命令: flutter create <项目名词>
8. 调试项目命令: flutter run



# 程序的基本代码结构
[目录](#toptop) 
```
//1. 导入包
import 'package:flutter/material.dart';

//2. 程序入口
void main() => runApp(MyApp());

//3. 应用结构
class MyApp extends StatelessWidget {
  final Widget title; //定义属性
  MyApp({this.title}); //构造函数
  @override //构造器
  Widget build(BuildContext context) {
    //返回一个 Widget
    return MaterialApp(
      //应用名称
      title: "Flutter Demo",
      theme: ThemeData(
        //蓝色主题
        primarySwatch: Colors.blue,
      ),
      //应用首页路由
      home: MyHomePage(title: 'MyHomePage'),
    );
  }
}

//4. 页面部件
class MyHomePage extends StatefulWidget {
  MyHomePage({
    Key key,
    this.title,
    this.initValue: 0,
  }) : super(key: key);

  final String title;
  final int initValue;

  @override
  _MyHomePageState createState() => _MyHomePageState();
}

//5. 状态类
class _MyHomePageState extends State<MyHomePage> {
  //变量，用于记录按钮点击的总次数
  int _counter;
  
  // 初始化 1) 生命周期方法
  @override
  void initState() {
    super.initState();
    //初始化状态
    _counter = widget.initValue;
    print("initState");
  }
  
  //自定义方法 设置状态的自增函数
  void _incrementCounter() {
    setState(() { _counter++; });
  }
  
  //build方法用来构建widget树
  //最终将widget树渲染到设备屏幕上
  //改变状态会刷新build
  // 初始化 3); 重载 3) 生命周期方法
  @override
  Widget build(BuildContext context) {
    print("build");
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'You have pushed the button this many times:',
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.display1,
            ),
          ],
        ),
      ),
      //浮动按钮
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: Icon(Icons.add),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );
  }
  // 重载 2) 生命周期方法
  @override
  void didUpdateWidget(MyHomePage oldWidget) {
    super.didUpdateWidget(oldWidget);
    print("didUpdateWidget");
  }
  // 移除 2) 生命周期方法
  @override
  void deactivate() {
    super.deactivate();
    print("deactive");
  }
  // 移除 3) 生命周期方法
  @override
  void dispose() {
    super.dispose();
    print("dispose");
  }
  // 重载 1) 移除 1) 生命周期方法
  @override
  void reassemble() {
    super.reassemble();
    print("reassemble");
  }
  // 初始化 2) 生命周期方法
  @override
  void didChangeDependencies() {
    super.didChangeDependencies();
    print("didChangeDependencies");
  }
}
```
## 导入包
[目录](#toptop) 
```
//android 视觉风格
import 'package:flutter/material.dart';
//ios 视觉风格
import 'package:flutter/cupertino.dart';
//基础部件包
import 'package:flutter/widgets.dart';
```
## 程序主入口
[目录](#toptop) 
```dart
// void main() => runApp( /*Widget*/ );
void main() => runApp(MyApp());
```

## 应用结构
[目录](#toptop) 
```
class MyApp extends StatelessWidget {
  final Widget title; //定义属性
  MyApp({this.title}); //构造函数
  @override //构造器
  Widget build(BuildContext context) {
    //返回一个 Widget
    return MaterialApp(
      //应用名称
      title: "Flutter Demo",
      theme: ThemeData(
        //蓝色主题
        primarySwatch: Colors.blue,
      ),
      //应用首页路由
      home: MyHomePage(title: 'MyHomePage'),
      //路由表
      routes:{
          "page1": (context) => Page1(),
      }
    );
  }
}
```
## 页面部件
[目录](#toptop) 
```
//部件分 有状态 StatefulWidget 和 无状态 StatelessWidget
class MyHomePage extends StatefulWidget {
  MyHomePage({
    Key key,
    this.title,
    this.initValue: 0,
  }) : super(key: key);

  final String title;
  final int initValue;
  
  //当部件为有状态时
  //因为刷新状态也要刷新build
  //所以把状态分出去单独写
  @override
  _MyHomePageState createState() => _MyHomePageState();
}
```
## 状态类 & 生命周期
[目录](#toptop) 
```
class _MyHomePageState extends State<MyHomePage> {
  int _counter;

  // 初始化 1) 生命周期方法
  @override
  void initState() {
    super.initState();
    //初始化状态
    _counter = widget.initValue;
    print("initState");
  }
  
  // 初始化 3); 重载 3) 生命周期方法
  @override
  Widget build(BuildContext context) {
    print("build");
    return Scaffold(
      body: Center(
        child:FlatButton(
          child: Text('$_counter'),
          onPressed:()=>setState(()=> ++_counter,
        ), 
      ),
    );
  }
  
  // 重载 2) 生命周期方法
  @override
  void didUpdateWidget(MyHomePage oldWidget) {
    super.didUpdateWidget(oldWidget);
    print("didUpdateWidget");
  }
  
  // 移除 2) 生命周期方法
  @override
  void deactivate() {
    super.deactivate();
    print("deactive");
  }
  
  // 移除 3) 生命周期方法
  @override
  void dispose() {
    super.dispose();
    print("dispose");
  }
  
  // 重载 1) 移除 1) 生命周期方法
  @override
  void reassemble() {
    super.reassemble();
    print("reassemble");
  }
  
  // 初始化 2) 生命周期方法
  @override
  void didChangeDependencies() {
    super.didChangeDependencies();
    print("didChangeDependencies");
  }
}
```
生命周期|执行方法
--|--
打开页面时|1. initState<br>2. didChangeDependencies<br>3. build
热重载时|1. reassemble<br>2. didUpdateWidget<br>3. build
移除时|1. reassemble<br>2. deactive<br>3. dispose
state变化时|只会刷新 Build 方法

- **initState**：当Widget第一次插入到Widget树时会被调用
- **didChangeDependencies**：当State对象的依赖发生变化时会被调用
- **build**：主要是用于构建Widget子树的，会在如下场景被调用：
    - 在调用initState()之后。
    - 在调用didChangeDependencies()之后。
    - 在调用didUpdateWidget()之后。
    - 在调用setState()之后。
    - 在State对象从树中一个位置移除后（会调用deactivate）又重新插入到树的其它位置之后。
- **reassemble**：专门为了开发调试而提供的，在热重载(hot reload)时会被调用，此回调在Release模式下永远不会被调用。
- **didUpdateWidget**：在widget重新构建时，Flutter framework会调用Widget.canUpdate来检测Widget树中同一位置的新旧节点，然后决定是否需要更新，如果Widget.canUpdate返回true则会调用此回调。Widget.canUpdate会在新旧widget的key和runtimeType同时相等时会返回true，也就是说在在新旧widget的key和runtimeType同时相等时didUpdateWidget()就会被调用。
- **deactivate**：当State对象从树中被移除时，会调用此回调。在一些场景下，Flutter framework会将State对象重新插到树中，如包含此State对象的子树在树的一个位置移动到另一个位置时（可以通过GlobalKey来实现）。如果移除后没有重新插入到树中则紧接着会调用dispose()方法。
- **dispose**：当State对象从树中被永久移除时调用；通常在此回调中释放资源。

> **注意**：
> 1. 不能在 initState 中调用 BuildContext.inheritFromWidgetOfExactType，该方法用于在 Widget 树上获取离当前 widget 最近的一个父级 InheritFromWidget。应该在在build（）方法或didChangeDependencies()中调用它。
> 2. @mustCallSuper标注的父类方法，都要在子类方法中先调用父类方法。