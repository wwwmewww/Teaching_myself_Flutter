# 资源

资源分为：

- 配置文件
- 静态数据(JSON)
- 图标和图片(JPEG, WebP, GIF, PNG, BMP, WBMP)

## 导入资源

1. 在 pubspec.yaml 文件中指定资源

    ```dart
    // pubspec.yaml
    flutter:
      assets:
      - assets/my_icon.png
      - assets/background.png
    ```

2. 通过 AssetBundle 加载资源

    1. loadString(字符串/text)

        ```dart
        import 'dart:async' show Future;
        import 'package:flutter/services.dart' show rootBundle;

        Future<String> loadAsset() async {
          return await rootBundle.loadString('assets/config.json');
        }
        ```

    2. load(图片/二进制)    DefaultAssetBundle.of()

        ```dart
        Widget build(BuildContext context) {
          // ...
          return new DecoratedBox(
            decoration: new BoxDecoration(
            image: new DecorationImage(
              image: new AssetImage('graphics/background.png'),
                // ...
              ),
              // ...
            ),
          );
          // ...
        }
        ```

    3. 引用依赖包中的资源

        ```dart
        new AssetImage('icons/heart.png', package: 'my_icons')
        ```

    4. 页可以打包 lib 文件夹下未在 pubspec.yaml 声明的资源

    ```dart
    flutter:
      assets:
        - packages/fancy_backgrounds/backgrounds/background1.png
    ```

## 平台资源

### 更新图标

- Android：项目根目录/android/app/src/main/res/mipmap-hdpi等文件夹下更换占位图标
- iOS：项目根目录/ios/Runner/Assets.xcassets/AppIcon.appiconset/ 目录下替换 占位图标

### 更新启动页

- Android：项目根目录/android/app/src/main/res/drawable/launch_background.xml

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <!-- Modify this file to customize your launch splash screen -->
    <layer-list xmlns:android="http://schemas.android.com/apk/res/android">
        <item android:drawable="@android:color/white" />

        <!-- You can insert your own image assets here -->
        <!-- <item>
			<bitmap
				android:gravity="center"
				android:src="@mipmap/launch_image" />
		</item> -->
        <!-- 添加启动页要显示的图片 splash_bg -->
        <!-- 在 /android/app/src/main/res/mipmap-XXX 文件夹下加入图片 -->
        <item android:drawable="@mipmap/splash_bg" />
    </layer-list>
    ```

- iOS

    1. 项目根目录/ios/Runner/Assets.xcassets/LaunchImage.imageset/ 文件夹下 添加图片 并命名为 LaunchImage.png、LaunchImage@2x.png、LaunchImage@3x.png。如果使用不同的文件名，还必须更新同一目录中的Contents.json文件
    2. ios系统比较简单,使用xcode打开项目ios工程，选择Runner/Runner/Assets.xcassets，然后根据提示拖入对应的启动图片
    ![ios_01](images/test_ios_01.png)


# 资源管理 ??
[目录](#toptop) 

和包管理一样，Flutter也使用pubspec.yaml文件来管理应用程序所需的资源
```
flutter:
  assets:
    - assets/my_icon.png
    - assets/background.png
```