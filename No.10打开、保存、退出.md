# 打开、保存、退出

### 1. 打开
```
 :e      在已经启动的Vim中打开一个文件夹
如     e path_to_file/filename
```

### 2. 保存
```
:w      保存当前编辑的文件（单词write的缩写）

:w file_temp    将当前文件另存为file_temp

```

### 3. 退出

只 **<font color="blue">退出编辑程序，而不保存编辑内容</font>** ：

```
:q     在未做修改的情况下退出
:q！  放弃所有修改，强制退出编辑程序
```
### 4. 保存退出

> 1. 在编辑模式下可以用 <font color="red">zz</font> 命令退出 Vim 编辑程序，该命令 **<font color="blue">保存对正文所做的修改，覆盖原始文件</font>**。


> 2. 保存并退出可以将两条命令结合起来使用 
**<font color="blue">注意命令顺序，先保存，后退出</font>**：
```
：wq
```