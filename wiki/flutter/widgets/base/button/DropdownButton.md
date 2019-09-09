# DropdownButton

[参考](https://api.flutter.dev/flutter/material/DropdownButton-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatelessWidget > IconButton

## 构建函数

```dart
DropdownButton({
  Key key,
  @required List<DropdownMenuItem<T>> items,
  T value,
  Widget hint,
  Widget disabledHint,
  @required ValueChanged<T> onChanged,
  int elevation: 8,
  TextStyle style,
  Widget underline,
  Widget icon,
  Color iconDisabledColor,
  Color iconEnabledColor,
  double iconSize: 24.0,
  bool isDense: false,
  bool isExpanded: false
})
```

## 参数 & 属性

- items → List<[DropdownMenuItem](#DropdownMenuItem)\<T>  
  *选择项列表*
- value → T  
  *已选择列表项,值为null,默认列表第一个*
- hint → Widget  
  *值为null时显示的部件*
- disabledHint → Widget
  *禁用时显示的部件*
- onChanged → ValueChanged\<T>  
  *选择事件*
- elevation → int  
  *列表打开时的z坐标*
- style → [TextStyle](#TextStyle)  
  *样式*
- underline → Widget  
  *下划线部件*
- icon → Widget  
  *图标*
- iconDisabledColor → Color  
  *图标禁用时颜色*
- iconEnabledColor → Color  
  *图标启用时颜色*
- iconSize → double  
  *图标大小*
- isDense → bool  
  *是否减少按钮的高度(z坐标)*
- isExpanded → bool  
  *是否按钮水平填满父级*

方法

- createState() → _DropdownButtonState\<T>
- createElement() → StatefulElement
- debugDescribeChildren() → List\<DiagnosticsNode>
- debugFillProperties(DiagnosticPropertiesBuilder properties) → void
- noSuchMethod(Invocation invocation) → dynamic
- toDiagnosticsNode({String name, DiagnosticsTreeStyle style }) → DiagnosticsNode
- toString({DiagnosticLevel minLevel: DiagnosticLevel.debug }) → String
- toStringDeep({String prefixLineOne: '', String prefixOtherLines, DiagnosticLevel minLevel: DiagnosticLevel.debug }) → String
- toStringShallow({String joiner: ', ', DiagnosticLevel minLevel: DiagnosticLevel.debug }) → String
- toStringShort() → String

问题：如何让开的的列表在按钮下方？？

## 举个例子

```dart
String dropdownValue = 'One';
@override
Widget build(BuildContext context) {
  return Scaffold(
    body: Center(
      child: DropdownButton<String>(
        value: dropdownValue,
        onChanged: (String newValue) {
          setState(() {
            dropdownValue = newValue;
          });
        },
        items: <String>['One', 'Two', 'Free', 'Four']
          .map<DropdownMenuItem<String>>((String value) {
            return DropdownMenuItem<String>(
              value: value,
              child: Text(value),
            );
          })
          .toList(),
      ),
    ),
  );
}
```
