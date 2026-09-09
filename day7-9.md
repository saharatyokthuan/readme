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
- [📘 วันที่ 7](#%f0%9f%93%98-day-7)
  - [เซ็ต](#set)
    - [การสร้างเซ็ต](#creating-a-set)
    - [การหาความยาวของเซ็ต](#getting-set-length)
    - [การเข้าถึงรายการในเซ็ต](#accessing-items-in-set)
    - [การตรวจสอบรายการ](#checking-an-item)
    - [การเพิ่มรายการเข้าไปในลิสต์](#adding-items-to-a-list)
    - [การลบรายการออกจากลิสต์](#removing-item-from-a-list)
    - [การล้างรายการในเซ็ต](#clearing-item-in-a-set)
    - [การลบเซ็ต](#deleting-a-set)
    - [การแปลงลิสต์เป็นเซ็ต](#converting-list-to-set)
    - [การรวมเซ็ตเข้าด้วยกัน](#joining-sets)
    - [การหาส่วนร่วม (intersection)](#finding-intersection-items)
    - [การตรวจสอบซับเซ็ตและซูเปอร์เซ็ต](#checking-subset-and-super-set)
    - [การตรวจสอบผลต่างระหว่างเซ็ตสองเซ็ต](#checking-difference-between-two-sets)
    - [การหาผลต่างสมมาตรระหว่างเซ็ตสองเซ็ต](#finding-symmetric-difference-between-two-sets)
    - [การรวมเซ็ต](#joining-set)
  - [💻 แบบฝึกหัด: วันที่ 7](#%f0%9f%92%bb-exercises-day-7)
- [📘 วันที่ 8](#%f0%9f%93%98-day-8)
  - [ดิกชันนารี](#dictionary)
    - [การสร้างดิกชันนารี](#creating-a-dictionary)
    - [ความยาวของดิกชันนารี](#dictionary-length)
    - [การเข้าถึงรายการในดิกชันนารี](#accessing-a-dictionary-items)
    - [การเพิ่มรายการเข้าไปในดิกชันนารี](#adding-item-to-a-dictionary)
    - [การแก้ไขรายการในดิกชันนารี](#modifying-item-in-a-dictionary)
    - [การตรวจสอบคีย์ในดิกชันนารี](#checking-a-key-in-a-dictionary)
    - [การลบรายการที่เป็นคีย์ออกจากดิกชันนารี](#removing-key-items-from-dictionary)
    - [การเปลี่ยนดิกชันนารีเป็นรายการในลิสต์](#changing-dictionary-to-list-items)
    - [การล้างรายการในลิสต์ของดิกชันนารี](#clearing-dictionary-list-items)
    - [การลบดิกชันนารี](#deleting-dictionary)
    - [การคัดลอกดิกชันนารี](#copy-a-dictionary)
    - [การรับคีย์ของดิกชันนารีเป็นลิสต์](#getting-dictionary-keys-as-list)
    - [การรับค่าของดิกชันนารีเป็นลิสต์](#getting-dictionary-values-as-list)
  - [💻 แบบฝึกหัด: วันที่ 8](#%f0%9f%92%bb-exercises-day-8)
- [📘 วันที่ 9](#%f0%9f%93%98-day-9)
  - [เงื่อนไข (Conditionals)](#conditionals)
    - [เงื่อนไข If](#if-condition)
    - [If Else](#if-else)
    - [If elif else](#if-elif-else)
    - [รูปแบบย่อ (Short Hand)](#short-hand)
    - [เงื่อนไขซ้อน (Nested condition)](#nested-condition)
    - [เงื่อนไข if กับตัวดำเนินการทางตรรกะ and](#if-condition-and-and-logical-operator)
    - [เงื่อนไข if กับตัวดำเนินการทางตรรกะ or](#if-and-or-logical-operator)
  - [💻 แบบฝึกหัด: วันที่ 9](#%f0%9f%92%bb-exercises-day-9)

# 📘 วันที่ 7
## เซ็ต
ขอพาคุณย้อนกลับไปที่บทเรียนคณิตศาสตร์สมัยประถมหรือมัธยมสักหน่อย นิยามทางคณิตศาสตร์ของเซ็ตสามารถนำมาใช้ใน Python ได้เช่นกัน เซ็ตคือกลุ่มของสมาชิกที่ไม่ซ้ำกัน ไม่มีลำดับ และไม่มีดัชนี ใน Python เซ็ตถูกใช้เพื่อเก็บรายการที่ไม่ซ้ำกัน และเป็นไปได้ที่จะหา *ยูเนียน (union)*, *อินเตอร์เซกชัน (intersection)*, *ผลต่าง (difference)*, *ผลต่างสมมาตร (symmetric difference)*, *ซับเซ็ต (subset)*, *ซูเปอร์เซ็ต (super set)* และ *ดิสจอยต์เซ็ต (disjoint set)* ระหว่างเซ็ตต่าง ๆ
### การสร้างเซ็ต
เราใช้วงเล็บปีกกา, {} เพื่อสร้างเซ็ต
* การสร้างเซ็ตว่างเปล่า
```py
# syntax
st = {} 
# or
st = set()
```
* การสร้างเซ็ตที่มีรายการเริ่มต้น
```py
# syntax
st = {'item1', 'item2', 'item3', 'item4'}
```
**ตัวอย่าง:**

```py
# syntax
fruits = {'banana', 'orange', 'mango', 'lemon'}
```
### การหาความยาวของเซ็ต
เราใช้เมธอด **len()** เพื่อหาความยาวของเซ็ต
```py
# syntax
st = {'item1', 'item2', 'item3', 'item4'}
len(set)
```
**ตัวอย่าง:**

```py
fruits = {'banana', 'orange', 'mango', 'lemon'}
len(fruits)
```
### การเข้าถึงรายการในเซ็ต
เราใช้ลูป (loop) เพื่อเข้าถึงรายการ เราจะพูดถึงเรื่องนี้ในหัวข้อลูป
### การตรวจสอบรายการ
หากต้องการตรวจสอบว่ารายการหนึ่งมีอยู่ในลิสต์หรือไม่ให้ใช้ *in*
```py
# syntax
st = {'item1', 'item2', 'item3', 'item4'}
'item3' in st
```
**ตัวอย่าง:**

```py
fruits = {'banana', 'orange', 'mango', 'lemon'}
'mango' in fruits
```
### การเพิ่มรายการเข้าไปในลิสต์
เมื่อสร้างลิสต์แล้วเราไม่สามารถเปลี่ยนรายการได้ แต่เราสามารถเพิ่มรายการเพิ่มเติมได้
* เพิ่มรายการเดียวโดยใช้ *add()*
```py
# syntax
st = {'item1', 'item2', 'item3', 'item4'}
st.add('item5')
```
**ตัวอย่าง:**
```py
fruits = {'banana', 'orange', 'mango', 'lemon'}
fruits.add('lime')
```
* เพิ่มหลายรายการโดยใช้ *update()*
```py
# syntax
st = {'item1', 'item2', 'item3', 'item4'}
st.update(['item5','item6','item7'])
```
**ตัวอย่าง:**
```py
fruits = {'banana', 'orange', 'mango', 'lemon'}
vegetables = ('Tomato', 'Potato', 'Cabbage','Onion', 'Carrot')
fruits.update(vegetables)
```
### การลบรายการออกจากลิสต์
เราสามารถลบรายการออกจากลิสต์โดยใช้เมธอด *remove()* ถ้าไม่พบรายการนั้น เมธอด *remove()* จะทำให้เกิด error ดังนั้นควรตรวจสอบก่อนว่ารายการนั้นมีอยู่หรือไม่ อย่างไรก็ตาม เมธอด *discard()* จะไม่ทำให้เกิด error
```py
# syntax
st = {'item1', 'item2', 'item3', 'item4'}
st.remove('item2")
```
**ตัวอย่าง:**
```py
fruits = {'banana', 'orange', 'mango', 'lemon'}
fruits.pop()
```
### การล้างรายการในเซ็ต
ถ้าเราต้องการล้างหรือทำให้เซ็ตว่างเปล่า เราใช้เมธอด *clear*
```py
# syntax
st = {'item1', 'item2', 'item3', 'item4'}
st.clear()
```
**ตัวอย่าง:**
```py
fruits = {'banana', 'orange', 'mango', 'lemon'}
fruits.clear()
```
### การลบเซ็ต
ถ้าเราต้องการลบเซ็ตทั้งหมด เราใช้ตัวดำเนินการ *del*
```py
# syntax
st = {'item1', 'item2', 'item3', 'item4'}
del set
```

**ตัวอย่าง:**
```py
fruits = {'banana', 'orange', 'mango', 'lemon'}
del fruits
```
### การแปลงลิสต์เป็นเซ็ต
เราสามารถแปลงลิสต์เป็นเซ็ตและแปลงเซ็ตกลับเป็นลิสต์ได้ การแปลงลิสต์เป็นเซ็ตจะลบรายการที่ซ้ำกันออกไป และจะเหลือไว้เฉพาะรายการที่ไม่ซ้ำกันเท่านั้น
```py
# syntax
lst = ['item1', 'item2', 'item3', 'item4', 'item1']
st = set(lst)  # {'item2', 'item4', 'item1', 'item3'}
```

**ตัวอย่าง:**
```py
fruits = ['banana', 'orange', 'mango', 'lemon','orange', 'banana']
fruits = set(fruits) # {'mango', 'lemon', 'banana', 'orange'}
```

### การรวมเซ็ตเข้าด้วยกัน
เราสามารถรวมเซ็ตสองอันเข้าด้วยกันโดยใช้เมธอด *union()* หรือ *update()*
* Union
เมธอดนี้คืนค่าเป็นเซ็ตใหม่

```py
# syntax
st1 = {'item1', 'item2', 'item3', 'item4'}
st2 = {'item5', 'item6', 'item7', 'item8'}
st3 = st1.union(st2)
```
**ตัวอย่าง:**
```py
fruits = {'banana', 'orange', 'mango', 'lemon'}
vegetables = {'Tomato', 'Potato', 'Cabbage','Onion', 'Carrot'}
fruits.union(vegetables) # {'lemon', 'Carrot', 'Tomato', 'banana', 'mango', 'orange', 'Cabbage', 'Potato', 'Onion'}
```
* Update
เมธอดนี้จะแทรกเซ็ตอีกอันหนึ่งเข้าไป

```py
# syntax
st1 = {'item1', 'item2', 'item3', 'item4'}
st2 = {'item5', 'item6', 'item7', 'item8'}
st1.update(st2)
```
**ตัวอย่าง:**
```py
fruits = {'banana', 'orange', 'mango', 'lemon'}
vegetables = {'Tomato', 'Potato', 'Cabbage','Onion', 'Carrot'}
fruits.update(vegetables)
print(fruits) # {'lemon', 'Carrot', 'Tomato', 'banana', 'mango', 'orange', 'Cabbage', 'Potato', 'Onion'}
```
### การหาส่วนร่วม (intersection)
Intersection คืนค่าเซ็ตของรายการที่มีอยู่ในทั้งสองเซ็ต ดูตัวอย่าง

```py
# syntax
st1 = {'item1', 'item2', 'item3', 'item4'}
st2 = {'item3', 'item2'}
st1.intersection(st2) # {'item3', 'item2'}
```
**ตัวอย่าง:**
```py
whole_numbers = {0, 1, 2, 3, 4, 5, 6, 7, 8, 10}
even_numbers = {0, 2, 4, 6, 8, 10}
whole_numbers.intersection(even_numbers) # {0, 2, 4, 6, 8, 10}

python = {'p', 'y', 't', 'o','n'}
dragon = {'d', 'r', 'a', 'g', 'o','n'}
python.intersection(dragon)     # {'o', 'n'}
```

### การตรวจสอบซับเซ็ตและซูเปอร์เซ็ต
เซ็ตหนึ่งสามารถเป็นซับเซ็ตหรือซูเปอร์เซ็ตของเซ็ตอื่นได้:
* Subset: *issubset()*
* Super set: *issuperset*

```py
# syntax
st1 = {'item1', 'item2', 'item3', 'item4'}
st2 = {'item2', 'item3'}
st2.issubset(st1) # True
st1.issuperset(st2) # True
```
**ตัวอย่าง:**
```py
whole_numbers = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
even_numbers = {0, 2, 4, 6, 8, 10}
whole_numbers.issubset(even_numbers) # False, because it is super set
whole_numbers.issuperset(even_numbers) # True

python = {'p', 'y', 't', 'o','n'}
dragon = {'d', 'r', 'a', 'g', 'o','n'}
python.issubset(dragon)     # False
```

### การตรวจสอบผลต่างระหว่างเซ็ตสองเซ็ต
มันคืนค่าผลต่างระหว่างเซ็ตสองเซ็ต

```py
# syntax
st1 = {'item1', 'item2', 'item3', 'item4'}
st2 = {'item2', 'item3'}
st2.difference(st1) # {'item1', 'item4'} => st1\st2
```
**ตัวอย่าง:**
```py
whole_numbers = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
even_numbers = {0, 2, 4, 6, 8, 10}
whole_numbers.difference(even_numbers) # {1, 3, 5, 7}

python = {'p', 'y', 't', 'o','n'}
dragon = {'d', 'r', 'a', 'g', 'o','n'}
python.difference(dragon)     # {'p', 'y', 't'}
dragon.difference(python)     # {'d', 'r', 'a', 'g'}
```

### การหาผลต่างสมมาตรระหว่างเซ็ตสองเซ็ต
มันคืนค่าผลต่างสมมาตรระหว่างเซ็ตสองเซ็ต หมายความว่ามันคืนค่าเซ็ตที่มีรายการทั้งหมดจากทั้งสองเซ็ต ยกเว้นรายการที่มีอยู่ในทั้งสองเซ็ต ในทางคณิตศาสตร์คือ: (A\B) U (B\A)

```py
# syntax
st1 = {'item1', 'item2', 'item3', 'item4'}
st2 = {'item2', 'item3'}
# it mean (A\B)U(B)
st2.symmetric_difference(st1) # {'item1', 'item4'}
```
**ตัวอย่าง:**
```py
whole_numbers = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
even_numbers = {1, 2, 3, 4, 5}
whole_numbers.symmetric_difference(even_numbers) # {0, 6, 7, 8, 9, 10}

python = {'p', 'y', 't', 'o','n'}
dragon = {'d', 'r', 'a', 'g', 'o','n'}
python.symmetric_difference(dragon)  # {'r', 't', 'p', 'y', 'g', 'a', 'd'}
```
### การรวมเซ็ต
ถ้าเซ็ตสองอันไม่มีรายการร่วมกัน เราเรียกว่าดิสจอยต์เซ็ต (disjoint set) เราสามารถตรวจสอบได้ว่าเซ็ตสองอันมีรายการร่วมกันหรือแยกจากกันโดยใช้เมธอด *isdisjoint()*

```py
# syntax
st1 = {'item1', 'item2', 'item3', 'item4'}
st2 = {'item2', 'item3'}
st2.isdisjoint(st1) # False
```
**ตัวอย่าง:**
```py
even_numbers = {0, 2, 4 ,6, 8}
even_numbers = {1, 3, 5, 7, 9}
even_numbers.isdisjoint(odd_numbers) # True, because no common item

python = {'p', 'y', 't', 'o','n'}
dragon = {'d', 'r', 'a', 'g', 'o','n'}
python.disjoint(dragon)  # False, there is common items {'o', 'n'}
```

## 💻 แบบฝึกหัด: วันที่ 7
```py
# sets
it_companies = {'Facebook', 'Google', 'Microsoft', 'Apple', 'IBM', 'Oracle', 'Amazon'}
A = {19, 22, 24, 20, 25, 26}
B = {19, 22, 20, 25, 26, 24, 28, 27}
age = [22, 19, 24, 25, 26, 24, 25, 24]
```
1. หาความยาวของเซ็ต it_companies
2. เพิ่ม 'Twitter' เข้าไปใน it_companies
3. แทรกบริษัท IT หลายบริษัทพร้อมกันเข้าไปในเซ็ต it_companies
4. ลบบริษัทหนึ่งออกจากเซ็ต it_companies
5. remove และ discard ต่างกันอย่างไร
6. รวม A กับ B เข้าด้วยกัน
7. หาส่วนร่วม (intersection) ของ A และ B
8. A เป็นซับเซ็ตของ B หรือไม่
9. A และ B เป็นดิสจอยต์เซ็ตหรือไม่
10. รวม A กับ B และ B กับ A
11. ผลต่างสมมาตรระหว่าง A และ B คืออะไร
12. ลบเซ็ตทั้งหมดออก
13. แปลงลิสต์ ages เป็นเซ็ต แล้วเปรียบเทียบความยาวของลิสต์และเซ็ต อันไหนมากกว่ากัน ?
14. อธิบายความแตกต่างระหว่างชนิดข้อมูลต่อไปนี้: string, list, tuple และ set
15. *I am a teacher and I love to inspire and teach people.* ประโยคนี้ใช้คำที่ไม่ซ้ำกันกี่คำ

# 📘 วันที่ 8
## ดิกชันนารี
ดิกชันนารีคือกลุ่มของชนิดข้อมูลแบบคู่ key-value ที่ไม่มีลำดับและสามารถแก้ไขได้ (mutable)
### การสร้างดิกชันนารี
หากต้องการสร้างดิกชันนารีเราใช้วงเล็บปีกกา, {}
```py
# syntax
empty_dict = {}
# Dictionary with data values
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
```
**ตัวอย่าง:**
```py
person = {
    'first_name':'Asabeneh',
    'last_name':'Yetayeh',
    'age':250,
    'country':'Finland',
    'is_marred':True,
    'skills':['JavaScript', 'React', 'Node', 'MongoDB', 'Python']
    'address':{
        'street':'Space street',
        'zipcode':'02210'
    }
    }
```

ดิกชันนารีข้างต้นแสดงให้เห็นว่าค่า (value) สามารถเป็นชนิดข้อมูลใดก็ได้: string, boolean, list, tuple, set หรือดิกชันนารี

### ความยาวของดิกชันนารี
มันตรวจสอบจำนวนคู่ key-value ในดิกชันนารี
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
print(len(dct)) # 4
```
**ตัวอย่าง:**
```py
person = {
    'first_name':'Asabeneh',
    'last_name':'Yetayeh',
    'age':250,
    'country':'Finland',
    'is_marred':True,
    'skills':['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address':{
        'street':'Space street',
        'zipcode':'02210'
    }
    }
print(len(person)) # 7

```

### การเข้าถึงรายการในดิกชันนารี
เราสามารถเข้าถึงรายการในดิกชันนารีได้โดยอ้างอิงถึงชื่อคีย์ของมัน
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
print(dct['key1']) # item1
print(dct['key4']) # item4
```
**ตัวอย่าง:**
```py
person = {
    'first_name':'Asabeneh',
    'last_name':'Yetayeh',
    'age':250,
    'country':'Finland',
    'is_marred':True,
    'skills':['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address':{
        'street':'Space street',
        'zipcode':'02210'
    }
    }
print(person['first_name']) # Asabeneh
print(person['country'])    # Finland
print(person['skills'])     # ['HTML','CSS','JavaScript', 'React', 'Node', 'MongoDB', 'Python']
print(person['city'])       # Error
```
การเข้าถึงรายการด้วยชื่อคีย์จะทำให้เกิด error ถ้าคีย์นั้นไม่มีอยู่ เพื่อหลีกเลี่ยง error นี้ ก่อนอื่นเราต้องตรวจสอบว่าคีย์นั้นมีอยู่หรือไม่ หรือเราสามารถใช้เมธอด _get_ ได้ เมธอด get จะคืนค่า None ซึ่งเป็นชนิดข้อมูล NoneType object
object if the data
```py
person = {
    'first_name':'Asabeneh',
    'last_name':'Yetayeh',
    'age':250,
    'country':'Finland',
    'is_marred':True,
    'skills':['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address':{
        'street':'Space street',
        'zipcode':'02210'
    }
    }
print(person.get('first_name')) # Asabeneh
print(person.get('country'))    # Finland
print(person.get('skills')) #['HTML','CSS','JavaScript', 'React', 'Node', 'MongoDB', 'Python']
print(person.get('city'))   # None
```

### การเพิ่มรายการเข้าไปในดิกชันนารี

เราสามารถเพิ่มคู่คีย์และค่าใหม่เข้าไปในดิกชันนารีได้

```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
dct['key5'] = 'item5'
```
**ตัวอย่าง:**

```py
person = {
    'first_name':'Asabeneh',
    'last_name':'Yetayeh',
    'age':250,
    'country':'Finland',
    'is_marred':True,
    'skills':['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address':{
        'street':'Space street',
        'zipcode':'02210'
        }
}
person['job_title'] = 'Instructor'
person['skills'].append('HTML')
print(person)
```

### การแก้ไขรายการในดิกชันนารี
เราสามารถเพิ่มหรือแก้ไขรายการในดิกชันนารีได้
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
dct['key1'] = 'item-one'
```
**ตัวอย่าง:**
```py
person = {
    'first_name':'Asabeneh',
    'last_name':'Yetayeh',
    'age':250,
    'country':'Finland',
    'is_marred':True,
    'skills':['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address':{
        'street':'Space street',
        'zipcode':'02210'
    }
    }
person['first_name'] = 'Eyob'
person['age']
```

### การตรวจสอบคีย์ในดิกชันนารี
เราใช้ตัวดำเนินการ _in_ เพื่อตรวจสอบว่าคีย์หนึ่งมีอยู่ในดิกชันนารีหรือไม่
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
print('key2' in dct) # True
print('key5' in dct) # False
```

### การลบรายการที่เป็นคีย์ออกจากดิกชันนารี

- _pop(key)_: ลบรายการที่มีชื่อคีย์ที่ระบุ:
- _popitem()_: ลบรายการล่าสุด
- _del_: ลบรายการที่มีชื่อคีย์ที่ระบุ

```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
dct.pop('key1') # the first key pair removed
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
dct.popitem() # remove the last item
del dct['key2'] # remove key 2 item
```

**ตัวอย่าง:**

```py
person = {
    'first_name':'Asabeneh',
    'last_name':'Yetayeh',
    'age':250,
    'country':'Finland',
    'is_marred':True,
    'skills':['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address':{
        'street':'Space street',
        'zipcode':'02210'
    }
    }
person.pop('first_name')        # Remove the firstname item
person.popitem()                # Remove the lastname item
del person['is_married']        # Remove the is_married item
```

### การเปลี่ยนดิกชันนารีเป็นรายการในลิสต์
เมธอด *items()* เปลี่ยนดิกชันนารีให้เป็นลิสต์ของทูเพิล
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
print(dct.items()) # dict_items([('key1', 'item1'), ('key2', 'item2'), ('key3', 'item3'), ('key4', 'item4')])
```
### การล้างรายการในลิสต์ของดิกชันนารี
ถ้าเราไม่ต้องการรายการในดิกชันนารีอีกต่อไป เราสามารถล้างรายการเหล่านั้นได้โดยใช้เมธอด _clear()_
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
print(dct.clear()) # {}
```
### การลบดิกชันนารี
ถ้าเราไม่ใช้ดิกชันนารีนั้นแล้ว เราสามารถลบมันทั้งหมดได้
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
del dct
```
### การคัดลอกดิกชันนารี
เราคัดลอกดิกชันนารีโดยใช้เมธอด _copy()_ การใช้ copy จะช่วยหลีกเลี่ยงการเปลี่ยนแปลง (mutation) ของดิกชันนารีต้นฉบับ
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
dct_copy = dct.copy() # {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
```
### การรับคีย์ของดิกชันนารีเป็นลิสต์
เมธอด _keys()_ ให้เราได้คีย์ทั้งหมดของดิกชันนารีในรูปแบบลิสต์
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
keys = dct.keys()
print(keys)     # dict_keys(['key1', 'key2', 'key3', 'key4'])
```
### การรับค่าของดิกชันนารีเป็นลิสต์
เมธอด _values_ ให้เราได้ค่าทั้งหมดของดิกชันนารีในรูปแบบลิสต์
```py
# syntax
dct = {'key1':'item1', 'key2':'item2', 'key3':'item3', 'key4':'item4'}
values = dct.values()
print(values)     # dict_values(['item1', 'item2', 'item3', 'item4'])
```
## 💻 แบบฝึกหัด: วันที่ 8
1. สร้างดิกชันนารีว่างเปล่าชื่อ dog
2. เพิ่ม name, color, breed, legs, age เข้าไปในดิกชันนารี dog
3. สร้างดิกชันนารี student และเพิ่ม first_name, last_name, gender, age, marital status, skills, country, city และ address เป็นคีย์ของดิกชันนารี
4. หาความยาวของดิกชันนารี student
5. รับค่าของ skills และตรวจสอบชนิดข้อมูล ควรจะเป็นลิสต์
6. แก้ไขค่า skills โดยเพิ่มทักษะหนึ่งหรือสองทักษะเข้าไป
7. รับคีย์ของดิกชันนารีในรูปแบบลิสต์
8. รับค่าของดิกชันนารีในรูปแบบลิสต์
9. เปลี่ยนดิกชันนารีให้เป็นลิสต์ของทูเพิลโดยใช้เมธอด *items()*
10. ลบรายการหนึ่งในดิกชันนารีออก
11. ลบดิกชันนารีทั้งหมด


# 📘 วันที่ 9
## เงื่อนไข (Conditionals)
โดยปกติแล้ว คำสั่งในสคริปต์ Python จะถูกรันตามลำดับจากบนลงล่าง หากตรรกะการประมวลผลต้องการ ลำดับการรันแบบตามลำดับสามารถถูกเปลี่ยนแปลงได้ 2 วิธี:
* การรันแบบมีเงื่อนไข (Conditional execution): บล็อกของคำสั่งหนึ่งคำสั่งหรือมากกว่าจะถูกรันถ้านิพจน์บางอย่างเป็นจริง
* การรันแบบซ้ำ (Repetitive execution): บล็อกของคำสั่งหนึ่งคำสั่งหรือมากกว่าจะถูกรันซ้ำ ๆ ตราบใดที่นิพจน์บางอย่างยังเป็นจริงอยู่ ในหัวข้อนี้เราจะพูดถึงคำสั่ง *if*, *else*, *elif* ตัวดำเนินการเปรียบเทียบและตัวดำเนินการทางตรรกะที่เราเรียนไปในหัวข้อก่อนหน้าจะมีประโยชน์ในที่นี้

### เงื่อนไข If
ใน Python และภาษาโปรแกรมมิงอื่น ๆ คำสำคัญ *if* ใช้เพื่อตรวจสอบว่าเงื่อนไขเป็นจริงหรือไม่ และเพื่อรันบล็อกโค้ด อย่าลืม indentation หลังเครื่องหมายโคลอน
```py
# syntax
if condition:
    this part of code run for truthy condition
```
**ตัวอย่าง:**
```py
a = 3
if a > 0:
    print('A is a positive number')
# a is a positive number
```
ดังที่คุณเห็นในเงื่อนไขข้างต้น 3 มากกว่า 0 และเป็นจำนวนบวก เงื่อนไขเป็นจริงและบล็อกโค้ดจึงถูกรัน อย่างไรก็ตาม ถ้าเงื่อนไขเป็นเท็จ เราจะไม่เห็นผลลัพธ์ใด ๆ เพื่อจะเห็นผลลัพธ์ของเงื่อนไขที่เป็นเท็จ เราควรมีอีกบล็อกหนึ่ง ซึ่งก็คือ *else*

### If Else
ถ้าเงื่อนไขเป็นจริง บล็อกแรกจะถูกรัน ถ้าไม่เป็นจริง เงื่อนไข else จะถูกรันแทน
```py
# syntax
if condition:
    this part of code run for truthy condition
else:
     this part of code run for false condition
```
**ตัวอย่าง:**
```py
a = 3
if a < 0:
    print('A is a positive number')
else:
    print('A is a negative number')
```
เงื่อนไขข้างต้นเป็นเท็จ ดังนั้นบล็อก else จึงถูกรัน แล้วถ้าเงื่อนไขของเรามีมากกว่าสองอย่างล่ะ ? เราจะใช้ *elif*
### If elif else
ในชีวิตประจำวันของเรา เราตัดสินใจกันทุกวัน เราไม่ได้ตัดสินใจโดยตรวจสอบเงื่อนไขเพียงหนึ่งหรือสองอย่าง แต่ตรวจสอบหลายเงื่อนไข เช่นเดียวกับชีวิต การเขียนโปรแกรมก็เต็มไปด้วยเงื่อนไขเช่นกัน เราใช้ *elif* เมื่อเรามีหลายเงื่อนไข
```py
# syntax
if condition:
    code
elif condition:
    code
else:
    code

```
**ตัวอย่าง:**
```py
a = 0
if a > 0:
    print('A is a positive number')
elif a < 0:
    print('A is a negative number')
else:
    print('A is zero')
```
### รูปแบบย่อ (Short Hand)

```py
# syntax
code if condition else code
```
**ตัวอย่าง:**
```py
a = 3
print('A is positive') if a > 0 else print('A is negative')
```

### เงื่อนไขซ้อน (Nested condition)
เงื่อนไขสามารถซ้อนกันได้
```py
# syntax
if condition:
    code
    if condition:
    code
```
**ตัวอย่าง:**
```py
a = 0
if a > 0:
    if a % 2 == 0:
        print('A is positive even integer')
    else:
        print('A positive number')
elif a == 0:
    print('Zero')
else:
    print('A negative number')

```
เราสามารถหลีกเลี่ยงการเขียนเงื่อนไขซ้อนได้โดยใช้ตัวดำเนินการทางตรรกะ *and*

### เงื่อนไข if กับตัวดำเนินการทางตรรกะ and
```py
# syntax
if condition and condition:
    code
```
**ตัวอย่าง:**
```py
a = 0
if a > 0 and a % 2 == 0:
        print('A is even positive integer')
elif a > 0 and a % 2 !== 0:
     print('A is positive integer') 
elif a == 0:
    print('Zero')
else:
    print('A negative number')
```
### เงื่อนไข if กับตัวดำเนินการทางตรรกะ or
```py
# syntax
if condition or condition:
    code
```
**ตัวอย่าง:**
```py
a = 0
if a > 0 or  % 2 == 0:
        print('A is positive integer')
elif a == 0:
    print('Zero')
else:
    print('A negative number')
```

## 💻 แบบฝึกหัด: วันที่ 9
1. รับค่าจากผู้ใช้โดยใช้ input("Enter your age:") ถ้าผู้ใช้อายุ 18 ปีขึ้นไป ให้แสดงข้อความว่า You are old enough to drive แต่ถ้าอายุไม่ถึง 18 ปี ให้แสดงข้อความบอกว่าต้องรออีกกี่ปี ผลลัพธ์:
    ```sh
    Enter your age: 30
    You are old enough to drive.
    Output:
    Enter your age:15
    You are left with 3 years to drive.
    ```
1. เปรียบเทียบค่าของ my_age และ your_age โดยใช้ if … else จากการเปรียบเทียบให้พิมพ์ว่าใครอายุมากกว่ากัน (ฉันหรือคุณ) ใช้ input("Enter your age:") เพื่อรับค่าอายุ ผลลัพธ์:
    ```sh
    Enter your age: 30
    You are 5 years older than me.
    ```
1. รับตัวเลขสองตัวจากผู้ใช้โดยใช้ input prompt ถ้า a มากกว่า b ให้คืนค่าว่า a มากกว่า b ถ้า a น้อยกว่า b ให้คืนค่าว่า a น้อยกว่า b มิฉะนั้น a เท่ากับ b ผลลัพธ์:
    ```sh
    Enter number one: 4
    Enter number two: 3
    4 is greater than 3
    ```
1. เขียนโค้ดที่ให้เกรดแก่นักเรียนตามคะแนนของพวกเขา:
    ```sh
    90-100, A
    80-89, B
    70-79, C
    60-69, D
    0-59, F
    ```
1. ตรวจสอบว่าฤดูกาลคือฤดูใบไม้ร่วง ฤดูหนาว ฤดูใบไม้ผลิ หรือฤดูร้อน ถ้าผู้ใช้ป้อน:
เดือนกันยายน ตุลาคม หรือพฤศจิกายน ฤดูกาลคือฤดูใบไม้ร่วง
เดือนธันวาคม มกราคม หรือกุมภาพันธ์ ฤดูกาลคือฤดูหนาว
เดือนมีนาคม เมษายน หรือพฤษภาคม ฤดูกาลคือฤดูใบไม้ผลิ
เดือนมิถุนายน กรกฎาคม หรือสิงหาคม ฤดูกาลคือฤดูร้อน
1. ลิสต์ต่อไปนี้มีผลไม้บางชนิด:
    ```sh
    fruits = ['banana', 'orange', 'mango', 'lemon']
    ```
    ถ้าผลไม้ชนิดหนึ่งไม่มีอยู่ในลิสต์ ให้เพิ่มผลไม้นั้นเข้าไปในลิสต์และพิมพ์ลิสต์ที่แก้ไขแล้ว แต่ถ้าผลไม้นั้นมีอยู่แล้ว ให้พิมพ์ 'A fruit already exist in the list'
1. ที่นี่เรามีดิกชันนารี person
    ```py
    person = {
    'first_name':'Asabeneh',
    'last_name':'Yetayeh',
    'age':250,
    'country':'Finland',
    'is_marred':True,
    'skills':['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address':{
        'street':'Space street',
        'zipcode':'02210'
    }
    }
    ```
* ตรวจสอบว่าดิกชันนารี person มี skills อยู่หรือไม่ ถ้ามีคีย์ skills ให้ตรวจสอบและพิมพ์ทักษะที่อยู่ตรงกลางในลิสต์ skills
* ตรวจสอบว่าดิกชันนารี person มี skills อยู่หรือไม่ ถ้ามีคีย์ skills ให้ตรวจสอบว่ามีทักษะ 'Python' หรือไม่ และพิมพ์ทักษะนั้น
* ถ้าทักษะของบุคคลนั้นมีเพียง JavaScript และ React ให้พิมพ์ 'He is a front end developer' ถ้าทักษะมี Node, Python, MongoDB ให้พิมพ์ 'He is a backend developer' ถ้าทักษะมี React, Node และ MongoDB ให้พิมพ์ 'He is a fullstack developer' มิฉะนั้นให้พิมพ์ 'unknown title'
* ถ้าบุคคลนั้นแต่งงานแล้วและอาศัยอยู่ในฟินแลนด์ ให้พิมพ์ข้อความต่อไปนี้:
    ```py
    Asabeneh Yetayeh lives in Finland. He is married.
    ```
[<< ตอนที่ 2](day4-6.md) | [ตอนที่ 4 >>](day10-12.md)
***
