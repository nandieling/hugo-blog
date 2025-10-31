# Python 编程-入门到实践笔记
## 第二章：
title():字符串首字母大写。
upper():字符串全大写。
lower():字符串全小写。  
```
name = input("What's your name?")
name = name.title()
message = f"Hello {name} ,would you like to learn some Python today?"
print(message)
name = name.upper()
message = f"Hello {name} ,would you like to learn some Python today?"
print(message)
name = name.lower()
message = f"Hello {name} ,would you like to learn some Python today?"
print(message)  
```
f"{变量名}":格式化字符串，简化操作。
rstrip():临时删除字符串左边空格。
lstrip():临时删除字符串右边空格。
strip():临时删除字符串两边空格。
