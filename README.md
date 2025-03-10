![Image](https://github.com/user-attachments/assets/441ac8ee-2ef2-46a6-a387-4079ddb9cee9) 

การทำงานของ Ui คือ เราสามารถจิ้มไปที่ตัวรูปของกาเเฟ เพื่้อสามารถสั่งกาเเฟได้ โดยที่สามารถเลือกได้ 4 อย่าง คาปูชิโน่ ลาเต้ มอคค่า อเมริกาโน่ 

โดยที่เราสามารถเลือกจำนวนของกาเเฟได้ เเล้วจะคิดเป็นสินค้า ราคา จำนวนของสินค้าในตารางหลังกดสั่งที่รูป ถ้าสั่งหมดก็จะรวมเป็นค่าเดียวตรง Total 


![Image](https://github.com/user-attachments/assets/c25d9592-f961-4828-a418-7d92e04ec18d)



 GPACalculator
![Image](https://github.com/user-attachments/assets/25ba4abf-a699-403b-b9d4-6e21b7ea8e12) 

**Form1** เป็น UI หลักที่รับค่า **GPAX** จากผู้ใช้และเรียกใช้คลาส `GPACalculator`
- **GPACalculator** เป็นคลาสที่ใช้จัดการข้อมูล **GPAX** คำนวณค่าเฉลี่ย ค่ามากที่สุด ค่าต่ำสุด และจำนวนรายการที่ป้อน
- **ความสัมพันธ์ (Association)** ระหว่าง `Form1` และ `GPACalculator` เป็นแบบ **uses** เนื่องจาก `Form1` ใช้งาน `GPACalculator` เพื่อประมวลผลข้อมูล
