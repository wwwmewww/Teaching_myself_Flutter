<span id="toptop"></span>
[toc]

# dart:core
[点我返回目录](#toptop)<br>
## Object 基础对象类型
## bool 布尔型
## num 数值 包括 int 和 double
## int 整型
.parse(String str) 把字符串转换成数字
```
assert(int.parse('42') == 42);
assert(int.parse('0x42') == 66); //hex
assert(int.parse('42', radix: 16) == 66);
assert(double.parse('0.50') == 0.5);
assert(42.toString() == '42');
```
## double 浮点型
.parse(String str) 把字符串转换成数字
```
assert(double.parse('0.50') == 0.5);
```
```
//转换字符串
assert(123.456.toString() == '123.456');
//保留小数位
assert(123.456.toStringAsFixed(2) == '123.46');
//科学计数法
assert(123.456.toStringAsPrecision(2) == '1.2e+2');
assert(double.parse('1.2e+2') == 120.0);
```
toStringAsFixed() 数转字保留小数位
toStringAsPrecision() 转科学计数法字符串

## BigInt 任意大整数
## String 字符串
## StringBuffer
## StringSink
## Runes
## RuneIterator
## Match 在字符串中搜索的结果。
## Pattern 在字符串中进行基本搜索的接口。

## List 数组
## Map 字典
## MapEntry 
## Set 集合
对象的集合，其中每个对象只能出现一次。
## Null
保留字null表示作为该类唯一实例的对象。
## Function 函数

## DateTime 日期时间
## Duration 一段时间
## Stopwatch 一个简单的秒表界面来测量经过的时间。

## RegExp 正则表达式
[目录](#toptop) [参考](https://api.dartlang.org/stable/2.5.0/dart-core/RegExp-class.html)<br>

构造函数
```dart
RegExp(
  String source,
  { //可选参数
    bool multiLine: false,
    bool caseSensitive: true,
    @Since("2.4")
    bool unicode: false,
    @Since("2.4")
    bool dotAll: false
  }
)
```
参数 & 属性
- source → String  
  *正则表达式字符串*
- isMultiLine → bool  
  *是否匹配多行*
- isCaseSensitive → bool  
  *区分大小写*
- isUnicode → bool  
  *是否处于Unicode模式*
- isDotAll → bool  
  *“.”是否与行结束符匹配*
- pattern → String  
  *正则表达式字符串*

方法
- allMatches(String input, [ int start = 0 ]) → Iterable<RegExpMatch>  
  *返回输入时正则表达式匹配项的 iterable*
- firstMatch(String input) → RegExpMatch  
  *在字符串输入中搜索正则表达式的第一个匹配项。如果没有匹配项，则返回null*
- hasMatch(String input) → bool  
  *返回正则表达式在字符串输入中是否匹配*
- stringMatch(String input) → String  
  *返回此正则表达式在输入中的第一个子字符串匹配*
- matchAsPrefix(String string, [ int start = 0 ]) → Match  
  *将此模式与字符串的开头 pattern*

静态方法
- escape(String text) → String
  *返回与文本匹配的正则表达式*

```dart
RegExp exp = new RegExp(r"(\w+)");
String str = "Parse my string";
Iterable<RegExpMatch> matches = exp.allMatches(str);
```

## RegExpMatch 正则表达式匹配

## BidirectionalIterator<E> 迭代器
## Comparable 比较

## Expando 允许向object添加新属性
## Future 异步对象

## Invocation 对象的成员调用的代表
## Iterable<E> 迭代：按顺序访问值
## Iterator<E> 迭代器

## pragma 提示工具
## ~~Provisional~~ 弃用了
## Sink 数据的一般目的地
## StackTrace 由所有堆栈跟踪对象实现的接口

## Stream 串流
## Symbol 镜像使用的不透明名称
## Type 类型的运行时表示

## Uri 解析URI
## UriData 访问数据结构的一种方法：uri

标记
## @Deprecated 标记为已弃用
计划在以后删除已弃用的功能
```
@Deprecated('migration')
```

# Constants
## deprecated → const Deprecated 将功能标记为不推荐使用，直到下一个版本。
```dart
const Deprecated("next release")
```
## override → const Object
注释@override将实例成员标记为重写同名的超类成员
```
const _Override()
```
## ~~provisional~~ → const Null
在DART 2开发过程中使用的注释。
## ~~proxy~~ → const Object
此批注已弃用，将在DART 2中删除。
```
const _Proxy()
```

# Functions
## identical(Object a, Object b) → bool 检查两个引用是否指向同一对象。
## identityHashCode(Object object) → int 返回对象的标识哈希代码。
## print(Object object) → void 打印输出


# Typedefs
## Comparator<T>(T a, T b) → int
泛型比较函数的签名。

# ERROR
## AbstractClassInstantiationError 尝试实例化抽象类时引发错误。
## ArgumentError 当函数传递不可接受的参数时引发的错误。
## AssertionError 当assert语句失败时运行时系统引发的错误。
## CastError 转换操作失败时运行时系统引发的错误。
## ConcurrentModificationError 迭代期间修改集合时出错。
## CyclicInitializationError 无法初始化延迟初始化的变量时引发错误。
## Error 程序失败时抛出的错误对象。
## Exception 由所有核心库异常实现的标记接口。
## FallThroughError 当控件到达开关盒结尾时引发的错误。
## FormatException 当字符串或某些其他数据不具有预期格式且无法分析或处理时引发异常。
## IndexError 索引不在0..indexable.length-1范围内时使用的专用范围错误。
## IntegerDivisionByZeroException
## NoSuchMethodError 对象上NoSuchMethod的默认实现引发的错误。
## NullThrownError 尝试抛出null时引发错误。
## OutOfMemoryError
## RangeError 由于索引超出有效范围而引发错误。
## StackOverflowError
## StateError 对象的当前状态不允许该操作。
## TypeError 类型断言失败时运行时系统引发的错误。
## UnimplementedError 由尚未实现的操作引发。
## UnsupportedError 对象不允许该操作。



[点我返回目录](#toptop)<br>

# dart:math 数字运算库
[点我返回目录](#toptop)
```
import 'dart:math';
```
## 常量
[点我返回目录](#toptop)
常量|类型|值
--|--|--
e|double|2.718281828459045
ln2|double|0.6931471805599453
ln10|double|2.302585092994046
log2e|double|1.4426950408889634
log10e|double|0.4342944819032518
pi|double|3.1415926535897932
sqrt1_2|double|0.7071067811865476
sqrt2|double|1.4142135623730951
## 方法
[点我返回目录](#toptop)
方法定义|说明|参数区间|返值区间
--|--|--|--
double ==sin==(num radians);|正弦|
double ==asin==(num x);|反正弦|-1..1|-PI/2..PI/2
double ==cos==(num radians);|余弦
double ==acos==(num x);|反余弦|-1..1|0..PI
double ==tan==(num radians);|正切
double ==atan==(num x);|反正切|非NaN|-PI/2..PI/2
double ==atan2==(num a, num b);|反正切2||-PI..PI
double ==log==(num x);|对数函数
double ==exp==(num x);|以e为底的指数函数
num ==pow==(num x, num exponent);|求次方
double ==sqrt==(num x);|开方|
T ==max==<T extends num>(T a, T b);|求最大值
T ==min==<T extends num>(T a, T b);|求最小值
## Random 类
[点我返回目录](#toptop)
#### Random([int seed])
Random随机数构造函数
#### Random.secure();
创建加密安全的随机数生成器。factory
#### nextBool() -> bool
生成随机布尔值
#### nextDouble() → double
生成在0.0（含）到 1.0（不含）之间均匀分布的非负随机浮点值
#### nextInt(int max) → int
生成在0（含）到 max（含）之间均匀分布非负随机整数

### Point 类
[点我返回目录](#toptop)
#### Point(T x, T y)
#### magnitude → double
得到原点（0，0）和该点之间的直线（欧几里得）距离。
#### x → T
此点的x坐标
#### y → T
此点的y坐标
#### distanceTo(Point<T> other) → double
返回此点与其他点之间的距离
#### squaredDistanceTo(Point<T> other) → T
返回此点与其他点之间的平方距离。
### Rectangle 类
[点我返回目录](#toptop)
#### Rectangle(T left, T top, T width, T height)
#### Rectangle.fromPoints(Point<T> a, Point<T> b)
#### left → T
#### top → T
#### width → T
#### height → T
#### topLeft → Point<T>
#### topRight → Point<T>
#### right → T
#### bottom → T
#### bottomLeft → Point<T>
#### bottomRight → Point<T>
#### boundingBox(Rectangle<T> other) → Rectangle<T>
返回一个完全包含此和其他项的新矩形
#### containsPoint(Point<num> another) → bool
测试另一个是在里面还是沿着边缘。
#### containsRectangle(Rectangle<num> another) → bool
测试这是否完全包含另一个。
#### intersection(Rectangle<T> other) → Rectangle<T>
计算这个和其他的交集。
#### intersects(Rectangle<num> other) → bool
如果与其他项相交，则返回true。
### MutableRectangle 类
[点我返回目录](#toptop)
#### MutableRectangle(T left, T top, T width, T height)
#### MutableRectangle.fromPoints(Point<T> a, Point<T> b)
#### left ↔ T
#### top ↔ T
#### width ↔ T
#### height ↔ T
#### topLeft → Point<T>
#### topRight → Point<T>
#### right → T
#### bottom → T
#### bottomLeft → Point<T>
#### bottomRight → Point<T>
#### boundingBox(Rectangle<T> other) → Rectangle<T>
返回一个完全包含此和其他项的新矩形
#### containsPoint(Point<num> another) → bool
测试另一个是在里面还是沿着边缘。
#### containsRectangle(Rectangle<num> another) → bool
测试这是否完全包含另一个。
#### intersection(Rectangle<T> other) → Rectangle<T>
计算这个和其他的交集。
#### intersects(Rectangle<num> other) → bool
如果与其他项相交，则返回true。
## dart:async 异步库
[点我返回目录](#toptop)
```
import 'dart:async';
```
# dart:collection
# dart:convert
# dart:developer
# dart:typed_data



