# Widgets

## 基础部件

| 文本类                 | 说明   |
| ---------------------- | ------ |
| [Text](Text)           | 文本   |
| [TextField](TextField) | 输入框 |

| 图像类                  | 说明 |
| ----------------------- | ---- |
| [Image](/widgets/Image) | 图片 |
| Icon                    | 图标 |

| 按钮类               | 说明     |
| -------------------- | -------- |
| RaisedButton         | 漂浮按钮 |
| FlatButton           | 扁平按钮 |
| OutlineButton        | 边框按钮 |
| IconButton           | 图标按钮 |
| DropdownButton       | 下拉按钮 |
| FloatingActionButton | 悬浮按钮 |
| BackButton           | 后退按钮 |
| CloseButton          | 关闭按钮 |
| Checkbox             | 复选按钮 |
| Radio                | 单选按钮 |
| Switch               | 开关按钮 |

| 表单类                      | 说明 |
| --------------------------- | ---- |
| Form                        | 表单 |
| FormState                   |
| FormField                   |
| FormFieldState              |
| DropdownButtonFormField\<T> |

| 进度条                    | 说明       |
| ------------------------- | ---------- |
| LinearProgressIndicator   | 直线进度条 |
| CircularProgressIndicator | 圆形进度条 |

## 样式容器

| 对齐类                   | 说明           |
| ------------------------ | -------------- |
| Align                    | 对齐           |
| [Center](widgets/Center) | 居中对齐       |
| Baseline                 | 基线对齐       |
| padding                  | 内填充         |
| FittedBox                | 缩放及调整位置 |

| 宽高类               | 说明                                           |
| -------------------- | ---------------------------------------------- |
| ConstrainedBox       | 对子组件添加额外的约束                         |
| UnconstrainedBox     | 不会对子组件产生任何限制                       |
| SizeBox              | 给子元素指定固定宽高                           |
| AspectRatio          | 指定子组件的长宽比                             |
| LimitedBox           | 指定最大宽高                                   |
| FractionallySizedBox | 根据父容器宽高的百分比来设置子组件宽高等       |
| SizedBox             | 大小                                           |
| IntrinsicWidth       | 调整不显示宽高部件到固定宽度，有效率问题，少用 |
| IntrinsicHeight      | 调整不显示宽高部件到固定高度,有效率问题，少用  |

| 裁剪类                       | 说明                               |
| ---------------------------- | ---------------------------------- |
| [Offstage](widgets/Offstage) | 是否显示                           |
| OverflowBox                  | 超出是否显示                       |
| ClipOval                     | 剪裁成圆                           |
| ClipRRect                    | 剪裁圆角矩形                       |
| ClipRect                     | 剪裁为实际占用的矩形大小(溢出剪裁) |

| 样式类       | 说明                     |
| ------------ | ------------------------ |
| DecoratedBox | 装饰(背景、边框、渐变等) |

| 变换类     | 说明           |
| ---------- | -------------- |
| Transform  | 变换(矩阵)     |
| RotatedBox | 旋转(改变布局) |

| 综合类           | 说明                           |
| ---------------- | ------------------------------ |
| Container        | 及绘制、定位、尺寸的容器部件; 不显示其大小时,会变成0   |
| SizedOverflowBox | 集合了 SizedBox 和 OverflowBox |

CustomSingleChildLayout

## 布局容器

| 线性类 | 说明 |
| ------ | ---- |
| Flex   |
| Row    | 水平 |
| Column | 垂直 |

| 流式     | 说明             |
| -------- | ---------------- |
| Wrap     |
| Flow     | 实现复杂，效率高 |
| GridView | 滚动的多列列表   |
| Table    | 表格，不滚动     |

| 堆叠类       | 说明                     |
| ------------ | ------------------------ |
| Stack        | 堆叠，用 Positioned 定位 |
| indexedStack | 显示第index个child       |

| 列表类   | 说明                                                                                                                                                  |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| ListView | 非常常用的控件，涉及到数据列表展示的，一般情况下都会选用该控件。ListView跟GridView相似，基本上是一个slivers里面只包含一个SliverList的CustomScrollView |
| ListBody | 按给定的轴方向，按照顺序排列子节点；一般都会配合ListView或者Column等控件使用                                                                          |

CustomMultiChildLayout

## 框架容器

## [Material_Components_widgets](Material_Components_widgets)

## PreferredSizeWidget

appbar
tabbar

| 溅墨        | 说明     |
| ----------- | -------- |
| InkWell     | 溅墨效果 |
| InkResponse |

1. Hero 过度动画 最好在两个页面中使用一样的部件

    ```dart
    //起始页
    class MyHomePage extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        Hero(
          tag: 'dash', //添加标签
          Image.asset('images/dash.jpg'), //过度的图片
        ),
      }
    }
    //目标页
    class MyDetailPage extends StatelessWidget {
      @override
      Widget build(BuildContext context) {
        Hero(
          tag: 'dash', //添加标签
          Image.asset('images/dash.jpg'), //过度的图片
        ),
      }
    }
    ```

2. MediaQuery 获取屏幕尺寸

    ```dart
    var deviceData = MediaQuery.of(context);
    var screenSize = deviceData.size; //屏幕尺寸
    var deviceOrientation = deviceData.orientatio; //设备方向
    var fontScaling = deviceData.textScaleFactor; //字体缩放因子
    var notchInset = deviceData.padding; //内填充
    var noAnimations = deviceData.disableAnimations; //是否关闭动画
    var screenContrast = deviceData.platformBrightness; //屏幕对比度
    ```
