# Radio

单选按钮

[参考](https://api.flutter.dev/flutter/material/Radio-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > Radio

## 构造函数

```dart
Radio({
  Key key,
  @required T value,
  @required T groupValue,
  @required ValueChanged<T> onChanged,
  Color activeColor,
  MaterialTapTargetSize materialTapTargetSize
})
```

## 参数 & 属性

- value → T  
  *单选按钮的值*
- groupValue → T  
  *单选按钮组的值*
- onChanged → ValueChanged\<T>  
  *更改回调*
- activeColor → [Color](#Color)  
  *选中颜色*
- materialTapTargetSize → [MaterialTapTargetSize](#MaterialTapTargetSize)  
  *配置点击区的最小尺寸*

## 举个例子

```dart
enum SingingCharacter { lafayette, jefferson }
SingingCharacter _character = SingingCharacter.lafayette;
Widget build(BuildContext context) {
  return Center(
    child: Column(
      children: <Widget>[
        ListTile(
          title: const Text('Lafayette'),
          leading: Radio(
            value: SingingCharacter.lafayette,
            groupValue: _character,
            onChanged: (SingingCharacter value) {
              setState(() { _character = value; });
            },
          ),
        ),
        ListTile(
          title: const Text('Thomas Jefferson'),
          leading: Radio(
            value: SingingCharacter.jefferson,
            groupValue: _character,
            onChanged: (SingingCharacter value) {
              setState(() { _character = value; });
            },
          ),
        ),
      ],
    ),
  );
}
```
