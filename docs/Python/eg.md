# Python：小练习 

> 练习题是从网上搜集来的，部分题目提供了多种解答

## 5行代码

在2000-3200中，找到所有可以被7整除，但不是5的倍数的整数

```python
for i in range(2000,3201):
    if i % 7 == 0 and i % 5 != 0:
        print(i)
```

打印出所有的水仙花数，153=1\^3+5\^3+3\^3

```python
for i in range(100,1000):
    j = str(i)
    if (int(j[0])**3+int(j[1])**3+int(j[2])**3) == int(j):
        print(i)
```

摄氏度和华氏度的转变

请输入温度：110C

转换温度为：230.0F

```python
data = input('请输入温度：')
if data[-1] == 'C':
    print('转换温度为：'+str(9*float(str(data[:-1]))/5+32)+'F')
else:
    print('转换温度为：'+str((float(str(data[:-1]))-32)*5/9)+'C')
```

有四个数字：5，6，7，8，能组成多少不相同的，且不重复的三位数

```python
for i in range(5,9):
    for j in range(5,9):
        for k in range(5,9):
            if i!=j and j!=k and i!=k:
                print(i*100+j*10+k)
```

```python
import itertools
data = [5,6,7,8]
for i in itertools.permutations (data, 3):
    print(i[0]*100+i[1]*10+i[2])
```

## 10行代码

鸡兔同笼，头35，脚94。问鸡和兔各有几只？

```python
head = 35
foot = 94

#  假设鸡是i，兔子是j
for i in range(head): 
    j = head - i
    if (i*2 + j*4) == foot:
        print (i,j)
```

创建一个函数，如果 PIN 有效则返回 True，如果不是则返回 False。PIN 码只能包含 4 位数或 6 位数字。

```python
def solution(pin):
    if len(pin) != 4 and len(pin) != 6:
        return False
    return(pin.isdigit())

print(solution('1234'))
```

已知一组学生的成绩，要求根据成绩给出等级。

- 成绩>=90，是A
- 成绩60-89之间，是B
- 成绩60以下，是C

```python
StudentScore = [90,80,75,50]
UpdateScore = []
for score in StudentScore:
    if score >= 90:
        UpdateScore.append("A")
    elif score >= 60 and score <= 89:
        UpdateScore.append("B")
    else:
        UpdateScore.append("C")
print(UpdateScore)        
```

用代码打印出一个菱形

![image-20200413131112919](http://cdn.zhaojingyi0126.com/IMG/image-20200413131112919.png)

```python
number = 4
for i in range(1,2*number):
    if i <= number:
        print(" "*abs(number-i)+"*"*(2*i-1))
    else:        
        print(" "*abs(number-i)+"*"*((2*i-1)-4*(i-number)))
```

给定整数序列， 求这个序列中子序列和的最大值。（子序列是指序列中连续的一部分，不能把所有的正整数相加。不会做的同学，可以把两个#去掉，看一下中间过程）

```python
number = [-2, 11, 8, -4, -1, 16, 5, 0]
sum_n = []
for i in range(len(number)):
    sum_n.append(number[i])
    # print(number[i])
    for j in range(i):
        sum_n.append(sum(number[j:i+1]))
        # print(number[j:i+1],"—>",sum(number[j:i+1]))
print(max(sum_n))
```

创建一个函数，该函数返回列表中指定元素出现的所有索引。

```python
def solution(lst, el):
    location = []
    for i in range(len(lst)):
        if lst[i]== el:
            location.append(i)
    return location

print(solution(["a", "a", "b", "a", "b", "a"], "a"))
print(solution([1, 5, 5, 2, 7], 5))
print(solution([1, 5, 5, 2, 7], 8))
```

假设一个n级台阶的梯子，每次可以走1步，也可以走2步。爬这个n级梯子总共有几种方法

```python
n = 20
def step(n):
    if n == 2:
        return 2
    elif n == 1:
        return 1
    else:
        return step(n-1) + step(n-2)  
s = step(n)
print(s)
```

创建一个函数，输入三个参数：字符串，2个字母。在字符串中，如果第一个字母都出现在第二个字母之前，则返回True。

```python
def solution(s, first, second):
    loc_second = s.index(second)
    s = s[::-1]
    loc_first = len(s)-s.index(first)+1    
    return loc_first<loc_second    

print(solution("a rabbit jumps joyfully", "a", "j"))
print(solution("knaves knew about waterfalls", "k", "w"))
print(solution("happy birthday", "a", "y"))
print(solution("precarious kangaroos", "k", "a"))
```

```python
def solution(s, first, second):
	fInd = max([i for i in range(len(s)) if s[i] == first])
	sInd = min([i for i in range(len(s)) if s[i] == second])
	return fInd < sInd

print(solution("a rabbit jumps joyfully", "a", "j"))
```

## 20行代码

判断一个字符串是否可以扩展成单词

```python
def judgestr(word,word_ref):
    for i in word:
        loc = word_ref.find(i)
        if  loc == -1:
            return False
        else:
            word_ref = word_ref[loc+1:]
    return True
        
word_ref = "beautiful"
word = "betul"
print(judgestr(word,word_ref))
```

模拟打牌，判断游戏是否继续

如果和对家的颜色或者数字一致，就可以出牌，输出"keep going..."

如果手里只剩一张牌了，输出"Uno!"

如果牌全都出完了，输出"You win!"

```python
def decision(cards,face_up_card):
    # 确定对面上家出牌的颜色和数字
    face_up_color = face_up_card.split(" ")[0]
    face_up_number = face_up_card.split(" ")[1]
    
    # 确认你手中的牌
    for card in cards:
        if card.split(" ")[0] == face_up_color or card.split(" ")[1] == face_up_number:
            cards.remove(card)
            break
    # 判断    
    if len(cards) == 1:
        print ("Uno!")
    elif len(cards) == 0:
        print ("You win!")
    else:
        print ("keep going...")
    
decision(["yellow 3","red 3"],"red 10")    
decision(["blue 1"],"blue 10")    
decision(["blue 1","green 2","yellow 4","red 2"],"blue 5") 
```

## 30行代码

注册邮箱时建立的新密码只有满足一些规则后才能创建成功。请你创建一个验证密码的函数，以符合以下规则：长度在 6 到 24 个之间。 至少一个大写字母（ A-Z ）。 至少一个小写字母（ a-z ）。 至少一个数字（ 0-9 ）。 最多 2 个重复字符：“aa” 可以；“aaa” 不行。 支持的特殊字符：！ @＃$％^＆*（）+ = _ - {} [] :; “'？ <> ,.

```python
def solution(password):
    if len(password)>24 or len(password)<6:
        return False
    for p in password:       
        if p.isdigit():
            p_digit = True
            break
        else:
            p_digit = False
    for p in password:        
        if p.islower():
            p_lower = True
            break
        else:
            p_lower = False
    for p in password:       
        if p.isupper():
            p_upper = True
            break
        else:
            p_upper = False
    if p_digit==p_lower==p_upper==False:
        if not (p in "！ @＃$％^＆*（）+ = _ - {} [] :; “'？ <> ,."):
            return False
    
    for i in range(len(password)-2):
        if password[i] == password[i+1] and password[i+1] == password[i+2]:
            return False
        
    if p_digit==p_lower==p_upper==True:
        return True    
    else:
        return False

print(solution("iLoveYou"))
```

```python
def solution(password):
	count1 = 0
	count2 = 0
	count3 = 0
	if len(password) < 6 or len(password) > 24:
		return False
	for ch in password:
		if ch.isupper():
			count1 += 1
		if ch.islower():
			count2 += 1
		if ch.isdigit():
			count3 += 1
	if count1 < 1 or count2 < 1 or count3 < 1:
		return False
	for i in range(len(password)-2):
		if password[i] == password[i+1] and password[i+1] == password[i+2]:
			return False
	return True

print(solution('iLoveYou'))
```

将一串数组以“Z 形”放入n个桶中

![1559109206865](http://cdn.zhaojingyi0126.com/IMG/1559109206865.png)

```python
def ListZ(data,step):
    #补充矩阵
    for i in range(step):
        if len(data) % step != 0:
            data.append(None)
            
    # 翻转偶数列
    for i in range(0,len(data),step):
        if (i/step) % 2 != 0:        
            data[i:i+step] = data[i+step-1:i-1:-1]   
            
    # 重新排列数组
    Zdata = []  
    for i in range(step):    
        data_ramp = [data[j] for j in range(i,len(data),step)]
        if None in data_ramp:
            data_ramp.remove(None)
        Zdata.append(data_ramp)
    return Zdata

data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14]
step = 4
Zdata = ListZ(data,step)
print(Zdata)
```

```python
def split_bucket(array, n):
    buckets = [[] for _ in range(n)]
    for i ,num in enumerate(array):
        if (i // n) % 2 == 0:
            bucket = buckets[i % n]
        else:
            bucket = buckets[-(i % n) - 1]
        bucket.append(num)
    return buckets
if __name__ == '__main__':
    data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14]
    step = 4
    Zdata = split_bucket(data,step)
    print(Zdata)
```

```python
def split_bucket(array, step):
    array_step = [array[i:i+2*step-2] for i in range(0,len(array),2*step-2)] 
    buckets = [[] for _ in range(step)]
    for i, num1 in enumerate(array_step):
        for j, num2 in enumerate(num1):    
            if (j // step)  == 0:
                bucket = buckets[j % step]
                bucket.append(num2)
            else:
                for k in range(step):
                    if k == (j%step+1):
                        bucket = buckets[-k-1]
                        bucket.append(str(num2))
                    else:
                        bucket = buckets[-k-1]
                        bucket.append(" ")
    return buckets
if __name__ == '__main__':
    array = "ABCDEFGHIJKLMNOPQRSTUVWXYZABCDEFGHIJKLMNOPQRSTUVWXYZ"
    array = list(array)
    step = 6    
    Zdata = split_bucket(array,step)
    for i in range(step):
        print("".join('%s' %id for id in Zdata[i]))
```