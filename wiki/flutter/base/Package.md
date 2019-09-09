# Package

## Dart 引入导出

1. 导入 Dart 库  
   ```import 'dart:math';```
2. 导入 pubspec.yaml 中的依赖第三方库  
   ```import 'package:provider/provider.dart';```
3. 只导入库中某个  
   ```import 'dart:math' show sum;```
4. 除了sum其余都导入  
   ```import 'dart:math' hide sum;```
5. 导入路径包 base为flutter根目录  
   ```import 'package:base/components/swiper.dart';```
6. 别名导入包  
   ```import 'package:lib2/lib2.dart' as lib2;```
7. 延迟加载  
   ```import 'package:greetings/hello.dart' deferred as hello;```

# 包管理
[目录](#toptop) 

配置文件pubspec.yaml（位于项目根目录）来管理第三方依赖包
```dart
//pubspec.yaml

```
- name：应用或包名称。
- description: 应用或包的描述、简介。
- version：应用或包的版本号。
- dependencies：应用或包依赖的其它包或插件。
- dev_dependencies：开发环境依赖的工具包（而不是flutter应用本身依赖的包）
- flutter：flutter相关的配置选项。
