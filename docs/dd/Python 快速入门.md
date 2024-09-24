# 1.数据类型

在 Python 中，数值类型、字符串、列表、元组、字典和集合是基本的数据类型。下面是针对每个类型的示例和操作。

## 1. 数值类型操作

 整数 `int`、浮点数 `float`、复数 `complex`

```python
# 整数操作
a = 10
b = 3
print("整数加法:", a + b)  # 13
print("整数减法:", a - b)  # 7
print("整数乘法:", a * b)  # 30
print("整数除法:", a / b)  # 3.3333...

# 浮点数操作
x = 10.5
y = 2.3
print("浮点数加法:", x + y)  # 12.8
print("浮点数除法:", x / y)  # 4.565217391304348

# 复数操作
z1 = 2 + 3j
z2 = 1 + 2j
print("复数加法:", z1 + z2)  # (3+5j)
print("复数乘法:", z1 * z2)  # (-4+7j)

# 类型转换
print("整数转浮点数:", float(a))  # 10.0
print("浮点数转整数:", int(x))  # 10
```

## 2. 字符串操作

```python
# 字符串拼接
str1 = "Hello"
str2 = "World"
result = str1 + " " + str2
print("拼接字符串:", result)  # Hello World

# 字符串分割
sentence = "I am learning Python"
words = sentence.split()  # 默认按空格分割
print("分割后的列表:", words)  # ['I', 'am', 'learning', 'Python']

name = "Alice"
age = 25
height = 5.4
formatted_str = "My name is %s and I am %d years old. My height is %.1f feet." % (name, age, height)
print(formatted_str)
# 输出: My name is Alice and I am 25 years old. My height is 5.4 feet.
# %s：表示字符串
# %d：表示整数
# %f：表示浮点数（可指定小数位，如 %.1f）

name = "Alice"
age = 25
height = 5.4
formatted_str = "My name is {} and I am {} years old. My height is {:.1f} feet.".format(name, age, height)
print(formatted_str)
# 输出: My name is Alice and I am 25 years old. My height is 5.4 feet.

# 常用方法
print("字符串长度:", len(sentence))  # 19
print("连接列表为字符串:", " ".join(words))  # I am learning Python
```

## 3. 列表操作

```## python
# 列表创建-空列表
fruits = []
print("列表元素:", fruits)  # []

# 列表创建
fruits = ["apple", "banana", "cherry"]
print("列表元素:", fruits)  # ["apple", "banana", "cherry"]

# 列表索引与切片
print("第一个元素:", fruits[0])  # apple
print("切片:", fruits[1:3])  # ['banana', 'cherry']

# 添加元素
fruits.append("orange")
print("添加后列表:", fruits)  # ['apple', 'banana', 'cherry', 'orange']

# 删除元素
fruits.remove("banana")
print("删除元素后列表:", fruits)  # ['apple', 'cherry', 'orange']

# 列表排序
fruits.sort()
print("排序后列表:", fruits)  # ['apple', 'cherry', 'orange']
```

## 4. 元组操作

```python
# 元组创建-空元组
my_tuple = ()
print("元组元素:", my_tuple) # ()

# 元组创建
my_tuple = (1, 2, 3, "hello")
print("元组元素:", my_tuple) #(1, 2, 3, "hello")

# 元组索引
print("第一个元素:", my_tuple[0])  # 1

# 元组不可变性
# my_tuple[0] = 10  # 这行代码会导致错误，元组不能修改

# 元组支持切片
print("切片:", my_tuple[1:3])  # (2, 3)
```

##  5. 字典操作

```python
# 字典创建-空字典
person = {}
print("字典元素:", person)  # {}

# 字典创建
person = {"name": "John", "age": 30, "city": "New York"}
print("字典元素:", person)  # {"name": "John", "age": 30, "city": "New York"}

# 访问字典
print("姓名:", person["name"])  # John

# 修改字典
person["age"] = 31
print("修改后的年龄:", person["age"])  # 31

# 添加键值对
person["job"] = "Engineer"
print("添加工作信息后:", person)

# 删除键值对
del person["city"]
print("删除城市信息后:", person)

# 使用字典方法
print("所有键:", person.keys())  # dict_keys(['name', 'age', 'job'])
print("所有值:", person.values())  # dict_values(['John', 31, 'Engineer'])
```

## 6. 集合操作

```python
# 集合创建
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# 添加元素
set1.add(5)
print("添加元素后的集合:", set1)  # {1, 2, 3, 4, 5}

# 删除元素
set1.remove(2)
print("删除元素后的集合:", set1)  # {1, 3, 4, 5}

# 集合运算
print("交集:", set1 & set2)  # {3, 4, 5}
print("并集:", set1 | set2)  # {1, 3, 4, 5, 6}
print("差集:", set1 - set2)  # {1}
```

---

# 2.变量与赋值

在 Python 中，变量是用来存储数据的容器。在你定义一个变量时，你可以为它赋值，而 Python 会根据你赋的值动态地确定该变量的类型。让我们通过以下几个例子来解释这些概念：

## 1. **定义变量和赋值**

在 Python 中，定义变量的过程其实就是给一个名称赋值。你不需要指定变量的类型，Python 会根据你赋的值来自动决定类型。

```python
# 定义一个整数类型的变量
number = 10

# 定义一个浮点数类型的变量
pi = 3.14

# 定义一个字符串类型的变量
name = "Alice"

# 定义一个布尔类型的变量
is_student = True
```

在上面的例子中：

- `number` 被赋值为整数 `10`
- `pi` 被赋值为浮点数 `3.14`
- `name` 被赋值为字符串 `"Alice"`
- `is_student` 被赋值为布尔值 `True`

## 2. **变量命名规则**

在 Python 中，变量命名有一些规则和最佳实践：

- 变量名必须以字母或下划线 `_` 开头，后面可以跟字母、数字或下划线。
- 变量名区分大小写，因此 `Name` 和 `name` 是两个不同的变量。
- 避免使用 Python 的保留字作为变量名，例如 `if`、`while`、`class` 等。

```python
# 正确的命名
user_name = "Bob"
userAge = 25
_userId = "abc123"

# 错误的命名
# 1user = "error"    # 变量名不能以数字开头
# def = "error"      # 变量名不能是保留字
```

## 3. **变量类型的动态分配**

Python 是一种动态类型的语言，这意味着你不需要显式地声明变量的类型，Python 会根据赋值的内容自动推断类型。

```python
# Python 会自动判断类型
x = 5          # 整数类型
x = "Hello"    # 现在 x 是字符串类型
x = 3.14       # 现在 x 是浮点数类型
```

在这个例子中，`x` 最初是一个整数，后来被重新赋值为字符串，最后被赋值为浮点数。这就是动态类型的含义。

## 4. **避免使用保留字**

Python 有一些保留字，它们有特定的用途，不能作为变量名使用。你可以使用以下代码来查看所有保留字：

```python
import keyword
print(keyword.kwlist)
```

这些保留字包括 `if`、`else`、`for`、`while`、`class` 等。使用保留字作为变量名会导致语法错误。

---

# 3.控制结构

在 Python 中，条件语句和循环语句是编程的核心概念，它们帮助我们控制程序的流向。下面是 `if`、`elif`、`else` 条件语句以及 `for` 和 `while` 循环的用法示例。

## 1. **条件语句：`if`、`elif` 和 `else`**

条件语句用于根据某些条件执行不同的代码块。

```python
age = 20

# if 条件
if age < 18:
    print("You are a minor.")

# if else 条件 
if age < 18:
    print("You are a minor.")
else:
    print("You are a senior citizen.")

# if elif else 条件 
if age < 18:
    print("You are a minor.")
elif age >= 18 and age < 65:
    print("You are an adult.")
else:
    print("You are a senior citizen.")
```

在这个示例中：

- 如果 `age` 小于 18，程序输出 "You are a minor."
- 如果 `age` 在 18 和 65 之间，程序输出 "You are an adult."
- 否则，程序输出 "You are a senior citizen."

## 2. **`for` 循环**

`for` 循环用于遍历一个序列（例如列表、字符串、元组等）。

```python
# 遍历一个列表
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# 使用 range() 生成一个数字序列
for i in range(5):
    print(i)  # 输出 0 到 4
```

- 在第一个例子中，`for` 循环遍历 `fruits` 列表并逐一输出列表中的每个元素。
- 在第二个例子中，`range(5)` 生成从 0 到 4 的数字序列，`for` 循环遍历并输出这些数字。

## 3. **`while` 循环**

`while` 循环会一直执行某个代码块，直到给定的条件为 `False` 为止。

```python
count = 0
while count < 5:
    print(count)
    count += 1  # 递增 count 的值
```

在这个例子中，`while` 循环每次检查 `count` 是否小于 5。如果是，它就打印 `count`，并增加它的值。循环在 `count` 等于 5 时结束。

## 4. **`break` 和 `continue`**

- `break` 用于终止循环。
- `continue` 用于跳过当前循环的剩余部分，并开始下一次迭代。

```python
# 使用 break
for i in range(10):
    if i == 5:
        break  # 当 i 等于 5 时终止循环
    print(i)

# 使用 continue
for i in range(10):
    if i % 2 == 0:
        continue  # 如果 i 是偶数，则跳过此迭代
    print(i)  # 只打印奇数
```

- 在第一个例子中，当 `i` 等于 5 时，`break` 语句将终止循环。
- 在第二个例子中，`continue` 语句跳过偶数的迭代，因此只输出奇数。

通过这些例子，你可以学习如何使用 `if`、`elif`、`else` 进行条件判断，以及如何使用 `for` 和 `while` 循环遍历序列和控制循环流。 `break` 和 `continue` 语句可以帮助你更精细地控制循环执行的方式。

---

# 4.函数

## 1. **使用 `def` 定义函数，传递参数，返回值**

```python
# 定义一个简单的加法函数，传递两个参数并返回结果
def add_numbers(a, b):
    return a + b

# 调用函数并打印返回值
result = add_numbers(3, 5)
print(f"The result is: {result}")
```

在这个例子中，定义了一个函数 `add_numbers`，它接受两个参数 `a` 和 `b`，返回它们的和。

## 2. **默认参数**

```python
# 定义一个函数，带有一个默认参数
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

# 调用时提供两个参数
print(greet("Alice", "Hi"))

# 调用时只提供一个参数，使用默认的 greeting 值
print(greet("Bob"))
```

在这个例子中，`greeting` 是一个带有默认值 `"Hello"` 的参数。如果没有传递 `greeting`，函数会使用默认值。

## 3. **可变参数 `*args`**

```python
# 使用 *args 定义一个可以接受多个参数的函数
def sum_numbers(*args):
    total = 0
    for num in args:
        total += num
    return total

# 调用函数时可以传递任意数量的参数
print(sum_numbers(1, 2, 3))  # 输出 6
print(sum_numbers(4, 5, 6, 7, 8))  # 输出 30
```

`*args` 允许你传递任意数量的位置参数。它在函数内部作为一个元组使用。

## 4. **可变参数 `**kwargs`**

```python
# 使用 **kwargs 定义一个接受任意数量关键字参数的函数
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

# 调用函数时传递多个关键字参数
print_info(name="Alice", age=30, city="New York")
```

`**kwargs` 允许你传递任意数量的关键字参数，它们在函数内部被作为字典处理。

## 5. **综合示例：使用默认参数、`*args` 和 `**kwargs`**

```python
# 定义一个包含默认参数、*args 和 **kwargs 的函数
def describe_person(name, age=30, *hobbies, **details):
    print(f"Name: {name}")
    print(f"Age: {age}")
    print("Hobbies:", ', '.join(hobbies))
    for key, value in details.items():
        print(f"{key}: {value}")

# 调用函数并传递不同类型的参数
describe_person("John", 25, "reading", "swimming", city="New York", job="Engineer")
```

在这个例子中：

- `name` 是必需参数；
- `age` 是默认参数，默认为 30；
- `*hobbies` 接受可变数量的位置参数；
- `**details` 接受可变数量的关键字参数。

---

# 5.模块与包

## 1. **创建和导入模块**

在 Python 中，模块是一个包含 Python 代码的文件，可以包含函数、类、变量等。模块有助于组织代码，使代码更易于维护和复用。

首先，创建一个 Python 文件（比如 `my_module.py`），并定义一些函数和变量。

```python
# my_module.py

# 定义一个简单的函数
def greet(name):
    return f"Hello, {name}!"

# 定义一个变量
version = "1.0"
```

导入并使用自定义模块，在另一个文件中（比如 `main.py`）导入并使用 `my_module`。

```python
# main.py

# 导入自定义模块
import my_module

# 调用模块中的函数
greeting = my_module.greet("Alice")
print(greeting)

# 访问模块中的变量
print(f"Module version: {my_module.version}")
```

这样，你就创建了一个模块 `my_module.py`，并在 `main.py` 中导入和使用它。

## 2. **使用 `import` 导入内置模块**

Python 提供了许多内置模块，这些模块包含了标准库中常用的功能，可以直接导入使用。

```python
# 导入内置的 math 模块
import math

# 使用 math 模块中的函数
result = math.sqrt(16)
print(f"The square root of 16 is: {result}")

# 使用 math 模块中的常量
pi_value = math.pi
print(f"Value of pi: {pi_value}")
```

在这个例子中，`math` 是 Python 的内置模块，它提供了常见的数学函数和常量。

## 3. **安装和使用第三方包**

安装第三方包，你可以使用 `pip` 安装第三方包，例如安装 `requests` 库：

```bash
pip install requests
```

安装好之后，可以在 Python 代码中导入并使用该包。例如，使用 `requests` 库发起 HTTP 请求：

```python
# 导入 requests 库
import requests

# 使用 requests 发起一个 GET 请求
response = requests.get('https://api.github.com')

# 打印响应的状态码
print(f"Status code: {response.status_code}")

# 打印响应的 JSON 数据
print("Response JSON:", response.json())
```

## 4. **导入模块的不同方式**

除了常规的 `import` 语法外，还有几种导入模块的方式：

使用 `from` 导入特定函数或变量

```python
# 从 math 模块中只导入 sqrt 函数
from math import sqrt

# 直接使用导入的函数
result = sqrt(25)
print(f"The square root of 25 is: {result}")
```

为模块起别名

```python
# 为 requests 模块起一个简短的别名
import requests as req

# 使用别名调用模块函数
response = req.get('https://api.github.com')
print(f"Status code: {response.status_code}")
```

## 5. **综合示例：导入自定义模块、内置模块和第三方库**

```python
# my_math.py (自定义模块)
def add(a, b):
    return a + b
```

```python
# main.py
import my_math  # 导入自定义模块
import math  # 导入内置模块
import requests  # 导入第三方库

# 使用自定义模块
print(f"Add 2 and 3: {my_math.add(2, 3)}")

# 使用内置模块
print(f"Pi value: {math.pi}")

# 使用第三方库
response = requests.get('https://httpbin.org/get')
print(f"Response status: {response.status_code}")
```

这些例子展示了如何创建和导入模块、导入内置模块、使用 `pip` 安装并导入第三方包。

---

