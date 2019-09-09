# TextFormField

[参考](https://api.flutter.dev/flutter/material/TextField-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > TextField

## 构造函数

```dart
TextField({
  Key key,
  TextEditingController controller,
  FocusNode focusNode,
  InputDecoration decoration: const InputDecoration(),
  TextInputType keyboardType,
  TextInputAction textInputAction,
  TextCapitalization textCapitalization: TextCapitalization.none,
  TextStyle style,
  StrutStyle strutStyle,
  TextAlign textAlign: TextAlign.start,
  TextAlignVertical textAlignVertical,
  TextDirection textDirection,
  bool readOnly: false,
  bool showCursor,
  bool autofocus: false,
  bool obscureText: false,
  bool autocorrect: true,
  int maxLines: 1,
  int minLines,
  bool expands: false,
  int maxLength,
  bool maxLengthEnforced: true,
  ValueChanged<String> onChanged,
  VoidCallback onEditingComplete,
  ValueChanged<String> onSubmitted,
  List<TextInputFormatter> inputFormatters,
  bool enabled,
  double cursorWidth: 2.0,
  Radius cursorRadius,
  Color cursorColor,
  Brightness keyboardAppearance,
  EdgeInsets scrollPadding: const EdgeInsets.all(20.0),
  DragStartBehavior dragStartBehavior: DragStartBehavior.start,
  bool enableInteractiveSelection,
  GestureTapCallback onTap,
  InputCounterWidgetBuilder buildCounter,
  ScrollController scrollController,
  ScrollPhysics scrollPhysics
})
```

## 参数 & 属性

- controller → [TextEditingController](#TextEditingController)  
  *编辑框的控制器,读写内容,监听事件*
- focusNode → [FocusNode](#FocusNode)  
  *聚焦节点*
- decoration → [InputDecoration](#InputDecoration)  
  *外观描述,文本/背景/边框等*
- keyboardType → [TextInputType](#TextInputType)  
  *键盘类型*
- textInputAction → [TextInputAction](#TextInputAction)  
  *键盘按钮类型*
- textCapitalization → [TextCapitalization](#TextCapitalization)  
  *设置大小写键盘*
- style → [TextStyle](#TextStyle)  
  *样式*
- strutStyle → [StrutStyle](#StrutStyle)
- textAlign → [TextAlign](#TextAlign)  
  *文字水平对齐*
- textAlignVertical → [TextAlignVertical](#TextAlignVertical)  
  *文字垂直对齐*
- textDirection → [TextDirection](#TextDirection)
  *文字方向*
- readOnly → bool
  *是否只读*
- showCursor → bool
  *是否显示光标*
- autofocus → bool
  *是否自动获取焦点*
- obscureText → bool
  *是否隐藏输入内容(密码)*
- autocorrect → bool  
  *是否启用自动更正*
- maxLines → int  
  *最大行数*
- minLines → int  
  *最小行数*
- expands → bool  
  *是否填充父级*
- maxLength → int  
  *最大字符数*
- maxLengthEnforced → bool
  *是否允许超过最大字符数*
- onChanged → ValueChanged\<String>
  *改变回调*
- onEditingComplete → VoidCallback  
  *提交编辑内容回调(键盘完成键)*
- onSubmitted → ValueChanged\<String>  
  *提交回调(参数为编辑内容)*
- inputFormatters → List<[TextInputFormatter](#TextInputFormatter)>  
  *指定输入格式*
- enabled → bool  
  *是否启用*
- cursorWidth → double
  *光标宽度*
- cursorRadius → [Radius](#Radius)  
  *光标圆角*
- cursorColor → [Color](#Color)  
  *光标颜色*
- keyboardAppearance → Brightness  
  *键盘的外观*
- scrollPadding → [EdgeInsets](#EdgeInsets)  
  *滑动内填充*
- dragStartBehavior → [DragStartBehavior](#DragStartBehavior)  
  *确定拖动开始的行为*
- enableInteractiveSelection → bool  
  *是否启用交互选项(剪切/复制/黏贴)*
- onTap → GestureTapCallback  
  *点击回调*
- buildCounter → [InputCounterWidgetBuilder](https://api.flutter.dev/flutter/material/InputCounterWidgetBuilder.html)  
  *生成自定义InputDecorator.counter部件的回调*
- scrollController → [ScrollController](#ScrollController)
  *垂直滑动控制器*
- scrollPhysics → ScrollPhysics  
  *滚动物理*
- selectionEnabled → bool  
  *启用 enableInteractiveSelection 和 obscureText 则为true*

## 常量

- noMaxLength → const int  
  ```-1```

## 举个例子

```dart
Column(
  children: <Widget>[
    TextField(
      autofocus: true,
      decoration: InputDecoration(
          labelText: "用户名",
          hintText: "用户名或邮箱",
          prefixIcon: Icon(Icons.person)
      ),
    ),
    TextField(
      decoration: InputDecoration(
          labelText: "密码",
          hintText: "您的登录密码",
          prefixIcon: Icon(Icons.lock)
      ),
      obscureText: true,
    ),
  ],
);
```
