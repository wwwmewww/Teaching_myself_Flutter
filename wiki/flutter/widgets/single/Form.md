# Form

[参考](https://api.flutter.dev/flutter/widgets/Form-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > TextField

## 构造函数

```dart
Form({
  Key key,
  @required Widget child,
  bool autovalidate: false,
  WillPopCallback onWillPop,
  VoidCallback onChanged
})
```

## 参数 & 属性

- child → Widget  
  *子部件*
- autovalidate → bool  
  *如果为true，则表单字段将在每次更改后立即验证并更新其错误文本。否则，您必须调用FormState.validate进行验证*
- onWillPop → WillPopCallback  
  *允许表单否决用户尝试关闭包含表单的 ModalRoute*
- onChanged → VoidCallback  
  *当其中一个表单字段更改时调用*

## 静态方法

- of(BuildContext context) → FormState  
  *返回包含给定上下文的最接近的 FormState*

## 举个例子

```dart
final _formKey = GlobalKey<FormState>();

@override
Widget build(BuildContext context) {
  return Form(
    key: _formKey,
    child: Column(
      crossAxisAlignment: CrossAxisAlignment.start,
      children: <Widget>[
        TextFormField(
          validator: (value) {
            if (value.isEmpty) {
              return 'Please enter some text';
            }
            return null;
          },
        ),
        Padding(
          padding: const EdgeInsets.symmetric(vertical: 16.0),
          child: RaisedButton(
            onPressed: () {
              // Validate will return true if the form is valid, or false if
              // the form is invalid.
              if (_formKey.currentState.validate()) {
                // Process data.
              }
            },
            child: Text('Submit'),
          ),
        ),
      ],
    ),
  );
}
```

```dart
// Flutter code sample for widgets.Form.1

// This example shows a [Form] with one [TextFormField] and a [RaisedButton]. A
// [GlobalKey] is used here to identify the [Form] and validate input.

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
  final _formKey = GlobalKey<FormState>();

  @override
  Widget build(BuildContext context) {
    return Form(
      key: _formKey,
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: <Widget>[
          TextFormField(
            validator: (value) {
              if (value.isEmpty) {
                return 'Please enter some text';
              }
              return null;
            },
          ),
          Padding(
            padding: const EdgeInsets.symmetric(vertical: 16.0),
            child: RaisedButton(
              onPressed: () {
                // Validate will return true if the form is valid, or false if
                // the form is invalid.
                if (_formKey.currentState.validate()) {
                  // Process data.
                }
              },
              child: Text('Submit'),
            ),
          ),
        ],
      ),
    );
  }
}
```
