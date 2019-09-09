# ConstrainedBox 限制部件容器 单子容器

    ```dart
    //让单行文本 变成多行
    ConstrainedBox(
      constraints: BoxConstraints(
        maxWidth: 200,
      ),
      child: Text(
        'Delicious Candy',
        textAlign: TextAlign.center,
      ),
    )
    ```

# ConstrainedBox 子项尺寸限制
[目录](#toptop) [参考](https://api.flutter.dev/flutter/widgets/ConstrainedBox-class.html) 
```
//构建函数
ConstrainedBox({
  Key key,
  @required BoxConstraints constraints,
  Widget child
})
//例：
ConstrainedBox(
  constraints: const BoxConstraints.expand(),
  child: const Card(child: Text('Hello World!')),
)
```
参数 & 属性
<span id="aligment"></span>
- 强加给子项的额外限制 constraints → BoxConstraints
- 子项部件 child → Widget
