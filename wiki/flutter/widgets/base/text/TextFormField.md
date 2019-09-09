# TextFormField

[参考](https://api.flutter.dev/flutter/material/TextFormField-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > FormField\<String> > TextFormField

## 构造函数

```dart
TextFormField({
  Key key,
  TextEditingController controller, //编辑文本控制器
  String initialValue, //初始化显示的文本
  FocusNode focusNode, //聚焦节点
  InputDecoration decoration: const InputDecoration(), //输入描述
  TextInputType keyboardType, //键盘类型
  TextCapitalization textCapitalization: TextCapitalization.none, //设置大小写键盘
  TextInputAction textInputAction,
  TextStyle style,
  StrutStyle strutStyle,
  TextDirection textDirection,
  TextAlign textAlign: TextAlign.start,
  bool autofocus: false, //是否自动聚焦
  bool readOnly: false, //是否只读
  bool showCursor, //是否显示光标
  bool obscureText: false, //是否用"圆点"替换输入字符
  bool autocorrect: true, //是否启用自动更正
  bool autovalidate: false, //是否每次更改都要验证和更改错误文本
  bool maxLengthEnforced: true, //是否允许超过最大字符数
  int maxLines: 1, //最大行
  int minLines,    //最小行
  bool expands: false, //是否填充父级
  int maxLength,  //最大长度
  VoidCallback onEditingComplete, //提交编辑内容回调(键盘完成键)
  ValueChanged<String> onFieldSubmitted, //提交回调(参数为编辑内容)
  FormFieldSetter<String> onSaved,  //当最终值保存到 FormState.save 时的回调方法
  FormFieldValidator<String> validator, //验证输入的回调方法。如果输入无效，则返回要显示的错误字符串，否则返回null
  List<TextInputFormatter> inputFormatters, //指定输入格式
  bool enabled: true, //是否启用
  double cursorWidth: 2.0, //光标宽度
  Radius cursorRadius, //光标圆角半径
  Color cursorColor, //光标颜色
  Brightness keyboardAppearance, //键盘的外观
  EdgeInsets scrollPadding: const EdgeInsets.all(20.0), //滑动内填充
  bool enableInteractiveSelection: true, //是否启用交互选项(剪切/复制/黏贴)
  InputCounterWidgetBuilder buildCounter //生成自定义InputDecorator.counter部件的回调
})
```

## 参数 & 属性

- controller → TextEditingController  
  *控制正在编辑的文本*
- initialValue → String  
  *初始化显示的文本,默认为空*
- focusNode → [FocusNode](#FocusNode)  
  *聚焦节点*
- decoration → [InputDecoration](#InputDecoration)  
  *外观描述,文本/背景/边框等*
- keyboardType → [TextInputType](#TextInputType)  
  *键盘类型*
- textCapitalization → [TextCapitalization](#TextCapitalization)  
  *设置大小写键盘*
- textInputAction → [TextInputAction](#TextInputAction)  
  *键盘按钮类型*
- style → [TextStyle](#TextStyle)  
  *样式*
- strutStyle → [StrutStyle](#StrutStyle)
- textDirection → [TextDirection](#TextDirection)
  *文字方向*
- textAlign → [TextAlign](#TextAlign)  
  *文字水平对齐*
- autofocus → bool
  *是否自动获取焦点*
- readOnly → bool
  *是否只读*
- showCursor → bool
  *是否显示光标*
- obscureText → bool
  *是否隐藏输入内容(密码)*
- autocorrect → bool  
  *是否启用自动更正*
- autovalidate → bool  
  *如为 true,则在每次更改后立即验证和更新其错误文本.否则,必须调用 FormFieldState.validate进行验证.如自动验证,则忽略此值*
- maxLengthEnforced → bool
  *是否允许超过最大字符数*
- maxLines → int  
  *最大行数*
- minLines → int  
  *最小行数*
- expands → bool  
  *是否填充父级*
- maxLength → int  
  *最大字符数*
- onEditingComplete → VoidCallback  
  *提交编辑内容回调(键盘完成键)*
- onFieldSubmitted → ValueChanged\<String>  
  *提交回调(参数为编辑内容)*
- onSaved → FormFieldSetter\<String>  
  *当最终值保存到 FormState.save 时的回调方法*
- validator → FormFieldValidator\<String>  
  *验证输入的回调方法。如果输入无效，则返回要显示的错误字符串，否则返回null*
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
- enableInteractiveSelection → bool  
  *是否启用交互选项(剪切/复制/黏贴)*
- buildCounter → [InputCounterWidgetBuilder](https://api.flutter.dev/flutter/material/InputCounterWidgetBuilder.html)  
- builder → FormFieldBuilder\<String>  
  *返回表示此窗体字段的小部件的函数。它将表单字段状态作为输入传递，其中包含此字段的当前值和验证状态*
