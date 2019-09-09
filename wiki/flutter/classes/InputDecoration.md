# InputDecoration
[目录](#toptop) [inputDecoration](#inputDecoration) [参考](https://api.flutter.dev/flutter/material/InputDecoration-class.html)
```
//构造函数
InputDecoration({
  Widget icon,
  String labelText,
  TextStyle labelStyle,
  String helperText,
  TextStyle helperStyle,
  String hintText,
  TextStyle hintStyle,
  int hintMaxLines,
  String errorText,
  TextStyle errorStyle,
  int errorMaxLines,
  bool hasFloatingPlaceholder: true,
  bool isDense,
  EdgeInsetsGeometry contentPadding,
  Widget prefixIcon,
  Widget prefix,
  String prefixText,
  TextStyle prefixStyle,
  Widget suffixIcon,
  Widget suffix,
  String suffixText,
  TextStyle suffixStyle,
  Widget counter,
  String counterText,
  TextStyle counterStyle,
  bool filled,
  Color fillColor,
  Color focusColor,
  Color hoverColor,
  InputBorder errorBorder,
  InputBorder focusedBorder,
  InputBorder focusedErrorBorder,
  InputBorder disabledBorder,
  InputBorder enabledBorder,
  InputBorder border,
  bool enabled: true,
  String semanticCounterText,
  bool alignLabelWithHint
})

//定义与输入字段大小相同的InputDecorator
InputDecoration.collapsed({
  @required String hintText,
  bool hasFloatingPlaceholder: true,
  TextStyle hintStyle,
  bool filled: false,
  Color fillColor,
  Color focusColor,
  Color hoverColor,
  InputBorder border: InputBorder.none,
  bool enabled: true
})
```
参数 & 属性
<span id="inputBorder"></span>
- 图标部件 icon → Widget
- 描述输入字段的文本 labelText → String
- labelText的样式(出现在输入框上面时) labelStyle → [TextStyle](#TextStyle)
- 帮助文本 helperText → String
- helperText的样式 helperStyle → [TextStyle](#TextStyle)
- 提示文本 hintText → String
- hintText的样式 hintStyle → [TextStyle](#TextStyle)
- hintText最大行数 hintMaxLines → int
<span id="edgeInsetsGeometry"></span>
- 内填充 contentPadding → [EdgeInsetsGeometry](#EdgeInsetsGeometry)
- 前缀图标部件 prefixIcon → Widget
- 前缀部件 prefix → Widget
- 前缀文本 prefixText → String
- prefixText的样式 prefixStyle → [TextStyle](#TextStyle)
- 后缀图标部件 suffixIcon → Widget
- 后缀部件 suffix → Widget
- 后缀文本 suffixText → String
- suffixText的样式 suffixStyle → [TextStyle](#TextStyle)
- 字符计数器部件,为null则用counterText代替 counter → Widget
- 错误文本 errorText → String
- errorText的样式 errorStyle → [TextStyle](#TextStyle)
- errorText最大行数 errorMaxLines → int
- 标签是否浮在焦点上 hasFloatingPlaceholder → bool
- 输入子项是否密集显示(减少垂直空间) isDense → bool
- 字符数文本 counterText → String
- counterText的样式 counterStyle → [TextStyle](#TextStyle)
- counterText的盲文提示 semanticCounterText → String
- 是否填充 filled → bool
- 填充颜色 fillColor → [Color](#Color)
- 填充时且聚焦时的颜色,与fillColor混合 focusColor → [Color](#Color)
- 悬停时的颜色 hoverColor → [Color](#Color)
- 边框 border → [InputBorder](#InputBorder)
- 禁用时边框 disabledBorder → [InputBorder](#InputBorder)
- 启用时边框 enabledBorder → [InputBorder](#InputBorder)
- 聚焦时且未有错误时的边框 focusedBorder → [InputBorder](#InputBorder)
- 聚焦时且显示错误时的边框 focusedErrorBorder → [InputBorder](#InputBorder)
- 无聚焦和显示错误时的边框 errorBorder → [InputBorder](#InputBorder)
- false不显示 helperText、counterText、errorText以及降低透明度 enabled → bool
- alignLabelWithHint → bool ？？
- 装饰器是否与输入的问题大小相同 isCollapsed → bool
