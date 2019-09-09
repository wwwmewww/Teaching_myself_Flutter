# Duration

[参考]()

构造函数

```dart
Duration({
  int days: 0, //天
  int hours: 0, //时
  int minutes: 0, //分
  int seconds: 0, //秒
  int milliseconds: 0, //毫秒
  int microseconds: 0, //微秒
})
//例:
Duration fastestMarathon = new Duration(hours:2, minutes:3, seconds:2);
```

参数 & 属性

- inDays → int  
  *天*
- inHours → int  
  *时*
- inMinutes → int  
  *分*
- inSeconds → int  
  *秒*
- inMilliseconds → int  
  *毫秒*
- inMicroseconds → int  
  *微秒*
- isNegative → bool  
  *是否负数*

常量

- zero → const Duration  
  *归零* ```const Duration(seconds: 0)```
- microsecondsPerMillisecond → const int  
  *微秒/毫秒* ```1000```
- microsecondsPerSecond → const in  
  *微秒/秒* ```microsecondsPerMillisecond * millisecondsPerSecond```
- microsecondsPerMinute → const int  
  *微秒/分* ```microsecondsPerSecond * secondsPerMinute```
- microsecondsPerHour → const int  
  *微秒/时* ```microsecondsPerMinute * minutesPerHour```
- microsecondsPerDay → const int  
  *微秒/天* ```microsecondsPerHour * hoursPerDay```
- millisecondsPerSecond → const int  
  *毫秒/秒* ```1000```
- millisecondsPerMinute → const int  
  *毫秒/分* ```millisecondsPerSecond * secondsPerMinute```
- millisecondsPerHour → const int  
- *毫秒/时* ```millisecondsPerMinute * minutesPerHour```
- millisecondsPerDay → const int  
  *毫秒/天* ```millisecondsPerHour * hoursPerDay```
- secondsPerMinute → const int  
  *秒/分* ```60```
- secondsPerHour → const int  
  *秒/时* ```secondsPerMinute * minutesPerHour```
- secondsPerDay → const int  
  *秒/天* ```secondsPerHour * hoursPerDay```
- minutesPerHour → const int  
  *分/时* ```60```
- minutesPerDay → const int  
  *分/天* ```minutesPerHour * hoursPerDay```
- hoursPerDay → const int  
  *时/天* ```24```

方法

- abs() → Duration  
  *绝对值*
- compareTo(Duration other) → int  
  *值相等反 0*
- toString() → String  
  *转字符串*
