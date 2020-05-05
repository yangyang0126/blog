> 更新于2020年4月

# 一、程序的安装和运行

## 1.1 资源推荐

Python 官方中文文档：[Python 3.7.3 文档](https://docs.python.org/zh-cn/3/)

Github：[Github开源Python项目](https://github.com/vinta/awesome-python)

免费教程：[廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1016959663602400)

付费课程：[扇贝编程](https://web.shanbay.com/codetime/home)

书籍：[Python编程：从入门到实践](https://weread.qq.com/web/reader/19532980715c01921954a54kc81322c012c81e728d9d180)-埃里克·马瑟斯

书籍：[使用Python自动执行无聊的工作](https://automatetheboringstuff.com)-Al Sweigart

书籍：[如何像计算机科学家一样思考](http://openbookproject.net/thinkcs/python/english3e/)-Peter Wentworth

书籍：[艰苦学习Python](https://docs.scrapy.org/en/latest/intro/tutorial.html)

## 1.2 各类编程语言的区别

除Python之外，还有C、C++、Java等编程语言，各自都有适用的领域。
- 对性能要求非常高的软件，比如操作系统或者图像处理，通常会用`C`或者`C++`编写
- 安卓上的APP一般都用`Java`，苹果APP一般用`Object C`或者`Swift`
- `Python`通常用于数据分析、网络爬虫、人工智能，也可以用于网站或者APP的服务器端程序

Python的优点：语法简洁，既适合初学者入门，也能应用在人工智能等高端领域

（摘自[扇贝编程](https://web.shanbay.com/codetime/home)）
## 1.3 安装Python
（部分转自廖雪峰老师的教程 [安装Python](https://www.liaoxuefeng.com/wiki/1016959663602400/1016959)）

### 在Mac上安装Python

如果你正在使用Mac，系统是OS X>=10.9，那么系统自带的Python版本是2.7。要安装最新的Python 3.7，有两个方法：

方法一：从Python官网下载Python 3.7的[安装程序](https://www.python.org/ftp/python/3.7.0/python-3.7.0-macosx10.9.pkg)，双击运行并安装；

方法二：如果安装了[Homebrew](https://brew.sh/)，直接通过命令`brew install python3`安装即可。

### 在Linux上安装Python

如果你正在使用Linux，那我可以假定你有Linux系统管理经验，自行安装`Python 3`应该没有问题，否则，请换回Windows系统。

### 在Windows上安装Python

Python官网地址：https://www.python.org/downloads/windows/

![](http://cdn.zhaojingyi0126.com/IMG/17569167-9ea07ee86868fabd.png)

首先，我们根据自己系统类型（32 位或 64 位）来选择合适的版本点击下载，一般我们选择 `executable installer `就行。86-64就是64位，86（不带64）就是32位

![17569167-78288525fdd04944](http://cdn.zhaojingyi0126.com/IMG/17569167-78288525fdd04944.png)

各个版本的区别是：

- `embeddable zip file`：嵌入式版本，可以集成到其它应用中
- `web-based installer`：联网方式安装
- `executable installer`：可执行文件(*.exe)方式安装

我们这里选择了` Windows x86-64 executable installer`（我电脑是64位的），下载完成后双击打开，可以看到如下图所示的界面。

如果你网速不行，打不开网页的话，这里提供了**Windows 64位 Python3.8**版本的安装包。百度云链接：https://pan.baidu.com/s/1THithgcL1OzNcEn6yemjzQ 。提取码：lu4j

![17569167-2db1f1f33da6720e](http://cdn.zhaojingyi0126.com/IMG/17569167-2db1f1f33da6720e.png)

特别要注意勾上```Add Python 3.7 to PATH```，然后点“Install Now”即可完成安装。

安装结束之后，在开始菜单栏可以看到Python的安装内容

![image-20200326161813669](http://cdn.zhaojingyi0126.com/IMG/image-20200326161813669.png)

点击`IDLE(Python 3.8 64-bit)`，打开编辑器，界面长这样

![image-20200326162054517](http://cdn.zhaojingyi0126.com/IMG/image-20200326162054517.png)

## 1.4 安装Spyder

我个人是更喜欢`Spyder`的开发环境，会比这个默认的好看方便（每个人喜好不同，不安装也无所谓）

![](http://cdn.zhaojingyi0126.com/IMG/image-20200316100136007.png)

我选择安装`anaconda`，因为里面不仅带了`Spyder`，还自带了`Jupyter Notebook`

`anaconda`官网网址：https://www.anaconda.com/distribution/

网速不行的，可以从百度云下载。冬冬同学帮我们上传了百度云。链接：https://pan.baidu.com/s/18PAQXckpxZBJG0Fw4nE2eQ 提取码：xtuw

![image-20200316095746988](http://cdn.zhaojingyi0126.com/IMG/image-20200316095746988.png)

安装之后，就可以看到`Spyder`

![image-20200316095938368](http://cdn.zhaojingyi0126.com/IMG/image-20200316095938368.png)



## 1.5 命令提示符

命令提示符是我们一定要知道的一个东西，因为安装库，都靠它。

先说明一点，用spyder或者默认Python，安装库的**位置**是不一样的。

### 默认Python

如果你用的是默认的Python，那么命令提示符用的是系统自带的

Win7系统：开始菜单—>附件—>命令提示符

Win10系统：开始菜单—>Windows系统—>命令提示符

或者直接搜索`cmd`

![image-20200316094919989](http://cdn.zhaojingyi0126.com/IMG/image-20200316094919989.png)

输入```Python```，会显示你的版本号

![image-20200316095048893](http://cdn.zhaojingyi0126.com/IMG/image-20200316095048893.png)

### Spyder

如果你用的是Spyder，很有可能，你在**命令提示符**装的库，它根本感受不到

你需要在`Anaconda Prompt` 里面输入

![image-20200326203512696](http://cdn.zhaojingyi0126.com/image-20200326203349259.png)

同样输入```Python```，会显示你的版本号

![image-20200326203349259](http://cdn.zhaojingyi0126.com/image-20200326203512696.png)

后面安装库的时候，一定要注意这一点。如果是用Spyder，要在`Anaconda Prompt` 里面安装。

当然，安装的命令，是一模一样的，只是输入的地方不一样

## 1.6 安装Python库

Python依赖于很多库，这里的库，是**根据自己需要**安装的。为什么要安装库。就差不多相当于站在巨人的肩膀上吧。人家大神把很多功能写好了，我们拿过来用就行。安装的代码是 `pip install 库的名称`。

爬虫需要的最基础的库是`requests`，那我们安装的时候，输入

```bash
pip install requests
```

如果你安装好这个库了，系统会提示你`already satisfied`

![image-20200326204017120](http://cdn.zhaojingyi0126.com/image-20200326204017120.png)

再比如，我想要一个操作PDF相关的库`pdfplumber`。打开**命令提示符**，输入

```bash
pip install pdfplumber
```

Python安装库的时候是这样的

![17569167-ffe90d49de366d8d](http://cdn.zhaojingyi0126.com/IMG/17569167-ffe90d49de366d8d.png)

如果界面出现（红色框里的）提示，更新所有自带的库即可

输入`python -m pip install --upgrade pip`

![image-20200316095328745](http://cdn.zhaojingyi0126.com/IMG/image-20200316095328745.png)

最后，是不是每一个库都需要安装呢？不是的！有些库是Python自带的，比如`turtle`，你不需要安装，也能直接用。学会装库之后，我们开始写代码啦~

## 1.7 向你的新世界说Hello
如果你是默认的Python，在开始菜单栏，打开IDLE

![](http://cdn.zhaojingyi0126.com/IMG/image-20200316095423016.png)

输入如下代码。`Print`表示输入这行文字。注意，引号要用英文输入法，不能用中文输入法哟~
```
print("Hello, World!")
```
你在向新世界说Hello的时候，新世界也在向你说Hello呀~

![17569167-227993f8db17019f](http://cdn.zhaojingyi0126.com/IMG/17569167-227993f8db17019f.png)

- 下次开始写代码的时候，可以打开```File-New```，新建一个，操作更方便。右边写代码，左边出结果

![17569167-756668c86a091e43](http://cdn.zhaojingyi0126.com/IMG/17569167-756668c86a091e43.png)

如果你是Spyder界面，那就打开Spyder输入，代码都是一样哒。点绿色的箭头运行，Spyder的输出在界面的右侧

![image-20200326204932095](http://cdn.zhaojingyi0126.com/image-20200326204932095.png)

## 1.8 实践：画个小猪佩奇吧

![](http://cdn.zhaojingyi0126.com/IMG/ezgif.com-crop.gif)

把以下代码贴进去，直接运行就可以了。先不管为什么要这样写代码，咱们后面再研究。总之，Python是个好玩的东西~

```python
import turtle as t
 
t.pensize(4)
t.hideturtle()
t.colormode(255)
t.color((255, 155, 192), "pink")
t.setup(840, 500)
t.speed(10)
 
# 鼻子
t.pu()
t.goto(-100,100)
t.pd()
t.seth(-30)
t.begin_fill()
a = 0.4
for i in range(120):
    if 0 <= i < 30 or 60 <= i < 90:
        a = a+0.08
        t.lt(3)  # 向左转3度
        t.fd(a)  # 向前走a的步长
    else:
        a = a-0.08
        t.lt(3)
        t.fd(a)
        t.end_fill()
 
t.pu()
t.seth(90)
t.fd(25)
t.seth(0)
t.fd(10)
t.pd()
t.pencolor(255, 155, 192)
t.seth(10)
t.begin_fill()
t.circle(5)
t.color(160, 82, 45)
t.end_fill()
 
t.pu()
t.seth(0)
t.fd(20)
t.pd()
t.pencolor(255, 155, 192)
t.seth(10)
t.begin_fill()
t.circle(5)
t.color(160, 82, 45)
t.end_fill()
 
# 头
t.color((255, 155, 192), "pink")
t.pu()
t.seth(90)
t.fd(41)
t.seth(0)
t.fd(0)
t.pd()
t.begin_fill()
t.seth(180)
t.circle(300, -30)
t.circle(100, -60)
t.circle(80, -100)
t.circle(150, -20)
t.circle(60, -95)
t.seth(161)
t.circle(-300, 15)
t.pu()
t.goto(-100, 100)
t.pd()
t.seth(-30)
a = 0.4
for i in range(60):
    if 0 <= i < 30 or 60 <= i <90:
        a = a+0.08
        t.lt(3)  # 向左转3度
        t.fd(a)  # 向前走a的步长
    else:
        a = a-0.08
        t.lt(3)
        t.fd(a)
        t.end_fill()
 
# 耳朵
t.color((255, 155, 192), "pink")
t.pu()
t.seth(90)
t.fd(-7)
t.seth(0)
t.fd(70)
t.pd()
t.begin_fill()
t.seth(100)
t.circle(-50, 50)
t.circle(-10, 120)
t.circle(-50, 54)
t.end_fill()
 
t.pu()
t.seth(90)
t.fd(-12)
t.seth(0)
t.fd(30)
t.pd()
t.begin_fill()
t.seth(100)
t.circle(-50, 50)
t.circle(-10, 120)
t.circle(-50, 56)
t.end_fill()
 
#眼睛
t.color((255, 155, 192), "white")
t.pu()
t.seth(90)
t.fd(-20)
t.seth(0)
t.fd(-95)
t.pd()
t.begin_fill()
t.circle(15)
t.end_fill()
 
t.color("black")
t.pu()
t.seth(90)
t.fd(12)
t.seth(0)
t.fd(-3)
t.pd()
t.begin_fill()
t.circle(3)
t.end_fill()
 
t.color((255, 155, 192), "white")
t.pu()
t.seth(90)
t.fd(-25)
t.seth(0)
t.fd(40)
t.pd()
t.begin_fill()
t.circle(15)
t.end_fill()
 
t.color("black")
t.pu()
t.seth(90)
t.fd(12)
t.seth(0)
t.fd(-3)
t.pd()
t.begin_fill()
t.circle(3)
t.end_fill()
 
# 腮
t.color((255, 155, 192))
t.pu()
t.seth(90)
t.fd(-95)
t.seth(0)
t.fd(65)
t.pd()
t.begin_fill()
t.circle(30)
t.end_fill()
 
# 嘴
t.color(239, 69, 19)
t.pu()
t.seth(90)
t.fd(15)
t.seth(0)
t.fd(-100)
t.pd()
t.seth(-80)
t.circle(30, 40)
t.circle(40, 80)
 
# 身体
t.color("red", (255, 99, 71))
t.pu()
t.seth(90)
t.fd(-20)
t.seth(0)
t.fd(-78)
t.pd()
t.begin_fill()
t.seth(-130)
t.circle(100,10)
t.circle(300,30)
t.seth(0)
t.fd(230)
t.seth(90)
t.circle(300,30)
t.circle(100,3)
t.color((255,155,192),(255,100,100))
t.seth(-135)
t.circle(-80,63)
t.circle(-150,24)
t.end_fill()
 
# 手
t.color((255,155,192))
t.pu()
t.seth(90)
t.fd(-40)
t.seth(0)
t.fd(-27)
t.pd()
t.seth(-160)
t.circle(300,15)
t.pu()
t.seth(90)
t.fd(15)
t.seth(0)
t.fd(0)
t.pd()
t.seth(-10)
t.circle(-20,90)
 
t.pu()
t.seth(90)
t.fd(30)
t.seth(0)
t.fd(237)
t.pd()
t.seth(-20)
t.circle(-300,15)
t.pu()
t.seth(90)
t.fd(20)
t.seth(0)
t.fd(0)
t.pd()
t.seth(-170)
t.circle(20,90)
 
# 脚
t.pensize(10)
t.color((240,128,128))
t.pu()
t.seth(90)
t.fd(-75)
t.seth(0)
t.fd(-180)
t.pd()
t.seth(-90)
t.fd(40)
t.seth(-180)
t.color("black")
t.pensize(15)
t.fd(20)
 
t.pensize(10)
t.color((240, 128, 128))
t.pu()
t.seth(90)
t.fd(40)
t.seth(0)
t.fd(90)
t.pd()
t.seth(-90)
t.fd(40)
t.seth(-180)
t.color("black")
t.pensize(15)
t.fd(20)
 
# 尾巴
t.pensize(4)
t.color((255, 155, 192))
t.pu()
t.seth(90)
t.fd(70)
t.seth(0)
t.fd(95)
t.pd()
t.seth(0)
t.circle(70, 20)
t.circle(10, 330)
t.circle(70, 30)

t.hideturtle()
t.done()
```

# 二、入门语句

> 本章内容运行环境：`Jupyter Notebook`
>
> 关于`Jupyter Notebook`的使用，可以参考：https://www.zhihu.com/question/266988943 （由Clover提供）
>
> 本单元视频链接：https://v.youku.com/v_show/id_XNDYyMTI4OTA5Mg==.html

## 2.1 输入输出和注释

```python
input("你叫什么名字：")   # 这时候可以输入你的名字
print("欢迎你学习Python")  # 屏幕输出结果用print
```
```#```代表注释，不参与程序执行

```print```代表输出

```input```代表输入


## 2.2 数据类型和变量
### 1) 变量
**变量**：在计算机程序中，变量不仅可以为整数或浮点数，还可以是字符串

**变量命名**： 只能有```字母```、```_```、```数字```，其中数字不可以放在开头，比如`3_a_b`，程序就直接报错了

![](http://cdn.zhaojingyi0126.com/image-20200405190326652.png) 

变量赋值：用等号``` = ```为变量赋值

```
phone_number = "我的电话是：18899998888" 
```
在实际使用中，希望大家可以起一点有意义的变量名，比如`name`、 `age` 这种，而不要都是`a`、`b`、`c`、`d`、`e`、`f`，这不仅别人看不懂你写的是什么，可能后面你自己都不记得，这个变量是干嘛的了。写代码的时候多注释，是个好习惯。

### 2) 数字
- int (有符号整数)，比如` -3`、`5`、`20`
- bool (布尔值)，`True`或者`False`
- float (浮点值)，比如`3.14`、`0.9`
- complex (复数)，比如`2+8i`

### 3) 字符串
- 引号引起来的一串字，可以是英文，也可以是数字，还可以用 emoji 表情哟。

- 引号可以是：单引号``` '字符串'```，双引号``` "字符串"```，三引号```'''字符串'''```

  ```ord()```：获取字符的整数表示

  ```chr()```：把编码转换为对应的字符

![](http://cdn.zhaojingyi0126.com/image-20200405190838317.png)

字符串的联结：```+```

```python
text_1 = "今天我"
text_2 = "很开心"
full_text = text_1 + text_2
print(full_text)
# 输出：今天我很开心
```

如果需要将数值与字符串联结，先用` str() `将**将其他类型转为字符串**，再将其与字符串联结。关于各种类型的相互转换，可参考【第八章 数据类型转换】

```python
print("先挣" + str(1) + "个亿再说。")
# 输出：先挣1个亿再说。
```
**多行字符串**

- 当字符串包含多行信息，尤其文本包含大量引号的时候，我们可以使用```  """ ``` ``` """ ``` 或者```  ''' ``` ``` '''```  包裹字符串。
- 计算机读到第一个``` """``` 时，会知道在下一个``` """``` 出现之前，被包裹的信息都是字符串。
- 这种方法可以减少错误，提高代码可读性。
```python
Song = """
Well I wonder could it be
When I was dreaming about you baby
You were dreaming of me
"""
```

如果```"""``` ``` """ ```之中的信息不被赋值于变量，则会被Python视作为注释。比如在代码开头，备注写代码的时间和作者。
```python
"""
Created on Tue May 22 2019
@author: YangYang
"""
```


## 2.3 转义字符
刚刚上面提到，引号`' text '`在代码，是用于表示字符串的。那假设，我需要输入一段文字，里面本来就有引号怎么办？或者我要表示换行怎么办？

这里就涉及到了转义字符，用`\`来表示

```python
\'  # 表示单引号
\"  # 表示双引号
\n  # 表示换行符
\\  # 表示反斜线
```
比如要输出`I'm fine`，你可以这样写
```python
print("I\'m fine")
```


## 2.4 算术运算符
单目运算符正号（+）和负号（－）， 双目运算符， +，－，*，/，%，还有 ** ，分别表示加法，减法， 乘法， 除法， 取余， 和幂运算。

**加减乘除**：通过``` +  -  *  / ```符号分别进行加、减、乘、除四种运算

```python
print(3+5)   # 输出：8
print(4-5)   # 输出：-1
print(5*2)   # 输出：10
print(6/2)   # 输出：3.0
```
**指数**：通过``` ** ```符号实现指数运算

```python
print(10 ** 2)   # 10 的平方，输出 100
print(4 ** 3)    # 4 的立方，输出 64
print(4 ** 0.5)  # 4 的平方根（0.5次方），输出 2
```

**余数**：通过``` %```符号进行余数运算

```python
print(29 % 5) # 输出 4
print(3 % 2)  # 输出 1
print(44 % 2) # 输出 0
```

**加等**：通过```+= ```符号进行加等运算

```python
A = 1
A += 2  # 等效于A = A+2
print(A) 
# 输出：3
```

```+=``` 符号还可以用来联结字符串

```python
# 将 Python 官方文档网址赋值于web_address
web_address = "https://docs.python.org"
# 将 Python中文教程部分网址 赋值于 cn
cn = "/zh-cn/3/tutorial/"
# 将 cn 合并于web_address
web_address += cn
print(web_address)
 # 输出：https://docs.python.org/zh-cn/3/tutorial/
```

上面提到，在字符串里面+表示把两个字符串连接起来。在数字计算中+表示相加计算，这里来看个例子
```python
print(2+5)  #  输出7
print('2'+'5')  # 输出25
```
第一行的2+5，没有引号，代表直接计算。2+5=7
第二行的'2'+'5'，代表2这个字符，和5这个字符，连接起来，就是25，这个25，还是一个字符

## 2.5 help和dir

### help

如果你不清楚一些系统的基础函数要怎么用，你可以用`help`

比如，`print`输出的时候，可以指定结束标记，不指定的时候，默认是换行符。你可以用`help`查看一下

```python
help(print)
```

输出

```python
Help on built-in function print in module builtins:

print(...)
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
    
    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newline.
    flush: whether to forcibly flush the stream.
```

这时候，你就可以看到`print`的完整用法

### dir

`dir`可以查看，这个对象有哪些属性

比如看看一个整形`int`可以有哪些操作

```python
dir(int)
```

输出

```python
['__abs__',
 '__add__',
 '__and__',
 '__bool__',
 '__ceil__',
 '__class__',
 '__delattr__',
 '__dir__',
 '__divmod__',
 '__doc__',
 '__eq__',
 '__float__',
 '__floor__',
 '__floordiv__',
 '__format__',
 '__ge__',
 '__getattribute__',
 '__getnewargs__',
 '__gt__',
 '__hash__',
 '__index__',
 '__init__',
 '__init_subclass__',
 '__int__',
 '__invert__',
 '__le__',
 '__lshift__',
 '__lt__',
 '__mod__',
 '__mul__',
 '__ne__',
 '__neg__',
 '__new__',
 '__or__',
 '__pos__',
 '__pow__',
 '__radd__',
 '__rand__',
 '__rdivmod__',
 '__reduce__',
 '__reduce_ex__',
 '__repr__',
 '__rfloordiv__',
 '__rlshift__',
 '__rmod__',
 '__rmul__',
 '__ror__',
 '__round__',
 '__rpow__',
 '__rrshift__',
 '__rshift__',
 '__rsub__',
 '__rtruediv__',
 '__rxor__',
 '__setattr__',
 '__sizeof__',
 '__str__',
 '__sub__',
 '__subclasshook__',
 '__truediv__',
 '__trunc__',
 '__xor__',
 'bit_length',
 'conjugate',
 'denominator',
 'from_bytes',
 'imag',
 'numerator',
 'real',
 'to_bytes']
```

这时候就可以看到关于`int`的所有的，系统自带的，函数和方法

## 2.6 实践

任意输入两个数字（用到`input`）

输出两个数字的和、差、乘积（用到`print`和`运算`）

输出格式要求如下（用到了转义字符换行`\n`）

```markdown
输入的数字是：1,2
他们的和是3
他们的差是-1
他们的乘积是2
```

请在作业的最后一行输出：

```
昵称：第2节课作业
```

# 三、字符串

>本章内容运行环境：`Jupyter Notebook`
>
>本单元视频链接：https://v.youku.com/v_show/id_XNDYyMjY0ODgyOA==.html

我们在之前的数据类型里面讲过，字符串就是一系列的字符，用引号引起来，可以是英文，也可以是数。引号可以是单引号``` '字符串'```，双引号``` "字符串"```，三引号```'''字符串'''```

关于字符串，我们之前提到了几个常用的**函数**

`str()`：将数字转变为字符串

```ord()```：获取字符的整数表示

```chr()```：把编码转换为对应的字符

## 3.1 什么是方法

方法就是执行一些指定的操作，比如，将字符串中的所有英文字母变成大写

一般表示成

```markdown
操作对象.方法名称()
```

## 3.2 大小写转换

```.upper()``` 将字符串中的所有英文字母变成大写

```.lower()``` 将字符串中的所有英文字母变成小写

```.swapcase() ```将大小写字母转换

```.title() ```将所有单词首字母大写

```python
text = "HELLO world"
text.upper()  # 输出： 'HELLO WORLD'
text.lower()  # 输出： 'hello world'
text.swapcase()  # 输出： 'hello WORLD'
text.title()  # 输出： 'Hello World'
```
## 3.3 删空格或指定字符

```.strip()```  删除字符串开头和结尾，两端的**空格**

`.rstrip()` 删除右边的**空格**

`.lstrip()` 删除左边的**空格**

```python
text = "   Hello world!        "
print(text.strip())  # 输出：'Hello world!'
print(text.rstrip())  # 输出：'   Hello world!'
print(text.lstrip())  # 输出：'Hello world!    '    
```

`.strip("***")`  删除指定字符

```python
text = "!!!!!!   Hello world   !!!!!!!"
print(text.strip("!"))  # 输出：'   Hello world'
print(text.rstrip("!"))  # 输出：'!!!!!!   Hello world   '
print(text.lstrip("!"))  # 输出：'   Hello world   !!!!!!!'
```

## 3.4 字符变成变量

`.format()` 可以将字符串中的部分字符变成变量

可以直接根据位置对应

```python
singer = "陈奕迅"
song = "《浮夸》"
print("我最喜欢的歌是{}的{}".format(singer,song))  
# 输出：我最喜欢的歌是陈奕迅的《浮夸》
```

也可以关键词对应

```python
print("我最喜欢的球星是{country}的{star}".format(star = "C罗",country = "葡萄牙")) 
# 输出：我最喜欢的球星是葡萄牙的C罗
```

## 3.5 切割字符串

`.split()` 切割字符串

```python
text = "I love you."
print(text.split())  # 什么都不填，默认是空格
# 输出：['I', 'love', 'you.']
```

```python
email = "zhaojingyi0126@163.com"
print(email.split("@")) # 根据@切割
# 输出：['zhaojingyi0126', '163.com']
```

```python
text = "I love you."
print(text.split()[0])  # 输出：I
print(text.split()[1])  # 输出：love
print(text.split()[2])  # 输出：you.
```

## 3.6 替换字符串

```.replace()```  替换字符串中的某一部分

```python
text = "我爱吃苹果"
new_text = text.replace("苹果","哈密瓜")
print(new_text)
# 输出： '我爱吃哈密瓜'
```

## 3.7 查找字符

```b.find(a)```  返回字符串 a 在字符串 b中第一次出现所在的索引位置

```python
text = "Hello World"
find_l = text.find("l")
print(find_l) 
# 输出：2
# 这个是指出现的位置,从0开始数
```

## 3.8 倒序

str```[::-1] ``` 将**列表**倒序

```python
text = "Hello World"
text[::-1]
# 输出： 'dlroW olleH'
```

## 3.9 字符串所有方法

```python
dir(str)
```

```python
 'capitalize',
 'casefold',
 'center',
 'count',
 'encode',
 'endswith',
 'expandtabs',
 'find',
 'format',
 'format_map',
 'index',
 'isalnum',
 'isalpha',
 'isascii',
 'isdecimal',
 'isdigit',
 'isidentifier',
 'islower',
 'isnumeric',
 'isprintable',
 'isspace',
 'istitle',
 'isupper',
 'join',
 'ljust',
 'lower',
 'lstrip',
 'maketrans',
 'partition',
 'replace',
 'rfind',
 'rindex',
 'rjust',
 'rpartition',
 'rsplit',
 'rstrip',
 'split',
 'splitlines',
 'startswith',
 'strip',
 'swapcase',
 'title',
 'translate',
 'upper',
 'zfill'
```

## 3.10 实践：清洗豆瓣数据

我在[豆瓣电影 Top 250](https://movie.douban.com/top250)上面，右击**查看源代码**，可以看到关于**《肖申克的救赎》**的详情

```html
text = """
<div class="info">
	<div class="hd">
		<a href="https://movie.douban.com/subject/1292052/" class="">
			<span class="title">肖申克的救赎</span>
			<span class="title">&nbsp;/&nbsp;The Shawshank Redemption</span>
			<span class="other">&nbsp;/&nbsp;月黑高飞(港)  /  刺激1995(台)</span>
		</a>
		<span class="playable">[可播放]</span>
	</div>
	<div class="bd">
		<p class="">
			导演: 弗兰克·德拉邦特 Frank Darabont&nbsp;&nbsp;&nbsp;主演: 蒂姆·罗宾斯 Tim Robbins /...<br>
			1994&nbsp;/&nbsp;美国&nbsp;/&nbsp;犯罪 剧情
		</p>

	<div class="star">
		<span class="rating5-t"></span>
		<span class="rating_num" property="v:average">9.7</span>
		<span property="v:best" content="10.0"></span>
		<span>1966737人评价</span>
	</div>

	<p class="quote">
		<span class="inq">希望让人自由。</span>
	</p>
"""
```

用今天学习的字符串的方法，把数据清洗出来，汇总成一句话：

```
《肖申克的救赎》，豆瓣评分9.7，1966737人评价。推荐理由：希望让人自由。
```

思路：

1、先想一下，输出要怎么构成？

```python
title = "肖申克的救赎"
rate = "9.7"
number = "1966737人评价"
quote = "希望让人自由。"
print("《{}》，豆瓣评分{}，{}。推荐理由：{}".format(title, rate, number, quote))
```

2、怎么获取到这些数据？可以有几种方法？

一层一层切割开来，选择合适的关键词切

3、完整代码

```python
text = """--------"""  # text的内容在上面
title = text.split('</span>')[0].split('>')[-1]
rate = text.split('v:average\">')[1].split('</span>')[0]
number = text.split('star')[1].split('<span>')[1].split('</span>')[0]
quote = text.split('inq')[1].split('>')[1].split('<')[0]
print("《{}》，豆瓣评分{}，{}。推荐理由：{}".format(title, rate, number, quote))
```

请在作业的最后一行输出：

```
昵称：第3节课作业
```

# 四、列表

> 本章内容运行环境：`Jupyter Notebook`
>
> 本单元视频链接：https://v.youku.com/v_show/id_XNDYyNDA0NTI4MA==.html

## 4.1 列表定义

列表是指 Python 中包含一组有序元素的对象

*   列表以方括号```[```开头，以```]```结尾
*   列表中的每个元素用 ```,```隔开

```python
num = [1, 3, 2, 4]
```

### 列表元素类型

列表中除了可以存放字符串以外，也可以放数值类数据，还可以包含列表，以下几种都可以

```python
num = [1, 3, 2, 4]
name = ["Tony", "Peter", "Kevin", "David"]
aList = [123, 'abc', 4.56, ['inner', 'list'], 7+9j]
```

### 空列表

列表里可以什么元素都没有

```python
empty_list = []   # empty_list 为空列表
```

### range生成列表

```range() ``` 需要输入一个数值，比如 n，然后返回一组数字

```python
my_range = range(2,20,2)
print(list(my_range))
# 输出：[2, 4, 6, 8, 10, 12, 14, 16, 18]
```

## 4.2 访问列表

### 选择列表元素

*   从左至右数：起始位置为 ```0 ```，用``` [] ```包裹目标元素的索引位置
*   从右至左数：起始位置为```  -1```，需要在索引位置的数字前加上负号

```python
letter = ["a", "b", "c", "d", "e", "f", "g", "h"]
print(letter[0])      #  输出："a"
print(letter[-1])     #  输出："h"
print(letter[-1].title())     #  输出："H",把首字母大写
```

### 截取列表

```python
letter = ["a", "b", "c", "d", "e", "f", "g", "h"]
print(letter[2:6])
# 输出： ['c', 'd', 'e', 'f']
```

- 如果想从列表中第一个元素开始截取，```: ```前的数字可以省略```list[:5] ```
- 如果想截取到列表的最后一个元素，```: ```后的数字可以省略`list[1:] `
- 也可以用负数索引位置从右至左截取列表`list[-4:-1] `

```python
number = [1,2,3,4,5,6,7,8,9,10]
print(number[:3])
# 输出：[1, 2, 3]
print(number[3:])
# 输出：[4, 5, 6, 7, 8, 9, 10]
print(number[-3:])
# 输出：[8, 9, 10]
```

### 查找元素位置

`.index()`，查找元素出现的位置（**第一次**出现的位置）

```python
name = ['Yangyang','Lindy','Alice','Leimei','Jack','Yangyang']
name.index('Yangyang')
# 输出：0
```

## 4.3 组队组合

### 列表连接

Python 中，可以用 ```+ ```来连接多个列表

列表只能和列表相连接，如果将列表和字符串或数值连接，计算机会报错

```python
zoo = ["大象", "熊猫", "猩猩", "海獭"]
new_animals = ["长颈鹿", "虎", "羊驼"]
zoo = zoo + new_animals
print(zoo)
# 输出：['大象', '熊猫', '猩猩', '海獭', '长颈鹿', '虎', '羊驼']
```

### 扩展列表

`.extend`：在列表末尾一次性追加另一个序列中的多个值

```python
zoo = ["大象", "熊猫", "猩猩", "海獭"]
new_animals = ["长颈鹿", "虎", "羊驼"]
zoo.extend(new_animals)  
print(zoo)
# 输出：['大象', '熊猫', '猩猩', '海獭', '长颈鹿', '虎', '羊驼']
```

### 列表组队

`zip()` 将两个列表中的元素一一组成对，形成一个新的对象

```python
name = ["吴承恩", "罗贯中", "施耐庵", "曹雪芹、高鹗"]
book = ["西游记", "三国演义", "水浒传", "红楼梦"]
name_and_book = zip(name, book)
print(name_and_book)
# 输出：<zip object at 0x1086a0288>  该对象在内存中的位置
print(list(name_and_book))
# 输出：[('吴承恩', '西游记'), ('罗贯中', '三国演义'), ('施耐庵', '水浒传'), ('曹雪芹、高鹗', '红楼梦')]
```

## 4.4 修改、添加、删除元素

### 添加元素

`.append() `为列表添加元素

当列表中有其他元素时，append() 将新元素添加至**所有元素之后**

```python
my_list = []
my_list.append(1)
my_list.append(2.0)
my_list.append(3)
my_list.append('jjj')
my_list.append(1)
print(my_list)
# 输出：[1, 2.0, 3, 'jjj', 1]
```

### 插入元素

`.insert(位置，插入元素)`为列表插入元素

```python
name = ['lindy','Alice','Leimei','Jack']
name.insert(0,'Yangyang')
print(name)
# 输出：['Yangyang', 'lindy', 'Alice', 'Leimei', 'Jack']
```

### 修改列表值

```python
name = ['lindy','Alice','Leimei','Jack']
name[2] = 'Yangyang'
print(name)
#输出：['lindy', 'Alice', 'Yangyang', 'Jack']
```

### 删除列表值

如果你确切的知道要删除元素的索引：用del 语句

```python
name = ['Yangyang','lindy','Alice','Leimei','Jack']
del name[1]
print(name)
#输出：['Yangyang', 'Alice', 'Leimei', 'Jack']
```

如果你不知道要删除元素的索引：用remove()方法

```python
name = ['Yangyang','lindy','Alice','Leimei','Jack']
name.remove('Alice')
print(name)
# 输出：['Yangyang', 'lindy', 'Leimei', 'Jack']
```

关于删除元素，还有一种方法，这种方法是，你虽然删除了这个元素，但是这个元素的内容，你还是要用的。这时候，我们用`.pop()`方法

```python
name = ['Yangyang','lindy','Alice','Leimei','Jack']
name_pop = name.pop()  # 默认弹出最后一个
print(name)
print(name_pop)
# 输出：
# ['Yangyang', 'lindy', 'Alice', 'Leimei']
# Jack
```

弹出列表中任何位置的元素

```python
name = ['Yangyang','lindy','Alice','Leimei','Jack']
name_pop = name.pop(2)
print(name)
print(name_pop)
# 输出：
# ['Yangyang', 'lindy', 'Leimei', 'Jack']
# Alice
```

## 4.5 列表操作

### 串联若干字符

```.join()```  串联若干字符，这是一个**字符串**的方法，但是可以处理列表数据，将列表的数据连接起来

```python
text = ["I","Love","You"]
print(" ".join(text))  # 输出： I Love You
print("、".join(text))  # 输出： I、Love、You
```

### 获取列表长度

```len()  ```返回列表、字符串长度

```python
name = ['Yangyang','lindy','Alice','Leimei','Jack']
print(len(name)) 
# 输出：5

sentence = "临渊羡鱼不如退而结网"
print(len(sentence))  
# 输出：10
```

### 列表排序

`.sort()`：永久排序，按字母顺序或者数字

```python
name = ['Yangyang','Lindy','Alice','Leimei','Jack']
name.sort()  # 正着排
print(name)
# 输出：
# ['Alice', 'Jack', 'Leimei', 'Lindy', 'Yangyang']

number = [3,77,44,278,35,1,5567,58]
number.sort()
print(number)
# 输出：
# [1, 3, 35, 44, 58, 77, 278, 5567]

name = ['Yangyang','Lindy','Alice','Leimei','Jack']
name.sort(reverse=True)  # 倒着排
print(name)
# 输出：
# ['Yangyang', 'Lindy', 'Leimei', 'Jack', 'Alice']

# 数字和字母在一起
number = ['3','23456645','6789','Yangyang','Lindy','Alice','Leimei','Jack']
number.sort()
print(number)
# 输出：
# ['23456645', '3', '6789', 'Alice', 'Jack', 'Leimei', 'Lindy', 'Yangyang']
```

`sorted()`：临时排序

```python
name = ['Yangyang','Lindy','Alice','Leimei','Jack']
print(sorted(name))  # 正着排
print(name)
# 输出：
# ['Alice', 'Jack', 'Leimei', 'Lindy', 'Yangyang']
# ['Yangyang', 'Lindy', 'Alice', 'Leimei', 'Jack']
```

### 计算元素出现次数

```count(n) ```返回元素 n在列表中出现的次数

```python
zoo = ["熊猫", "长颈鹿", "金丝猴", "熊猫", "长颈鹿", "大象", "熊猫", "海獭", "羊驼", "熊猫", "海獭", "金丝猴", "熊猫", "大象", "长颈鹿", "羊驼"]
print(zoo.count("熊猫"))
# 输出 5，元素"熊猫"在列表 zoo 中出现5次
```

### 拷贝和清空列表

```python
# clear
name = ['Yangyang','Lindy','Alice','Leimei','Jack','Yangyang']
name.clear()
print(name)
# 输出：[]
```

```python
# copy
name = ['Yangyang','Lindy','Alice','Leimei','Jack','Yangyang']
name1 = name.copy()
print(name1)
# 输出：['Yangyang', 'Lindy', 'Alice', 'Leimei', 'Jack', 'Yangyang']
```

**copy和直接赋值的不同：**

如果直接赋值，改变赋值的对象`number1`，原来的`number`也会被修改

```python
number = [2,3,4,5,6,7,8]
number1 = number
number1[1] = 1
print(number)
print(number1)
# 输出：
# [2, 1, 4, 5, 6, 7, 8]
# [2, 1, 4, 5, 6, 7, 8]
```

如果是copy，则相互不影响

```python
number = [2,3,4,5,6,7,8]
number1 = number.copy()
number1[1] = 1
print(number)
print(number1)
# 输出：
# [2, 3, 4, 5, 6, 7, 8]
# [2, 1, 4, 5, 6, 7, 8]
```

## 4.6 列表所有方法

```python
dir(list)
```

```python
 'append',  # 添加列表元素
 'clear',  # 清空列表
 'copy',  # 拷贝列表
 'count',  # 返回元素在列表中出现的次数
 'extend',  # 拓展列表
 'index',  #查找元素出现的位置
 'insert',  # 插入列表元素
 'pop',  # 删除列表元素,这个元素你还要用
 'remove',  # 删除列表元素，根据内容删
 'reverse',  # 反转列表元素
 'sort' # 永久性排序
```

`zip()` ：将两个列表中的元素一一组成对，形成一个新的对象

`range(a,b,c) `：a,b,c为数字。a为开始，b为结尾，c为间隔；a省略时默认为0，c省略时默认为1

```len() ```：返回列表、字符串长度

`sorted()`：临时排序

`del`：删除列表元素-根据位置

## 4.7 列表计算

```python
number = list(range(20))
print(number)
# 输出：[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]

print(min(number))
# 输出：0

print(max(number))
# 输出：19

print(sum(number))
# 输出：190
```

## 4.8 实践：操作列表

建立一个空列表，把你最喜欢的五个东西依次添加进去，然后把所有的方法，都给它倒腾一遍，确保自己能熟练运用。

请在作业的最后一行输出：

```
昵称：第4节课作业
```

# 五、循环

> 本章内容运行环境：`Jupyter Notebook`
>
> 本单元视频链接：https://v.youku.com/v_show/id_XNDYyNTQ1MTcyMA==.html

## 5.1 for 循环

```python
for item in list_of_items:
    pass
```

- `in`后面，是一个列表
- `for -- in ---:`    不要忘记这个`:`
- 下一行要缩进，缩进几个字符都可以，但是要保证上下文统一

这里需要注意，在Python中，```缩进```非常非常非常重要。

学过C或者MATLAB等其他编程语言的同学应该了解，一般是用```｛｝```来把函数包裹起来，系统通过```｛```判定函数开始，```｝```判定函数结束。

但是Python是通过```缩进```来判断的，所以你的```缩进```必须一致。比如都用2个空格，或者都用4个空格。

```python
nameList = ['Yangyang','Lindy','Alice','Leimei','Jack']
for eachName in nameList:
    print(eachName)
    
# 输出：
# Yangyang
# Lindy
# Alice
# Leimei
# Jack
```

```python
nameList = ['Yangyang','Lindy','Alice','Leimei','Jack']
for eachName in nameList:
    print(eachName, ', Hello')
    
# 输出：
# Yangyang , Hello
# Lindy , Hello
# Alice , Hello
# Leimei , Hello
# Jack , Hello
```

看一下缩进的区别

```python
nameList = ['Yangyang','Lindy','Alice','Leimei','Jack']
for eachName in nameList:
    print(eachName)
    print('Hello!')
    
# 输出：
# Yangyang
# Hello!
# Lindy
# Hello!
# Alice
# Hello!
# Leimei
# Hello!
# Jack
# Hello!
```

```python
nameList = ['Yangyang','Lindy','Alice','Leimei','Jack']
for eachName in nameList:
    print(eachName)
print('Hello!')

# 输出：
# Yangyang
# Lindy
# Alice
# Leimei
# Jack
# Hello!
```

### range()

在上一章列表里，我们学习了可以用`range()`函数生成列表

```python
for i in range(5):  # 等价于range(0,5,1)
    print(i)
    
# 输出：
0
1
2
3
4
```

练习：生成一个列表[0,1,4,9,16,25,36,49....]

```python
squares = []
for i in range(10):
    squares.append(i**2)
print(squares)
# 输出：[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

练习：生成九九乘法表

```python
for i in range(1,10):
    for j in range(1,i+1):
        print("{}*{}={}".format(i,j,i*j),end=" ")
    print("\n")
```

![image-20200410102715297](http://cdn.zhaojingyi0126.com/IMG/image-20200410102715297.png)

## 5.2 列表推导式

（大概了解就可以，现在没办法掌握，也没关系）

拿刚刚求平方的代码为例，我们原来是这么写的

```python
squares = []
for i in range(10):
    squares.append(i**2)
print(squares)

#输出：[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

有了列表推导式，我们可以这么写

```python
squares = [i**2 for i in range(10)]
print(squares)

#输出：[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

两者的输出是一样的，只是列表推导式更简洁和高效

## 5.3 while 循环


```python
while expression:
    pass
```

```while ```循环的内容会一直循环执行， 直到 expression 值为假（条件失效）， 循环结束

```
count = 0
while (count < 9):
    print( 'the index is:', count)
    count += 1

#输出：
the index is: 0
the index is: 1
the index is: 2
the index is: 3
the index is: 4
the index is: 5
the index is: 6
the index is: 7
the index is: 8
```

while循环常常用于你不确定，这个循环，要循环多少次

用《[Python编程：从入门到实践](https://weread.qq.com/web/reader/19532980715c01921954a54kc81322c012c81e728d9d180)，7.2.2节》中的一个例子：

不管用户输入什么，系统都会重复一遍，直到用户输入“quit”，程序结束

```python
print("Tell me something, and I will repeat it back to you:")
message = ""
while message != "quit":
    message = input("Your input:")
    print("Output:",message)
# 输出：
# Tell me something, and I will repeat it back to you:
# Your input:hi,I'm yangyang
# Output: hi,I'm yangyang
# Your input:quit
# Output: quit
```

避免无限循环

```python
x = 1
while x <= 5:
    print(x)
    x += 1
```

如果你忘记了`x += 1`，这个程序就会陷入无限循环

可以通过`Ctrl+C`退出，也可以直接把软件关了。。

## 5.4 break 和 continue

break：停止循环（直接退出了）
举个例子：在一大堆```士```中，找到```土```，就结束（break）

```python
shi_and_tu = ["士","士","士","士","士","士","士","土","士","士","士","士"]
for char in shi_and_tu:
    print(char)
    if char == "土":
        print("我找到土啦！")
        break
```

continue：跳过循环（本次退出，下次还来）
举个例子：未满18岁的输出，超过18岁的，就跳过（continue）

```python
ages = [16, 15, 23, 33, 67, 8, 10, 32]
for age in ages:
    if age >= 18:
        continue
    print(age)
    print("未达到18岁，不可以买酒")
```

## 5.5 实践：输出豆瓣首页数据

【小练习】

给定整数序列， 求这个序列中子序列和的最大值

```python
number = [-2, 11, 8, -4, -1, 16, 5, 0]
sum_n = []
for i in range(len(number)):
    sum_n.append(number[i])
    for j in range(i):
        sum_n.append(sum(number[j:i+1]))
print(max(sum_n))
```

【清洗豆瓣数据】

结合**【3.11节，字符串】**的实践，输出[豆瓣电影 Top 250](https://movie.douban.com/top250)，前25部电影详情

思路：

1. 先去网站上，把所有内容贴下来，保存到`txt`文件中
2. 读取txt文件
3. 切割字符串
4. 加入循环，输出前25项结果

注意：

1. 注意`txt`文件的路径，要么和代码保存在一个路径下面，要么把路径写正确
2. `for` 循环别忘记冒号`:`
3. 注意缩进，保持统一

参考代码：

```python
text = open('D:/Python/html_text.txt', 'rb')
text = text.read().decode('utf-8')
movies = text.split('class="grid_view\">')[1].split('<li>')  #movies此时是一个列表

for i in range(1,len(movies)):
    movie = movies[i]    # 把movies这个列表的值，依次取出
    title = movie.split('</span>')[0].split('>')[-1]
    rate = movie.split('v:average\">')[1].split('</span>')[0]
    number = movie.split('star')[1].split('<span>')[1].split('</span>')[0]
    quote = movie.split('inq')[1].split('>')[1].split('<')[0]
    year = movie.split(' <p class="">')[1].split('<br>')[1].split('&nbsp')[0].strip()
    print("{},《{}》，豆瓣评分{}，{}。推荐理由：{}".format(year,title, rate, number, quote))
```

![](http://cdn.zhaojingyi0126.com/IMG/image-20200409104516529.png)

请在作业的最后一行输出：

```
昵称：第5节课作业
```

# 六、元组

## 6.1 定义元组

元组和列表相似，列表是[---]，元组是(---)

```python
number = (200,100,50)
type(number)
# 输出：tuple
```

## 6.2 访问元组

```python
number = (200,100,50)
print(number[0])
print(number[1])
print(number[2])
# 输出：
# 200
# 100
# 50
```

## 6.3 修改元组变量

**元组的元素是不能修改的**

比如，我试图重新赋值，这时候程序会报错

```python
number = (200,100,50)
number[0] = 300
print(number)
# 输出：'tuple' object does not support item assignment
```

但是这个操作，在列表里，是没问题的

```python
number = [200,100,50]
number[0] = 300
print(number)
# 输出：[300, 100, 50]
```

虽然元组的元素不能修改，但是我可以把整个元组都改掉

```python
number = (200,100,50)
number = (100,50)
print(number)
# 输出：(100, 50)
```

## 6.4 遍历元组中所有的值

```python
numbers = (200,100,50)
for number in numbers:
    print(number)
# 输出：
# 200
# 100
# 50
```

## 6.5 元组和列表的区别

相比于列表，元组是更简单的数据结构

元组的元素是不能修改的

如果需要储存的一组值，在整个程序里都不变，可以用元组

# 七、字典

> 本章内容运行环境：`Jupyter Notebook`
>
> 本单元视频链接：https://v.youku.com/v_show/id_XNDYyOTMzMjQ0MA==.html

## 7.1 字典定义

字典是一组**无序**键值对的集合

假设我们在一个英语网站学习，每天会背单词、做听力、做阅读。现在有一组数据：你背了单词（bdc） 30个；做了听力（listen）5句；做了阅读（read）2篇。我们可以创建一个`study`的字典将它们存放：

```python
study = {"bdc":30, "listen":5, "read":2}
```

1. 字典用 {} 包裹
2. 其中` "bdc" : 30`为一对键值对，其中`"bdc"`为键（key），`30` 为值（value）
3. 每对键值对由英文逗号` , `隔开
4. 最好在每一个逗号与下一个键值对之间用空格相隔，方读代码。

## 7.2 创建字典

在 Python 字典中：

键可以是字符串，也可以是数值

值可以是任何数据类型：字符串、数值、列表，甚至还可以是字典

```python
shanbey = {"study": {"bdc": {"num_today": 25, "used_time": 5.0}, "listen": {"num_today": 0,"used_time": 0}}}
print(shanbey)
```

这边展示了一个字典，value还是字典的例子（一般网页数据都长这样）。我们拆解一下这个字典

```python
"study": 
    {
    "bdc": 
        {
        "num_today": 25,
        "used_time": 5.0
   		}, 
    "listen": 
        {
        "num_today": 0,
        "used_time": 0
        }
	}
```

### 空字典

```python
study = {}
type(study)
# 输出：dict
```

### 合并列表

```zip() ```创建字典：用zip() 将两个列表合并为一个字典

```python
name = ["bdc", "listen", "read", "sentence"]
number = [30, 5, 2, 10]
zip_study = zip(name, number)
study = {key:value for key,value in zip_study}
print(study)
# 输出：{'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
```

先用```zip() ```将列表 `name` 和 `number`合并在变量`zip_study` 中。（在【4.3 列表】里讲过zip的用法）

接着，遍历 `zip_study`，把`name`作为key，`number`作为值

```python
key:value for key,value in zip_study
```
这用到了我们之前提到的列表推导式（5.2节），我们可以把这行代码分开，理解为
```python
for key,value in zip_study:
    key:value  #这是字典组成的样子
```
## 7.3 为字典添加键

添加新键：用以下语句为字典添加新键

```python
study = {'bdc': 30, 'listen': 5, 'read': 2}

# 字典[新键] = 新值
study['sentence'] = 10

print(study)
# 输出：{'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
```

```.update()```：用 .update() 一次性向字典加入多对键值对

```python
study = {'bdc': 30}
study.update({ 'listen': 5, 'read': 2, 'sentence': 10}) 
print(study)
# 输出：{'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
```

更新字典值：如果有一个键对应的值需要变动，用添加键时的方法，重新为该键赋新值

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
study['sentence'] = 200
print(study)
# 输出：{'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 200}
```

## 7.4 字典取值

可以通过字典的键来获取其对应的值：```字典[键]```

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
print(study['sentence'])
# 输出：10
```

字典无效键：当取字典键值时，如果键并不存在于字典中，该键无效，计算机会返回错误。

```python
study = {'listen': 5, 'read': 2, 'sentence': 10}
print(study['bdc'])
# KeyError: 'bdc' ，系统会报错
```

```.get()```：根据键来取字典中相应的值

如果键不存在于字典中，.get() 默认返回 None

当键不存在于字典中时，也可以手动设置返回值

```python
study = {'listen': 5, 'read': 2, 'sentence': 10}
print(study.get('listen'))  # 输出：5
print(study.get('bdc'))  # 输出：None
print(study.get('bdc','没有背单词'))  # 输出：没有背单词
```

## 7.5 try 和 except

`try`和 `except`条件判断，帮助检查代码中可能存在的错误

计算机会先执行 `try`条件下的语句，一旦出现例外情况，比如错误 NameError 或者 ValueError，计算机会终止执行 `try`条件下的语句，并且当该例外情况满足 `except`中指定的条件，计算机会执行`except` 中的语句。

```try/except ```取值：如果字典中没有相应的键，还可以用`try/except`的方法来捕获 `KeyError` 的出现。

```python
study = {'listen': 5, 'read': 2, 'sentence': 10}
try:
    print(study['bdc'])
except:
    print("没有背单词")
# 输出：没有背单词
```

## 7.6 删除字典键

```.pop() ``` ：删除字典中的键及其值

如果需要删除的键不在字典之中，在 .pop() 方法中加上对应的参数，.pop() 返回该参数

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
print(study.pop('sentence')) # 输出：10
print(study) 
# 输出：{'bdc': 30, 'listen': 5, 'read': 2}
```

## 7.7 获取所有的键和值

### 获取字典所有的键

我们可以用两种方法获得字典中所有的键。

```list(目标字典)```：

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
print(list(study))
# ['bdc', 'listen', 'read', 'sentence']
```

```.keys() ```：

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
for name in study.keys():
    print(name)
# 输出：
bdc
listen
read
sentence
```

列表推导式

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
name = [key for key in study.keys()]
print(name)
# 输出：['bdc', 'listen', 'read', 'sentence']
```

### 获得字典所有的值

```.values()``` 获得字典中所有的值

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
for number in study.values():
    print(number)
# 输出：
30
5
2
10
```

列表推导式

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
number = [value for value in study.values()]
print(number)
# 输出：[30, 5, 2, 10]
```

### 获得字典中所有的键值对

用``` .items() ```获取字典中的所有键值对

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
for key,value in study.items():
    print("学习"+key+"的数量为"+str(value))
# 输出：
# 学习bdc的数量为30
# 学习listen的数量为5
# 学习read的数量为2
# 学习sentence的数量为10
```

## 7.8 字典所有方法

```python
dir(dict)
```

```python
 'clear',
 'copy',
 'fromkeys',
 'get',  # 根据键来取字典中相应的值
 'items',  # 获取字典中的所有键值对
 'keys',  # 获取字典中的所有键
 'pop',  # 删除
 'popitem',
 'setdefault',
 'update',  # 更新多对键值对
 'values'  # 获取字典中的所有值
```

## 7.9 实践：清洗扇贝打卡数据

清洗扇贝打卡数据

扇贝打卡数据：https://www.shanbay.com/api/v1/checkin/user/------/ ，最后一部分，是你的扇贝ID

```python
import requests  # 导入requests模块
ID = "16888030"  # 扇贝ID
web = "https://www.shanbay.com/api/v1/checkin/user/"+str(ID)+"/"  # 网址：打卡记录
res = requests.get(web)  # requests发起请求，静态网页用get
LearningData = res.json()  # LearningData就是字典格式

NickName = LearningData['data'][0]['user']['nickname']  # 获取昵称

for LearningDataDaily in LearningData['data']:
    checkin_date =  LearningDataDaily['checkin_date']
    try:
        bdc_num_today = LearningDataDaily['stats']['bdc']['num_today']
        bdc_used_time = LearningDataDaily['stats']['bdc']['used_time']
    except:  
        bdc_num_today = 0
        bdc_used_time = 0.0        
    print("{}，{}背单词{}个，用时{}分钟".format(checkin_date,NickName,bdc_num_today,bdc_used_time))
    
# 输出：
2020-04-09，洋阳背单词25个，用时5.0分钟
2020-04-08，洋阳背单词25个，用时28.0分钟
2020-04-07，洋阳背单词45个，用时6.0分钟
2020-04-06，洋阳背单词25个，用时19.0分钟
2020-04-05，洋阳背单词25个，用时6.0分钟
2020-04-04，洋阳背单词25个，用时6.0分钟
2020-04-03，洋阳背单词25个，用时6.0分钟
2020-04-02，洋阳背单词25个，用时17.0分钟
2020-04-01，洋阳背单词0个，用时0.0分钟
2020-03-31，洋阳背单词25个，用时15.0分钟
2020-03-30，洋阳背单词25个，用时7.0分钟
2020-03-29，洋阳背单词25个，用时10.0分钟
2020-03-28，洋阳背单词0个，用时0.0分钟
2020-03-27，洋阳背单词25个，用时8.0分钟
2020-03-26，洋阳背单词25个，用时15.0分钟
2020-03-25，洋阳背单词25个，用时12.0分钟
2020-03-24，洋阳背单词25个，用时13.0分钟
2020-03-23，洋阳背单词25个，用时67.0分钟
2020-03-22，洋阳背单词0个，用时0.0分钟
2020-03-21，洋阳背单词0个，用时0.0分钟
```

请在作业的最后一行输出：

```
昵称：第6节课作业
```

# 八、数据类型转换

整形 `int`

```python
number = 100
```

字符串 `str`

```python
name = 'Yangyang'
```

列表 `list`

```python
name_list = ['Yangyang', 'Lindy', 'Alice', 'Leimei', 'Jack']
```

元组 `tuple`

```python
name_tuple = ('Yangyang', 'Lindy', 'Alice', 'Leimei', 'Jack')
```

字典 `dict`

```python
study = {"bdc":30, "listen":5, "read":2}
```

![image-20200410141441363](http://cdn.zhaojingyi0126.com/IMG/image-20200410141441363.png)

【字符串】转【整形】

```python
int('25')
# 输出：
# 25
```

【整形】转【字符串】

```python
str(3820594)
# 输出：
# '3820594'
```

【字符串】转【列表】
（数字不能直接转列表）

```python
list('3820594')  
# 输出：
# ['3', '8', '2', '0', '5', '9', '4']
```

 【列表】转【元组】

```python
tuple(list('3820594'))
# 输出：
# ('3', '8', '2', '0', '5', '9', '4')
```


 【元组】转【列表】

```python
list(tuple('3820594'))
# 输出：
# ['3', '8', '2', '0', '5', '9', '4']
```

【元组】转【字符串】

```python
number = ('3', '8', '2', '0', '5', '9', '4')
"".join(number)
# 输出：
# '3820594'
```

【列表】转【字符串】

```python
number = ['3', '8', '2', '0', '5', '9', '4']
"".join(number)
# 输出：
# '3820594'
```

【字典】转【列表】，只有key，没有value

```python
study = {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
print(list(study))
# 输出：
# ['bdc', 'listen', 'read', 'sentence']
```

【两个列表】转【字典】

```python
name = ["bdc", "listen", "read", "sentence"]
number = [30, 5, 2, 10]
study = {key:value for key,value in zip(name, number)}
print(study)
# 输出：
# {'bdc': 30, 'listen': 5, 'read': 2, 'sentence': 10}
```

# 九、条件

> 本章内容运行环境：`Jupyter Notebook`
>
> 本单元视频链接：https://v.youku.com/v_show/id_XNDYzMDc0NzYwMA==.html

## 9.1 布尔值

布尔值，Python中有专门的数据类型：`bool`

布尔值有两个：`True`和 `False`（首字母须大写）,也被称作布尔变量

## 9.2 运算符

`==` 和`!=`，分别表示“相等”和“不等”

```python
name = "yangyang"  # 这是赋值
name == "yangyang"  # 这是判断：是否相等
# 如果相等，返回True
# 如果不相等，返回False
```

```python
18 == 19  # 返回False
18 != 19  # 返回True
```

`> 、< 、 >= 、<=`分别对应：大于、小于、大于等于和小于等于四种比较关系

## 9.3 逻辑符号

- `and`：将两个条件判断联结起来，只有当前后两个条件都为 True时，整个 and 联结条件才判断为 True，否则为 False
- `or`：前后至少有一个 True，则 or 联结的整个判断条件为 True。如果 or 前后都是 False，则 or 联结的整个判断条件也为 False
- `not`：当 not 放在 True 或者 False 之前，得到相反的逻辑值结果

```python
a>18 and a<20  # and
a<18 or a>20  # or
not(a<18)  # not
```

## 9.4 if 语句

条件语句遵循以下基本逻辑：如果……，那么……

- `if`等同于 “如果”， : 等同于 “那么”。另外，在if 语句下方的代码，需要缩进
- `else`一般在条件判断的结尾，判断那些没有满足 if 条件的状况
- `elif`是 else if 的缩写，当 `elif`之前的条件不被满足时，计算机会验证 `elif`中的判断条件是否为 `True`

```python
a = 3
if a > 2:
  print("a大于2")
elif a > 1:
  print("a大于1")
# 输出：
# a大于2
```

## 9.5 实践

【小练习】

1. 用代码打印出一个菱形

   ![](http://cdn.zhaojingyi0126.com/IMG/image-20200413131112919.png)

2. 鸡兔同笼，头35，脚94。问鸡和兔各有几只？

3. 打印出所有的水仙花数，水仙花数的要求是一个三位数（比如153），满足这个规律：153=1\^3+5\^3+3\^3

4. 有一个单词和一个字符串，判断字符串是否可以扩展成这个单词

5. 参考答案：[Python：小练习](Python/eg.md)

【实践】

在昨天清洗扇贝打卡的基础上，进阶一下

1. 获取10个人的打卡数据
2. 计算他们最近7天的打卡情况（单词部分）
3. 如果他们7天内，总学习时间超过1小时，判定为“学习认真”
4. 如果没有超过1小时，判定为“需要继续努力呀”

```python
IDs = ['49793185','60782137','210260232','40793353','41273824','64839964','66470683','37166209',
'58575787','2492821']  # 扇贝ID

# 输出：
# 最近一周，Lily Cao背单词125个，用时55.0分钟,需要继续努力呀
# 最近一周，o蟲o背单词300个，用时87.0分钟,学习认真
# 最近一周，莲背单词420个，用时81.0分钟,学习认真
# 最近一周，罱背单词140个，用时95.0分钟,学习认真
# 最近一周，Abbey?背单词700个，用时375.0分钟,学习认真
# 最近一周，Melody背单词700个，用时64.0分钟,学习认真
# 最近一周，一棵甜橙树背单词200个，用时53.0分钟,需要继续努力呀
# 最近一周，lj背单词239个，用时57.0分钟,需要继续努力呀
# 最近一周，i think i背单词300个，用时57.0分钟,需要继续努力呀
# 最近一周，珊瑚背单词350个，用时106.0分钟,学习认真
```

参考代码

```python
import requests  # 导入requests模块
IDs = ['49793185','60782137','210260232','40793353','41273824','64839964','66470683','37166209',
'58575787','2492821']  # 扇贝ID

for ID in IDs:
    web = "https://www.shanbay.com/api/v1/checkin/user/"+str(ID)+"/"  # 网址：打卡记录
    res = requests.get(web)  # requests发起请求，静态网页用get
    LearningData = res.json()  # LearningData就是字典格式

    NickName = LearningData['data'][0]['user']['nickname']  # 获取昵称

    bdc_num = 0
    bdc_used_time = 0
    
    for day in range(7):
        LearningDataDaily  = LearningData['data'][day]
        checkin_date =  LearningDataDaily['checkin_date']
        try:
            bdc_num += LearningDataDaily['stats']['bdc']['num_today']
            bdc_used_time += LearningDataDaily['stats']['bdc']['used_time']
        except:  
            bdc_num += 0
            bdc_used_time += 0.0        
    if bdc_num > 60:
        print("最近一周，{}背单词{}个，用时{}分钟,学习认真".format(NickName,bdc_num,bdc_used_time))
    else:
        print("最近一周，{}背单词{}个，用时{}分钟,需要继续努力呀".format(NickName,bdc_num,bdc_used_time))
```

请在作业的最后一行输出：

```
昵称：第7节课作业
```

# 十、函数

> 本章内容运行环境：`Jupyter Notebook`
>
> 本单元视频链接：https://v.youku.com/v_show/id_XNDYzMjIyMjU4OA==.html

## 10.1 定义函数

定义一个函数要使用```def```语句，```参数```不是必须的
```python
# def 函数名（参数）：
def my_abs(x):
```
```函数体```在```函数名```下方，需要**缩进**。这里定义一个判断绝对值的函数```my_abs```。
```python
def my_abs(x):
    if x >= 0:
        return x
    else:
        return -x
```
### 空函数
如果想定义一个什么事也不做的空函数，可以用```pass```语句：
```python
def my_abs(x):
    pass
```
```pass```语句什么都不做，那有什么用？

```pass```可以用来作为占位符，比如现在还没想好怎么写函数的代码，就可以先放一个```pass```，让代码能运行起来。

## 10.2 调用函数
```python
# 函数名（参数）
my_abs(2)
```
![image-20200406185845120](http://cdn.zhaojingyi0126.com/image-20200406185845120.png)

注意： 刚刚的代码是在调试窗口写的，所以可以直接输出结果

当你在文档中写代码，并且你需要屏幕上输出结果，你需要加`Print`，或者你在调试窗口调用它

![](http://cdn.zhaojingyi0126.com/IMG/image-20200407090613413.png)

调用函数的时候，参数也不是必须的，比如你可以直接```my_abs()```，这时候，我们就需要函数设定一个默认参数。

## 10.3 参数

### 默认参数
- 函数的参数可以有一个默认值
- 默认参数以赋值语句的形式提供
- 函数调用时如果没有提供这个参数， 它就取这个值做为默认值
刚刚定义过的```my_abs```函数，我们重新修改一下
```
def my_abs(x=3):
    if x >= 0:
        return x
    else:
        return -x
```
如果调用函数的时候，没有输入任何参数，那默认x就是3
如果输入了参数，那以输入的参数为准，忽略默认值

![](http://cdn.zhaojingyi0126.com/image-20200406190147837.png)

## 10.4 传递参数

### 位置参数

- 一个函数可以有多个参数，各个参数用逗号隔开
- 在定义函数时有N个参数，在调用时，也需要提供N个参数

举例，我们定义一个求最大值的参数

```python
def my_max(number1, number2):
    if number1 > number2:
        print(number1 )
    else:
        print(number2)
```
在这个例子中，我们看到，输入的参数，默认第一个就是```number1```，第二个就是```number2```，这是**位置参数**

### 关键字参数
比如我函数里面，定义了10个参数，那每次必须都要按照位置写，挺容易搞错的。这时候，我们可以用关键字参数。

举个列子，输出我的名字和爱好

```python
def my_hobby(name, hobby):
    print(name+"喜欢"+hobby)
```
可以看到，没有指定关键词的时候，默认就是按照位置来选择参数（看第二行的输出）
如果我们指定```name```是```YangYang```，那么就是按照指定的关键字来对应参数
```python
my_hobby("YangYang","Python")
# 输出：YangYang喜欢Python
my_hobby("Python","YangYang")
# 输出：Python喜欢YangYang
my_hobby(hobby="Python",name="YangYang")
# 输出：YangYang喜欢Python
```
## 10.5 返回
```python
def my_max(number1, number2):
    if number1 > number2:
        return number1
    else:
        return number2
```
在我们刚刚的代码中，已经看到，用```return```返回我们要的值

`return`后面可以直接加计算

```python
def my_add(number1, number2):
	return number1+number2

my_add(3,4)
# 输出：7
````

### 多值返回
我们可以一口气返回很多个值
```python
def my_cal(number1, number2):
	my_add = number1+number2    # 加法
	my_minus = number1-number2  # 减法
	return my_add,my_minus

my_cal(5,3)
# 输出：(8, 2)
```

## 10.6 作用域
最后，我们讲一下**全局作用域**和**局部作用域**

简单来说，定义在函数**内部**的，就是局部作用域

- 全局变量，在函数的外面，在整个代码中都有作用
- 局部变量，在函数的里面，只在局部作用域有作用
- 在函数内部，你可以调用全局变量
- 在函数外部，你无法使用局部变量

```python
global_str = 'foo'
def foo():
    local_str = 'bar'
    return global_str + local_str
```
```global_str ```是一个全局变量

```local_str``` 是一个局部变量

来个例子

```python
a = 2
def my_cal():
	a = 3
print(a)
# 输出：2
```
- 在函数外部，我定义了一个全局变量```a```，```a```的值是2

- 在函数内部，我定义了一个局部变量```a```，```a```的值是3

我在函数外，输出```a```，```a```的值还是2。所以，函数内的操作，和全局变量没关系。那我在函数内定义这个```a```，有什么用？

```python
a = 2
def my_cal():
	a = 3
	print(a)
my_cal()   #调用函数
# 输出：3
```
在这个函数内部，值确实变成3了。当我调用这个函数的时候，内部的值发生了变化

最后，就记住：

局部变量，只能用在函数里面，在函数里面，是有作用的

但是到了函数外面，局部变量就没作用了，只看全局变量

**怎么判断是不是在函数里面？**

看缩进。缩进很重要。

缩进的位置相同，代表它们是一个等级的

## 10.7 传递任意数量的参数

### *args

传入0个或任意个参数，`*args` 表示任意个无名参数，类型为 `tuple`

```python
def function(a,*args):
	pass
```

举个例子

```python
def number(*num):
    print(num)
number(1,2,3)
number(1,2,3,4,5,6)
# 输出：
# (1, 2, 3)
# (1, 2, 3, 4, 5, 6)
```

### **kwargs

`**kwargs`表示关键字参数，类型为 `dict`

任意数量的参数可以和位置参数，或者关键词参数结合起来

比如统计班级学生的情况，有两个信息是必须要知道的，姓名和年龄，其他信息，可以由学生自己填写

```python
def build_student(name,age,**other):
    student = {}
    student['name'] = name
    student['age'] = age
    for key,value in other.items():
        student[key] = value
    return student

print(build_student('yangyang', 18, hobby='Python'))
print(build_student('york', 20, hobby='Study', like='Wife'))

# 输出：
# {'name': 'yangyang', 'age': 18, 'hobby': 'Python'}
# {'name': 'york', 'age': 20, 'hobby': 'Study', 'like': 'Wife'}
```

## 10.8 内置函数

> 根据官网内容整理
>
> https://docs.python.org/zh-cn/3.7/library/functions.html#any

> Python 解释器内置了很多函数和类型，您可以在任何时候使用它们。以下按字母表顺序列出它们。

|                                                              |                                                              |                                                              |                                                              |                                                              |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- | ------------------------------------------------------------ |
| [`abs()`](https://docs.python.org/zh-cn/3.7/library/functions.html#abs) | [`delattr()`](https://docs.python.org/zh-cn/3.7/library/functions.html#delattr) | [`hash()`](https://docs.python.org/zh-cn/3.7/library/functions.html#hash) | [`memoryview()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-memoryview) | [`set()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-set) |
| [`all()`](https://docs.python.org/zh-cn/3.7/library/functions.html#all) | [`dict()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-dict) | [`help()`](https://docs.python.org/zh-cn/3.7/library/functions.html#help) | [`min()`](https://docs.python.org/zh-cn/3.7/library/functions.html#min) | [`setattr()`](https://docs.python.org/zh-cn/3.7/library/functions.html#setattr) |
| [`any()`](https://docs.python.org/zh-cn/3.7/library/functions.html#any) | [`dir()`](https://docs.python.org/zh-cn/3.7/library/functions.html#dir) | [`hex()`](https://docs.python.org/zh-cn/3.7/library/functions.html#hex) | [`next()`](https://docs.python.org/zh-cn/3.7/library/functions.html#next) | [`slice()`](https://docs.python.org/zh-cn/3.7/library/functions.html#slice) |
| [`ascii()`](https://docs.python.org/zh-cn/3.7/library/functions.html#ascii) | [`divmod()`](https://docs.python.org/zh-cn/3.7/library/functions.html#divmod) | [`id()`](https://docs.python.org/zh-cn/3.7/library/functions.html#id) | [`object()`](https://docs.python.org/zh-cn/3.7/library/functions.html#object) | [`sorted()`](https://docs.python.org/zh-cn/3.7/library/functions.html#sorted) |
| [`bin()`](https://docs.python.org/zh-cn/3.7/library/functions.html#bin) | [`enumerate()`](https://docs.python.org/zh-cn/3.7/library/functions.html#enumerate) | [`input()`](https://docs.python.org/zh-cn/3.7/library/functions.html#input) | [`oct()`](https://docs.python.org/zh-cn/3.7/library/functions.html#oct) | [`staticmethod()`](https://docs.python.org/zh-cn/3.7/library/functions.html#staticmethod) |
| [`bool()`](https://docs.python.org/zh-cn/3.7/library/functions.html#bool) | [`eval()`](https://docs.python.org/zh-cn/3.7/library/functions.html#eval) | [`int()`](https://docs.python.org/zh-cn/3.7/library/functions.html#int) | [`open()`](https://docs.python.org/zh-cn/3.7/library/functions.html#open) | [`str()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-str) |
| [`breakpoint()`](https://docs.python.org/zh-cn/3.7/library/functions.html#breakpoint) | [`exec()`](https://docs.python.org/zh-cn/3.7/library/functions.html#exec) | [`isinstance()`](https://docs.python.org/zh-cn/3.7/library/functions.html#isinstance) | [`ord()`](https://docs.python.org/zh-cn/3.7/library/functions.html#ord) | [`sum()`](https://docs.python.org/zh-cn/3.7/library/functions.html#sum) |
| [`bytearray()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-bytearray) | [`filter()`](https://docs.python.org/zh-cn/3.7/library/functions.html#filter) | [`issubclass()`](https://docs.python.org/zh-cn/3.7/library/functions.html#issubclass) | [`pow()`](https://docs.python.org/zh-cn/3.7/library/functions.html#pow) | [`super()`](https://docs.python.org/zh-cn/3.7/library/functions.html#super) |
| [`bytes()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-bytes) | [`float()`](https://docs.python.org/zh-cn/3.7/library/functions.html#float) | [`iter()`](https://docs.python.org/zh-cn/3.7/library/functions.html#iter) | [`print()`](https://docs.python.org/zh-cn/3.7/library/functions.html#print) | [`tuple()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-tuple) |
| [`callable()`](https://docs.python.org/zh-cn/3.7/library/functions.html#callable) | [`format()`](https://docs.python.org/zh-cn/3.7/library/functions.html#format) | [`len()`](https://docs.python.org/zh-cn/3.7/library/functions.html#len) | [`property()`](https://docs.python.org/zh-cn/3.7/library/functions.html#property) | [`type()`](https://docs.python.org/zh-cn/3.7/library/functions.html#type) |
| [`chr()`](https://docs.python.org/zh-cn/3.7/library/functions.html#chr) | [`frozenset()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-frozenset) | [`list()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-list) | [`range()`](https://docs.python.org/zh-cn/3.7/library/functions.html#func-range) | [`vars()`](https://docs.python.org/zh-cn/3.7/library/functions.html#vars) |
| [`classmethod()`](https://docs.python.org/zh-cn/3.7/library/functions.html#classmethod) | [`getattr()`](https://docs.python.org/zh-cn/3.7/library/functions.html#getattr) | [`locals()`](https://docs.python.org/zh-cn/3.7/library/functions.html#locals) | [`repr()`](https://docs.python.org/zh-cn/3.7/library/functions.html#repr) | [`zip()`](https://docs.python.org/zh-cn/3.7/library/functions.html#zip) |
| [`compile()`](https://docs.python.org/zh-cn/3.7/library/functions.html#compile) | [`globals()`](https://docs.python.org/zh-cn/3.7/library/functions.html#globals) | [`map()`](https://docs.python.org/zh-cn/3.7/library/functions.html#map) | [`reversed()`](https://docs.python.org/zh-cn/3.7/library/functions.html#reversed) | [`__import__()`](https://docs.python.org/zh-cn/3.7/library/functions.html#__import__) |
| [`complex()`](https://docs.python.org/zh-cn/3.7/library/functions.html#complex) | [`hasattr()`](https://docs.python.org/zh-cn/3.7/library/functions.html#hasattr) | [`max()`](https://docs.python.org/zh-cn/3.7/library/functions.html#max) | [`round()`](https://docs.python.org/zh-cn/3.7/library/functions.html#round) |                                                              |

## 10.9 实践

【小练习】

定义一个除法函数，如果除数为0，输出“0不能作除数！”

回顾一下`try`和 `except`判断，帮助检查代码中可能存在的错误

计算机会先执行 `try`条件下的语句，一旦出现例外情况，比如错误 NameError 或者 ValueError，计算机会终止执行 `try`条件下的语句，并且当该例外情况满足 `except`中指定的条件，计算机会执行`except` 中的语句。

```python
def divide_num(num1,num2):
  try:
    result = num1 / num2
    print (result)
  except ZeroDivisionError:
    print ("0不能作除数！")
```

其他小练习，可点击：[Python：小练习](Python/eg.md)

【实践】

用函数，重写【第九章】的实践题

比如：我可以构建一个函数`bdc`，计算大家背单词的情况

```python
def bdc(LearningData,days):
    ------
    return bdc_num,bdc_used_time
```

完整代码

```python
import requests  # 导入requests模块
IDs = ['49793185','60782137','210260232','40793353','41273824','64839964','66470683','37166209',
'58575787','2492821']  # 扇贝ID

def bdc(LearningData,days):
    bdc_num = 0
    bdc_used_time = 0
    
    for day in range(days):
        LearningDataDaily  = LearningData['data'][day]
        checkin_date =  LearningDataDaily['checkin_date']
        try:
            bdc_num += LearningDataDaily['stats']['bdc']['num_today']
            bdc_used_time += LearningDataDaily['stats']['bdc']['used_time']
        except:  
            bdc_num += 0
            bdc_used_time += 0.0  
    return bdc_num,bdc_used_time

for ID in IDs:
    web = "https://www.shanbay.com/api/v1/checkin/user/"+str(ID)+"/"  # 网址：打卡记录
    res = requests.get(web)  # requests发起请求，静态网页用get
    LearningData = res.json()  # LearningData就是字典格式

    NickName = LearningData['data'][0]['user']['nickname']  # 获取昵称

    days = 8
    bdc_num,bdc_used_time = bdc(LearningData,days)
    
    if bdc_num > 60:
        print("最近{}天，{}背单词{}个，用时{}分钟,学习认真".format(days, NickName, bdc_num, bdc_used_time))
    else:
        print("最近{}天，{}背单词{}个，用时{}分钟,需要继续努力呀".format(days, NickName, bdc_num, bdc_used_time))
```

还有，你可以构建一个函数，把单词、阅读、听力都输出

```python
import requests  # 导入requests模块
ID = "29834875"  # 扇贝ID
web = "https://www.shanbay.com/api/v1/checkin/user/"+str(ID)+"/"  # 网址：打卡记录
res = requests.get(web)  # requests发起请求，静态网页用get
LearningData = res.json()  # LearningData就是字典格式

NickName = LearningData['data'][0]['user']['nickname']  # 获取昵称

def GetInfo(ClassInfo):
    try:
        num_today = LearningDataDaily['stats'][ClassInfo]['num_today']
        used_time = LearningDataDaily['stats'][ClassInfo]['used_time']
    except:  
        num_today = 0
        used_time = 0.0  
    return num_today,used_time

for LearningDataDaily in LearningData['data']:
    checkin_date =  LearningDataDaily['checkin_date']
    bdc_num_today,bdc_used_time = GetInfo('bdc')
    listen_num_today,listen_used_time = GetInfo('listen')
    read_num_today, read_used_time = GetInfo('read')
    print("{}，{}背单词{}个，用时{}分钟，听力{}，用时{}分钟，阅读{}，用时{}分钟".format(
            checkin_date,NickName,
            bdc_num_today,bdc_used_time,
            listen_num_today,listen_used_time,
            read_num_today,read_used_time))
```

请在作业的最后一行输出：

```
昵称：第8节课作业
```

# 十一、模块

Python有一个标准库（不需要pip安装），里面涉及了很多内置模块

Python标准库（中文版）：https://docs.python.org/zh-cn/3/library/  

PyPI：https://pypi.org

## 11.1 导入模块

导入整个模块

```python
import 模块名
```

导入特定的函数

```python
from 模块名 import 函数名
```

如果模块或函数名太长，你觉得使用起来不方便，你可以设定它的缩写

```python
from 模块名 import 函数名 as 缩写名称
import 模块名 as 缩写名称
```

导入所有函数

```python
from 模块名 import *
```

## 11.2 常用库

### 数据处理

```python
import datatime  # 基础日期和时间数据类型
import calendar  # 通用日历函数
import random  # 生成随机数
import math  # 数学函数
import cmath  # 复数运算函数
import time  # 时间的访问和转换
import statistics  # 统计函数
import faker  # 创建伪数据，包括姓名、地址、电话等等
import numpy
import pandas
```

### 网页处理

```python
import requests #  访问网页
import re  # 正则化表达
```

### 文档处理

```python
import xlwt  # 写入Excel
```

### 游戏处理

```python
import pygame
```

### 数据可视化

```python
import plotly
import bokeh
import matplotlib
import seaborn
import missingno
import pygal
```

### [优秀的库推荐](Python/14.md)

从数据处理到人工智能

从Web解析到网络空间

从人机交互到艺术设计

## 11.3 内置模块

### this

```python
import this # 来感受一下创始人的初心
```

> The Zen of Python, by Tim Peters
>
> Beautiful is better than ugly.
>
> Explicit is better than implicit.
>
> Simple is better than complex.
>
> Complex is better than complicated.
>
> Flat is better than nested.
>
> Sparse is better than dense.
>
> Readability counts.
>
> Special cases aren't special enough to break the rules.
>
> Although practicality beats purity.
>
> Errors should never pass silently.
>
> Unless explicitly silenced.
>
> In the face of ambiguity, refuse the temptation to guess.
>
> There should be one-- and preferably only one --obvious way to do it.
>
> Although that way may not be obvious at first unless you're Dutch.
>
> Now is better than never.
>
> Although never is often better than *right* now.
>
> If the implementation is hard to explain, it's a bad idea.
>
> If the implementation is easy to explain, it may be a good idea.
>
> Namespaces are one honking great idea -- let's do more of those!

附上一段翻译

> 优美胜于丑陋（Python 以编写优美的代码为目标）
>
> 明了胜于晦涩（优美的代码应当是明了的，命名规范，风格相似）
>
> 简洁胜于复杂（优美的代码应当是简洁的，不要有复杂的内部实现）
>
> 复杂胜于凌乱（如果复杂不可避免，那代码间也不能有难懂的关系，要保持接口简洁）
>
> 扁平胜于嵌套（优美的代码应当是扁平的，不能有太多的嵌套）
>
> 间隔胜于紧凑（优美的代码有适当的间隔，不要奢望一行代码解决问题）
>
> 可读性很重要（优美的代码是可读的）
>
> 即便假借特例的实用性之名，也不可违背这些规则（这些规则至高无上）
>
> 不要包容所有错误，除非你确定需要这样做（精准地捕获异常，不写 except:pass 风格的代码）
>
> 当存在多种可能，不要尝试去猜测
>
> 而是尽量找一种，最好是唯一一种明显的解决方案（如果不确定，就用穷举法）
>
> 虽然这并不容易，因为你不是 Python 之父（这里的 Dutch 是指 Guido ）
>
> 做也许好过不做，但不假思索就动手还不如不做（动手之前要细思量）
>
> 如果你无法向人描述你的方案，那肯定不是一个好方案；反之亦然（方案测评标准）
>
> 命名空间是一种绝妙的理念，我们应当多加利用（倡导与号召）
>
> ————————————————
>
> 版权声明：本文为CSDN博主「赖勇浩」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
>
> 原文链接：https://blog.csdn.net/gzlaiyonghao/article/details/2151918

### datetime

> 提供用于处理日期和时间的类
>
> 在支持日期时间数学运算的同时，实现的关注点更着重于如何能够更有效地解析其属性用于格式化输出和数据操作。

举个例子：计算距离特定事件天数的例子

```python
from datetime import date

# 获取今天的日期
today = date.today()
print(today)

# 我的生日日期，年份保持不变
my_birthday = date(today.year, 1, 26)
print(my_birthday)

if my_birthday < today:
    my_birthday = my_birthday.replace(year=today.year + 1)

# 计算两个日期的差
time_to_birthday = abs(my_birthday - today)
print(time_to_birthday.days)

# 输出：
# 2020-04-14
# 2020-01-26
# 287
```

### time

```python
# 计算代码的运行时间
import time
start = time.time()

"""
此处是代码
"""

end = time.time()
print("花费", end-start, "秒")
```

### calendar

它提供了其它与日历相关的实用函数

```python
import calendar
calendar.prmonth(2020, 4)
# 输出：
     April 2020
Mo Tu We Th Fr Sa Su
       1  2  3  4  5
 6  7  8  9 10 11 12
13 14 15 16 17 18 19
20 21 22 23 24 25 26
27 28 29 30
```

```python
calendar.prcal(2020)
```

![](http://cdn.zhaojingyi0126.com/IMG/image-20200414104643853.png)

### random

```python
import random
random.random()
# 输出：0.4176217805064072（产生0到1之间的随机浮点数)
random.randint(1,10)
# 输出：3（产生1到10的一个整数型随机数）
random.uniform(1.1,5.4)
# 输出:3.1108641423436807（产生1.1到5.4之间的随机浮点数，区间可以不是整数）
random.choice(["A","B"])
# 输出：A（从序列中随机选取一个元素）
random.randrange(1,100,2)
# 输出：5（生成从1到100的间隔为2的随机整数）
```

### math

```python
import math
math.fabs()  # 绝对值
math.pow()  #次方计算
math.sqrt()  #平方根计算
math.pi()  #圆周率数值
```

### statistics

> 该模块提供了用于计算数字 ([`Real`](https://docs.python.org/zh-cn/3/library/numbers.html#numbers.Real)-valued) 数据的数理统计量的函数。此模块针对图形和科学计算器的水平。

| 方法                                                         | 解释                                         |
| ------------------------------------------------------------ | -------------------------------------------- |
| [`mean()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.mean) | 数据的算术平均数（“平均数”）                 |
| [`fmean()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.fmean) | 快速的，浮点算数平均数。                     |
| [`geometric_mean()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.geometric_mean) | 数据的几何平均数                             |
| [`harmonic_mean()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.harmonic_mean) | 数据的调和均值                               |
| [`median()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.median) | 数据的中位数（中间值）                       |
| [`median_low()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.median_low) | 数据的低中位数                               |
| [`median_high()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.median_high) | 数据的高中位数                               |
| [`median_grouped()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.median_grouped) | 分组数据的中位数，即第50个百分点。           |
| [`mode()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.mode) | 离散的或标称的数据的单模（最常见的值）。     |
| [`multimode()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.multimode) | 离散的或标称的数据的模式列表（最常见的值）。 |
| [`quantiles()`](https://docs.python.org/zh-cn/3/library/statistics.html#statistics.quantiles) | 将数据以相等的概率分为多个间隔。             |

## 11.4 实践

设计一个抽奖活动，输入参与人数、参与人姓名、参与人ID，输入中奖人名单

[Faker](https://faker.readthedocs.io/en/master/)库需要安装：`pip install Faker`

它用来伪造数据，支持多种语言。可以伪造地址、身份证号、城市、邮箱、姓名、职业等等等。

详情可戳：https://faker.readthedocs.io/en/master/locales/zh_CN.html

```python
from faker import Faker
import random

fake = Faker(locale = 'zh_CN')  # 伪造中文数据

n = input("请输入参与人数：")
m = input("请输入中奖人数：")

# 构造ID和人名
list_name = []
list_ID = list(range(0,int(n)))
for _ in range(int(n)):
  list_name.append(fake.name())

# 开始抽奖，随机抽取
print("\n")
print("中奖名单：")
for _ in range(int(m)):
    ID_random = random.choice(list_ID)
    location = list_ID.index(ID_random)
    print("ID：{}，{}".format(ID_random, list_name[location]))
    list_name.remove(list_name[location])
    list_ID.remove(list_ID[location])
    
# 输出：

# 请输入参与人数：20
# 请输入中奖人数：2

# 中奖名单：
# ID：5，林文
# ID：9，韩秀珍
```

请在作业的最后一行输出：

```
昵称：第9节课作业
```

