# 正则表达式（Regular Expressions）
 
**定义：当给Vim指定搜索字符串时，可以包含具有特殊含义的字符。包含这些特殊字符的搜索字符串称为正则表达式（RegularExpressions）。**
```
例如：

要搜索一行正文，这行正文的开头包含 struct 字。下面的命令做不到这一点：

:/struct/

因为它只找出在行中任意位置包含 struct的第一行，并不一定在行的开始包含 struct 。

解决问题的办法是在搜索字符串前面加上特殊字符 ^ ：

：/^struct/
```
<font color="blue">**^ 字符比较每行开头的字符串。** </font>

所以  <font color="green">:/^struct/</font> 的命令表示：找出以字符串 struct 开头的行。

下表给出大多数特殊字符和它们的含义：

> <font color="blue">^          放在字符串前面，匹配行首的字</font>
> <font color="blue">$         放在字符串后面，匹配行尾的字</font>
> <font color="blue">\<         匹配一个字的字头</font>
> <font color="blue">\>         匹配一个字的字尾</font>
> <font color="blue">.          匹配任何单个正文字符</font>
> <font color="blue">[str]     匹配 str 中任何单个字符</font>
> <font color="blue">[^str]    匹配任何不在 str 中的单个字符</font>
> <font color="blue">[a - b]   匹配 a 到 b 之间任意一字符</font>
> <font color="blue">*           匹配前一个字符的0次或多次出现</font>
> <font color="blue">\          转义后面的字符</font>

**链接**

《正则表达式30分钟入门》:
[http://deerchao.net/tutorials/regex/regex.htm]()

《Vim正则表达式详解》:
[http://blog.csdn.net/salc3k/article/details/8222397]()