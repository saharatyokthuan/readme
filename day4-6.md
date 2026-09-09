![30DaysOfPython](./images/30DaysOfPython_banner3@2x.png)

🧳 [ตอนที่ 1: วันที่ 1 - 3](day1-3.md)  
🧳 [ตอนที่ 2: วันที่ 4 - 6](day4-6.md)  
🧳 [ตอนที่ 3: วันที่ 7 - 9](day7-9.md)  
🧳 [ตอนที่ 4: วันที่ 10 - 12](day10-12.md)  
🧳 [ตอนที่ 5: วันที่ 13 - 15](day13-15.md)  
🧳 [ตอนที่ 6: วันที่ 16 - 18](day16-18.md)  
🧳 [ตอนที่ 7: วันที่ 19 - 21](day19-21.md)  
🧳 [ตอนที่ 8: วันที่ 22 - 24](day22-24.md)  
🧳 [ตอนที่ 9: วันที่ 25 - 27](day25-27.md)  
🧳 [ตอนที่ 10: วันที่ 28 - 30](day28-30.md) 

---
- [วันที่ 4](#day-4)
  - [สตริง](#string)
    - [การสร้างสตริง](#creating-a-string)
    - [การต่อสตริง (Concatenation)](#string-concatenation)
    - [Escape Sequences ในสตริง](#escape-sequences-in-string)
    - [การจัดรูปแบบสตริง](#string-formating)
      - [การจัดรูปแบบสตริงแบบเก่า (ตัวดำเนินการ %)](#old-style-string-formatting--operator)
      - [การจัดรูปแบบสตริงแบบใหม่ (str.format)](#new-style-string-formatting-strformat)
      - [String Interpolation / f-Strings (Python 3.6+)](#string-interpolation--f-strings-python-36)
    - [สตริงใน Python ในฐานะลำดับของตัวอักษร](#python-strings-as-sequences-of-characters)
      - [การแกะ (Unpacking) ตัวอักษร](#unpacking-characters)
      - [การเข้าถึงตัวอักษรในสตริงด้วยดัชนี (index)](#accessing-characters-in-strings-by-index)
      - [การตัด (Slicing) สตริงใน Python](#slicing-python-strings)
      - [การกลับด้านสตริง](#reversing-a-string)
      - [การข้ามตัวอักษรขณะตัด (slicing)](#skipping-characters-while-slicing)
    - [เมธอดของสตริง](#string-methods)
  - [💻 แบบฝึกหัด - วันที่ 4](#%f0%9f%92%bb-exercises---day-4)
- [วันที่ 5](#day-5)
  - [ลิสต์](#lists)
    - [วิธีสร้างลิสต์](#how-to-create-a-list)
    - [การเข้าถึงรายการในลิสต์ด้วยดัชนีบวก](#accessing-list-items-using-positive-indexing)
    - [การเข้าถึงรายการในลิสต์ด้วยดัชนีลบ](#accessing-list-items-using-negative-indexing)
    - [การแกะ (Unpacking) รายการในลิสต์](#unpacking-list-items)
    - [การตัด (Slicing) รายการจากลิสต์](#slicing-items-from-list)
    - [การแก้ไขลิสต์](#modifying-list)
    - [การตรวจสอบรายการในลิสต์](#check-items-in-a-list)
    - [การเพิ่มรายการในลิสต์](#adding-item-in-a-list)
    - [การแทรกรายการเข้าไปในลิสต์](#inserting-item-in-to-a-list)
    - [การลบรายการออกจากลิสต์](#removing-item-from-list)
    - [การลบรายการโดยใช้ pop](#removing-item-using-pop)
    - [การลบรายการโดยใช้ del](#removing-item-using-del)
    - [การล้างรายการในลิสต์](#clearing-list-items)
    - [การคัดลอกลิสต์](#copying-a-list)
    - [การรวมลิสต์เข้าด้วยกัน](#joining-lists)
    - [การนับจำนวนรายการในลิสต์](#counting-items-in-a-list)
    - [การหาดัชนีของรายการ](#finding-index-of-an-item)
    - [การกลับด้านลิสต์](#reversing-a-list)
    - [การเรียงลำดับรายการในลิสต์](#sorting-list-items)
  - [💻 แบบฝึกหัด: วันที่ 5](#%f0%9f%92%bb-exercises-day-5)
- [วันที่ 6:](#day-6)
  - [ทูเพิล](#tuple)
    - [การสร้างทูเพิล](#creating-tuple)
    - [ความยาวของทูเพิล](#tuple-length)
    - [การเข้าถึงรายการในทูเพิล](#accessing-tuple-items)
    - [การตัด (Slicing) ทูเพิล](#slicing-tuples)
    - [การเปลี่ยนทูเพิลเป็นลิสต์](#changing-tuples-to-list)
    - [การตรวจสอบรายการในลิสต์](#checking-an-item-in-a-list)
    - [การรวมทูเพิลเข้าด้วยกัน](#joining-tuples)
    - [การลบทูเพิล](#deleting-tuple)
  - [💻 แบบฝึกหัด: วันที่ 6](#%f0%9f%92%bb-exercises-day-6)

# วันที่ 4

## สตริง

ข้อความคือชนิดข้อมูลสตริง ข้อมูลใด ๆ ที่เขียนเป็นข้อความคือสตริง ข้อมูลใด ๆ ที่อยู่ภายใต้เครื่องหมายคำพูดเดี่ยวหรือคู่คือสตริง มีเมธอดของสตริงและฟังก์ชันในตัวมากมายสำหรับจัดการกับชนิดข้อมูลสตริง หากต้องการตรวจสอบความยาวของสตริงให้ใช้เมธอด len()

### การสร้างสตริง

```py
letter = 'P'                # A string could be a single character or a bunch of texts
print(letter)               # P
print(len(letter))          # 1
greeting = 'Hello, World!'  # String could be  a single or double quote,"Hello, World!"
print(greeting)             # Hello, World!
print(len(greeting))        # 13
sentence = "I hope you are enjoying 30 days of python challenge"
print(sentence)
```

สตริงหลายบรรทัดถูกสร้างขึ้นโดยใช้เครื่องหมายคำพูดสามตัว ''' หรือ """ ดูตัวอย่างด้านล่าง

```py
multiline_string = '''I am a teacher and enjoy teaching.
I didn't find anything as rewarding as empowering people.
That is why I created 30 days of python.'''
print(multiline_string)
# Another way of doing the same thing
multiline_string = """I am a teacher and enjoy teaching.
I didn't find anything as rewarding as empowering people.
That is why I created 30 days of python."""
print(multiline_string)
```

### การต่อสตริง (Concatenation)

เราสามารถเชื่อมสตริงสองอันเข้าด้วยกันได้ การผสานหรือเชื่อมสตริงสองอันเข้าด้วยกันเรียกว่าการต่อสตริง (concatenation) ดูตัวอย่างด้านล่าง

  ```py
  first_name = 'Asabeneh'
  last_name = 'Yetayeh'
  space = ' '
  full_name = first_name  +  space + last_name
  print(full_name) # Asabeneh Yetayeh
  # Checking length of a string using len() builtin function
  print(len(first_name))  # 8
  print(len(last_name))   # 7
  print(len(first_name) > len(last_name)) # True
  print(len(full_name)) # 15
  ```

### Escape Sequences ในสตริง

ใน Python และภาษาโปรแกรมมิงอื่น ๆ เครื่องหมาย \ ตามด้วยตัวอักษรหนึ่งตัวคือ escape sequence มาดู escape character ที่พบบ่อยที่สุดกัน:

* \n: ขึ้นบรรทัดใหม่
* \t: แท็บ หมายถึง (8 ช่องว่าง)
* \\\\: แบ็กสแลช
* \\': เครื่องหมายคำพูดเดี่ยว (')
* \\": เครื่องหมายคำพูดคู่ (")

```py
print('I hope every one enjoying the python challenge.\nDo you ?') # line break
print('Days\tTopics\tExercises')
print('Day 1\t3\t5')
print('Day 2\t3\t5')
print('Day 3\t3\t5')
print('Day 4\t3\t5')
print('This is a back slash  symbol (\\)') # To write a back slash
print('In every programming language it starts with \"Hello, World!\"') 

# output
I hope every one enjoying the python challenge.
Do you ?
Days	Topics	Exercises
Day 1	5	    5
Day 2	6	    20
Day 3	5	    23
Day 4	1	    35
This is a back slash  symbol (\)
In every programming language it starts with "Hello, World!"
```

### การจัดรูปแบบสตริง

#### การจัดรูปแบบสตริงแบบเก่า (ตัวดำเนินการ %)

ใน Python มีวิธีจัดรูปแบบสตริงอยู่หลายวิธี ในหัวข้อนี้เราจะพูดถึงบางวิธี
ตัวดำเนินการ "%" ใช้เพื่อจัดรูปแบบชุดของตัวแปรที่อยู่ใน "ทูเพิล" (ลิสต์ขนาดคงที่) ร่วมกับสตริงรูปแบบ (format string) ซึ่งประกอบด้วยข้อความปกติร่วมกับ "ตัวระบุอาร์กิวเมนต์" (argument specifiers) สัญลักษณ์พิเศษอย่าง "%s", "%d", "%f", "%.<จำนวนหลัก>f"

* %s - สตริง (หรืออ็อบเจ็กต์ใด ๆ ที่มีการแสดงผลเป็นสตริง เช่น ตัวเลข)
* %d - จำนวนเต็ม
* %f - จำนวนทศนิยม
* %.<จำนวนหลัก>f - จำนวนทศนิยมที่มีจำนวนหลักด้านขวาของจุดคงที่

```py
# Strings only
first_name = 'Asabeneh'
last_name = 'Yetayeh'
language = 'Python'
formatted_string = 'I am %s %s. I teach %s' %(first_name, last_name, language)
print(formatted_string)

# Strings  and numbers
radius = 10
pi = 3.14
area = pi * radius ** 2
formatted_string = 'The area of radius %d is %.2f.' %(radius, area) # 2 refers the 2 significant digits after the point

python_libraries = ['Django', 'Flask', 'Numpy', 'Pandas']
formatted_string = 'The following are python libraries:' % python_libraries
print(formatted_string) # "The following are python libraries:['Django', 'Flask', 'Numpy', 'Pandas']"
```
#### การจัดรูปแบบสตริงแบบใหม่ (str.format)
การจัดรูปแบบนี้ถูกนำมาใช้ใน Python เวอร์ชัน 3

```py

first_name = 'Asabeneh'
last_name = 'Yetayeh'
language = 'Python'
formatted_string = 'I am {} {}. I teach {}'.format(first_name, last_name, language)
print(formatted_string)
a = 4
b = 3

print('{} + {} = {}'.format(a, b, a + b))
print('{} - {} = {}'.format(a, b, a - b))
print('{} * {} = {}'.format(a, b, a * b))
print('{} / {} = {:.2f}'.format(a, b, a / b)) # limits it to two digits after decimal
print('{} % {} = {}'.format(a, b, a % b))
print('{} // {} = {}'.format(a, b, a // b))
print('{} ** {} = {}'.format(a, b, a ** b))

# output
4 + 3 = 7
4 - 3 = 1
4 * 3 = 12
4 / 3 = 1.33
4 % 3 = 1
4 // 3 = 1
4 ** 3 = 64

# Strings  and numbers
radius = 10
pi = 3.14
area = pi * radius ** 2
formatted_string = 'The area of radius {} is {:.2f}.'.format(radius, area) # 2 digits after decimal
print(formatted_string)

```
#### String Interpolation / f-Strings (Python 3.6+)
การจัดรูปแบบสตริงแบบใหม่อีกวิธีหนึ่งคือ string interpolation หรือ f-strings สตริงเริ่มต้นด้วย f และเราสามารถแทรกข้อมูลลงในตำแหน่งที่สอดคล้องกันได้
```py
a = 4
b = 3
print(f'{a} + {b} = {a +b}')
print(f'{a} - {b} = {a - b}')
print(f'{a} * {b} = {a * b}')
print(f'{a} / {b} = {a / b:.2f}') 
print(f'{a} % {b} = {a % b}')
print(f'{a} // {b} = {a // b}')
print(f'{a} ** {b} = {a ** b}')
```

### สตริงใน Python ในฐานะลำดับของตัวอักษร
สตริงใน Python เป็นลำดับของตัวอักษร และใช้วิธีการเข้าถึงพื้นฐานร่วมกับลำดับอื่น ๆ ของ Python เช่น ลิสต์และทูเพิล วิธีที่ง่ายที่สุดในการดึงตัวอักษรเดี่ยว ๆ ออกจากสตริง (และสมาชิกแต่ละตัวจากลำดับใด ๆ) คือการแกะ (unpack) ตัวอักษรเหล่านั้นเข้าสู่ตัวแปรที่สอดคล้องกัน
#### การแกะ (Unpacking) ตัวอักษร
```
language = 'Python'
a,b,c,d,e,f = language # unpacking sequence characters into variables
print(a) # P
print(b) # y
print(c) # t 
print(d) # h
print(e) # o
print(f) # n
```
#### การเข้าถึงตัวอักษรในสตริงด้วยดัชนี (index)
  ในการเขียนโปรแกรม การนับเริ่มต้นจากศูนย์ ดังนั้นตัวอักษรแรกของสตริงจะอยู่ที่ดัชนี 0 และตัวอักษรสุดท้ายของสตริงจะอยู่ที่ตำแหน่งความยาวของสตริงลบ 1

  ![String index](./images/string_index.png)
  
```py
language = 'Python'
first_letter = language[0]
print(first_letter) # P
second_letter = language[1]
print(second_letter) # y
last_index = len(language) - 1
last_letter = language[last_index]
print(last_letter) # n
```
หากเราต้องการเริ่มนับจากด้านขวา เราสามารถใช้ดัชนีลบได้ -1 คือดัชนีสุดท้าย
```py
language = 'Python'
last_letter = language[-1]
print(last_letter) # n
second_last = language[-2]
print(second_last) # o
  ```

#### การตัด (Slicing) สตริงใน Python

ใน Python เราสามารถตัดสตริงย่อยออกจากสตริงได้

```py
language = 'Python'
first_three = language[0:3] # starts at zero index and up to 3 but not include 3
last_three = language[3:6]
print(last_three) # hon
# Another way
last_three = language[-3:]
print(last_three)   # hon
last_three = language[3:]
print(last_three)   # hon
```

#### การกลับด้านสตริง

เราสามารถกลับด้านสตริงใน Python ได้อย่างง่ายดาย

```py
greeting = 'Hello, World!'
print(greeting[::-1]) # !dlroW ,olleH
```

#### การข้ามตัวอักษรขณะตัด (slicing)
เป็นไปได้ที่จะข้ามตัวอักษรขณะตัด (slicing) โดยส่งอาร์กิวเมนต์ step ให้กับเมธอด slice
```py
language = 'Python'
pto = language[0,6:2] # 
print(pto) # Pto
```

### เมธอดของสตริง
มีเมธอดของสตริงมากมายที่ช่วยให้เราจัดรูปแบบสตริงได้ ดูตัวอย่างเมธอดของสตริงบางส่วนในตัวอย่างต่อไปนี้:

* capitalize(): แปลงตัวอักษรตัวแรกของสตริงให้เป็นตัวพิมพ์ใหญ่
```py
challenge = 'thirty days of python'
print(challenge.capitalize()) # 'Thirty days of python'
```
* count(): คืนค่าจำนวนครั้งที่สตริงย่อยปรากฏในสตริง, count(substring, start=.., end=..)
```py
challenge = 'thirty days of python'
print(challenge.count('y')) # 3
print(challenge.count('y', 7, 14)) # 1
print(challenge.count('th')) # 2`
```
* endswith(): ตรวจสอบว่าสตริงลงท้ายด้วยข้อความที่ระบุหรือไม่
```py
challenge = 'thirty days of python'
print(challenge.endswith('on'))   # True
print(challenge.endswith('tion')) # False
```
* expandtabs(): แทนที่ตัวอักษรแท็บด้วยช่องว่าง ขนาดแท็บเริ่มต้นคือ 8 สามารถรับอาร์กิวเมนต์ขนาดแท็บได้
```py
challenge = 'thirty\tdays\tof\tpython'
print(challenge.expandtabs())   # 'thirty  days    of      python'
print(challenge.expandtabs(10)) # 'thirty    days      of        python'
```
* find(): คืนค่าดัชนีของการปรากฏครั้งแรกของสตริงย่อย
```py
challenge = 'thirty days of python'
print(challenge.find('y'))  # 5
print(challenge.find('th')) # 0
```
* format(): จัดรูปแบบสตริงให้แสดงผลได้สวยงามขึ้น
    ดูรายละเอียดเพิ่มเติมเกี่ยวกับการจัดรูปแบบสตริงได้ที่[ลิงก์นี้](https://www.programiz.com/python-programming/methods/string/format)
```py
first_name = 'Asabeneh'
last_name = 'Yetayeh'
job = 'teacher'
country = 'Finland'
sentence = 'I am {} {}. I am a {}. I live in {}.'.format(first_name, last_name, job, country)
print(sentence) # I am Asabeneh Yetayeh. I am a teacher. I live in Finland.

radius = 10
pi = 3.14
area = pi * radius ** 2
result = 'The area of circle with {} is {}'.format(str(radius), str(area))
print(result) # The area of circle with 10 is 314.0
```
* index(): คืนค่าดัชนีของสตริงย่อย
```py
challenge = 'thirty days of python'
print(challenge.find('y'))  # 5
print(challenge.find('th')) # 0
```
* isalnum(): ตรวจสอบว่าเป็นตัวอักษรและตัวเลข (alphanumeric)
```py
challenge = 'ThirtyDaysPython'
print(challenge.isalnum()) # True

challenge = '30DaysPython'
print(challenge.isalnum()) # True

challenge = 'thirty days of python'
print(challenge.isalnum()) # False

challenge = 'thirty days of python 2019'
print(challenge.isalnum()) # False
```
* isalpha(): ตรวจสอบว่าตัวอักษรทั้งหมดเป็นตัวอักษร (alphabet) หรือไม่
```py
challenge = 'thirty days of python'
print(challenge.isalpha()) # True
num = '123'
print(num.isalpha())      # False
```
* isdecimal(): ตรวจสอบตัวอักษรทศนิยม
```py
challenge = 'thirty days of python'
print(challenge.find('y'))  # 5
print(challenge.find('th')) # 0
```
* isdigit(): ตรวจสอบตัวอักษรที่เป็นตัวเลข (digit)
```py
challenge = 'Thirty'
print(challenge.isdigit()) # False
challenge = '30'
print(challenge.digit())   # True
```
* isdecimal(): ตรวจสอบตัวอักษรทศนิยม
```py
num = '10'
print(num.isdecimal()) # True
num = '10.5'
print(num.isdecimal()) # False
```

* isidentifier(): ตรวจสอบว่าเป็นตัวระบุ (identifier) ที่ถูกต้อง หมายถึงตรวจสอบว่าสตริงเป็นชื่อตัวแปรที่ถูกต้องหรือไม่
```py
challenge = '30DaysOfPython'
print(challenge.isidentifier()) # False, because it starts with a number
challenge = 'thirty_days_of_python'
print(challenge.isidentifier()) # True
```

* islower(): ตรวจสอบว่าตัวอักษรทั้งหมดในสตริงเป็นตัวพิมพ์เล็กหรือไม่
```py
challenge = 'thirty days of python'
print(challenge.islower()) # True
challenge = 'Thirty days of python'
print(challenge.islower()) # False
```
* isupper(): คืนค่าว่าตัวอักษรทั้งหมดเป็นตัวพิมพ์ใหญ่หรือไม่
```py
challenge = 'thirty days of python'
print(challenge.isupper()) #  False
challenge = 'THIRTY DAYS OF PYTHON'
print(challenge.isupper()) # True
```

* isnumeric(): ตรวจสอบตัวอักษรที่เป็นตัวเลข (numeric)
```py
num = '10'
print(num.isnumeric())      # True
print('ten'.isnumeric())    # False
```
* join(): คืนค่าสตริงที่ถูกต่อเข้าด้วยกัน
```py
web_tech = ['HTML', 'CSS', 'JavaScript', 'React']
result = '#, '.join(web_tech)
print(result) # 'HTML# CSS# JavaScript# React'
```
* strip(): ลบตัวอักษรทั้งด้านหน้าและด้านหลัง
```py
challenge = ' thirty days of python '
print(challenge.strip('y')) # 5
```
* replace(): แทนที่สตริงย่อยภายในสตริง
```py
challenge = 'thirty days of python'
print(challenge.replace('python', 'coding')) # 'thirty days of coding'
```
* split(): แบ่งสตริงจากด้านซ้าย
```py
challenge = 'thirty days of python'
print(challenge.split()) # ['thirty', 'days', 'of', 'python']
```
* title(): คืนค่าสตริงในรูปแบบ Title Case
```py
challenge = 'thirty days of python'
print(challenge.title()) # Thirty Days Of Python
```
* swapcase(): สลับตัวพิมพ์ใหญ่-เล็กของสตริง
  เมธอด swapcase() ของสตริงแปลงตัวอักษรพิมพ์ใหญ่ทั้งหมดให้เป็นตัวพิมพ์เล็กและตัวอักษรพิมพ์เล็กทั้งหมดให้เป็นตัวพิมพ์ใหญ่ของสตริงที่กำหนด แล้วคืนค่ากลับมา
```py
challenge = 'thirty days of python'
print(challenge.swapcase())   # THIRTY DAYS OF PYTHON
challenge = 'Thirty Days Of Python'
print(challenge.swapcase())  # tHIRTY dAYS oF pYTHON
```
* startswith(): ตรวจสอบว่าสตริงขึ้นต้นด้วยสตริงที่ระบุหรือไม่
```py
challenge = 'thirty days of python'
print(challenge.startswith('thirty')) # True

challenge = '30 days of python'
print(challenge.startswith('thirty')) # False
```

## 💻 แบบฝึกหัด - วันที่ 4
1. ต่อสตริง 'Thirty', 'Days', 'Of', 'Python' ให้เป็นสตริงเดียว, 'Thirty Days Of Python'
2. ต่อสตริง 'Coding', 'For', 'All' ให้เป็นสตริงเดียว, 'Coding For All'
3. ประกาศตัวแปรชื่อ company และกำหนดค่าเริ่มต้นเป็น "Coding For All"
4. พิมพ์ company โดยใช้ *print()*
5. พิมพ์ความยาวของสตริง company โดยใช้เมธอด *len()* และ *print()*
6. เปลี่ยนตัวอักษรทั้งหมดให้เป็นตัวพิมพ์ใหญ่โดยใช้เมธอด *upper()*
7. เปลี่ยนตัวอักษรทั้งหมดให้เป็นตัวพิมพ์เล็กโดยใช้เมธอด *lower()*
8. ใช้เมธอด capitalize(), title(), swapcase() เพื่อจัดรูปแบบค่าของสตริง *Coding For All*
9.  ตัด (slice) เอาคำแรกของสตริง *Coding For All*
10. ตรวจสอบว่าสตริง *Coding For All* มีคำว่า Coding อยู่หรือไม่ โดยใช้เมธอด index, find หรือเมธออื่น ๆ
11. แทนที่คำว่า coding ในสตริง 'Coding For All' ด้วย Python
12. เปลี่ยน Python for Everyone เป็น Python for All โดยใช้เมธอด replace หรือเมธอดอื่น ๆ
13. แบ่งสตริง 'Coding For All' ที่ช่องว่างโดยใช้เมธอด split()
14. "Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon" แบ่งสตริงที่เครื่องหมายจุลภาค
15. ตัวอักษรที่ดัชนี 0 ในสตริง *Coding For All* คืออะไร
16. ดัชนีสุดท้ายของสตริง *Coding For All* คืออะไร
17. ตัวอักษรที่ดัชนี 10 ในสตริง "Coding For All" คืออะไร
18. สร้างคำย่อ (acronym) ของชื่อ 'Python For Everyone'
19. สร้างคำย่อ (acronym) ของชื่อ 'Coding For All'
20. ใช้ index เพื่อหาตำแหน่งการปรากฏครั้งแรกของ C ในสตริง Coding For All
21. ใช้ index เพื่อหาตำแหน่งการปรากฏครั้งแรกของ F ในสตริง Coding For All
22. ใช้ rfind เพื่อหาตำแหน่งการปรากฏครั้งสุดท้ายของ l ในสตริง Coding For All People
23. ใช้ index หรือ find เพื่อหาตำแหน่งการปรากฏครั้งแรกของคำว่า because ในประโยคต่อไปนี้: 'You cannot end a sentence with because because because is a conjunction'
24. ใช้ rindex เพื่อหาตำแหน่งการปรากฏครั้งสุดท้ายของคำว่า because ในประโยคต่อไปนี้: 'You cannot end a sentence with because because because is a conjunction'
25. ตัด (slice) เอาวลี because because because ในประโยคต่อไปนี้: 'You cannot end a sentence with because because because is a conjunction'
26. หาตำแหน่งการปรากฏครั้งแรกของคำว่า because ในประโยคต่อไปนี้: 'You cannot end a sentence with because because because is a conjunction'
27. ตัด (slice) เอาวลี because because because ในประโยคต่อไปนี้: 'You cannot end a sentence with because because because is a conjunction'
28. Coding For All ขึ้นต้นด้วยสตริงย่อย *Coding* หรือไม่ ?
29. Coding For All ลงท้ายด้วยสตริงย่อย *coding* หรือไม่ ?
30. '&nbsp;&nbsp; Coding For All &nbsp;&nbsp;&nbsp; &nbsp;' &nbsp;, ลบช่องว่างหน้าและหลังในสตริงที่กำหนดออก
31. ตัวแปรใดต่อไปนี้จะคืนค่า True เมื่อใช้เมธอด isidentifier()
    * 30DaysOfPython
    * thirty_days_of_python
32. ต่อไปนี้คือรายชื่อไลบรารี Python บางส่วน: ['Django', 'Flask', 'Bottle', 'Pyramid', 'Falcon'] จงรวมลิสต์เข้าด้วยกันโดยใช้สตริง hash และช่องว่างคั่น
33. ใช้ newline escape sequence เพื่อเขียนประโยคต่อไปนี้
    ```py
    I am enjoying this challenge.
    I just wonder what is next.
    ```
34. ใช้ tab escape sequence เพื่อเขียนประโยคต่อไปนี้
    ```py
    Name      Age     Country
    Asabeneh  250     Finland
    ```
35. ใช้เมธอดจัดรูปแบบสตริงเพื่อแสดงผลดังนี้:
```sh
radius = 10
area = 3.14 * radius ** 2
The area of radius 10 is 314 meters squares. 
```
36. สร้างผลลัพธ์ต่อไปนี้โดยใช้เมธอดจัดรูปแบบสตริง:
```sh
8 + 6 = 14
8 - 6 = 2
8 * 6 = 48
8 / 6 = 1.33
8 % 6 = 2
8 // 6 = 1
8 ** 6 = 262144
```
# วันที่ 5
## ลิสต์
ใน Python มีชนิดข้อมูลกลุ่ม (collection) 4 ประเภทดังนี้:
* List (ลิสต์): กลุ่มข้อมูลที่มีลำดับและสามารถแก้ไขได้ (modifiable) อนุญาตให้มีสมาชิกซ้ำกันได้
* Tuple (ทูเพิล): กลุ่มข้อมูลที่มีลำดับและไม่สามารถแก้ไขได้ (immutable) อนุญาตให้มีสมาชิกซ้ำกันได้
* Set (เซ็ต): กลุ่มข้อมูลที่ไม่มีลำดับและไม่มีดัชนี ไม่มีสมาชิกซ้ำกัน
* Dictionary (ดิกชันนารี): กลุ่มข้อมูลที่ไม่มีลำดับ สามารถแก้ไขได้ (modifiable) และมีดัชนี ไม่มีสมาชิกซ้ำกัน

ลิสต์คือกลุ่มของข้อมูลต่างชนิดกันที่มีลำดับและสามารถแก้ไขได้ (mutable) ลิสต์อาจว่างเปล่าหรือมีรายการที่เป็นชนิดข้อมูลต่าง ๆ ก็ได้
### วิธีสร้างลิสต์
ใน Python เราสามารถสร้างลิสต์ได้ 2 วิธี:
* ใช้ฟังก์ชันในตัว list
```py
# syntax
lst = list()
```
```py
empty_list = list() # this is an empty list, no item in the list
print(len(empty_list)) # 0
```
* ใช้วงเล็บเหลี่ยม, []
```py
# syntax
lst = []
```
```py
empty_list = [] # this is an empty list, no item in the list
print(len(empty_list)) # 0
```

ลิสต์ที่มีค่าเริ่มต้น เราใช้ *len()* เพื่อหาความยาวของลิสต์
```py
fruits = ['banana', 'orange', 'mango', 'lemon']                     # list of fruits
vegetables = ['Tomato', 'Potato', 'Cabbage','Onion', 'Carrot']      # list of vegetables
animal_products = ['milk', 'meat', 'butter', 'yoghurt']             # list of animal products
web_techs = ['HTML', 'CSS', 'JS', 'React','Redux', 'Node', 'MongDB'] # list of web technologies
countries = ['Finland', 'Estonia', 'Denmark', 'Sweden', 'Norway']

# Print the lists and it length
print('Fruits:', fruits)
print('Number of fruits:', len(fruits))
print('Vegetables:', vegetables)
print('Number of vegetables:', len(vegetables))
print('Animal products:',animal_products)
print('Number of animal products:', len(animal_products))
print('Web technologies:', web_techs)
print('Number of web technologies:', len(web_techs))
print('Countries:', countries)
print('Number of countries:', len(countries))
```
```sh
output
Fruits: ['banana', 'orange', 'mango', 'lemon']
Number of fruits: 4
Vegetables: ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot']
Number of vegetables: 5
Animal products: ['milk', 'meat', 'butter', 'yoghurt']
Number of animal products: 4
Web technologies: ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB']
Number of web technologies: 7
Countries: ['Finland', 'Estonia', 'Denmark', 'Sweden', 'Norway']
Number of countries: 5
```
* ลิสต์สามารถมีรายการที่เป็นชนิดข้อมูลต่างกันได้
```py
 lst = ['Asabeneh', 250, True, {'country':'Finland', 'city':'Helsinki'}] # list containing different data types
```
### การเข้าถึงรายการในลิสต์ด้วยดัชนีบวก
เราเข้าถึงแต่ละรายการในลิสต์โดยใช้ดัชนีของมัน ดัชนีของลิสต์เริ่มต้นที่ 0 ภาพด้านล่างแสดงให้เห็นชัดเจนว่าดัชนีเริ่มต้นตรงไหน
![List index](./images/list_index.png)
```py
fruits = ['banana', 'orange', 'mango', 'lemon'] 
first_fruit = fruits[0] # we are accessing the first item using its index
print(first_fruit)      # banana
second_fruit = fruits[1]
print(second_fruit)     # orange
last_fruit = fruits[3]
print(last_fruit) # lemon
# Last index
last_index = len(fruits) - 1
last_fruit = fruits[last_index]
```
### การเข้าถึงรายการในลิสต์ด้วยดัชนีลบ
ดัชนีลบหมายถึงการเริ่มนับจากด้านท้าย -1 หมายถึงรายการสุดท้าย -2 หมายถึงรายการรองสุดท้าย

![List negative indexing](./images/list_negative_indexing.png)
```py
fruits = ['banana', 'orange', 'mango', 'lemon']
first_fruit = fruits[-4]
last_fruit = fruits[-1]
second_last = fruits[-2]
print(first_fruit)      # banana
print(last_fruit)       # lemon
print(second_last)      # mango
```
### การแกะ (Unpacking) รายการในลิสต์
```py
lst = ['item','item2','item3', 'item4', 'item5']
first_item, second_item, third_item, *rest = lst
print(first_item)     # item1
print(second_item)    # item1
print(third_item)     # item2
print(rest)           # ['item4', 'item5']

```
```py
# First Example
fruits = ['banana', 'orange', 'mango', 'lemon','lime','apple']
first_fruit, second_fruit, third_fruit, *rest = lst
print(first_fruit)     # banana
print(second_fruit)    # orange
print(third_fruit)     # mango
print(rest)           # ['lemon','lime','apple']
# Second Example about unpacking list
first, second, third,*rest, tenth = [1,2,3,4,5,6,7,8,9,10]
print(first)
print(second)
print(third)
print(rest)
print(tenth)
# Third Example about unpacking list
countries = ['Germany', 'France','Belgium','Sweden','Denmark','Finland','Norway','Iceland','Estonia']
gr, fr, bg, sw, *scandic, es = countries
print(gr)
print(fr)
print(bg)
print(sw)
print(scandic)
print(es)
```
### การตัด (Slicing) รายการจากลิสต์
* ดัชนีบวก: เราสามารถระบุช่วงของดัชนีบวกโดยระบุจุดเริ่มต้นและจุดสิ้นสุด ค่าที่คืนกลับมาจะเป็นลิสต์ใหม่
```py
fruits = ['banana', 'orange', 'mango', 'lemon'] 
all_fruits = fruits[0:4] # it returns all the fruits
# this is also give the same result as the above
all_fruits = fruits[0:] # if we don't set where to stop it takes all the rest
orange_and_mango = fruits[1:3] # it does not include the end index
orange_mango_lemon = fruits[1:]
```
* ดัชนีลบ: เราสามารถระบุช่วงของดัชนีลบโดยระบุจุดเริ่มต้นและจุดสิ้นสุด ค่าที่คืนกลับมาจะเป็นลิสต์ใหม่
```py
fruits = ['banana', 'orange', 'mango', 'lemon'] 
all_fruits = fruits[-4:] # it returns all the fruits
# this is also give the same result as the above
orange_and_mango = fruits[-3:-1] # it does not include the end index
orange_mango_lemon = fruits[-3:]
```
### การแก้ไขลิสต์
ลิสต์เป็นกลุ่มข้อมูลที่มีลำดับซึ่งสามารถแก้ไขได้ (mutable) มาลองแก้ไขลิสต์ผลไม้กัน
```py
fruits = ['banana', 'orange', 'mango', 'lemon'] 
fruits[0] = 'Avocado' 
print(fruits)       #  ['avocado', 'orange', 'mango', 'lemon']
fruits[1] = 'apple'
print(fruits)       #  ['avocado', 'apple', 'mango', 'lemon']
last_index = len(fruits)
fruits[last_index] = 'lime'
print(fruits)        #  ['avocado', 'apple', 'mango', 'lime']
```
### การตรวจสอบรายการในลิสต์
```py
fruits = ['banana', 'orange', 'mango', 'lemon']
does_exist = 'banana' in fruits
print(does_exist)  # True
does_exist = 'lime' in fruits
print(does_exist)  # False
```
### การเพิ่มรายการในลิสต์
หากต้องการเพิ่มรายการที่ท้ายลิสต์ที่มีอยู่แล้วเราใช้เมธอด
```py
# syntax
lst = list()
lst.append(item)
```
```py
fruits = ['banana', 'orange', 'mango', 'lemon']
fruits.append('apple')
print(fruits)           # ['banana', 'orange', 'mango', 'lemon', 'apple']
fruits.append('lime')   # ['banana', 'orange', 'mango', 'lemon', 'apple', 'lime']
print(fruits)
```
### การแทรกรายการเข้าไปในลิสต์
ใช้เมธอด insert() เพื่อแทรกรายการเดียวที่ดัชนีที่ระบุในลิสต์ โปรดสังเกตว่ารายการอื่น ๆ จะถูกเลื่อนไปทางขวา
```py
# syntax
lst = ['item1', 'item2']
lst.insert(index, item)
```
```py
fruits = ['banana', 'orange', 'mango', 'lemon']
fruits.insert(2, 'apple') # insert apple between orange and mango
print(fruits)           # ['banana', 'orange', 'apple', 'mango', 'lemon']
fruits.insert(3, 'lime')   # ['banana', 'orange', 'apple', 'mango', 'lime','lemon']
print(fruits)
```
### การลบรายการออกจากลิสต์
เมธอด remove ลบรายการที่ระบุออกจากลิสต์
```py
# syntax
lst = ['item1', 'item2']
lst.remove(item)
```
```py
fruits = ['banana', 'orange', 'mango', 'lemon']
fruits.remove('banana')
print(fruits)  # ['orange', 'mango', 'lemon']
fruits.remove('lemon')
print(fruits)  # ['orange', 'mango']
```
### การลบรายการโดยใช้ pop
เมธอด pop() ลบรายการที่ดัชนีที่ระบุ (หรือรายการสุดท้ายถ้าไม่ระบุดัชนี):
```py
# syntax
lst = ['item1', 'item2']
lst.pop()       # last item
lst.pop(index)
```
```py
fruits = ['banana', 'orange', 'mango', 'lemon']
fruits.pop()     
print(fruits)       # ['banana', 'orange', 'mango']

fruits.remove(0)     
print(fruits)       # ['orange', 'mango']    
```
### การลบรายการโดยใช้ del
คีย์เวิร์ด del ลบรายการที่ดัชนีที่ระบุ และยังสามารถใช้ลบลิสต์ทั้งหมดได้เช่นกัน

```py
# syntax
lst = ['item1', 'item2']
del lst[index] # only a single item
del lst        # to delete the list completely
```
```py
fruits = ['banana', 'orange', 'mango', 'lemon']
del fruits[0]     
print(fruits)       # ['orange', 'mango', 'lemon']

del fruits[1]     
print(fruits)       # ['orange', 'lemon']
del fruits
print(fruits)       # This should give: NameError: name 'fruits' is not defined
```
### การล้างรายการในลิสต์
เมธอด clear() ล้างลิสต์ให้ว่างเปล่า:
```py
# syntax
lst = ['item1', 'item2']
lst.clear()
```
```py
fruits = ['banana', 'orange', 'mango', 'lemon']
fruits.clear()     
print(fruits)       # []   
```
### การคัดลอกลิสต์
เป็นไปได้ที่จะคัดลอกลิสต์โดยกำหนดค่าใหม่ให้กับตัวแปรใหม่ด้วยวิธี list2 = list1 ตอนนี้ list2 เป็นการอ้างอิงถึง list1 การเปลี่ยนแปลงใด ๆ ที่เราทำใน list2 จะแก้ไขต้นฉบับ list1 ด้วย แต่มีหลายกรณีที่เราไม่ต้องการแก้ไขต้นฉบับ แต่ต้องการมีสำเนาที่แยกต่างหาก วิธีหนึ่งในการหลีกเลี่ยงปัญหาข้างต้นคือการใช้ *copy()*
```py
# syntax
lst = ['item1', 'item2']
lst_copy = lst.copy()
```
```py
fruits = ['banana', 'orange', 'mango', 'lemon']
fruits_copy = fruits.copy()     
print(fruits_copy)       # ['banana', 'orange', 'mango', 'lemon']
```
### การรวมลิสต์เข้าด้วยกัน
มีหลายวิธีในการรวมหรือต่อลิสต์ตั้งแต่สองลิสต์ขึ้นไปเข้าด้วยกันใน Python

* เครื่องหมายบวก (+)
```py
# syntax
list3 = list1 +list2
```
```py
positive_numbers = [1, 2, 3,4,5]
zero = [0]
negative_numbers = [-5,-4,-3,-2,-1]
integers = negative_numbers + zero + positive_numbers
print(integers)
fruits = ['banana', 'orange', 'mango', 'lemon']
vegetables = ['Tomato', 'Potato', 'Cabbage','Onion', 'Carrot'] 
fruits_and_vegetables = fruits + vegetables
print(fruits_and_vegetables )

```
```py
# output
[-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5]
['banana', 'orange', 'mango', 'lemon', 'Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot']
```
  * การรวมโดยใช้เมธอด extend()

```py
# syntax
lst1 = ['item1', 'item2']
lst2 = ['item3', 'item4','item5']
list1.extend(list2)
```
```py
num1 = [0, 1, 2, 3]
num2= [4, 5,6]
num1.extend(num2)
print('Numbers:', num1)
negative_numbers = [-5,-4,-3,-2,-1]
positive_numbers = [1, 2, 3,4,5]
zero = [0]

negative_numbers.extend(zero)
negative_numbers.extend(positive_numbers)
print('Integers:', negative_numbers)
fruits = ['banana', 'orange', 'mango', 'lemon']
vegetables = ['Tomato', 'Potato', 'Cabbage','Onion', 'Carrot'] 
fruits.extend(vegetables)
print('Fruits and vegetables:', fruits )

```
```py
Numbers: [0, 1, 2, 3, 4, 5, 6]
Integers: [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5]
Fruits and vegetables: ['banana', 'orange', 'mango', 'lemon', 'Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot']
```

### การนับจำนวนรายการในลิสต์
เมธอด count() คืนค่าจำนวนครั้งที่รายการปรากฏในลิสต์:
  ```py
  # syntax
  lst = ['item1', 'item2']
  lst.count(item) 
  ```
  ```py
  fruits = ['banana', 'orange', 'mango', 'lemon']
  print(fruits.count('orange'))   # 1
  ages = [22, 19, 24, 25, 26, 24, 25, 24]
  print(ages.count(24))           # 3
  ```
### การหาดัชนีของรายการ
เมธอด count() คืนค่าดัชนีของรายการในลิสต์:
  ```py
  # syntax
  lst = ['item1', 'item2']
  lst.index(item) 
  ```
  ```py
  fruits = ['banana', 'orange', 'mango', 'lemon']
  print(fruits.index('orange'))   # 1
  ages = [22, 19, 24, 25, 26, 24, 25, 24]
  print(ages.index(24))           # 2, the first occurrence
  ```
### การกลับด้านลิสต์
เมธอด reverse() กลับลำดับของลิสต์
  ```py
  # syntax
  lst = ['item1', 'item2']
  lst.reverse() 

  ```
  ```py
  fruits = ['banana', 'orange', 'mango', 'lemon']
  fruits.reverse()
  print(fruits.reverse())  
  ages = [22, 19, 24, 25, 26, 24, 25, 24]
  ages.reverse()
  print(ages.reverse())         
  ```
  ```py
  ['lemon', 'mango', 'orange', 'banana']
  [24, 25, 24, 26, 25, 24, 19, 22]
  ```
### การเรียงลำดับรายการในลิสต์
เพื่อเรียงลำดับลิสต์เราสามารถใช้เมธอด sort() หรือฟังก์ชันในตัว sorted() เมธอด sort() จัดเรียงรายการในลิสต์ใหม่ตามลำดับจากน้อยไปมากและแก้ไขลิสต์ต้นฉบับ ถ้า reverse เท่ากับ true จะจัดเรียงจากมากไปน้อย
* sort():
  ```py
  # syntax
  lst = ['item1', 'item2']
  lst.sort()                # ascending
  lst.sort(reverse=True)    # descending
  ```
  **ตัวอย่าง:**

  ```py
  fruits = ['banana', 'orange', 'mango', 'lemon']
  fruits.sort()
  print(fruits) 
  fruits.sort(reverse=True)
  print(fruits)
  ages = [22, 19, 24, 25, 26, 24, 25, 24]
  ages.sort()
  print(ages) 
  ages.sort(reverse=True)
  print(ages)           
  ```
  ```sh
  ['banana', 'lemon', 'mango', 'orange']
  ['orange', 'mango', 'lemon', 'banana']
  [19, 22, 24, 24, 24, 25, 25, 26]
  [26, 25, 25, 24, 24, 24, 22, 19]
  ```
  sorted(): คืนค่าลิสต์ที่จัดเรียงแล้วโดยไม่แก้ไขต้นฉบับ
  **ตัวอย่าง:**
   ```py
  fruits = ['banana', 'orange', 'mango', 'lemon']
  fruits = sorted(fruits)
  print(fruits)     # ['banana', 'lemon', 'mango', 'orange']
  # Reverse order
  fruits = ['banana', 'orange', 'mango', 'lemon']
  fruits = sorted(fruits,reverse=True)
  print(fruits)     # ['orange', 'mango', 'lemon', 'banana']          
  ```
  
## 💻 แบบฝึกหัด: วันที่ 5
1. ประกาศลิสต์ว่างเปล่า
2. ประกาศลิสต์ที่มีรายการมากกว่า 5 รายการ
3. หาความยาวของลิสต์ของคุณ
4. รับรายการแรก รายการกลาง และรายการสุดท้ายของลิสต์
5. ประกาศลิสต์ชื่อ mixed_data_types ใส่ (ชื่อ, อายุ, ส่วนสูง, สถานภาพสมรส, ที่อยู่) ของคุณลงไป
6. ประกาศตัวแปรลิสต์ชื่อ it_companies และกำหนดค่าเริ่มต้นเป็น Facebook, Google, Microsoft, Apple, IBM, Oracle และ Amazon
7. พิมพ์ลิสต์โดยใช้ *print()*
8. พิมพ์จำนวนบริษัทในลิสต์
9. พิมพ์บริษัทแรก บริษัทกลาง และบริษัทสุดท้าย
10. พิมพ์การแก้ไขบริษัทใดบริษัทหนึ่ง
11. เพิ่มบริษัท IT เข้าไปใน it_companies
12. แทรกบริษัท IT ตรงกลางของลิสต์บริษัท
13. เปลี่ยนรายการหนึ่งใน it_companies ให้เป็นตัวพิมพ์ใหญ่
14. รวม it_companies เข้าด้วยกันด้วยสตริง '#;&nbsp; '
15. ตรวจสอบว่ามีบริษัทหนึ่ง ๆ อยู่ในลิสต์ it_companies หรือไม่
16. เรียงลำดับลิสต์โดยใช้เมธอด sort()
17. กลับลำดับลิสต์แบบมากไปน้อยโดยใช้เมธอด reverse()
18. ตัด (slice) เอาบริษัท 3 อันดับแรกออกจากลิสต์
19. ตัด (slice) เอาบริษัท 3 อันดับสุดท้ายออกจากลิสต์
20. ตัด (slice) เอาบริษัท IT ที่อยู่ตรงกลางออกจากลิสต์
21. ลบบริษัท IT อันดับแรกออกจากลิสต์
22. ลบบริษัท IT ที่อยู่ตรงกลางออกจากลิสต์
23. ลบบริษัท IT อันดับสุดท้ายออกจากลิสต์
24. ลบรายการบริษัท IT ทั้งหมด
25. ทำลายลิสต์บริษัท IT
26. รวมลิสต์ต่อไปนี้เข้าด้วยกัน:
    ```py
    front_end = ['HTML', 'CSS', 'JS', 'React', 'Redux']
    back_end = ['Node','Express', 'MongoDB']
    ```
27. หลังจากรวมลิสต์ในข้อ 26 แล้ว ให้คัดลอกลิสต์ที่รวมแล้วและกำหนดให้กับตัวแปร full_stack จากนั้นแทรก Python และ SQL ต่อจาก Redux
28. ต่อไปนี้คือลิสต์อายุของนักเรียน 10 คน:
```sh
ages = [19, 22, 19, 24, 20, 25, 26, 24, 25, 24]
```
  * เรียงลำดับลิสต์แล้วหาอายุน้อยสุดและมากสุด
  * บวกอายุน้อยสุดกับอายุมากสุด
  * หาค่ามัธยฐานของอายุ (รายการกลางหนึ่งรายการหรือสองรายการกลางหารด้วยสอง)
  * หาค่าเฉลี่ยของอายุ (ผลรวมทุกรายการหารด้วยจำนวนรายการ)
  * หาพิสัยของอายุ (มากสุดลบน้อยสุด)
  * เปรียบเทียบค่าของ (น้อยสุด - ค่าเฉลี่ย) กับ (มากสุด - ค่าเฉลี่ย) โดยใช้เมธอด *abs()*
29. หาประเทศที่อยู่ตรงกลางใน[ลิสต์ประเทศ](day/tree/master/data/countries.py)
30. แบ่งลิสต์ประเทศออกเป็นสองลิสต์เท่า ๆ กัน ถ้าเป็นจำนวนคู่ แต่ถ้าไม่ใช่ ให้ครึ่งแรกมีประเทศมากกว่าหนึ่งประเทศ
31. ['China', 'Russia', 'USA', 'Finland', 'Sweden', 'Norway', 'Denmark'] จงแกะเอาสามประเทศแรกออกมา และที่เหลือเป็นกลุ่มประเทศสแกนดิเนเวีย

# วันที่ 6:
## ทูเพิล
ทูเพิลคือกลุ่มของข้อมูลต่างชนิดกันที่มีลำดับและไม่สามารถแก้ไขได้ (immutable) ทูเพิลเขียนด้วยวงเล็บกลม, () เมื่อสร้างทูเพิลแล้ว เราไม่สามารถเปลี่ยนแปลงค่าของมันได้ เราไม่สามารถเพิ่ม แทรก หรือลบรายการในทูเพิลได้ เพราะมันไม่สามารถแก้ไขได้ (mutable) ต่างจากลิสต์ ทูเพิลมีเมธอดน้อยมาก เมธอดที่เกี่ยวข้องกับทูเพิล:
* tuple(): สำหรับสร้างทูเพิลว่างเปล่า
* count(): สำหรับนับจำนวนรายการที่ระบุในทูเพิล
* index(): สำหรับหาดัชนีของรายการที่ระบุในทูเพิล
* ตัวดำเนินการ +: สำหรับรวมทูเพิลตั้งแต่สองอันขึ้นไปและสร้างทูเพิลใหม่
### การสร้างทูเพิล

* ทูเพิลว่างเปล่า: การสร้างทูเพิลว่างเปล่า
  ```py
  # syntax
  empty_tuple = () 
  # or using the tuple constructor
  empty_tuple = tuple()
  ```
* ทูเพิลที่มีค่าเริ่มต้น
  ```py
  # syntax
  tpl = ('item1', 'item2','item3')
  ```
  * 
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  ```
### ความยาวของทูเพิล
เราใช้เมธอด *len()* เพื่อหาความยาวของทูเพิล
  ```py
  # syntax
  tpl = ('item1', 'item2', 'item3')
  len(tpl)
  ```
### การเข้าถึงรายการในทูเพิล
* ดัชนีบวก
เช่นเดียวกับชนิดข้อมูลลิสต์ เราใช้ดัชนีบวกหรือลบเพื่อเข้าถึงรายการในทูเพิล
![Accessing tuple items](images/tuples_index.png)

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3')
  first_item = tpl[0]
  second_item = tpl[1]
  ```
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  first_fruit = fruits[0]
  second_fruit = fruits[1]
  last_index =len(fruits) - 1
  last_fruit = fruits[las_index]
  ```
* ดัชนีลบ
ดัชนีลบหมายถึงการเริ่มนับจากด้านท้าย -1 หมายถึงรายการสุดท้าย -2 หมายถึงรายการรองสุดท้าย และดัชนีลบที่เท่ากับความยาวของลิสต์หมายถึงรายการแรก
![Tuple Negative indexing](images/tuple_negative_indexing.png)
  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  first_item = tpl[-4]
  second_item = tpl[-3]
  ```
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  first_fruit = fruits[-4]
  second_fruit = fruits[-3]
  last_fruit = fruits[-1]
  ```
### การตัด (Slicing) ทูเพิล
เราสามารถตัดทูเพิลย่อยออกมาได้โดยระบุช่วงของดัชนีว่าจะเริ่มต้นและสิ้นสุดตรงไหนในทูเพิล ค่าที่คืนกลับมาจะเป็นทูเพิลใหม่ที่มีรายการตามที่ระบุ

* ช่วงของดัชนีบวก

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  all_items = tpl[0:4]         # all items
  all_items = tpl[0:]         # all items
  middle_two_items = tpl[1:3]  # does not include item at index 3
  ```
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  all_fruits = fruits[0:4]    # all items
  all_fruits= fruits[0:]      # all items
  orange_mango = fruits[1:3]  # doesn't include item at index 3
  orange_to_the_rest = fruits[1:]
  ```

* ช่วงของดัชนีลบ

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  all_items = tpl[-4:]         # all items
  middle_two_items = tpl[-3:-1]  # does not include item at index 3
  ```
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  all_fruits = fruits[-4:]    # all items
  orange_mango = fruits[-3:-1]  # doesn't include item at index 3
  orange_to_the_rest = fruits[-3:]
  ```
### การเปลี่ยนทูเพิลเป็นลิสต์
เราสามารถเปลี่ยนทูเพิลเป็นลิสต์และลิสต์เป็นทูเพิลได้ ทูเพิลไม่สามารถแก้ไขได้ (immutable) ถ้าเราต้องการแก้ไขทูเพิล เราควรเปลี่ยนเป็นลิสต์ก่อน
  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  lst = list(tpl)
  ```
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  fruits = list(fruits)
  fruits[0] = 'apple'
  print(fruits)     # ['apple', 'orange', 'mango', 'lemon']
  fruits = tuple(fruits)
  print(fruits)     # ('apple', 'orange', 'mango', 'lemon')
  ```
### การตรวจสอบรายการในลิสต์
เราสามารถตรวจสอบได้ว่ารายการหนึ่งมีอยู่ในลิสต์หรือไม่โดยใช้ *in* ซึ่งจะคืนค่าบูลีน
  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  'item2' in tpl # True
  ```
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  'orange' in fruits # True
  'apple' in fruits # False
  fruits[0] = 'apple'
  ```
### การรวมทูเพิลเข้าด้วยกัน
เราสามารถรวมทูเพิลตั้งแต่สองอันขึ้นไปเข้าด้วยกันโดยใช้ตัวดำเนินการ +
  ```py
  # syntax
  tpl1 = ('item1', 'item2', 'item3')
  tpl2 = ('item4', 'item5','item6')
  tpl3 = tpl1 + tpl2
  ```
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')                    
  vegetables = ('Tomato', 'Potato', 'Cabbage','Onion', 'Carrot')
  fruits_and_vegetables = fruits + vegetables 
  ```
### การลบทูเพิล
เราไม่สามารถลบรายการเดียวในทูเพิลได้ แต่สามารถลบทูเพิลทั้งหมดได้โดยใช้ *del*
  ```py
  # syntax
  tpl1 = ('item1', 'item2', 'item3')
  del tpl1

  ```
  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon') 
  del fruits                  
  ```


## 💻 แบบฝึกหัด: วันที่ 6
1. สร้างทูเพิลว่างเปล่า
2. สร้างทูเพิลที่มีชื่อพี่น้องผู้หญิงและพี่น้องผู้ชายของคุณ
3. รวมทูเพิลพี่น้องผู้ชายและพี่น้องผู้หญิงเข้าด้วยกัน แล้วกำหนดให้กับตัวแปร siblings
4. คุณมีพี่น้องกี่คน ?
5. แก้ไขทูเพิล siblings โดยเพิ่มชื่อพ่อและแม่ของคุณ แล้วกำหนดให้กับตัวแปร family_members
6. แกะ (unpack) siblings และ parents ออกจาก family_members
7. สร้างทูเพิลผลไม้ ผัก และผลิตภัณฑ์จากสัตว์ รวมทั้งสามทูเพิลเข้าด้วยกันแล้วกำหนดให้กับตัวแปรชื่อ food_stuff
8. ตัด (slice) เอารายการกลางออกจากลิสต์ food_staff
9. ตัด (slice) เอาสามรายการแรกและสามรายการสุดท้ายออกจากลิสต์ food_staff
10. ลบลิสต์ food_staff ทั้งหมด
11. ตรวจสอบว่ารายการหนึ่งมีอยู่ในทูเพิลหรือไม่:
* ตรวจสอบว่า 'Estonia' เป็นประเทศแถบนอร์ดิกหรือไม่
* ตรวจสอบว่า 'Iceland' เป็นประเทศแถบนอร์ดิกหรือไม่
  ```py
  nordic_countries = ('Denmark', 'Finland','Iceland', 'Norway', 'Sweden')
  ```

[<< ตอนที่ 1](day1-3.md) | [ตอนที่ 3 >>](day7-9.md)
