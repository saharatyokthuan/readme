

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

- [วันที่ 1](#day1)
  - [welcome](#welcome)
  - [บทนำ](#บทนำ)
  - [ทำไมต้อง Python ?](#ทำไมต้อง)
  - [การตั้งค่าสภาพแวดล้อม](#environment-setup)
    - [การติดตั้ง Python](#installing-python)
    - [Python Shell](#python-shell)
    - [การติดตั้ง Visual Studio Code](#installing-visual-studio-code)
      - [วิธีใช้งาน visual studio code](#how-to-use-visual-studio-code)
  - [พื้นฐาน Python](#basic-python)
    - [ไวยากรณ์ของ Python](#python-syntax)
    - [การเว้นวรรค (Indentation) ใน Python](#python-indentation)
    - [คอมเมนต์](#comment)
    - [ชนิดข้อมูล](#data-types)
      - [ตัวเลข](#number)
      - [สตริง](#string)
      - [บูลีน](#booleans)
      - [ลิสต์](#list)
      - [ดิกชันนารี](#dictionary)
      - [ทูเพิล](#tuple)
      - [เซ็ต](#set)
    - [การตรวจสอบชนิดข้อมูล](#checking-data-types)
    - [ไฟล์ Python](#python-file)
  - [💻 แบบฝึกหัด - วันที่ 1](#%f0%9f%92%bb-exercises---day-1)
- [📘 วันที่ 2](#%f0%9f%93%98-day-2)
  - [ฟังก์ชันในตัว (Built in functions)](#built-in-functions)
  - [ตัวแปร](#variables)
  - [ชนิดข้อมูล](#data-types-1)
  - [การตรวจสอบชนิดข้อมูลและการแปลงชนิดข้อมูล](#checking-data-types-and-casting)
  - [ตัวเลข](#number-1)
  - [💻 แบบฝึกหัด - วันที่ 2](#%f0%9f%92%bb-exercises---day-2)
- [📘 วันที่ 3](#%f0%9f%93%98-day-3)
  - [บูลีน](#boolean)
  - [ตัวดำเนินการ (Operators):](#operators)
    - [ตัวดำเนินการกำหนดค่า (Assignment Operators):](#assignment-operators)
    - [ตัวดำเนินการทางคณิตศาสตร์ (Arithmetic Operators):](#arithmetic-operators)
    - [ตัวดำเนินการเปรียบเทียบ (Comparison Operators)](#comparison-operators)
    - [ตัวดำเนินการทางตรรกะ (Logical Operators)](#logical-operators)
  - [💻 แบบฝึกหัด - วันที่ 3](#%f0%9f%92%bb-exercises---day-3)

# <a id="day1"> วันที่ 1 </a>

## <a id="welcome">ยินดีต้อนรับ</a>

**ขอแสดงความยินดี** ที่ตัดสินใจเข้าร่วมความท้าทาย **_30 วันกับ Python_** ในความท้าทายนี้คุณจะได้เรียนรู้ทุกสิ่งที่จำเป็นในการเป็นโปรแกรมเมอร์ Python รวมถึงแนวคิดพื้นฐานของการเขียนโปรแกรมทั้งหมด เมื่อจบความท้าทายนี้ คุณจะได้รับใบประกาศนียบัตร **_30DaysOfPython_**

[เข้าร่วมช่อง telegram เพื่อขอความช่วยเหลือ](https://t.me/ThirtyDaysOfPython)

## บทนำ

Python เป็นภาษาโปรแกรมมิงระดับสูงสำหรับการเขียนโปรแกรมทั่วไป เป็นซอฟต์แวร์โอเพนซอร์ส ความท้าทาย 30 วันนี้จะช่วยให้คุณเรียนรู้ Python เวอร์ชันล่าสุด นั่นคือ Python 3 ทีละขั้นตอน เนื้อหาถูกแบ่งออกเป็น 30 วัน โดยแต่ละวันจะมีหัวข้อหลายหัวข้อพร้อมคำอธิบายที่เข้าใจง่าย ตัวอย่างจากสถานการณ์จริง และแบบฝึกหัดลงมือทำมากมาย

ความท้าทายนี้ออกแบบมาสำหรับทั้งผู้เริ่มต้นและมืออาชีพที่ต้องการเรียนรู้ภาษาโปรแกรมมิง Python

## ทำไมต้อง Python ?

Python เป็นภาษาโปรแกรมมิงที่ใกล้เคียงกับภาษามนุษย์มาก จึงเรียนรู้และใช้งานได้ง่าย
Python ถูกใช้งานในหลากหลายอุตสาหกรรม รวมถึง Google มันถูกนำไปใช้พัฒนาเว็บแอปพลิเคชัน เดสก์ท็อปแอปพลิเคชัน งานดูแลระบบ และไลบรารีด้าน machine learning Python เป็นภาษาที่ได้รับความนิยมอย่างสูงในวงการ data science และ machine learning ผมหวังว่าเหตุผลเหล่านี้จะเพียงพอที่จะทำให้คุณเริ่มเรียน Python ได้แล้ว Python กำลังครองโลก และคุณควรจะเริ่มเรียนมันก่อนที่มันจะครองคุณ

## การตั้งค่าสภาพแวดล้อม

### การติดตั้ง Python

หากต้องการรันสคริปต์ Python คุณต้องติดตั้ง Python ก่อน มา[ดาวน์โหลด](https://www.python.org/) Python กัน
หากคุณใช้ Windows ให้คลิกปุ่มที่วงกลมสีแดงไว้

[![ติดตั้งบน Windows](./images/installing_on_windows.png)](https://www.python.org/)

หากคุณใช้ macOS ให้คลิกปุ่มที่วงกลมสีแดงไว้

[![ติดตั้งบน Windows](./images/installing_on_macOS.png)](https://www.python.org/)

หากต้องการตรวจสอบว่าติดตั้ง Python แล้วหรือยัง ให้พิมพ์คำสั่งต่อไปนี้ในเทอร์มินัลของเครื่อง

```shell
python --version
```

![เวอร์ชันของ Python](./images/python_versio.png)

จากเทอร์มินัลจะเห็นว่าตอนนี้ผมใช้ _python เวอร์ชัน 3.7.5_ อยู่ หากคุณสามารถเห็นเวอร์ชันของ Python ได้ ยอดเยี่ยมมาก แสดงว่าติดตั้ง Python บนเครื่องของคุณเรียบร้อยแล้ว ไปยังหัวข้อถัดไปกันเลย

### Python Shell

Python เป็นภาษาสคริปต์แบบ interpreted จึงไม่จำเป็นต้องคอมไพล์ ซึ่งหมายความว่ามันจะรันโค้ดทีละบรรทัด Python มาพร้อมกับ _Python Shell (Python Interactive Shell)_ ซึ่งใช้สำหรับรันคำสั่ง Python ทีละคำสั่งและดูผลลัพธ์

Python Shell จะรอรับโค้ด Python จากผู้ใช้ เมื่อคุณพิมพ์โค้ดเข้าไป มันจะตีความโค้ดนั้นและแสดงผลลัพธ์ในบรรทัดถัดไป
เปิดเทอร์มินัลหรือ command prompt (cmd) แล้วพิมพ์:

```shell
python
```

![Python Scripting Shell](images/opening_python_shell.png)

Python interactive shell จะเปิดขึ้นและรอให้คุณพิมพ์โค้ด Python คุณจะพิมพ์สคริปต์ Python ต่อจากสัญลักษณ์ >>> แล้วกด Enter
มาลองเขียนสคริปต์แรกของเราบน python scripting shell กัน

![Python script on python shell](images/adding_on_python_shell.png)

เยี่ยมมาก คุณเขียนสคริปต์ Python แรกของคุณบน python interactive shell แล้ว แล้วเราจะปิด shell นี้อย่างไร ?
หากต้องการปิด shell ให้พิมพ์คำสั่ง **exit()** ต่อจากสัญลักษณ์ >> แล้วกด Enter

![Exit from python shell](images/exit_from_shell.png)

ตอนนี้คุณรู้แล้วว่าจะเปิดและปิด python interactive shell อย่างไร

Python จะให้ผลลัพธ์แก่คุณถ้าคุณเขียนสคริปต์ที่ Python เข้าใจ แต่ถ้าไม่เข้าใจ มันจะคืนค่า error กลับมา มาลองทำผิดพลาดโดยตั้งใจดูว่า Python จะคืนอะไรกลับมา

![Invalid Syntax Error](./images/invalid_syntax_error.png)

จาก error ที่คืนกลับมาจะเห็นว่า Python ฉลาดพอที่จะรู้ว่าเราทำผิดพลาดตรงไหน ซึ่งก็คือ _Syntax Error: invalid syntax_ การใช้ x เป็นเครื่องหมายคูณใน Python ถือเป็น syntax error เพราะ (x) ไม่ใช่ไวยากรณ์ที่ถูกต้องใน Python แทนที่จะใช้ (**x**) เราใช้เครื่องหมายดอกจัน (*) สำหรับการคูณ error ที่คืนกลับมาบอกอย่างชัดเจนว่าต้องแก้ไขอะไร
กระบวนการค้นหาและแก้ไข error ในโปรแกรมเรียกว่า *การดีบัก (debugging)* มาดีบักกันโดยเปลี่ยน * แทนที่ **x**

![Fixing Syntax Error](./images/fixing_syntax_error.png)

บั๊กของเราถูกแก้ไขแล้ว โค้ดรันได้และเราได้ผลลัพธ์ตามที่คาดหวัง ในฐานะโปรแกรมเมอร์ คุณจะพบ error ลักษณะนี้ทุกวัน การรู้วิธีดีบักเป็นสิ่งที่ดี การจะดีบักเก่งได้ คุณควรเข้าใจว่ากำลังเจอ error ประเภทไหน เช่น SyntaxError, IndexError, ModuleNotFoundError, KeyError, ImportError ฯลฯ เราจะพูดถึง **_ชนิดของ error_** ต่าง ๆ ใน Python เพิ่มเติมในหัวข้อถัดไป

มาฝึกใช้ python interactive shell กันต่อ ไปที่เทอร์มินัลหรือ command prompt แล้วพิมพ์คำว่า **python**

![Python Scripting Shell](images/opening_python_shell.png)

Python interactive shell เปิดขึ้นแล้ว มาลองทำคณิตศาสตร์พื้นฐาน (บวก ลบ คูณ หาร มอดุโล ยกกำลัง) กัน
มาคำนวณคณิตศาสตร์กันก่อนที่จะเขียนโค้ด Python:

- 2 + 3 = 5
- 3 - 2 = 1
- 3 \* 2 = 6
- 3 / 2 = 1.5
- 3 ^ 2 = 3 x 3 = 9

ใน Python เรามีการดำเนินการเพิ่มเติมดังนี้:

- 3 % 2 = 1 => หมายถึงการหาเศษที่เหลือจากการหาร
- 3 // 2 = 1 => หมายถึงการหารแบบตัดเศษทิ้ง

มาเปลี่ยนนิพจน์ทางคณิตศาสตร์ข้างต้นให้เป็นโค้ดกัน python shell เปิดอยู่แล้ว มาเขียนคอมเมนต์ไว้ที่จุดเริ่มต้นของ shell กัน
_คอมเมนต์_ คือส่วนของโค้ดที่ Python ไม่รัน เราจึงสามารถทิ้งข้อความไว้ในโค้ดเพื่อให้โค้ดอ่านง่ายขึ้นได้ Python จะไม่รันส่วนที่เป็นคอมเมนต์ คอมเมนต์ใน Python เริ่มต้นด้วยสัญลักษณ์ hash (#)
นี่คือวิธีเขียนคอมเมนต์ใน Python

```shell
 # comment starts with hash
 # this is a python comment itself because it starts with a (#) symbol
```

![Maths on python shell](./images/maths_on_python_shell.png)

ก่อนไปหัวข้อถัดไป มาฝึกใช้ python interactive shell กันต่ออีกหน่อย ปิด shell ที่เปิดอยู่โดยพิมพ์ _exit()_ แล้วเปิดใหม่อีกครั้ง มาฝึกวิธีเขียนข้อความบน python shell กัน

![Writing String on python shell](images/writing_string_on_shell.png)

### การติดตั้ง Visual Studio Code

python interactive shell เหมาะสำหรับลองและทดสอบโค้ดสคริปต์เล็ก ๆ แต่ไม่เหมาะกับโปรเจกต์ขนาดใหญ่ ในสภาพแวดล้อมการทำงานจริง นักพัฒนาใช้ code editor ต่าง ๆ ในการเขียนโค้ด ในความท้าทาย 30 วันกับ Python นี้เราจะใช้ visual studio code ซึ่งเป็น text editor แบบโอเพนซอร์สที่ได้รับความนิยมมาก ผมเป็นแฟนของ vscode และแนะนำให้[ดาวน์โหลด](https://code.visualstudio.com/) visual studio code แต่ถ้าคุณชอบ editor ตัวอื่น ก็ใช้ตัวที่คุณมีอยู่ได้เลย

[![Visual Studio Code](./images/vscode.png)](https://code.visualstudio.com/)

หากคุณติดตั้ง visual studio code แล้ว มาดูวิธีใช้งานกัน

#### วิธีใช้งาน visual studio code

เปิด visual studio code โดยดับเบิลคลิกที่ไอคอน visual studio เมื่อเปิดขึ้นมาแล้วคุณจะเห็นหน้าตาแบบนี้ ลองโต้ตอบกับไอคอนที่มีป้ายกำกับไว้ดู

![Visual studio Code](images/vscode_ui.png)

สร้างโฟลเดอร์ชื่อ 30DaysOfPython บนเดสก์ท็อปของคุณ จากนั้นเปิดโฟลเดอร์นี้ด้วย visual studio code

![Opening Project on Visual studio](./images/how_to_open_project_on_vscode.png)

![Opening a project](./images/opening_project.png)

หลังจากเปิดแล้ว คุณสามารถสร้างไฟล์และโฟลเดอร์ภายในไดเรกทอรีโปรเจกต์ของคุณ ซึ่งก็คือ 30DaysOfPython ได้ ดังที่เห็นด้านล่าง ผมได้สร้างไฟล์แรกชื่อ helloworld.py คุณก็สามารถทำแบบเดียวกันได้

![Creating a python file](./images/helloworld.png)

หลังจากเขียนโค้ดกันมาทั้งวัน คุณอยากปิด code editor แล้วใช่ไหม ? นี่คือวิธีปิดโปรเจกต์ที่เปิดอยู่

![Closing project](./images/closing_opened_project.png)

ขอแสดงความยินดี คุณตั้งค่าสภาพแวดล้อมการพัฒนาเสร็จเรียบร้อยแล้ว มาเริ่มเขียนโค้ดกันเลย

## พื้นฐาน Python

### ไวยากรณ์ของ Python

สคริปต์ Python สามารถเขียนบน python interactive shell หรือบน code editor ก็ได้ ไฟล์ Python มีนามสกุล .py

### การเว้นวรรค (Indentation) ใน Python

Indentation คือช่องว่างในข้อความ หลายภาษาใช้ indentation เพื่อเพิ่มความอ่านง่ายของโค้ด แต่ Python ใช้ indentation เพื่อสร้างบล็อกของโค้ด ในภาษาโปรแกรมมิงอื่น ๆ จะใช้วงเล็บปีกกาในการสร้างบล็อกของโค้ดแทนการเว้นวรรค บั๊กที่พบบ่อยอย่างหนึ่งเมื่อเขียนโค้ด Python คือการเว้นวรรคผิด

![Indentation Error](images/indentation.png)

### คอมเมนต์

คอมเมนต์มีความสำคัญมากในการทำให้โค้ดอ่านง่ายขึ้นและใช้ทิ้งข้อสังเกตไว้ในโค้ดของเรา Python จะไม่รันส่วนที่เป็นคอมเมนต์ในโค้ดของเรา
ข้อความใดก็ตามที่เริ่มต้นด้วย hash (#) ใน Python ถือเป็นคอมเมนต์

**ตัวอย่าง: คอมเมนต์บรรทัดเดียว**

```shell
    # This is the first comment
    # This is the second comment
    # Python is eating the world
```

**ตัวอย่าง: คอมเมนต์หลายบรรทัด**

สามารถใช้เครื่องหมายคำพูดสามตัว (triple quote) สำหรับคอมเมนต์หลายบรรทัดได้ ถ้าไม่ได้ถูกกำหนดค่าให้กับตัวแปร

```shell
"""This is multiline comment
multiline comment take multiple lines.
python is eating the world
"""
```

### ชนิดข้อมูล

ใน Python มีชนิดข้อมูลหลายประเภท เราจะเริ่มจากชนิดที่พบบ่อยที่สุดก่อน

#### ตัวเลข

    - Integer (จำนวนเต็ม): จำนวนเต็ม (ลบ ศูนย์ และบวก)
        ตัวอย่าง:
        ... -3, -2, -1, 0, 1, 2, 3 ...
    - Float (ทศนิยม): จำนวนทศนิยม
        ตัวอย่าง
        ... -3.5, -2.25, -1.0, 0.0, 1.1, 2.2, 3.5 ...
    - Complex (จำนวนเชิงซ้อน)
        ตัวอย่าง
        1 + j, 2 + 4j

#### สตริง

กลุ่มของตัวอักษรตั้งแต่หนึ่งตัวขึ้นไปที่อยู่ภายใต้เครื่องหมายคำพูดเดี่ยวหรือคู่ ถ้าสตริงมีมากกว่าหนึ่งประโยคเราจะใช้เครื่องหมายคำพูดสามตัว

**ตัวอย่าง:**

```py
'Asabeneh'
'Finland'
'Python'
'I love teaching'
'I hope you are enjoying the first day'
```

#### บูลีน

ชนิดข้อมูลบูลีนมีเพียงค่า True หรือ False เท่านั้น

**ตัวอย่าง:**

```python
    True  #  if the light on, if it is on the value is True
    False # if the light off, if it is off the value is False
```

#### ลิสต์

ลิสต์ใน Python เป็นกลุ่มข้อมูลแบบมีลำดับที่สามารถเก็บข้อมูลต่างชนิดกันได้ ลิสต์คล้ายกับ array ใน JavaScript

**ตัวอย่าง:**

```py
['Banana', 'Orange', 'Mango', 'Avocado'] # all the same data type in the list
['Banana', 10, False, 9.81] # different data types in the list
```

#### ดิกชันนารี

ดิกชันนารีใน Python เป็นกลุ่มข้อมูลแบบไม่มีลำดับที่เก็บข้อมูลในรูปแบบคู่ key:value

**ตัวอย่าง:**

```py
{'name':'Asabeneh', 'country':'Finland', age:250, 'is_married':True}
```

#### ทูเพิล

ทูเพิลเป็นกลุ่มข้อมูลแบบมีลำดับที่เก็บข้อมูลต่างชนิดกันได้เหมือนลิสต์ แต่ทูเพิลไม่สามารถแก้ไขได้หลังจากถูกสร้างขึ้นแล้ว มันเป็นชนิดข้อมูลที่ไม่สามารถเปลี่ยนแปลงได้ (immutable)

**ตัวอย่าง**

```py
('Asabeneh', 'Brook', 'Abraham', 'Lidiya')
```

#### เซ็ต

เซ็ตเป็นชนิดข้อมูลกลุ่มที่คล้ายกับลิสต์และทูเพิล แต่ต่างจากลิสต์และทูเพิลตรงที่เซ็ตไม่ใช่กลุ่มข้อมูลแบบมีลำดับ เช่นเดียวกับในคณิตศาสตร์ เซ็ตใน Python เก็บเฉพาะรายการที่ไม่ซ้ำกันเท่านั้น

ในหัวข้อถัดไป เราจะลงรายละเอียดเกี่ยวกับชนิดข้อมูลแต่ละแบบใน Python ให้ครบถ้วนมากขึ้น

**ตัวอย่าง:**

```py
{3.14, 9.81, 2.7} # order is not important in set
```

### การตรวจสอบชนิดข้อมูล

หากต้องการตรวจสอบชนิดข้อมูลของข้อมูลใดข้อมูลหนึ่ง เราใช้ฟังก์ชัน **type** ในเทอร์มินัลต่อไปนี้คุณจะเห็นชนิดข้อมูลต่าง ๆ ใน Python:

![Checking Data types](./images/checking_data_types.png)

### ไฟล์ Python

ก่อนอื่นให้เปิดโฟลเดอร์โปรเจกต์ของคุณ 30DaysOfPython ถ้าคุณยังไม่มีโฟลเดอร์นี้ ให้สร้างโฟลเดอร์ชื่อ 30DaysOfPython ภายในโฟลเดอร์นี้ ให้สร้างไฟล์ชื่อ helloworld.py ทีนี้มาทำสิ่งที่เราทำบน python interactive shell โดยใช้ visual studio code กัน
python interactive shell จะพิมพ์ผลลัพธ์โดยไม่ต้องใช้ **print** แต่บน visual studio code เราต้องใช้ฟังก์ชันในตัว **print(ข้อมูลที่ต้องการพิมพ์)** เพื่อดูผลลัพธ์

**ตัวอย่าง:**
helloworld.py

```py
# Day 1 - 30DaysOfPython Challenge
print(2 + 3)             # addition(+)
print(3 - 1)             # subtraction(-)
print(2 * 3)             # multiplication(*)
print(3 / 2)             # division(/)
print(3 ** 2)            # exponential(**)
print(3 % 2)             # modulus(%)
print(3 // 2)            # Floor division operator(//)

# Checking data types
print(type(10))          # Int
print(type(3.14))        # Float
print(type(1 + 3j))      # Complex number
print(type('Asabeneh'))  # String
print(type([1, 2, 3]))   # List
print(type({'name':'Asabeneh'})) # Dictionary
print(type({9.8, 3.14, 2.7}))    # Set
print(type((9.8, 3.14, 2.7)))    # Tuple
```

![Running python script](./images/running_python_script.png)

🌕  คุณเยี่ยมมาก คุณเพิ่งทำแบบฝึกหัดวันที่ 1 เสร็จแล้ว และกำลังก้าวสู่ความยิ่งใหญ่ ตอนนี้มาทำแบบฝึกหัดเพื่อลับสมองและลับกล้ามเนื้อกันบ้าง

## 💻 แบบฝึกหัด - วันที่ 1

1. ตรวจสอบเวอร์ชันของ Python ที่คุณใช้อยู่
2. เปิด python interactive shell และทำการดำเนินการต่อไปนี้ โดยใช้ตัวถูกดำเนินการ (operand) เป็น 3 และ 4 ดูตัวอย่างด้านบน
   - การบวก (+)
   - การลบ (-)
   - การคูณ (\*)
   - มอดุโล (%)
   - การหาร (/)
   - ยกกำลัง (\*\*)
   - การหารแบบตัดเศษ (//)
3. เขียนสตริงบน python interactive shell สตริงมีดังนี้:
   - ชื่อของคุณ
   - นามสกุลของคุณ
   - ประเทศของคุณ
   - I am enjoying 30 days of python
4. ตรวจสอบชนิดข้อมูลของข้อมูลต่อไปนี้:
   - 10
   - 9.8
   - 3.14
   - 4 - 4j
   - ['Asabeneh', 'Python', 'Finland']
   - ชื่อของคุณ
   - นามสกุลของคุณ
   - ประเทศของคุณ
5. สร้างโฟลเดอร์ชื่อ day_1 ภายในโฟลเดอร์ 30DaysOfPython ภายในโฟลเดอร์ day_1 ให้สร้างไฟล์ python ชื่อ helloword.py แล้วทำข้อ 1, 2, 3 และ 4 ซ้ำอีกครั้ง อย่าลืมใช้ _print()_ เมื่อคุณทำงานกับไฟล์ python นำทางไปยังไดเรกทอรีที่คุณบันทึกไฟล์ไว้ แล้วรันไฟล์นั้น

# 📘 วันที่ 2

## ฟังก์ชันในตัว (Built in functions)

ใน Python เรามีฟังก์ชันในตัวมากมาย ฟังก์ชันในตัวสามารถใช้งานได้แบบ global ฟังก์ชันในตัวของ Python ที่ใช้กันบ่อยที่สุดบางส่วนได้แก่ _print()_, _len()_, _type()_, _int()_, _float()_, _str()_, _input()_, _list()_, _dict()_, _min()_, _max()_, _sum()_, _sorted()_, _open()_, _file()_, _help()_ และ _dir()_ ในตารางต่อไปนี้คุณจะเห็นรายการฟังก์ชันในตัวของ Python แบบครบถ้วน ซึ่งนำมาจาก[เอกสารของ python](https://docs.python.org/2/library/functions.html)

![Built in Functions](images/builtin-functions.png)

มาเปิด python shell แล้วเริ่มใช้ฟังก์ชันในตัวที่พบบ่อยที่สุดบางส่วนกัน

![Built in functions](images/builtin-functions_practice.png)

มาฝึกใช้ฟังก์ชันในตัวต่าง ๆ กันต่อ

![Help and Dir Built in Functions](/images/help_and_dir_builtin.png)

จากเทอร์มินัลข้างต้นจะเห็นว่า Python มีคำสงวน (reserved words) เราจะไม่ใช้คำสงวนเหล่านี้ในการตั้งชื่อตัวแปรหรือฟังก์ชัน เราจะพูดถึงตัวแปรในหัวข้อถัดไป

ผมเชื่อว่าตอนนี้คุณคุ้นเคยกับฟังก์ชันในตัวแล้ว มาฝึกฝนฟังก์ชันในตัวกันอีกครั้งก่อนที่จะไปหัวข้อถัดไป

![Min Max Sum](images/builtin-functional-final.png)

## ตัวแปร

ตัวแปรใช้เก็บข้อมูลในหน่วยความจำของคอมพิวเตอร์ ในหลายภาษาโปรแกรมมิงแนะนำให้ใช้ชื่อตัวแปรที่จดจำง่าย (mnemonic) ตัวแปรอ้างอิงถึงตำแหน่งหน่วยความจำที่เก็บข้อมูลไว้
ห้ามขึ้นต้นชื่อตัวแปรด้วยตัวเลข อักขระพิเศษ หรือเครื่องหมายขีดกลาง ตัวแปรสามารถมีชื่อสั้น ๆ ได้ (เช่น x, y, z) แต่แนะนำให้ใช้ชื่อที่สื่อความหมายมากกว่า (firstname, lastname, age, country)
กฎการตั้งชื่อตัวแปรใน Python

- ชื่อตัวแปรต้องขึ้นต้นด้วยตัวอักษรหรือเครื่องหมายขีดล่าง (underscore)
- ชื่อตัวแปรห้ามขึ้นต้นด้วยตัวเลข
- ชื่อตัวแปรมีได้เฉพาะตัวอักษร ตัวเลข และขีดล่างเท่านั้น (A-z, 0-9, และ \_)
- ชื่อตัวแปรมีความแตกต่างระหว่างตัวพิมพ์เล็กและใหญ่ (firstname, Firstname, FirstName และ FIRSTNAME ถือเป็นตัวแปรคนละตัวกัน)

ชื่อตัวแปรที่ถูกต้อง

```shell
firstname
lastname
age
country
city
first_name
last_name
capital_city
_if # if we want to use reserved word as a variable
year_2019
year2019
current_year_2019
num1
num2
```

ชื่อตัวแปรที่ไม่ถูกต้อง

```shell
first-name
num-1
1num
```

เราจะใช้รูปแบบการตั้งชื่อตัวแปรมาตรฐานของ Python ซึ่งเป็นที่นิยมใช้กันในหมู่นักพัฒนา Python จำนวนมาก ตัวอย่างด้านล่างคือตัวอย่างการตั้งชื่อตัวแปรมาตรฐาน โดยใช้ขีดล่างเมื่อชื่อตัวแปรยาว

เมื่อเรากำหนดชนิดข้อมูลใดข้อมูลหนึ่งให้กับตัวแปร เราเรียกว่าการประกาศตัวแปร (variable declaration) ตัวอย่างเช่นในตัวอย่างด้านล่าง ชื่อจริงของผมถูกกำหนดให้กับตัวแปร first_name เครื่องหมายเท่ากับคือตัวดำเนินการกำหนดค่า (assignment operator) การกำหนดค่าหมายถึงการเก็บข้อมูลไว้ในตัวแปร

_ตัวอย่าง:_

```py
# Variables in Python

first_name = 'Asabeneh'
last_name = 'Yetayeh'
country = 'Finland'
city = 'Helsinki'
age = 250
is_married = True
skills = ['HTML', 'CSS', 'JS', 'React', 'Python']
person_info = {
   'firstname':'Asabeneh',
   'lastname':'Yetayeh',
   'country':'Finland',
   'city':'Helsinki'
   }
```

มาใช้ฟังก์ชันในตัว _print()_ และ _len()_ กัน ฟังก์ชัน print สามารถรับหลายอาร์กิวเมนต์ได้ อาร์กิวเมนต์คือค่าที่เราส่งหรือใส่ไว้ในวงเล็บของฟังก์ชัน ดูตัวอย่างด้านล่าง

**ตัวอย่าง:**

```py
print('Hello, World!')
print('Hello',',', 'World','!') # it can take multiple arguments
print(len('Hello, World!')) # it takes only one argument
```

มาพิมพ์และหาความยาวของตัวแปรที่ประกาศไว้ด้านบนกัน:

**ตัวอย่าง:**

```py
# Printing the values stored in the variables

print('First name:', first_name)
print('First name length:', len(first_name))
print('Last name: ', last_name)
print('Last name length: ', len(last_name))
print('Country: ', country)
print('City: ', city)
print('Age: ', age)
print('Married: ', is_married)
print('Skills: ', skills)
print('Person information: ', person_info)
```

ตัวแปรสามารถประกาศในบรรทัดเดียวกันได้เช่นกัน:

**ตัวอย่าง:**

```py
first_name, last_name, country, age, is_married = 'Asabeneh', 'Yetayeh', 'Helsink', 250, True

print(first_name, last_name, country, age, is_married)
print('First name:', first_name)
print('Last name: ', last_name)
print('Country: ', country)
print('Age: ', age)
print('Married: ', is_married)
```

การรับค่าจากผู้ใช้โดยใช้ฟังก์ชันในตัว _input()_ มากำหนดข้อมูลที่ได้รับจากผู้ใช้ให้กับตัวแปร first_name และ age กัน
**ตัวอย่าง:**

```py
first_name = input('What is your name: ')
age = input('How old are you? ')

print(first_name)
print(age)
```

## ชนิดข้อมูล

ใน Python มีชนิดข้อมูลหลายประเภท ในการระบุชนิดข้อมูลเราใช้ฟังก์ชันในตัว _type_ ผมอยากให้คุณเข้าใจชนิดข้อมูลแต่ละแบบให้ดีจริง ๆ เพราะในการเขียนโปรแกรมนั้นทุกอย่างล้วนเกี่ยวข้องกับชนิดข้อมูล ผมได้แนะนำชนิดข้อมูลไปแล้วตั้งแต่ตอนต้น และมันจะปรากฏขึ้นอีกเรื่อย ๆ เพราะทุกหัวข้อล้วนเกี่ยวข้องกับชนิดข้อมูล เราจะพูดถึงชนิดข้อมูลอย่างละเอียดมากขึ้นในหัวข้อที่เกี่ยวข้องต่อไป

## การตรวจสอบชนิดข้อมูลและการแปลงชนิดข้อมูล

- ตรวจสอบชนิดข้อมูล: หากต้องการตรวจสอบชนิดข้อมูลของข้อมูลใดข้อมูลหนึ่ง เราใช้ _type_
  **ตัวอย่าง:**

```py
# Different python data types
# Let's declare different data types

first_name = 'Asabeneh'     # str
last_name = 'Yetayeh'       # str
country = 'Finland'         # str
city= 'Helsinki'            # str
age = 250                   # int, it is not my real age, don't worry about it

# Printing out types
print(type('Asabeneh'))     # str
print(type(first_name))     # str
print(type(10))             # int
print(type(3.14))           # float
print(type(1 + 1j))         # complex
print(type(True))           # bool
print(type([1, 2,3,4]))     # list
print(type({'name':'Asabeneh','age':250, 'is_married':250}))    # dict
print(type((1,2)))                                              # tuple
print(type(zip([1,2],[3,4])))                                   # set
```

- การแปลงชนิดข้อมูล (Casting): การแปลงข้อมูลจากชนิดหนึ่งไปเป็นอีกชนิดหนึ่ง เราใช้ _int()_, _float()_, _str()_, _list_
  เมื่อเราทำการดำเนินการทางคณิตศาสตร์ ตัวเลขที่อยู่ในรูปสตริงต้องถูกแปลงเป็น int หรือ float ก่อน ไม่เช่นนั้นจะเกิด error หากเราต้องการต่อ (concatenate) ตัวเลขกับสตริง ตัวเลขนั้นต้องถูกแปลงเป็นสตริงก่อน เราจะพูดถึงการต่อสตริงในหัวข้อ String
  **ตัวอย่าง:**

```py
# int to float

num_int = 10
print('num_int',num_int)         # 10
num_float = float(num_int)
print('num_float:', num_float)   # 10.0

# float to int

gravity = 9.81
print(int(gravity))             # 9

# int to str
num_int = 10
print(num_int)                  # 10
num_str = str(num_int)
print(num_str)                  # '10'

# str to int
num_str = '10.6'
print('num_int', int(num_str))      # 10
print('num_float', float(num_str))  # 10.6

# str to list
first = 'Asabeneh'
print(first_name)
print(first_name)                    # 'Asabeneh'
first_name_to_list = list(first_name)
print(first_name_to_list)            # ['A', 's', 'a', 'b', 'e', 'n', 'e', 'h']
```

## ตัวเลข

ตัวเลขเป็นชนิดข้อมูลหนึ่งใน Python

1. Integer (จำนวนเต็ม): จำนวนเต็ม (ลบ ศูนย์ และบวก)
    ตัวอย่าง:
        ... -3, -2, -1, 0, 1, 2, 3 ...

2. Floating Numbers (จำนวนทศนิยม)
    ตัวอย่าง:
        ... -3.5, -2.25, -1.0, 0.0, 1.1, 2.2, 3.5 ...

3. Complex Numbers (จำนวนเชิงซ้อน)
    ตัวอย่าง:
        1 + j, 2 + 4j, 1 - 1j

## 💻 แบบฝึกหัด - วันที่ 2

1. ภายในโฟลเดอร์ 30DaysOfPython ให้สร้างโฟลเดอร์ชื่อ day_2 ภายในโฟลเดอร์นี้ให้สร้างไฟล์ชื่อ variables.py
2. เขียนคอมเมนต์ Python ว่า 'Day 2: 30 Days of python programming'
3. ประกาศตัวแปรชื่อจริงและกำหนดค่าให้มัน
4. ประกาศตัวแปรนามสกุลและกำหนดค่าให้มัน
5. ประกาศตัวแปรชื่อเต็มและกำหนดค่าให้มัน
6. ประกาศตัวแปรประเทศและกำหนดค่าให้มัน
7. ประกาศตัวแปรเมืองและกำหนดค่าให้มัน
8. ประกาศตัวแปรอายุและกำหนดค่าให้มัน
9. ประกาศตัวแปรปีและกำหนดค่าให้มัน
10. ประกาศตัวแปร is_married และกำหนดค่าให้มัน
11. ประกาศตัวแปร is_true และกำหนดค่าให้มัน
12. ประกาศตัวแปร is_light_on และกำหนดค่าให้มัน
13. ประกาศตัวแปรหลายตัวในบรรทัดเดียว
14. ตรวจสอบชนิดข้อมูลของตัวแปรทั้งหมดโดยใช้ฟังก์ชันในตัว type()
15. ใช้ฟังก์ชันในตัว _len()_ หาความยาวของชื่อจริงของคุณ
16. เปรียบเทียบความยาวของชื่อจริงกับนามสกุลของคุณ
17. ประกาศ 5 เป็น num_one และ 4 เป็น num_two
    1. บวก num_one กับ num_two แล้วกำหนดค่าให้กับตัวแปร _total_
    2. ลบ num_two ออกจาก num_one แล้วกำหนดค่าให้กับตัวแปร _diff_
    3. คูณ num_two กับ num_one แล้วกำหนดค่าให้กับตัวแปร _product_
    4. หาร num_one ด้วย num_two แล้วกำหนดค่าให้กับตัวแปร _division_
    5. ใช้การหารแบบมอดุโลหาเศษของ num_two หารด้วย num_one แล้วกำหนดค่าให้กับตัวแปร _remainder_
    6. คำนวณ num_one ยกกำลัง num_two แล้วกำหนดค่าให้กับตัวแปร _exp_
    7. หาผลหารแบบตัดเศษของ num_one หารด้วย num_two แล้วกำหนดค่าให้กับตัวแปร _floor_division_
18. รัศมีของวงกลมวงหนึ่งเท่ากับ 30 เมตร
    1. คำนวณพื้นที่ของวงกลมและกำหนดค่าให้กับตัวแปร _area_of_circle_
    2. คำนวณเส้นรอบวงของวงกลมและกำหนดค่าให้กับตัวแปร _circum_of_circle_
    3. รับค่ารัศมีจากผู้ใช้แล้วคำนวณพื้นที่
19. ใช้ฟังก์ชันในตัว input เพื่อรับชื่อจริง นามสกุล ประเทศ และอายุจากผู้ใช้ แล้วเก็บค่าไว้ในตัวแปรที่สอดคล้องกัน
20. รัน help('keywords') บน python shell หรือในไฟล์ของคุณเพื่อตรวจสอบคำสงวน

# 📘 วันที่ 3

## บูลีน

ชนิดข้อมูลบูลีนแทนค่าใดค่าหนึ่งจากสองค่า: _True_ หรือ _False_ การใช้งานชนิดข้อมูลนี้จะชัดเจนขึ้นเมื่อคุณเริ่มเรียนตัวดำเนินการเปรียบเทียบ ตัวอักษรแรก **T** ของ True และ **F** ของ False ต้องเป็นตัวพิมพ์ใหญ่ ซึ่งต่างจาก JavaScript
**ตัวอย่าง: ค่าบูลีน**

```py
print(True)
print(False)
```

## ตัวดำเนินการ (Operators):

ภาษา Python รองรับตัวดำเนินการหลายประเภท ในหัวข้อนี้เราจะเน้นไปที่บางประเภทเท่านั้น

### ตัวดำเนินการกำหนดค่า (Assignment Operators):

ตัวดำเนินการกำหนดค่าใช้สำหรับกำหนดค่าให้กับตัวแปร ลองยกตัวอย่าง = เครื่องหมายเท่ากับในคณิตศาสตร์แสดงว่าค่าสองค่าเท่ากัน แต่ใน Python มันหมายถึงเรากำลังเก็บค่าไว้ในตัวแปรใดตัวแปรหนึ่ง เราเรียกสิ่งนี้ว่าการกำหนดค่า (assignment) ตารางด้านล่างแสดงตัวดำเนินการกำหนดค่าประเภทต่าง ๆ ใน Python ซึ่งนำมาจาก [w3school](https://www.w3schools.com/python/python_operators.asp)

![Assignment Operators](images/assignment_operators.png)

### ตัวดำเนินการทางคณิตศาสตร์ (Arithmetic Operators):

- การบวก (+): a + b
- การลบ (-): a -b
- การคูณ (_):a _ b
- การหาร (/): a / b
- มอดุโล (%):a % b
- การหารแบบตัดเศษ (//): a // b
- ยกกำลัง (**):a ** b

![Arithmetic Operators](./images/arithmetic_operators.png)

**ตัวอย่าง: จำนวนเต็ม**

```py
# Arithmetic Operations in Python
# Integers

print('Addition: ', 1 + 2)
print('Subtraction: ', 2 - 1)
print('Multiplication: ', 2 * 3)
print ('Division: ', 4 / 2)                         # Division in python gives floating number
print('Division: ', 6 / 2)
print('Division: ', 7 / 2)
print('Division without the remainder: ', 7 // 2)   # gives without the floating number or without the remaining
print('Modulus: ', 3 % 2)                           # Gives the remainder
print ('Division without the remainder: ',7 // 3)
print('Exponential: ', 3 ** 2)                      # it means 3 * 3
```

**ตัวอย่าง: จำนวนทศนิยม**

```py
# Floating numbers
print('Floating Number,PI', 3.14)
print('Floating Number, gravity', 9.81)
```

**ตัวอย่าง: จำนวนเชิงซ้อน**

```py
# Complex numbers
print('Complex number: ', 1+1j)
print('Multiplying complex number: ',(1+1j) * (1-1j))
```

มาประกาศตัวแปรและกำหนดชนิดข้อมูลตัวเลขให้มันกัน ผมจะใช้ชื่อตัวแปรตัวอักษรเดียวในตัวอย่างนี้ แต่จำไว้ว่าอย่าสร้างนิสัยประกาศตัวแปรแบบนี้ ชื่อตัวแปรควรจดจำได้ง่ายเสมอ

**ตัวอย่าง:**

```python
# Declaring the variable at the top first

a = 3 # a is a variable name and 3 is an integer data type
b = 2 # b is a variable name and 3 is an integer data type

# Arithmetic operations and assigning the result to a variable
total = a + b
diff = a - b
product = a * b
division = a / b
remainder = a % b
floor_division = a // b
exponential = a ** b

# I should have used sum instead of total but sum is a built-in function try to avoid overriding builtin functions
print(total) # if you don't label your print with some string, you never know from where is  the result is coming
print('a + b = ', total)
print('a - b = ', diff)
print('a * b = ', product)
print('a / b = ', division)
print('a % b = ', remainder)
print('a // b = ', floor_division)
print('a ** b = ', exponential)
```

**ตัวอย่าง:**

```py
print('== Addition, Subtraction, Multiplication, Division, Modulus ==')

# Declaring values and organizing them together
num_one = 3
num_two = 4

# Arithmetic operations
total = num_one + num_two
diff = num_two - num_one
product = num_one * num_two
div = num_two / num_two
remainder = num_two % num_one

# Printing values with label
print('total: ', total)
print('difference: ', diff)
print('product: ', product)
print('division: ', div)
print('remainder: ', remainder)
```

มาเริ่มเชื่อมโยงสิ่งที่เรารู้เข้าด้วยกันและนำไปใช้คำนวณ (พื้นที่, ปริมาตร, น้ำหนัก, เส้นรอบรูป, ระยะทาง, แรง) กัน

**ตัวอย่าง:**

```py
# Calculating area of a circle
radius = 10                                 # radius of a circle
area_of_circle = 3.14 * radius ** 2         # two * sign means exponent or power
print('Area of a circle:', area_of_circle)

# Calculating area of a rectangle
length = 10
width = 20
area_of_rectangle = length * width
print('Area of rectangle:', area_of_width)

# Calculating a weight of an object
mass = 75
gravity = 9.81
weight = mass * gravity
print(weight, 'N')                         # Adding unit to the weight
```

### ตัวดำเนินการเปรียบเทียบ (Comparison Operators)

ในการเขียนโปรแกรม เราเปรียบเทียบค่าต่าง ๆ กัน เราใช้ตัวดำเนินการเปรียบเทียบเพื่อเปรียบเทียบค่าสองค่า เราตรวจสอบว่าค่าหนึ่งมากกว่า น้อยกว่า หรือเท่ากับอีกค่าหนึ่งหรือไม่ ตารางต่อไปนี้แสดงตัวดำเนินการเปรียบเทียบของ Python ซึ่งนำมาจาก [w3shool](https://www.w3schools.com/python/python_operators.asp)

![Comparison Operators](./images/comparison_operators.png)
**ตัวอย่าง: ตัวดำเนินการเปรียบเทียบ**

```py
print(3 > 2)     # True, because 3 is greater than 2
print(3 >= 2)    # True, because 3 is greater than 2
print(3 < 2)     # False,  because 3 is greater than 2
print(2 < 3)     # True, because 2 is less than 3
print(2 <= 3)    # True, because 2 is less than 3
print(3 == 2)    # False, because 3 is not equal to 2
print(3 != 2)    # True, because 3 is not equal to 2
print(len('mango') == len('avocado'))  # False
print(len('mango') != len('avocado'))  # True
print(len('mango') < len('avocado'))   # True
print(len('milk') != len('meat'))      # False
print(len('milk') == len('meat'))      # True
print(len('tomato') == len('potato'))  # True
print(len('python') > len('dragon'))   # False


# Comparing something give either a True or False

print('True == True: ', True == True)
print('True == False: ', True == False)
print('False == False:', False == False)
print('True and True: ', True and True)
print('True or False:', True or False)

```

นอกจากตัวดำเนินการเปรียบเทียบข้างต้นแล้ว Python ยังใช้:

- _is_: คืนค่า true ถ้าตัวแปรทั้งสองเป็นอ็อบเจ็กต์เดียวกัน (x is y)
- _is not_: คืนค่า true ถ้าตัวแปรทั้งสองไม่ใช่อ็อบเจ็กต์เดียวกัน (x is not y)
- _in_: คืนค่า True ถ้าลิสต์มีรายการที่ระบุอยู่ (x in y)
- _not in_: คืนค่า True ถ้าลิสต์ไม่มีรายการที่ระบุอยู่ (x in y)

```py
print('1 is 1', 1 is 1)                   # True - because the data values are the same
print('1 is not 2', 1 is not 2)           # True - because 1 is not 2
print('A in Asabeneh', 'A' in 'Asabeneh') # True - A found in the string
print('B in Asabeneh', 'B' in 'Asabeneh') # False -there is no uppercase B
print('coding' in 'coding for all') # True - because coding for all has the word coding
print('a in an:', 'a' in 'an')      # True
print('4 is 2 ** 2:', 4 is 2 **2)   # True
```

### ตัวดำเนินการทางตรรกะ (Logical Operators)

ต่างจากภาษาโปรแกรมมิงอื่น ๆ Python ใช้คำสำคัญ _and_, _or_ และ _not_ สำหรับตัวดำเนินการทางตรรกะ ตัวดำเนินการทางตรรกะใช้เพื่อรวมนิพจน์เงื่อนไขเข้าด้วยกัน:

![Logical Operators](./images/logical_operators.png)

```py
print(3 > 2 and 4 > 3) # True - because both statements are true
print(3 > 2 and 4 < 3) # False - because the second statement is false
print(3 < 2 and 4 < 3) # False - because both statements are false
print(3 > 2 or 4 > 3)  # True - because both statements are true
print(3 > 2 or 4 < 3)  # True - because one of the statement is true
print(3 < 2 or 4 < 3)  # False - because both statements are false
print(not 3 > 2)     # False - because 3 > 2 is true, then not True gives False
print(not True)      # False - Negation, the not operator turns true to false
print(not False)     # True
print(not not True)  # True
print(not not False) # False
```

## 💻 แบบฝึกหัด - วันที่ 3

1. ประกาศอายุของคุณเป็นตัวแปรชนิด integer
2. ประกาศส่วนสูงของคุณเป็นตัวแปรชนิด float
3. ประกาศตัวแปรชนิดจำนวนเชิงซ้อน (complex number)
4. เขียนสคริปต์ที่ให้ผู้ใช้ป้อนฐานและความสูงของสามเหลี่ยม แล้วคำนวณพื้นที่ของสามเหลี่ยม (พื้นที่ = 0.5 x ฐาน x สูง)

```py
    Enter base: 20
    Enter height: 10
    The area of the triangle is 50
```

5. เขียนสคริปต์ที่ให้ผู้ใช้ป้อนด้าน a, ด้าน b และด้าน c ของสามเหลี่ยม แล้วคำนวณเส้นรอบรูปของสามเหลี่ยม (เส้นรอบรูป = a + b + c)

```py
Enter side a: 5
Enter side b: 4
Enter side c: 3
The perimeter of the triangle is 12
```

6. รับความยาวและความกว้างจากผู้ใช้ แล้วคำนวณพื้นที่ของสี่เหลี่ยมผืนผ้า (พื้นที่ = ความยาว x ความกว้าง) และเส้นรอบรูปของสี่เหลี่ยมผืนผ้า (เส้นรอบรูป = 2 x (ความยาว + ความกว้าง))
7. รับรัศมีจากผู้ใช้ แล้วคำนวณพื้นที่ของวงกลม (พื้นที่ = pi x r x r) และเส้นรอบวงของวงกลม (c = 2 x pi x r) โดยที่ pi = 3.14
8. คำนวณความชัน จุดตัดแกน x และจุดตัดแกน y ของ y = 2x -2
9. ความชันคือ (m = y2-y1/x2-x1) จงหาความชันระหว่างจุด (2, 2) และจุด (6,10)
10. เปรียบเทียบความชันของข้อ 10 และ 11
11. คำนวณค่าของ y (y = x^2 + 6x + 9) ลองใช้ค่า x หลาย ๆ ค่าแล้วหาว่าที่ค่า x ใด y จึงเท่ากับ 0
12. หาความยาวของคำว่า python และ jargon แล้วสร้างข้อความเปรียบเทียบที่มีค่าเป็นเท็จ (falsy)
13. ใช้ตัวดำเนินการ _and_ เพื่อตรวจสอบว่า 'on' อยู่ในทั้ง python และ jargon หรือไม่
14. _I hope this course is not full of jargon_ ใช้ตัวดำเนินการ _in_ เพื่อตรวจสอบว่า _jargon_ อยู่ในประโยคนี้หรือไม่
15. ไม่มี 'on' อยู่ทั้งใน dragon และ python
16. หาความยาวของข้อความ _python_ แล้วแปลงค่าเป็น float และแปลงเป็น string
17. เลขคู่คือเลขที่หารด้วย 2 ลงตัวและมีเศษเป็นศูนย์ คุณจะตรวจสอบว่าตัวเลขหนึ่งเป็นเลขคู่หรือไม่โดยใช้ Python ได้อย่างไร ?
18. ผลหารแบบตัดเศษของ 7 หารด้วย 3 เท่ากับค่าที่แปลงเป็น int ของ 2.7
19. ตรวจสอบว่าชนิดของ '10' เท่ากับ 10 หรือไม่
20. ตรวจสอบว่า int('9.8') เท่ากับ 10 หรือไม่
21. เขียนสคริปต์ที่ให้ผู้ใช้ป้อนจำนวนชั่วโมงและอัตราค่าจ้างต่อชั่วโมง แล้วคำนวณค่าจ้างของบุคคลนั้น

```py
Enter hours: 40
Enter rate per hour: 28
Your weekly earning is 1120
```

22. เขียนสคริปต์ที่ให้ผู้ใช้ป้อนจำนวนปี แล้วคำนวณจำนวนวินาทีที่คนคนหนึ่งมีชีวิตอยู่ได้ สมมติว่ามีคนที่มีชีวิตอยู่ถึงหนึ่งร้อยปี

```py
Enter number of yours you live: 100
You lived 3153600000 seconds.
```

23. เขียนสคริปต์ Python ที่แสดงตารางต่อไปนี้

```py
1 1 1 1 1
2 1 2 4 8
3 1 3 9 27
4 1 4 16 64
5 1 5 25 125
```

[ตอนที่ 2 >>](day4-6.md)