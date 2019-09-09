# FadeInImage 渐入图片 基础组件

    ```dart
    FadeInImage.assetNetwork(
      width: 300.0, //设置宽度
      height: 300.0, //设置高度
      fadeInDuration: const Duration(seconds: 1), //设置渐入时间
      fadeInCurve: Curves.bounceIn, //渐入图片的动画方式
      //本地占位符图片
      placeholder: 'assets/waiting.png',
      //内存图片
      //placeholder: localImageBytes,
      //让占位符图片成为透明的图像
      //import 'package:transparent_image/transparent_image.dart';
      //FadeInImage.memoryNetwork(
      //  placholder: kTransparentImage,
      image: 'https://example.com/image.png', //要显示的网络图片
    )
    ```
