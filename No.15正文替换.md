# 正文切换

利用 **<font color="red"> :s </font>** 命令可以实现字符串的替换。

```
:%s/str1/str2/        用字符串 str2 替换行中首次出现的字符串 str1
:s/str1/str2/g        用字符串 str2 替换行中所有出现的字符串 str1
:.,$ s/str1/str2/g    用字符串 str2 替换正文当前行到末尾所有出现的字符串 str1
:1,$ s/str1/str2/g    用字符串 str2 替换正文中所有出现的字符串 str1
:g/str1/s//str2/g     功能同上
:m,ns/str1/str2/g     将从m行到n行的str1替换成str2
```

从上述替换命令可以看到：

> 1. <font color="red">g</font> 放在命令末尾，表示对搜索字符串的每次出现进行替换,不止匹配每行中的第一次出现；不加<font color="red">g</font>表示只对搜索字符串的首次出现进行替换；<font color="red">g</font>放在命令开头，表示对正文中所有包含搜索字符串的行进行替换操作;
> 2. <font color="red">s</font> 表示后面跟着一串替换的命令；
> 3. <font color="red">%</font>表示替换范围是所有行，即全文。

另外一个实用的命令，在Vim中统计当前文件中字符串 str1 出现的次数，可用替换命令的变形：

    :%s/str1/&/gn