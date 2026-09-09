# 🐍 30 วัน พื้นฐาน Python

|# วัน | หัวข้อ                                                    |
|------|:---------------------------------------------------------:|
| 01  |  [บทนำ](./readme.md)|
| 02  |  [ตัวแปร, ฟังก์ชันในตัว](./02_Day_Variables_builtin_functions/02_variables_builtin_functions.md)|
| 03  |  [ตัวดำเนินการ](./03_Day_Operators/03_operators.md)|
| 04  |  [สตริง](./04_Day_Strings/04_strings.md)|
| 05  |  [ลิสต์](./05_Day_Lists/05_lists.md)|
| 06  |  [ทูเพิล](./06_Day_Tuples/06_tuples.md)|
| 07  |  [เซ็ต](./07_Day_Sets/07_sets.md)|
| 08  |  [ดิกชันนารี](./08_Day_Dictionaries/08_dictionaries.md)|
| 09  |  [เงื่อนไข](./09_Day_Conditionals/09_conditionals.md)|
| 10  |  [ลูป](./10_Day_Loops/10_loops.md)|
| 11  |  [ฟังก์ชัน](./11_Day_Functions/11_functions.md)|
| 12  |  [โมดูล](./12_Day_Modules/12_modules.md)|
| 13  |  [List Comprehension](./13_Day_List_comprehension/13_list_comprehension.md)|
| 14  |  [ฟังก์ชันลำดับสูง](./14_Day_Higher_order_functions/14_higher_order_functions.md)|
| 15  |  [ชนิดของ Error ใน Python](./15_Day_Python_type_errors/15_python_type_errors.md)|
| 16 |  [วันที่และเวลาใน Python](./16_Day_Python_date_time/16_python_datetime.md) |
| 17 |  [การจัดการข้อผิดพลาด](./17_Day_Exception_handling/17_exception_handling.md)|
| 18 |  [Regular Expressions](./18_Day_Regular_expressions/18_regular_expressions.md)|
| 19 |  [การจัดการไฟล์](./19_Day_File_handling/19_file_handling.md)|
| 20 |  [ตัวจัดการแพ็กเกจ Python](./20_Day_Python_package_manager/20_python_package_manager.md)|
| 21 |  [คลาสและอ็อบเจ็กต์](./21_Day_Classes_and_objects/21_classes_and_objects.md)|
| 22 |  [Web Scraping](./22_Day_Web_scraping/22_web_scraping.md)|
| 23 |  [Virtual Environment](./23_Day_Virtual_environment/23_virtual_environment.md)|
| 24 |  [สถิติ](./24_Day_Statistics/24_statistics.md)|
| 25 |  [Pandas](./25_Day_Pandas/25_pandas.md)|
| 26 |  [Python เว็บ](./26_Day_Python_web/26_python_web.md)|
| 27 |  [Python ร่วมกับ MongoDB](./27_Day_Python_with_mongodb/27_python_with_mongodb.md)|
| 28 |  [API](./28_Day_API/28_API.md)|
| 29 |  [การสร้าง API](./29_Day_Building_API/29_building_API.md)|
| 30 |  [บทสรุป](./30_Day_Conclusions/30_conclusions.md)|

<small>🧡🧡🧡 ขอให้มีความสุขกับการเขียนโค้ด 🧡🧡🧡</small>

---

<div>
<h2>💖 ผู้สนับสนุน</h2>

โลโก้บริษัทของคุณจะแสดงที่นี่

</div>

### 🙌 เป็นผู้สนับสนุน

คุณสามารถสนับสนุนโปรเจกต์นี้ได้โดยการเป็นผู้สนับสนุนบน **[GitHub Sponsors](https://github.com/sponsors/asabeneh)** หรือผ่าน [PayPal](https://www.paypal.me/asabeneh)

ทุกการมีส่วนร่วม ไม่ว่าจะมากหรือน้อย ล้วนสร้างความแตกต่างอย่างยิ่งใหญ่ ขอบคุณสำหรับการสนับสนุนของคุณ! 🌟

---

<div align="center">
  <h1>30 วัน พื้นฐาน Python: วันที่ 1 - บทนำ</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

  <sub>ผู้แต่ง:
  <a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
  <small>ฉบับปรับปรุงครั้งที่ 2: กรกฎาคม, 2021</small>
  </sub>
</div>

🇧🇷 [โปรตุเกส](./Portuguese/README.md)
🇨🇳 [จีน](./Chinese/README.md)
🇫🇷[ฝรั่งเศส](./French/README_fr.md)
[วันที่ 2 >>](./02_Day_Variables_builtin_functions/02_variables_builtin_functions.md)

![30DaysOfPython](./images/30DaysOfPython_banner3@2x.png)

- [🐍 30 วัน พื้นฐาน Python](#-30-วัน-พื้นฐาน-python)
    - [🙌 เป็นผู้สนับสนุน](#-เป็นผู้สนับสนุน)
- [📘 วันที่ 1](#-วันที่-1)
  - [ยินดีต้อนรับ](#ยินดีต้อนรับ)
  - [บทนำ](#บทนำ)
  - [ทำไมต้อง Python ?](#ทำไมต้อง-python-)
  - [การตั้งค่าสภาพแวดล้อม](#การตั้งค่าสภาพแวดล้อม)
    - [การติดตั้ง Python](#การติดตั้ง-python)
    - [Python Shell](#python-shell)
    - [การติดตั้ง Visual Studio Code](#การติดตั้ง-visual-studio-code)
      - [วิธีใช้งาน Visual Studio Code](#วิธีใช้งาน-visual-studio-code)
  - [พื้นฐาน Python](#พื้นฐาน-python)
    - [ไวยากรณ์ของ Python](#ไวยากรณ์ของ-python)
    - [การเว้นวรรคใน Python](#การเว้นวรรคใน-python)
    - [คอมเมนต์](#คอมเมนต์)
    - [ชนิดข้อมูล](#ชนิดข้อมูล)
      - [ตัวเลข](#ตัวเลข)
      - [สตริง](#สตริง)
      - [บูลีน](#บูลีน)
      - [ลิสต์](#ลิสต์)
      - [ดิกชันนารี](#ดิกชันนารี)
      - [ทูเพิล](#ทูเพิล)
      - [เซ็ต](#เซ็ต)
    - [การตรวจสอบชนิดข้อมูล](#การตรวจสอบชนิดข้อมูล)
    - [ไฟล์ Python](#ไฟล์-python)
  - [💻 แบบฝึกหัด - วันที่ 1](#-แบบฝึกหัด---วันที่-1)
    - [แบบฝึกหัด: ระดับ 1](#แบบฝึกหัด-ระดับ-1)
    - [แบบฝึกหัด: ระดับ 2](#แบบฝึกหัด-ระดับ-2)
    - [แบบฝึกหัด: ระดับ 3](#แบบฝึกหัด-ระดับ-3)

---

# 📘 วันที่ 1

## ยินดีต้อนรับ

**ขอแสดงความยินดี** ที่คุณตัดสินใจเข้าร่วมความท้าทายการเขียนโปรแกรม _30 วันกับ Python_ ในความท้าทายนี้ คุณจะได้เรียนรู้ทุกสิ่งที่จำเป็นในการเป็นโปรแกรมเมอร์ Python และแนวคิดทั้งหมดของการเขียนโปรแกรม เมื่อจบความท้าทายนี้ คุณจะได้รับใบประกาศนียบัตร _30DaysOfPython_

หากคุณต้องการมีส่วนร่วมอย่างจริงจังในความท้าทายนี้ คุณสามารถเข้าร่วมกลุ่ม Telegram [30DaysOfPython challenge](https://t.me/ThirtyDaysOfPython)

## บทนำ

Python เป็นภาษาโปรแกรมระดับสูงสำหรับการเขียนโปรแกรมทั่วไป เป็นภาษาโอเพนซอร์ส, แบบตีความ, และเชิงวัตถุ Python ถูกสร้างขึ้นโดยโปรแกรมเมอร์ชาวดัตช์ชื่อ Guido van Rossum ชื่อของภาษาโปรแกรม Python มาจากซีรีส์ตลกสเก็ตช์ของอังกฤษ *Monty Python's Flying Circus* เวอร์ชันแรกถูกเผยแพร่เมื่อวันที่ 20 กุมภาพันธ์ ค.ศ. 1991 ความท้าทาย 30 วันกับ Python นี้จะช่วยให้คุณเรียนรู้ Python เวอร์ชันล่าสุดอย่าง Python 3 ทีละขั้นตอน หัวข้อถูกแบ่งออกเป็น 30 วัน โดยแต่ละวันประกอบด้วยหลายหัวข้อพร้อมคำอธิบายที่เข้าใจง่าย ตัวอย่างจากโลกแห่งความจริง และแบบฝึกหัดปฏิบัติมากมาย

ความท้าทายนี้ออกแบบมาสำหรับผู้เริ่มต้นและมืออาชีพที่ต้องการเรียนรู้ภาษาโปรแกรม Python อาจใช้เวลา 30 ถึง 100 วันในการทำความท้าทายนี้ให้สำเร็จ ผู้ที่เข้าร่วมในกลุ่ม Telegram อย่างแข็งขันมีโอกาสสูงที่จะทำความท้าทายนี้สำเร็จ

ความท้าทายนี้อ่านง่าย เขียนด้วยภาษาอังกฤษแบบสนทนา น่าสนใจ กระตุ้น และในขณะเดียวกันก็ท้าทายมาก คุณต้องจัดสรรเวลามากพอเพื่อทำความท้าทายนี้ให้เสร็จ หากคุณเป็นผู้เรียนที่ชอบการมองเห็น คุณอาจรับชมบทเรียนวิดีโอได้ที่ช่อง YouTube <a href="https://www.youtube.com/channel/UC7PNRuno1rzYPb1xLa4yktw"> Washera</a> คุณอาจเริ่มจาก [วิดีโอ Python สำหรับผู้เริ่มต้นอย่างแท้จริง](https://youtu.be/OCCWZheOesI) สมัครสมาชิกช่อง แสดงความคิดเห็น และถามคำถามในวิดีโอ YouTube และกระตือรือร้น ผู้เขียนจะสังเกตเห็นคุณในที่สุด

ผู้เขียนชอบที่จะได้ยินความคิดเห็นของคุณเกี่ยวกับความท้าทายนี้ แบ่งปันความคิดของคุณเกี่ยวกับความท้าทาย 30DaysOfPython คุณสามารถแสดงความคิดเห็นของคุณได้ที่ [ลิงก์นี้](https://www.asabeneh.com/testimonials)

## ทำไมต้อง Python ?

เป็นภาษาโปรแกรมที่ใกล้เคียงกับภาษามนุษย์มาก และด้วยเหตุนี้ จึงง่ายต่อการเรียนรู้และใช้งาน Python ถูกใช้โดยอุตสาหกรรมและบริษัทต่างๆ (รวมถึง Google) มันถูกใช้เพื่อพัฒนาเว็บแอปพลิเคชัน แอปพลิเคชันเดสก์ท็อป การดูแลระบบ และไลบรารีแมชชีนเลิร์นนิง Python เป็นภาษาที่ได้รับการยอมรับอย่างสูงในชุมชนวิทยาศาสตร์ข้อมูลและแมชชีนเลิร์นนิง ฉันหวังว่านี่จะเพียงพอที่จะโน้มน้าวให้คุณเริ่มเรียนรู้ Python Python กำลังครองโลก และคุณกำลังทำลายมันก่อนที่มันจะกินคุณ

## การตั้งค่าสภาพแวดล้อม

### การติดตั้ง Python

ในการรันสคริปต์ Python คุณต้องติดตั้ง Python ก่อน มาที่ [ดาวน์โหลด](https://www.python.org/) Python กัน
หากคุณเป็นผู้ใช้ Windows ให้คลิกปุ่มที่วงกลมด้วยสีแดง

[![การติดตั้งบน Windows](./images/installing_on_windows.png)](https://www.python.org/)

หากคุณเป็นผู้ใช้ macOS ให้คลิกปุ่มที่วงกลมด้วยสีแดง

[![การติดตั้งบน Windows](./images/installing_on_macOS.png)](https://www.python.org/)

เพื่อตรวจสอบว่าติดตั้ง Python แล้วหรือไม่ ให้เขียนคำสั่งต่อไปนี้บนเทอร์มินัลของอุปกรณ์ของคุณ

```shell
python3 --version
