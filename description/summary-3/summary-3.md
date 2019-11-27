# แนวคำตอบ โจทย์ปัญหาชวนคิดชุดที่ 3

### 1. นิพจน์ (Expression) หมายถึงอะไร
#### แนวคำตอบ

**นิพจน์ (Expression)** ทางคณิตศาสตร์นั้นเป็นนิพจน์ในการคำนวณ ซึ่งนิพจน์ทางคณิตศาสตร์นั้นจะมีรูปแบบเหมือนกับสมการคณิตศาสตร์ แต่จะประกอบไปด้วย ค่าคงที่ หรือ ตัวแปร ซึ่งเรียกอีกอย่างหนึ่งว่า ตัวถูกดำเนินการ (Operand) แล้วเชื่อมกันด้วยเครื่องหมายทางคณิตศาสตร์ หรือเรียกอีกอย่างหนึ่งว่า ตัวดำเนินการ (Operator) นั่นเอง

---

### 2. จงเรียงลำดับความสำคัญของตัวดำเนินการ (Operators) จากลำดับความสำคัญสูงสุดไปยังความสำคัญต่ำสุด
    && , ||, ! , % , += , < , != , +

#### แนวคำตอบ

เรียงลำดับความสำคัญได้ดังนี้

    1. !
    2. %
    3. +
    4. <
    5. !=
    6. &&
    7. ||
    8. +=
    
---
### 3. จงนำค่าที่กำหนดให้ต่อไปนี้ไประบุค่าให้กับตัวแปรเพื่อใช้งานให้ถูกต้อง
#### แนวคำตอบ
    3.1 i*j++ ผลลัพธ์คือ 20 และ j คือ 3
    3.2 i*++j ผลลัพธ์คือ 30 และ j คือ 3 
    3.3 i*j-- ผลลัพธ์คือ 20 และ j คือ 1
    3.4 i*--j ผลลัพธ์คือ 10 และ j คือ 1
#### ที่มาของแนวคำตอบ
- [src/summary-3/3-3.c](https://github.com/Vixolence/jetavat-c-answer/blob/master/src/summary-3/3-3.c)
    
---
### 4. ถ้าต้องการเขียนโปรแกรมทำงานกับรูปแบบข้อมูลต่อไปนี้ ควรประกาศชนิดใดเพื่อใช้งาน (ตัวอักษร, ข้อความ, เลขจำนวนเต็ม หรือ เลขจำนวนจริง)
#### แนวคำตอบ
    4.1 (10 != 5) && (7 <= 7) ผลลัพธ์คือ จริง
    4.2 (2 < 5) || (9 <= 7)   ผลลัพธ์คือ จริง
    4.3 (8 == 8) && !(3 > 2)  ผลลัพธ์คือ เท็จ

#### คำอธิบายแนวคำตอบ
    4.1 (10 != 5) เป็นจริง
        (7 <= 7)  เป็นจริง 
        เชื่อมด้วย && ("และ" ในทางตรรกศาสตร์)

        จะได้ จริง และ จริง => จริง
    -------------------------------------
    4.2 (2 < 5)  เป็นจริง
        (9 <= 7) เป็นเท็จ
        เชื่อมด้วย || ("หรือ" ในทางตรรกศาสตร์)

        จะได้ จริง หรือ เท็จ => จริง
    -------------------------------------
    4.3 (8 == 8) เป็นจริง
        !(3 > 2) เป็นเท็จ (ติด ! ซึ่งไปทางนิเสธ)
        เชื่อมด้วย && ("และ" ในทางตรรกศาสตร์)

        จะได้ จริง และ เท็จ => เท็จ
#### ที่มาของแนวคำตอบ
- [src/summary-3/3-4.c](https://github.com/Vixolence/jetavat-c-answer/blob/master/src/summary-3/3-4.c)
---
### 5. จงลำดับความสำคัญของนิพจน์ต่อไปนี้

###### *ขอสงวนสิทธิ์ ให้แนวคำตอบเพียงความสำคัญแบบข้อความ* ######

##### 5.1. (A + B) * C
###### แนวคำตอบ

    1. (A + B) --- (1)
    2  (1) * C --- (2)

##### 5.2. A + B / C * D
###### แนวคำตอบ

    1. B / C --- (1)
    2. (1) * D --- (2)
    3. (2) + A --- (3)

##### 5.3. A - ( B - C ) * D - E
###### แนวคำตอบ

    1. - (B - C) --- (1)
    2. (1) * D --- (2)
    3. (2) + A --- (3)
    4. (3) - E --- (4)

##### 5.4. A + ( B - ( C + D ) ) * E / 2
###### แนวคำตอบ
    
    1. - (C + D) --- (1)
    2. (1) + B --- (2)
    3. (2) * E --- (3)
    4. (3) / 2 --- (4)
    5. (4) + A --- (5)

##### 5.5 A / B * C % D
    1. A / B --- (1)
    2. (1) * C --- (2)
    3. (2) % D --- (3)

---