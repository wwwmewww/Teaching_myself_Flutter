# Provider 状态管理

## 单 Provider 使用

```dart
import 'package:flutter/material.dart';
//引入 provider 包
import 'package:provider/provider.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    //创建Provider，在 Widget 外包一层
    return Provider<String>.value(
      //状态值
      value: "Hello World!",
      //其下的任何Widget都能获取到状态值
      child: MaterialApp(
        home: Home(),
      ),
    );
  }
}

class Home extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Text(
      //获取上面定义的状态值
      Provider.of<String>(context)
    );
  }
}
```

## 自定义 Widget 使用 Provider

```dart
//自定义的Widget
Provider<MyComplexClass>(
  //创建
  builder: (context) => MyComplexClass(),
  //释放
  dispose: (context, value) => value.dispose()
  //子项
  child: SomeWidget(),
)
```

## 多个 Provider

```dart
//在单Provider中，可以通过嵌套快速注入多个Provider
Provider<Foo>.value(
  value: foo,
  child: Provider<Bar>.value(
    value: bar,
    child: Provider<Baz>.value(
      value: baz,
      child: someWidget,
    )
  )
)
//使用 MultiProvider 提高可读性
MultiProvider(
  providers: [
    Provider<Foo>.value(value: foo),
    Provider<Bar>.value(value: bar),
    Provider<Baz>.value(value: baz),
  ],
  child: someWidget,
)
```

## ProxyProvider

在 3.0.0 版本新加的一种 provider。它将其它 Provider 的值组合起来，并将结果发送给Provider

```dart
Widget build(BuildContext context) {
  return MultiProvider(
    providers: [
      ChangeNotifierProvider(builder: (_) => Counter()),
      //创建一个包含其它 Provider 值的 Translations
      ProxyProvider<Counter, Translations>(
        builder: (_, counter, __) => Translations(counter.value),
      ),
    ],
    child: Foo(),
  );
}
//model
class Translations {
  const Translations(this._value);
  final int _value;
  String get title => 'You clicked $_value times';
}
```

## 使用 Consumer / Selector 取值

### Consumer

增加刷新 Widget 的颗粒度，减少 build 次数

```dart
Foo(
  child: Consumer<A>(
    builder: (_, a, child) {
      //当 A 刷新时，只有 Bar 会 rebuild  
      return Bar(a: a, child: child);
    },
    child: Baz(),
  ),
)
```

### Selector

如果对 Widget-tree 没有影响，可以忽略更改

```dart
Selector<List, int>(
  //只有当 list.length 改变时才会刷新
  selector: (_, list) => list.length,
  builder: (_, length, __) {
    return Text('$length');
  }
);
```

## Provider 应用到项目

### 1. 新建 Model

```dart
// Counter.dart
import 'package:flutter/material.dart' show ChangeNotifier;

class Counter with ChangeNotifier {
  int _count = 0;
  int get count => _count;

  void increment() {
    _count++;
    notifyListeners();
  }
}
```

### 2. 新建 Provider 统一处理 MultiProvider

```dart
// ProviderStore.dart
import 'package:provider/provider.dart'; //Provider
import './Counter.dart'; //引入 Models

class ProviderStore {
  // 用 MultiProvider 把 Model 注入到 Widget
  static inserted(child) {
    return MultiProvider(
      providers: [
        ChangeNotifierProvider(builder: (_) => TestModel()),
        //继续添加多个 Provider，并且也要引入 Provider 相关的 Model
      ],
      child: child,
    );
  }

  //用 Provider.of(context) 获取 state 数据
  static T of<T>(ctx) {
    return Provider.of(ctx);
  }

  //用 Consumer 获取 state 数据
  // builder 为 (context, model, child) {return widget(model:model,child:child);}
  // child 为 widget
  static Consumer consumer<T>(builder, {child}) {
    return Consumer<T>(
      builder: builder,
      child: child,
    );
  }

  // T1 为 model 类型 list
  // T2 为 改变值的类型，length
  // selector 为 (_, list) => list.length
  // builder 为 (_, length, __) { return Text('$length'); }
  static selector<T1, T2>(selector, builder) {
    Selector<T1, T2>(selector: selector, builder: builder);
  }
}
```

### 3. 使用 ProviderStore

```dart
// main.dart
import 'package:flutter/material.dart';
import './ProviderStore.dart';

void main() => runApp(App());

class App extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return ProviderStore.inserted(
      MaterialApp(
        home: Home(),
      ),
    );
  }
}

class Home extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Text(
      //获取上面定义的状态值
      ProviderStore.of<String>(context)
    );
  }
}
```

# 状态管理 ??
[目录](#toptop) 

以下是管理状态的最常见的方法：
- Widget管理自己的状态。
- Widget管理子Widget状态。
- 混合管理（父Widget和子Widget都管理状态）。

官方给出的一些原则可以帮助你做决定：
- 如果状态是用户数据，如复选框的选中状态、滑块的位置，则该状态最好由父Widget管理。
- 如果状态是有关界面外观效果的，例如颜色、动画，那么状态最好由Widget本身来管理。
- 如果某一个状态是不同Widget共享的则最好由它们共同的父Widget管理。

## Widget管理自身状态
[目录](#toptop) 

## 父Widget管理子Widget的状态
[目录](#toptop) 

## 混合状态管理
[目录](#toptop) 

## 全局状态管理 Provider
[目录](#toptop) 
1. Add Provider
```
//pubspec.yaml
dependencies:
  provider: ^3.0.0+1
```
2. Import it
```
import 'package:provider/provider.dart';
```