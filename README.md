# Transliteration

Transliteration Maven module for Java.
It converts special characters in unicode text into corresponding ascii letters, with support of nearly every common languages including CJK (Chinese, Japanese and Korean).

Ported from Node.js module: [https://github.com/andyhu/node-transliteration](https://github.com/andyhu/node-transliteration)

## Install

Upload to Maven rep - TO GO
Now just compile for local repository

## Usage
Add Maven dependency, :
import me.saitov.libs.transliteration.Transliteration;


### public static String transliterate(String input, Character separator)
__Options:__
```
Transliterate the string `str`. 
Characters which this module doesn't recognise will be converted to the character in the `unknown` parameter,
defaults to `?`.
```
If no `options` parameter provided it will use the above default values.

__Example__
```java
import me.saitov.libs.transliteration.Transliteration;
...
Transliteration.transliteration('你好，世界'); // Ni Hao ,Shi Jie
Transliteration.transliteration('Γεια σας, τον κόσμο'); // Geia sas, ton kosmo
Transliteration.transliteration('안녕하세요, 세계'); // annyeonghaseyo, segye
```

### public static String slugify(String str, boolean lowercase, Character separator)

Converts unicode string to slugs. So it can be safely used in URL or file name.

__Options:__
```
  lowercase:  result string in low, lowercase
  separator: separator between words 
```

__Example:__
```java
import me.saitov.libs.transliteration.Transliteration;
...
Transliteration.slugify('你好，世界', true, '-'); // ni-hao-shi-jie
Transliteration.slugify('你好，世界', false, '_'}); // Ni_Hao_Shi_Jie
```
