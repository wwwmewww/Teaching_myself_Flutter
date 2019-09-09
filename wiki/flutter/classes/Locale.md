# Locale
[目录](#toptop) [locale](#locale)
```
//构造函数
Locale(String _languageCode, [ String _countryCode ])
Locale.fromSubtags({String languageCode: 'und', String scriptCode, String countryCode })
```
参数 & 属性
- 国家&区域Subtag **countryCode** → String<br>```const Locale('de', 'DE')```[language-subtag](https://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) ??
- 语言Subtag **languageCode** → String<br>```const Locale('he')``` [language-subtag](https://www.iana.org/assignments/language-subtag-registry/language-subtag-registry)
- 脚本Subtag **scriptCode** → String<br>``````[Unicode CLDR supplemental data](http://cldr.unicode.org/index/downloads) ??
