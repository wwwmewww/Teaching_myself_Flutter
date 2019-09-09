# Image

[参考](https://api.flutter.dev/flutter/widgets/Image-class.html)

## 继承关系

> Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > Image

## 构造函数

```dart
Image({
  Key key,
  @required ImageProvider image,
  ImageFrameBuilder frameBuilder,
  ImageLoadingBuilder loadingBuilder,
  String semanticLabel,
  bool excludeFromSemantics: false,
  double width,
  double height,
  Color color,
  BlendMode colorBlendMode,
  BoxFit fit,
  AlignmentGeometry alignment: Alignment.center,
  ImageRepeat repeat: ImageRepeat.noRepeat,
  Rect centerSlice,
  bool matchTextDirection: false,
  bool gaplessPlayback: false,
  FilterQuality filterQuality: FilterQuality.low
})

//Creates a widget that displays an ImageStream obtained from an asset bundle. The key for the image is given by the name argument.
Image.asset(
  String name,
  {
    Key key,
    AssetBundle bundle,
    ImageFrameBuilder frameBuilder,
    String semanticLabel,
    bool excludeFromSemantics: false,
    double scale,
    double width,
    double height,
    Color color,
    BlendMode colorBlendMode,
    BoxFit fit,
    AlignmentGeometry alignment: Alignment.center,
    ImageRepeat repeat: ImageRepeat.noRepeat,
    Rect centerSlice,
    bool matchTextDirection: false,
    bool gaplessPlayback: false,
    String package,
    FilterQuality filterQuality: FilterQuality.low
})

//Creates a widget that displays an ImageStream obtained from a File.
Image.file(
  File file,
  {
    Key key,
    double scale: 1.0,
    ImageFrameBuilder frameBuilder,
    String semanticLabel,
    bool excludeFromSemantics: false,
    double width,
    double height,
    Color color,
    BlendMode colorBlendMode,
    BoxFit fit,
    AlignmentGeometry alignment: Alignment.center,
    ImageRepeat repeat: ImageRepeat.noRepeat,
    Rect centerSlice,
    bool matchTextDirection: false,
    bool gaplessPlayback: false,
    FilterQuality filterQuality: FilterQuality.low
})

//Creates a widget that displays an ImageStream obtained from a Uint8List.
Image.memory(
  Uint8List bytes,
  {
    Key key,
    double scale: 1.0,
    ImageFrameBuilder frameBuilder,
    String semanticLabel,
    bool excludeFromSemantics: false,
    double width,
    double height,
    Color color,
    BlendMode colorBlendMode,
    BoxFit fit,
    AlignmentGeometry alignment: Alignment.center,
    ImageRepeat repeat: ImageRepeat.noRepeat,
    Rect centerSlice,
    bool matchTextDirection: false,
    bool gaplessPlayback: false,
    FilterQuality filterQuality: FilterQuality.low
})

//Creates a widget that displays an ImageStream obtained from the network.
Image.network(
  String src,
  {
    Key key,
    double scale: 1.0,
    ImageFrameBuilder frameBuilder,
    ImageLoadingBuilder loadingBuilder,
    String semanticLabel,
    bool excludeFromSemantics: false,
    double width,
    double height,
    Color color,
    BlendMode colorBlendMode,
    BoxFit fit,
    AlignmentGeometry alignment: Alignment.center,
    ImageRepeat repeat: ImageRepeat.noRepeat,
    Rect centerSlice,
    bool matchTextDirection: false,
    bool gaplessPlayback: false,
    FilterQuality filterQuality: FilterQuality.low,
    Map<String, String> headers
})
```

## 参数 & 属性

- image → [ImageProvider](#ImageProvider)  
  *图片*
- frameBuilder → [ImageFrameBuilder](#ImageFrameBuilder)  
  *图片帧构建器* ```Widget ImageFrameBuilder (BuildContext context, Widget child, int frame, bool wasSynchronouslyLoaded)```
- loadingBuilder → [ImageLoadingBuilder](#ImageLoadingBuilder)  
  *加载构造器* ```Widget ImageLoadingBuilder (BuildContext context, Widget child, ImageChunkEvent loadingProgress)```
- semanticLabel → String  
  *盲文提示*
- excludeFromSemantics → bool  
  *是否在盲文提示中去除图片*
- width → double  
  *宽*
- height → double  
  *高*
- color → [Color](#Color)  
  *颜色*
- colorBlendMode → [BlendMode](#BlendMode)  
  *颜色混合模式*
- fit → [BoxFit](#BoxFit)
- alignment → [AlignmentGeometry](#AlignmentGeometry)  
  *对齐图像 左上角(-1.0,-1.0) 右下角(1.0,1.0)* ??
- repeat → [ImageRepeat](#ImageRepeat)  
  *图片重复*
- centerSlice → [Rect](#Rect)  
  *点九切图*
- matchTextDirection → bool  
  *是否匹配文字方向显示图片*
- gaplessPlayback → bool  
  *当图片源发生变化时,true继续显示,false不显示*
- filterQuality → [FilterQuality](#FilterQuality)  
  *图片品质过滤*
- name → String  
  *资源名称*
- bundle → AssetBundle  
  *资源加载器* ??
- scale → double  
  *缩放比例*
- package → String
  *包名*
- file → File
  *图片文件* ??
- bytes → Uint8List
  *内存地址* ??
- src → String  
  *图片源网址*
- headers → Map<String, String>  
  *HTTP头信息* ??

## 使用

```dart
//例: pubspec.yaml
flutter:
  assets:
    - images/cat.png
    - images/2x/cat.png
    - images/3.5x/cat.png
    - packages/my_icons/background1.png // 去掉 lib/
//使用
Image.asset('images/cat.png')
Image.asset('icons/heart.png', package: 'my_icons')
```
