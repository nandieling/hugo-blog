# <center> Python 编程-入门到实践笔记
## <center> 第一章 基础知识
1. 终端运行python：
```
一. win: 
1. CD 文件夹
2. 显示文件夹下文件列表: dir
3. python hello_world.py

二. linux mac
1. 显示文件夹下文件列表: ls
```
## <center> 第二章 变量和简单数据类型
1. 字符串大小写处理：
``` 
title():字符串首字母大写。
upper():字符串全大写。
lower():字符串全小写。  
```
2. 字符串中使用变量：
```
f"{变量名}"
```
3. 制表符和换行符
```
\t:制表符
\n:换行符
```
4. 删除空格
```
rstrip():临时删除字符串右边空格。
lstrip():临时删除字符串左边空格。
strip():临时删除字符串两边空格。
```
5. 删除前缀
```
removeprefix(前缀)
```
6. 删除文件后缀: removesuffix(后缀)
```
练习题2.8：删除后缀
removesuffix.py

file = "word.txt"
file_1 = file.removesuffix(".txt")
print(file_1)
```
7. 浮点数：只有运算中有有浮点数，运算结果就为浮点数。
8. 可以用下划线来区分位数：1_0000_0000
9. Python之禅
```
优美优于丑陋，

明了优于隐晦；

简单优于复杂，

复杂优于繁杂，

扁平优于嵌套，

稀疏优于稠密，

可读性很重要！

特例亦不可违背原则，

即使实用比纯粹更优。

错误绝不能悄悄忽略，

除非它明确需要如此。

面对不确定性，

拒绝妄加猜测。

任何问题应有一种，

且最好只有一种，

显而易见的解决方法。

尽管这方法一开始并非如此直观，

除非你是荷兰人。

做优于不做，

然而不假思索还不如不做。

很难解释的，必然是坏方法。

很好解释的，可能是好方法。

命名空间是个绝妙的主意，

我们应好好利用它。
```
# <center> 第三章 列表简介
1. 访问列表最后一个元素：lists[-1]
2. 列表末尾添加元素：lists.append('元素')
3. 指定位置插入元素：lists.insert(0, '元素')
4. 删除指定位置元素：del lists[0]
5. 删除指定位置元素，默认末尾：lists.pop(0)
6. 删除指定值元素：remove('元素')
7. 列表按字母顺序排序：lists.sort()
8. 列表按字母反向排序：lists.sort(reverse=True)
9. 临时排序：lists.sorted()
10. 列表长度：len(lists)

# <center> 第四章 操作列表
1. range(1, 5):返回1、2、3、4 四个数。
2. range(1, 100, 2): range函数可设置步数。
3. 列表最小值:min(lists)
4. 列表最大值:max(lists)
5. 列表求和:sum(lists)
6. 列表推导式:
```
生成1到10的数，并将每个数平方，然后将平方数作为元素储存在列表中

lists = [value**2 for value in range(1, 11)]
```
7. 习题4.3：使用一个循环打印1-20（含）。
```
number_lists(1-20).py

number_lists = range(1, 21)
for number in number_lists:
    print(number)
```
8. 习题4.4：创建一个包含数 1～1000000 的列表，再使用一个 for 循环将这些数打印出来。
```commandline
number_lists(1-1000000).py

number_lists = range(1, 100_0001)
for number in number_lists:
    print(number)
```
9. 习题4.5：创建一个包含数1～1000000的列表，再使用 min() 和 max() 核实该列表确实是从
1 开始到1000000结束的。另外，对这个列表调用函数sum（）。
```commandline
number_lists_min_max_sum(1-1000000).py

number_lists = range(1, 100_0001)
number_lists_min = min(number_lists)
number_lists_max = max(number_lists)
number_lists_sum = sum(number_lists)

print(number_lists_min)
print(number_lists_max)
print(number_lists_sum)

```
10. 习题4.6：通过给range()函数指定第三个参数来创建一个列表，其中包含1～20的奇数；再使用一个
for循环将这些数打印
```commandline
number_lists_odd(1-20).py

odd_number_lists = range(1, 21, 2)
for odd_number in odd_number_lists:
    print(odd_number)
```
11. 习题4.7：创建一个列表，其中包含 3～30 内能被 3 整除的数，再使用一个 for 循环将这个列表
中的数打出来。
```commandline
multiple_3_lists.py

multiple_3_lists = range(3, 31, 3)
for multiple_3 in multiple_3_lists:
    print(multiple_3)
```
12. 习题4.8：将同一个数乘三次称为立方。例如，在 Python 中，2 的立方用 2**3 表示。创建
一个列表，其中包含前 10 个整数（1～10）的立方，再使用一个 for 循环将这些立方数打印出来。
```commandline
cube_lists(1-10).py

cube_lists = [ value**3 for value in range(1, 11)]
for cube_number in cube_lists:
    print(cube_number)
```
13. 列表切片：lists[0, 3]:返回列表0-2的元素。也可不指定开头或末尾。
14. 习题4.10：选择你在本章编写的一个程序，在末尾添加几行代码，以完成如下任务。
打印消息“The first three items in the list are:”，再使用切片来打印列表的前三个元素。
打印消息“Three items from the middle of the list are:”，再使用切片来打印列表中间的三个元素。
打印消息“The last three items in the list are:”，再使用切片来打印列表末尾的三个元素。
```commandline
slice_lists.py

lists = range(1, 11)

notice_first_three = "The first three items in the list are:"
print(notice_first_three)

for number_first_three in lists[:3]:  # 打印列表前三个元素
    print(number_first_three)

notice_middle_three = "Three items from the middle of the list are:"
print(notice_middle_three)

middle_number = int(10/2)
for number_middle_three in lists[middle_number-1:middle_number+2]: # 打印列表中间的三个元素
    print(number_middle_three)

notice_last_three = "The last three items in the list are:"
print(notice_last_three)

for number_last_three in lists[-3:]:    # 打印列表最后的三个元素
    print(number_last_three)
```
15. 元组(tuple)：不可修改元素，但可重新定义元组。tuple = (1, 2 , 3)
# <center>  第五章 if语句

