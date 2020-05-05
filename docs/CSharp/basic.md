# 参考

书籍：[《C#从入门到精通（第2版）》](https://weread.qq.com/web/reader/0c3328005b1f940c3c4f8dakc81322c012c81e728d9d180)

# 常用数据类型

## 字符串

### 创建字符串



### 字符串的基本操作

判断两个字符串是否相等

```c#
string.Equals(str1, str2);
str1.Equals(str2);
str2.Equals(str1);
```

判断两个字符串大小

- str1 = str2，返回0
- str1 < str2，返回-1
- str1 > str2，返回1

```c#
str1.CompareTo(str2);
string.Compare(str1, str2);
```

判断字符串是否包含指定字符

```c#
str.Contains(指定字符);
str.Contains(指定字符串);
```

查找字符串中字符或者变量出现的位置

```c#
str.IndexOf(指定字符);  // 第一次出现的位置
str.LastIndexOf(指定字符);  // 最后一次出现的位置
```

取出指定长度的字符或字符串

```c#
str.SubString(起始位置, 字串长度);
str.SubString(起始位置);  // 默认取到结尾 
```

插入指定字符或字符串

```c#
str.Insert(起始位置, 指定字符串);
```

删除指定字符或字符串

```c#
str.Remove(起始位置, 字串长度);
str.Remove(起始位置);  // 默认删除到最后
```

替换指定字符或字符串，用 `字符2` 替换 `字符1`

```c#
str.Replace(字符1, 字符2)；
str.Replace(字符串1, 字符串2)；
```

去除字符串空格

```c#
str.Trim();
str.TrimStart();  // 去除头部空格
str.TrimEnd();  // 去除尾部空格
```

### StringBuilder

```c#
StringBuilder str1 = new StringBuilder();
str1.Append("我爱你");
str1.AppendLine("中国");
str1.Append("我的祖国");
Console.WriteLine(str1.ToString());
// 输出：
// 我爱你中国
// 我的祖国
```



## 数组

### 一维数组

```c#
string[] week = {"Mon","Tue","Wed","Thu","Fri","Sat","Sun"};
for(int i=0;i<week.Length;i++)
{
	Console.WriteLine(week[i]);
}
Console.ReadKey();  
```

### 二维数组

```c#
int[,] b = { { 1, 2, 3 }, { 4, 5, 6 }, { 7, 8, 9 } };
for (int i = 0; i < 3; i++)
    for (int j = 0; j < 3; j++)
        Console.WriteLine("{0}行{1}列元素为{2}", i, j, b[i, j]);
for (int i = 0; i < 3; i++)
{
    for (int j = 0; j < 3; j++)
    {
        Console.Write("{0,-5}", b[i, j]);
    }
    Console.WriteLine();
}
Console.ReadKey();
```

![image-20200410151110526](http://cdn.zhaojingyi0126.com/IMG/image-20200410151110526.png)

### 遍历二维数组

顺序是，先行，后列

```c#
int[,] a = { { 1, 2, 3 }, { 4, 5, 6 } };
foreach (int x in a)
{
    Console.Write(x);
}
Console.ReadKey();
// 输出：123456
```

### 多维数组和交错数组

```c#
int[][] c;
c = new int[3][];
c[0] = new int[] { 1, 2, 3 };
c[1] = new int[] { 4, 5, 6, 7 };
c[2] = new int[] { 8, 9, 10, 11, 12 };
for (int i = 0; i < c.Length; i++)
{
    for (int j = 0; j < c[i].Length; j++)
    {
        Console.Write("{0,-5}", c[i][j]);
    }
    Console.WriteLine();
}
Console.ReadKey();
```



![image-20200410152701046](http://cdn.zhaojingyi0126.com/IMG/image-20200410152701046.png)

### 数组的基本操作

```c#
// 数组的排序
Array.Sort(数组名);
    
// 数组的反转
Array.Reverse(数组名);

// 查找元素
Array.IndexOf(数组名, 要查找的值);

// 计算
数组名.Sum();
数组名.Max();
数组名.Min();
数组名.Average();
```

### 数组和字符串相互转化

用任意一个字符类型数组初始化字符串

```c#
char[] c = { 'H', 'e', 'l', 'l', 'o', ',', 'W', 'o', 'r', 'l', 'd' };
string str2 = new string(c);
Console.WriteLine(str2);
Console.ReadKey();
```

## 枚举

```c#
enum 枚举类型名{枚举成员列表}
```

# 面向对象



```C#
[访问修饰符] class类名
{
    // 类的主体
}
```

访问修饰符

- public

- protected

- private

- interenal

- protected internal

  



# 图形用户界面

## 窗体

`Form.cs[Design]`：窗体图形界面

`Foem.cs`：窗体后台代码

`Form.Designer.cs`：窗体设计

`Form.resx`：窗体资源

### 输入/输出方法

```
MessageBox.Show("消息内容");
```



```
MessageBox.Show("消息内容", "消息框标题");
```





### 消息框按钮

`MessageBoxButtons.OKCancel`

```
MessageBox.Show("消息内容", "消息框标题", 消息框按钮);
```

### 消息框图标

`MessageBoxIcon.Question` 
`MessageBoxIcon.Asterisk` 
`MessageBoxIcon.Information` 
`MessageBoxIcon.Error` 
`MessageBoxIcon.Stop` 
`MessageBoxIcon.Hand` 
`MessageBoxIcon.Exclamation` 
`MessageBoxIcon.Warning` 
`MessageBoxIcon.None`

```
MessageBox.Show("消息内容", "消息框标题", 消息框按钮, 消息框图标);
```

## 控件

所有的窗体控件，比如标签控件、文本框控件、按钮控件等全部都继承于System.Windows.Forms.Control。



Focus方法可设置此控件获得的焦点

Refresh方法可重画控件

Select方法可激活控件

Show方法可显示控件等。



## 程序结构和开发步骤

⑴ 创建和显示作为应用程序的主入口点的窗体。

⑵ 向窗体添加所需的控件。

⑶ 设置控件的属性。

⑷ 为控件添加事件处理程序。

⑸ 关闭窗体时，执行Dispose方法。

### 