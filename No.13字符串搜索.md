# 字符串搜索

在 **编辑模式** 中可以使用字符串搜索，在 **命令模式** 也可以使用字符串搜索，可以通过搜索该字符串到达指定行。

**正向搜索：将待搜索的字符串置于”两个的 <font color="red"> / </font> 之间。**

**反向搜索：将字符串放在两个 <font color="red"> ？</font> 之间。**

```
:/str/                    正向搜索，将光标移到下一个包含字符串 str 的行

:？str？                反向搜索，将光标移到上一个包含字符串 str 的行

:/str/w file             正向搜索，并将第一个包含字符串 str 的行写入 file 文件

:/str1/,/str2/w file    正向搜索，并将包含字符串 str1 的行，至包含字符串 str2 行写入 file 文件
```