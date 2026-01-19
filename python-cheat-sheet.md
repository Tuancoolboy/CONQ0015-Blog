# Python Cheat Sheet Toàn Diện - Hướng Dẫn Tham Khảo Nhanh

## Giới thiệu

Python là một ngôn ngữ lập trình mạnh mẽ và dễ học, được sử dụng rộng rãi trong nhiều lĩnh vực từ phát triển web đến khoa học dữ liệu và trí tuệ nhân tạo. Tài liệu này cung cấp một bản cheat sheet toàn diện giúp bạn nắm vững các khái niệm cơ bản đến nâng cao của Python một cách nhanh chóng và hiệu quả.

---

## Mục Lục

1. [Toán tử trong Python](#1-toán-tử-trong-python)
2. [Kiểu dữ liệu](#2-kiểu-dữ-liệu)
3. [Biến và Quy tắc đặt tên](#3-biến-và-quy-tắc-đặt-tên)
4. [Comments trong Python](#4-comments-trong-python)
5. [Các hàm cơ bản](#5-các-hàm-cơ-bản)
6. [Chuyển đổi kiểu dữ liệu](#6-chuyển-đổi-kiểu-dữ-liệu)
7. [Điều khiển luồng](#7-điều-khiển-luồng)
8. [Câu lệnh điều kiện](#8-câu-lệnh-điều-kiện)
9. [Vòng lặp](#9-vòng-lặp)
10. [Hàm (Functions)](#10-hàm-functions)
11. [Xử lý ngoại lệ](#11-xử-lý-ngoại-lệ)
12. [List](#12-list)
13. [Tuple](#13-tuple)
14. [Dictionary](#14-dictionary)
15. [Set](#15-set)
16. [Comprehensions](#16-comprehensions)
17. [Thao tác với String](#17-thao-tác-với-string)
18. [Lambda Functions](#18-lambda-functions)
19. [*args và **kwargs](#19-args-và-kwargs)
20. [Modules và Import](#20-modules-và-import)
21. [Lập trình hướng đối tượng (OOP)](#21-lập-trình-hướng-đối-tượng-oop)

---

## 1. Toán tử trong Python

Python cung cấp ba nhóm toán tử chính để thực hiện các phép toán và so sánh trong chương trình.

### 1.1. Toán tử số học

Các toán tử số học được sử dụng để thực hiện các phép tính toán học cơ bản:

| Toán tử | Mô tả | Ví dụ |
|---------|-------|-------|
| `+` | Phép cộng | `5 + 3 = 8` |
| `-` | Phép trừ | `10 - 4 = 6` |
| `*` | Phép nhân | `3 * 4 = 12` |
| `/` | Phép chia | `15 / 3 = 5.0` |
| `//` | Chia lấy phần nguyên | `17 // 5 = 3` |
| `%` | Chia lấy phần dư | `17 % 5 = 2` |
| `**` | Lũy thừa | `2 ** 3 = 8` |

**Ví dụ minh họa:**

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3
print(a % b)   # 1
print(a ** b)  # 1000
```

### 1.2. Toán tử so sánh

Toán tử so sánh giúp kiểm tra mối quan hệ giữa hai giá trị và trả về kết quả `True` hoặc `False`:

| Toán tử | Mô tả | Ví dụ |
|---------|-------|-------|
| `==` | Bằng nhau | `5 == 5` → `True` |
| `!=` | Khác nhau | `5 != 3` → `True` |
| `>` | Lớn hơn | `10 > 5` → `True` |
| `<` | Nhỏ hơn | `3 < 7` → `True` |
| `>=` | Lớn hơn hoặc bằng | `5 >= 5` → `True` |
| `<=` | Nhỏ hơn hoặc bằng | `4 <= 6` → `True` |

**Ví dụ:**

```python
x = 10
y = 20

print(x == y)  # False
print(x != y)  # True
print(x < y)   # True
print(x > y)   # False
print(x <= 10) # True
print(y >= 20) # True
```

### 1.3. Toán tử logic

Toán tử logic được sử dụng để kết hợp các điều kiện:

| Toán tử | Mô tả | Ví dụ |
|---------|-------|-------|
| `and` | Cả hai điều kiện đều đúng | `True and False` → `False` |
| `or` | Ít nhất một điều kiện đúng | `True or False` → `True` |
| `not` | Đảo ngược kết quả | `not True` → `False` |

**Ví dụ:**

```python
a = True
b = False

print(a and b)  # False
print(a or b)   # True
print(not a)    # False
print(not b)    # True

# Kết hợp với so sánh
age = 25
print(age >= 18 and age <= 65)  # True
```

---

## 2. Kiểu dữ liệu

Python hỗ trợ nhiều kiểu dữ liệu khác nhau, mỗi kiểu phục vụ cho các mục đích cụ thể:

| Kiểu dữ liệu | Mô tả | Ví dụ |
|--------------|-------|-------|
| `int` | Số nguyên | `42`, `-10`, `0` |
| `float` | Số thực | `3.14`, `-0.5`, `2.0` |
| `str` | Chuỗi ký tự | `"Hello"`, `'Python'` |
| `bool` | Giá trị logic | `True`, `False` |
| `list` | Danh sách có thứ tự | `[1, 2, 3]` |
| `tuple` | Bộ giá trị không đổi | `(1, 2, 3)` |
| `dict` | Từ điển (key-value) | `{'name': 'John'}` |
| `set` | Tập hợp không trùng lặp | `{1, 2, 3}` |

**Ví dụ kiểm tra kiểu dữ liệu:**

```python
# Sử dụng hàm type() để kiểm tra kiểu
print(type(42))           # <class 'int'>
print(type(3.14))         # <class 'float'>
print(type("Hello"))      # <class 'str'>
print(type(True))         # <class 'bool'>
print(type([1, 2, 3]))    # <class 'list'>
print(type((1, 2, 3)))    # <class 'tuple'>
print(type({'a': 1}))     # <class 'dict'>
print(type({1, 2, 3}))    # <class 'set'>
```

---

## 3. Biến và Quy tắc đặt tên

Biến là tên được gán cho các giá trị dữ liệu trong chương trình. Python cho phép bạn lưu trữ và thao tác với dữ liệu thông qua biến.

### Quy tắc đặt tên biến:

- Tên biến chỉ chứa chữ cái, số và dấu gạch dưới (`_`)
- Tên biến không được bắt đầu bằng số
- Tên biến phân biệt chữ hoa và chữ thường (`name` khác `Name`)
- Không sử dụng từ khóa của Python làm tên biến
- Nên sử dụng tên có ý nghĩa, dễ hiểu

**Ví dụ:**

```python
# Đúng
user_name = "John"
age = 25
total_score = 100
is_active = True

# Sai
# 2name = "John"  # Không thể bắt đầu bằng số
# user-name = "John"  # Không thể dùng dấu gạch ngang
# class = "Python"  # Không thể dùng từ khóa
```

---

## 4. Comments trong Python

Comments là những dòng mã không được thực thi, giúp giải thích logic và làm rõ ý nghĩa của code.

### 4.1. Inline Comment

Comment trên cùng một dòng với code:

```python
x = 10  # Khởi tạo biến x với giá trị 10
result = x * 2  # Nhân đôi giá trị của x
```

### 4.2. Multiline Comment

Comment nhiều dòng bằng cách sử dụng `#` ở đầu mỗi dòng:

```python
# Đây là một comment nhiều dòng
# Giúp giải thích logic phức tạp
# Có thể viết nhiều dòng như thế này
def calculate_sum(a, b):
    return a + b
```

### 4.3. Docstring

Docstring sử dụng ba dấu nháy kép để tạo documentation cho hàm hoặc class:

```python
def calculate_area(radius):
    """
    Tính diện tích hình tròn
    
    Tham số:
        radius (float): Bán kính của hình tròn
    
    Trả về:
        float: Diện tích hình tròn
    """
    return 3.14159 * radius ** 2
```

---

## 5. Các hàm cơ bản

### 5.1. Hàm print()

In dữ liệu ra màn hình console:

```python
print("Hello, World!")
print(42)
print("Giá trị là:", 100)

# In nhiều giá trị
name = "Python"
version = 3.9
print("Ngôn ngữ:", name, "Phiên bản:", version)

# Sử dụng f-string (Python 3.6+)
print(f"Chào mừng đến với {name} {version}")
```

### 5.2. Hàm input()

Nhận dữ liệu từ người dùng:

```python
# Nhận chuỗi
name = input("Nhập tên của bạn: ")
print(f"Xin chào, {name}!")

# Nhận số (cần chuyển đổi kiểu)
age = int(input("Nhập tuổi của bạn: "))
print(f"Bạn {age} tuổi")
```

### 5.3. Hàm len()

Tính độ dài của chuỗi, list, tuple, dict:

```python
text = "Python"
print(len(text))  # 6

numbers = [1, 2, 3, 4, 5]
print(len(numbers))  # 5

data = {'a': 1, 'b': 2, 'c': 3}
print(len(data))  # 3
```

### 5.4. Hàm ord() và chr()

Chuyển đổi giữa ký tự và mã Unicode:

```python
# ord() - chuyển ký tự sang mã Unicode
print(ord('A'))   # 65
print(ord('a'))   # 97
print(ord('0'))   # 48

# chr() - chuyển mã Unicode sang ký tự
print(chr(65))    # 'A'
print(chr(97))    # 'a'
```

---

## 6. Chuyển đổi kiểu dữ liệu

### 6.1. Chuyển đổi ngầm định (Implicit)

Python tự động chuyển đổi kiểu khi cần thiết:

```python
# int + float → float
result = 10 + 3.5
print(result)        # 13.5
print(type(result))  # <class 'float'>

# int + bool → int (True = 1, False = 0)
value = 5 + True
print(value)  # 6
```

### 6.2. Chuyển đổi tường minh (Explicit)

Lập trình viên tự chuyển đổi kiểu:

```python
# Chuyển sang chuỗi
number = 123
text = str(number)
print(text, type(text))  # '123' <class 'str'>

# Chuyển sang số nguyên
float_num = 7.8
int_num = int(float_num)
print(int_num)  # 7 (làm tròn xuống)

# Chuyển sang số thực
int_value = 42
float_value = float(int_value)
print(float_value)  # 42.0

# Chuyển chuỗi số sang số
num_str = "123"
num_int = int(num_str)
print(num_int)  # 123
```

---

## 7. Điều khiển luồng

### 7.1. Toán tử quan hệ

So sánh các giá trị và trả về `True` hoặc `False`:

```python
a = 10
b = 20

print(a == b)  # False
print(a != b)  # True
print(a < b)   # True
print(a > b)   # False
print(a <= 10) # True
print(b >= 20) # True
```

### 7.2. Toán tử Boolean

Kết hợp các điều kiện:

```python
x = 5
y = 10

# and - cả hai đều đúng
print(x > 0 and y > 0)  # True

# or - ít nhất một đúng
print(x > 10 or y > 5)  # True

# not - đảo ngược
print(not (x > 10))     # True
```

---

## 8. Câu lệnh điều kiện

### 8.1. Câu lệnh if

Thực thi code khi điều kiện đúng:

```python
age = 18

if age >= 18:
    print("Bạn đã trưởng thành")
```

### 8.2. Câu lệnh if-else

Thực thi một trong hai khối code:

```python
score = 85

if score >= 50:
    print("Đậu")
else:
    print("Rớt")
```

### 8.3. Câu lệnh if-elif-else

Kiểm tra nhiều điều kiện:

```python
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print(f"Điểm của bạn: {grade}")
```

### 8.4. Câu lệnh lồng nhau

```python
age = 25
has_license = True

if age >= 18:
    if has_license:
        print("Bạn có thể lái xe")
    else:
        print("Bạn cần bằng lái")
else:
    print("Bạn chưa đủ tuổi")
```

---

## 9. Vòng lặp

### 9.1. Vòng lặp for

Lặp qua một chuỗi các phần tử:

```python
# Lặp qua range
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4

# Range với điểm bắt đầu và kết thúc
for i in range(2, 10, 2):
    print(i)  # 2, 4, 6, 8

# Lặp qua list
fruits = ["apple", "banana", "orange"]
for fruit in fruits:
    print(fruit)

# Lặp qua string
for char in "Python":
    print(char)
```

### 9.2. Vòng lặp while

Lặp khi điều kiện còn đúng:

```python
count = 5
while count > 0:
    print(count)
    count -= 1
# Output: 5, 4, 3, 2, 1

# Vòng lặp vô hạn với break
while True:
    user_input = input("Nhập 'quit' để thoát: ")
    if user_input == 'quit':
        break
```

### 9.3. Lệnh điều khiển vòng lặp

**break** - Thoát khỏi vòng lặp:

```python
for i in range(10):
    if i == 5:
        break
    print(i)  # 0, 1, 2, 3, 4
```

**continue** - Bỏ qua lần lặp hiện tại:

```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)  # 1, 3, 5, 7, 9
```

**pass** - Giữ chỗ, không làm gì:

```python
for i in range(5):
    if i == 3:
        pass  # Sẽ làm gì đó sau
    else:
        print(i)
```

---

## 10. Hàm (Functions)

Hàm là khối code có thể tái sử dụng, giúp tổ chức code tốt hơn.

### 10.1. Định nghĩa hàm cơ bản

```python
def greet(name):
    """Hàm chào hỏi"""
    return f"Xin chào, {name}!"

message = greet("Python")
print(message)  # Xin chào, Python!
```

### 10.2. Hàm với nhiều tham số

```python
def add_numbers(a, b, c=0):
    """Cộng các số"""
    return a + b + c

print(add_numbers(1, 2))      # 3
print(add_numbers(1, 2, 3))   # 6
```

### 10.3. Hàm với giá trị mặc định

```python
def introduce(name, age=18, city="Hà Nội"):
    return f"{name}, {age} tuổi, sống ở {city}"

print(introduce("An"))                           # An, 18 tuổi, sống ở Hà Nội
print(introduce("Bình", 25))                     # Bình, 25 tuổi, sống ở Hà Nội
print(introduce("Cường", 30, "TP.HCM"))          # Cường, 30 tuổi, sống ở TP.HCM
```

### 10.4. Phạm vi biến (Scope)

```python
# Biến global
x = 10

def my_function():
    # Biến local
    y = 20
    print(x)  # Có thể truy cập biến global
    print(y)

my_function()
# print(y)  # Lỗi: y không tồn tại ở ngoài hàm

# Sử dụng global để thay đổi biến global
def change_global():
    global x
    x = 30

change_global()
print(x)  # 30
```

---

## 11. Xử lý ngoại lệ

Xử lý lỗi giúp chương trình không bị crash khi gặp lỗi.

### 11.1. try-except

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Không thể chia cho 0!")
```

### 11.2. try-except-else

```python
try:
    number = int(input("Nhập một số: "))
except ValueError:
    print("Vui lòng nhập số hợp lệ!")
else:
    print(f"Số bạn nhập: {number}")
```

### 11.3. try-except-finally

```python
try:
    file = open("data.txt", "r")
    content = file.read()
except FileNotFoundError:
    print("File không tồn tại!")
finally:
    print("Luôn thực thi phần này")
    # Đóng file hoặc dọn dẹp tài nguyên
```

### 11.4. Nhiều loại exception

```python
try:
    value = int(input("Nhập số: "))
    result = 10 / value
except ValueError:
    print("Lỗi: Không phải số!")
except ZeroDivisionError:
    print("Lỗi: Chia cho 0!")
except Exception as e:
    print(f"Lỗi khác: {e}")
```

---

## 12. List

List là cấu trúc dữ liệu lưu trữ nhiều phần tử có thứ tự.

### 12.1. Tạo và truy cập List

```python
# Tạo list
fruits = ["apple", "banana", "orange"]
numbers = [1, 2, 3, 4, 5]

# Truy cập phần tử
print(fruits[0])    # "apple"
print(fruits[-1])   # "orange" (phần tử cuối)

# Slicing
print(fruits[0:2])      # ["apple", "banana"]
print(fruits[:2])       # ["apple", "banana"]
print(fruits[1:])       # ["banana", "orange"]
```

### 12.2. Thay đổi List

```python
fruits = ["apple", "banana"]

# Thay đổi phần tử
fruits[0] = "grape"
print(fruits)  # ["grape", "banana"]

# Thêm phần tử
fruits.append("orange")        # Thêm vào cuối
fruits.insert(1, "mango")      # Chèn vào vị trí 1
print(fruits)  # ["grape", "mango", "banana", "orange"]

# Xóa phần tử
fruits.remove("banana")        # Xóa phần tử cụ thể
del fruits[0]                  # Xóa theo index
popped = fruits.pop()           # Xóa và trả về phần tử cuối
```

### 12.3. Các phương thức hữu ích

```python
numbers = [3, 1, 4, 1, 5, 9, 2, 6]

# Sắp xếp
numbers.sort()                  # Sắp xếp tại chỗ
sorted_nums = sorted(numbers)   # Trả về list mới đã sắp xếp

# Đảo ngược
numbers.reverse()

# Đếm
count = numbers.count(1)        # Số lần xuất hiện của 1

# Tìm index
index = numbers.index(4)        # Vị trí của 4

# Nối list
list1 = [1, 2, 3]
list2 = [4, 5, 6]
combined = list1 + list2        # [1, 2, 3, 4, 5, 6]

# Lặp qua list
for item in numbers:
    print(item)
```

---

## 13. Tuple

Tuple giống list nhưng không thể thay đổi sau khi tạo (immutable).

```python
# Tạo tuple
coordinates = (10, 20)
colors = ("red", "green", "blue")

# Truy cập phần tử
print(coordinates[0])  # 10
print(colors[-1])      # "blue"

# Slicing
print(colors[0:2])     # ("red", "green")

# Tuple không thể thay đổi
# coordinates[0] = 5  # Lỗi!

# Chuyển đổi
list_from_tuple = list(colors)
tuple_from_list = tuple([1, 2, 3])

# Unpacking
x, y = coordinates
print(x, y)  # 10 20
```

---

## 14. Dictionary

Dictionary lưu trữ dữ liệu dưới dạng cặp key-value.

### 14.1. Tạo và truy cập Dictionary

```python
# Tạo dictionary
student = {
    "name": "Nguyễn Văn A",
    "age": 20,
    "grade": "A"
}

# Truy cập giá trị
print(student["name"])         # "Nguyễn Văn A"
print(student.get("age"))      # 20
print(student.get("city", "N/A"))  # "N/A" (giá trị mặc định)

# Thay đổi giá trị
student["age"] = 21

# Thêm key-value mới
student["city"] = "Hà Nội"
```

### 14.2. Các phương thức hữu ích

```python
# Lấy tất cả keys
keys = student.keys()

# Lấy tất cả values
values = student.values()

# Lấy tất cả items (key-value pairs)
items = student.items()

# Lặp qua dictionary
for key, value in student.items():
    print(f"{key}: {value}")

# Xóa phần tử
del student["grade"]
removed = student.pop("age")    # Xóa và trả về giá trị

# Kiểm tra key có tồn tại
if "name" in student:
    print("Key 'name' tồn tại")

# Hợp nhất dictionaries
dict1 = {"a": 1, "b": 2}
dict2 = {"c": 3, "d": 4}
dict1.update(dict2)
```

---

## 15. Set

Set là tập hợp các phần tử duy nhất, không có thứ tự.

```python
# Tạo set
numbers = {1, 2, 3, 4, 5}
colors = set(["red", "green", "blue"])

# Set tự động loại bỏ phần tử trùng
duplicates = {1, 2, 2, 3, 3, 3}
print(duplicates)  # {1, 2, 3}

# Thêm phần tử
numbers.add(6)
numbers.update([7, 8, 9])

# Xóa phần tử
numbers.remove(1)   # Lỗi nếu không tồn tại
numbers.discard(10) # Không lỗi nếu không tồn tại

# Các phép toán tập hợp
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

print(set1 | set2)  # Hợp: {1, 2, 3, 4, 5, 6}
print(set1 & set2)  # Giao: {3, 4}
print(set1 - set2)  # Hiệu: {1, 2}
print(set1 ^ set2)  # Đối xứng: {1, 2, 5, 6}
```

---

## 16. Comprehensions

Comprehensions giúp tạo list, dict, set một cách ngắn gọn.

### 16.1. List Comprehension

```python
# Tạo list các số chẵn
evens = [x for x in range(10) if x % 2 == 0]
# [0, 2, 4, 6, 8]

# Tạo list bình phương
squares = [x**2 for x in range(5)]
# [0, 1, 4, 9, 16]

# Với điều kiện phức tạp
result = [x*2 if x > 5 else x for x in range(10)]
```

### 16.2. Dictionary Comprehension

```python
# Tạo dict từ list
numbers = [1, 2, 3, 4, 5]
squared_dict = {x: x**2 for x in numbers}
# {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

# Với điều kiện
even_squares = {x: x**2 for x in range(10) if x % 2 == 0}
```

### 16.3. Set Comprehension

```python
# Tạo set các số chẵn
evens_set = {x for x in range(10) if x % 2 == 0}
# {0, 2, 4, 6, 8}
```

---

## 17. Thao tác với String

### 17.1. Escape Sequences

```python
text = "Dòng 1\nDòng 2"      # Xuống dòng
tab_text = "Cột1\tCột2"       # Tab
quote = "Anh ấy nói \"Xin chào\""  # Dấu ngoặc kép
path = "C:\\Users\\Name"      # Dấu gạch chéo ngược
```

### 17.2. Multiline Strings

```python
multiline = """Đây là
một chuỗi
nhiều dòng"""

# Hoặc
multiline2 = "Dòng 1\n" \
             "Dòng 2\n" \
             "Dòng 3"
```

### 17.3. String Methods

```python
text = "  Hello Python  "

# Loại bỏ khoảng trắng
print(text.strip())        # "Hello Python"

# Chuyển đổi chữ hoa/thường
print(text.upper())       # "  HELLO PYTHON  "
print(text.lower())       # "  hello python  "
print(text.title())       # "  Hello Python  "

# Kiểm tra
print(text.isdigit())     # False
print(text.isalpha())     # False
print(text.isspace())     # False

# Tìm và thay thế
new_text = text.replace("Python", "World")

# Tách và nối
words = "apple,banana,orange".split(",")
# ["apple", "banana", "orange"]
joined = "-".join(words)
# "apple-banana-orange"

# Định dạng
name = "Python"
version = 3.9
formatted = f"Ngôn ngữ {name} phiên bản {version}"
# Hoặc
formatted2 = "Ngôn ngữ {} phiên bản {}".format(name, version)
```

### 17.4. String Slicing

```python
text = "Python Programming"

print(text[0:6])      # "Python"
print(text[:6])       # "Python"
print(text[7:])       # "Programming"
print(text[-11:])     # "Programming"
print(text[::-1])     # "gnimmargorP nohtyP" (đảo ngược)
```

---

## 18. Lambda Functions

Lambda là hàm ẩn danh, ngắn gọn:

```python
# Hàm thông thường
def multiply(x, y):
    return x * y

# Lambda tương đương
multiply_lambda = lambda x, y: x * y

print(multiply(3, 4))         # 12
print(multiply_lambda(3, 4))   # 12

# Sử dụng với map()
numbers = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, numbers))
# [1, 4, 9, 16, 25]

# Sử dụng với filter()
evens = list(filter(lambda x: x % 2 == 0, numbers))
# [2, 4]

# Sử dụng với sorted()
students = [("An", 20), ("Bình", 18), ("Cường", 22)]
sorted_by_age = sorted(students, key=lambda x: x[1])
# [("Bình", 18), ("An", 20), ("Cường", 22)]
```

---

## 19. *args và **kwargs

### 19.1. *args

Nhận số lượng tham số không xác định:

```python
def sum_all(*args):
    total = 0
    for num in args:
        total += num
    return total

print(sum_all(1, 2, 3))        # 6
print(sum_all(1, 2, 3, 4, 5))  # 15
```

### 19.2. **kwargs

Nhận số lượng keyword arguments không xác định:

```python
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="An", age=20, city="Hà Nội")
# name: An
# age: 20
# city: Hà Nội
```

### 19.3. Kết hợp cả hai

```python
def flexible_function(*args, **kwargs):
    print("Args:", args)
    print("Kwargs:", kwargs)

flexible_function(1, 2, 3, name="Python", version=3.9)
# Args: (1, 2, 3)
# Kwargs: {'name': 'Python', 'version': 3.9}
```

---

## 20. Modules và Import

### 20.1. Import module

```python
import math
print(math.pi)           # 3.141592653589793
print(math.sqrt(16))     # 4.0

# Import với alias
import datetime as dt
today = dt.date.today()

# Import cụ thể
from math import pi, sqrt
print(pi)
print(sqrt(25))

# Import tất cả (không khuyến khích)
from math import *
```

### 20.2. Tạo module riêng

**file: my_module.py**
```python
def greet(name):
    return f"Hello, {name}!"

PI = 3.14159
```

**file: main.py**
```python
import my_module

print(my_module.greet("Python"))
print(my_module.PI)
```

---

## 21. Lập trình hướng đối tượng (OOP)

Lập trình hướng đối tượng (OOP) là một phương pháp lập trình dựa trên khái niệm "đối tượng", giúp tổ chức code tốt hơn và tăng khả năng tái sử dụng.

### 21.1. Class và Object

**Class** là khuôn mẫu để tạo các đối tượng, trong khi **Object** là thể hiện cụ thể của class.

```python
# Định nghĩa class
class Student:
    # Thuộc tính class (shared by all instances)
    school_name = "Trường ABC"
    
    # Constructor (phương thức khởi tạo)
    def __init__(self, name, age, grade):
        # Thuộc tính instance (riêng của mỗi object)
        self.name = name
        self.age = age
        self.grade = grade
    
    # Phương thức instance
    def introduce(self):
        return f"Tôi là {self.name}, {self.age} tuổi, học lớp {self.grade}"
    
    def study(self, subject):
        return f"{self.name} đang học {subject}"

# Tạo object từ class
student1 = Student("Nguyễn Văn A", 20, "12A1")
student2 = Student("Trần Thị B", 19, "11B2")

# Truy cập thuộc tính
print(student1.name)        # "Nguyễn Văn A"
print(student1.age)         # 20
print(Student.school_name)  # "Trường ABC"

# Gọi phương thức
print(student1.introduce())  # "Tôi là Nguyễn Văn A, 20 tuổi, học lớp 12A1"
print(student2.study("Toán"))  # "Trần Thị B đang học Toán"
```

### 21.2. Encapsulation (Đóng gói)

Encapsulation giúp ẩn chi tiết triển khai và chỉ cho phép truy cập thông qua các phương thức công khai.

```python
class BankAccount:
    def __init__(self, account_number, initial_balance=0):
        # Thuộc tính private (bắt đầu bằng __)
        self.__account_number = account_number
        self.__balance = initial_balance
    
    # Phương thức public để truy cập balance
    def get_balance(self):
        return self.__balance
    
    def get_account_number(self):
        return self.__account_number
    
    # Phương thức để gửi tiền
    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
            return f"Đã gửi {amount}. Số dư hiện tại: {self.__balance}"
        return "Số tiền không hợp lệ"
    
    # Phương thức để rút tiền
    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount
            return f"Đã rút {amount}. Số dư còn lại: {self.__balance}"
        return "Số tiền không hợp lệ hoặc không đủ"

# Sử dụng
account = BankAccount("ACC001", 1000)
print(account.deposit(500))    # "Đã gửi 500. Số dư hiện tại: 1500"
print(account.withdraw(200))   # "Đã rút 200. Số dư còn lại: 1300"
print(account.get_balance())   # 1300

# Không thể truy cập trực tiếp thuộc tính private
# print(account.__balance)  # Lỗi: AttributeError
```

### 21.3. Inheritance (Kế thừa)

Kế thừa cho phép class con kế thừa thuộc tính và phương thức từ class cha.

```python
# Class cha (Parent/Super class)
class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species
    
    def make_sound(self):
        return "Một số âm thanh"
    
    def info(self):
        return f"{self.name} là một {self.species}"

# Class con (Child/Sub class)
class Dog(Animal):
    def __init__(self, name, breed):
        # Gọi constructor của class cha
        super().__init__(name, "Chó")
        self.breed = breed
    
    # Override phương thức của class cha
    def make_sound(self):
        return "Gâu gâu!"
    
    # Phương thức riêng của class con
    def fetch(self):
        return f"{self.name} đang đi lấy bóng"

class Cat(Animal):
    def __init__(self, name, color):
        super().__init__(name, "Mèo")
        self.color = color
    
    def make_sound(self):
        return "Meo meo!"
    
    def climb(self):
        return f"{self.name} đang leo cây"

# Sử dụng
dog = Dog("Lucky", "Golden Retriever")
cat = Cat("Mimi", "Vàng")

print(dog.info())         # "Lucky là một Chó"
print(dog.make_sound())   # "Gâu gâu!"
print(dog.fetch())        # "Lucky đang đi lấy bóng"

print(cat.info())         # "Mimi là một Mèo"
print(cat.make_sound())   # "Meo meo!"
print(cat.climb())        # "Mimi đang leo cây"
```

### 21.4. Multiple Inheritance (Đa kế thừa)

Python hỗ trợ đa kế thừa, cho phép một class kế thừa từ nhiều class cha.

```python
class Flyable:
    def fly(self):
        return "Đang bay"

class Swimmable:
    def swim(self):
        return "Đang bơi"

class Duck(Animal, Flyable, Swimmable):
    def __init__(self, name):
        super().__init__(name, "Vịt")
    
    def make_sound(self):
        return "Quạc quạc!"

# Sử dụng
duck = Duck("Donald")
print(duck.make_sound())  # "Quạc quạc!"
print(duck.fly())          # "Đang bay"
print(duck.swim())         # "Đang bơi"
```

### 21.5. Polymorphism (Đa hình)

Polymorphism cho phép các đối tượng khác nhau phản ứng khác nhau với cùng một phương thức.

```python
class Shape:
    def area(self):
        pass  # Phương thức trừu tượng

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height
    
    def area(self):
        return self.width * self.height

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14159 * self.radius ** 2

class Triangle(Shape):
    def __init__(self, base, height):
        self.base = base
        self.height = height
    
    def area(self):
        return 0.5 * self.base * self.height

# Polymorphism trong hành động
shapes = [
    Rectangle(5, 4),
    Circle(3),
    Triangle(6, 8)
]

for shape in shapes:
    print(f"Diện tích: {shape.area()}")
# Diện tích: 20
# Diện tích: 28.27431
# Diện tích: 24.0
```

### 21.6. Method Overriding và Overloading

**Method Overriding**: Ghi đè phương thức của class cha.

```python
class Parent:
    def show(self):
        print("Phương thức của class cha")

class Child(Parent):
    def show(self):
        print("Phương thức của class con (đã ghi đè)")
        super().show()  # Gọi phương thức của class cha

child = Child()
child.show()
# Phương thức của class con (đã ghi đè)
# Phương thức của class cha
```

**Method Overloading**: Python không hỗ trợ overloading trực tiếp, nhưng có thể dùng default parameters hoặc *args.

```python
class Calculator:
    def add(self, a, b=0, c=0):
        return a + b + c
    
    # Hoặc dùng *args
    def multiply(self, *args):
        result = 1
        for num in args:
            result *= num
        return result

calc = Calculator()
print(calc.add(5))              # 5
print(calc.add(5, 3))            # 8
print(calc.add(5, 3, 2))         # 10
print(calc.multiply(2, 3, 4))    # 24
```

### 21.7. Class Methods và Static Methods

**Class Method**: Phương thức hoạt động với class, không cần instance.

```python
class Person:
    population = 0
    
    def __init__(self, name):
        self.name = name
        Person.population += 1
    
    @classmethod
    def get_population(cls):
        return cls.population
    
    @classmethod
    def create_baby(cls, name):
        return cls(name)

print(Person.get_population())  # 0
p1 = Person("An")
p2 = Person("Bình")
print(Person.get_population())  # 2

baby = Person.create_baby("Bé")
print(Person.get_population())  # 3
```

**Static Method**: Phương thức không cần truy cập instance hay class.

```python
class MathUtils:
    @staticmethod
    def add(a, b):
        return a + b
    
    @staticmethod
    def multiply(a, b):
        return a * b

# Có thể gọi từ class hoặc instance
print(MathUtils.add(5, 3))      # 8
utils = MathUtils()
print(utils.multiply(4, 2))     # 8
```

### 21.8. Property Decorator

Property decorator cho phép truy cập phương thức như thuộc tính.

```python
class Temperature:
    def __init__(self, celsius):
        self._celsius = celsius
    
    @property
    def celsius(self):
        return self._celsius
    
    @celsius.setter
    def celsius(self, value):
        if value < -273.15:
            raise ValueError("Nhiệt độ không thể thấp hơn -273.15°C")
        self._celsius = value
    
    @property
    def fahrenheit(self):
        return self._celsius * 9/5 + 32
    
    @fahrenheit.setter
    def fahrenheit(self, value):
        self._celsius = (value - 32) * 5/9

temp = Temperature(25)
print(temp.celsius)        # 25
print(temp.fahrenheit)     # 77.0

temp.fahrenheit = 100
print(temp.celsius)        # 37.777...
```

### 21.9. Magic Methods (Dunder Methods)

Magic methods là các phương thức đặc biệt bắt đầu và kết thúc bằng `__`.

```python
class Book:
    def __init__(self, title, author, pages):
        self.title = title
        self.author = author
        self.pages = pages
    
    # String representation
    def __str__(self):
        return f"{self.title} bởi {self.author}"
    
    def __repr__(self):
        return f"Book('{self.title}', '{self.author}', {self.pages})"
    
    # Comparison operators
    def __eq__(self, other):
        return self.pages == other.pages
    
    def __lt__(self, other):
        return self.pages < other.pages
    
    def __le__(self, other):
        return self.pages <= other.pages
    
    # Arithmetic operators
    def __add__(self, other):
        return Book(
            f"{self.title} & {other.title}",
            f"{self.author} & {other.author}",
            self.pages + other.pages
        )
    
    # Length
    def __len__(self):
        return self.pages

book1 = Book("Python Guide", "Author A", 300)
book2 = Book("Java Guide", "Author B", 250)

print(book1)                    # "Python Guide bởi Author A"
print(len(book1))               # 300
print(book1 > book2)            # True
print(book1 == book2)           # False

combined = book1 + book2
print(combined)                  # "Python Guide & Java Guide bởi Author A & Author B"
```

### 21.10. Abstract Base Classes

Abstract Base Classes định nghĩa interface mà các class con phải triển khai.

```python
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass
    
    @abstractmethod
    def stop(self):
        pass
    
    def info(self):
        return "Đây là một phương tiện"

class Car(Vehicle):
    def start(self):
        return "Xe hơi đã khởi động"
    
    def stop(self):
        return "Xe hơi đã dừng"

class Motorcycle(Vehicle):
    def start(self):
        return "Xe máy đã khởi động"
    
    def stop(self):
        return "Xe máy đã dừng"

# Không thể tạo instance từ abstract class
# vehicle = Vehicle()  # Lỗi!

car = Car()
print(car.start())  # "Xe hơi đã khởi động"
```

### 21.11. Composition vs Inheritance

**Inheritance**: "is-a" relationship (là một).

**Composition**: "has-a" relationship (có một).

```python
# Inheritance
class Engine:
    def start(self):
        return "Động cơ đã khởi động"

class Car:
    def __init__(self):
        # Composition: Car HAS-A Engine
        self.engine = Engine()
    
    def start(self):
        return self.engine.start()

car = Car()
print(car.start())  # "Động cơ đã khởi động"
```

### 21.12. Ví dụ tổng hợp: Hệ thống quản lý thư viện

```python
class Book:
    def __init__(self, isbn, title, author):
        self.isbn = isbn
        self.title = title
        self.author = author
        self.is_borrowed = False
    
    def __str__(self):
        status = "Đã mượn" if self.is_borrowed else "Có sẵn"
        return f"{self.title} - {self.author} ({status})"

class LibraryMember:
    def __init__(self, member_id, name):
        self.member_id = member_id
        self.name = name
        self.borrowed_books = []
    
    def borrow_book(self, book):
        if not book.is_borrowed:
            book.is_borrowed = True
            self.borrowed_books.append(book)
            return f"{self.name} đã mượn {book.title}"
        return f"{book.title} đã được mượn"
    
    def return_book(self, book):
        if book in self.borrowed_books:
            book.is_borrowed = False
            self.borrowed_books.remove(book)
            return f"{self.name} đã trả {book.title}"
        return f"{self.name} không mượn {book.title}"

class Library:
    def __init__(self, name):
        self.name = name
        self.books = []
        self.members = []
    
    def add_book(self, book):
        self.books.append(book)
    
    def register_member(self, member):
        self.members.append(member)
    
    def list_available_books(self):
        return [book for book in self.books if not book.is_borrowed]

# Sử dụng
library = Library("Thư viện Trung tâm")

book1 = Book("001", "Python Programming", "Author A")
book2 = Book("002", "Data Science", "Author B")

library.add_book(book1)
library.add_book(book2)

member = LibraryMember("M001", "Nguyễn Văn A")
library.register_member(member)

print(member.borrow_book(book1))  # "Nguyễn Văn A đã mượn Python Programming"
print(library.list_available_books())  # [book2]
```

---

## Kết luận

Tài liệu này đã cung cấp một cái nhìn tổng quan về các khái niệm cơ bản và nâng cao trong Python. Để thành thạo Python, hãy thực hành thường xuyên và xây dựng các dự án thực tế. Python là một ngôn ngữ mạnh mẽ và linh hoạt, với cộng đồng lớn và nhiều thư viện hỗ trợ, giúp bạn giải quyết nhiều vấn đề khác nhau một cách hiệu quả.

---

## Tài liệu tham khảo

Tài liệu này được tổng hợp và tham khảo từ 
   - URL: https://realpython.com/cheatsheets/python/
   - URL: https://200lab.io/blog/python-cheat-sheet-danh-cho-nguoi-moi-phan-1
   - URL: https://labex.io/pythoncheatsheet/

---

