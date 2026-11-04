CPU Scheduling Simulator Operating Systems

รายวิชา: CS422 Operating Systems (OS)

1.Project Overview
      CPU Scheduling Simulator เป็นโปรแกรมจำลองการจัดตารางการทำงานของ CPU (CPU Scheduling) ที่พัฒนาขึ้นเพื่อศึกษาและทำความเข้าใจหลักการทำงานของอัลกอริทึมการจัดตาราง CPU ในระบบปฏิบัติการ (Operating Systems)
      
       โปรแกรมช่วยให้ผู้ใช้งานสามารถกำหนดจำนวน Process และ Burst Time ของแต่ละ Process จากนั้นเลือกอัลกอริทึมที่ต้องการทดสอบ เพื่อแสดงลำดับการทำงานผ่าน Gantt Chart พร้อมคำนวณค่าต่าง ๆ ที่เกี่ยวข้อง เช่น Start Time, Completion Time, Turnaround Time และ Waiting Time

      โปรแกรมรองรับอัลกอริทึมทั้งหมด 3 รูปแบบ ได้แก่ FCFS, SJF (Non-preemptive) และ Round Robin (RR) โดยผู้ใช้งานสามารถเปรียบเทียบผลลัพธ์ของแต่ละอัลกอริทึมได้

2.Project Objectives
•	เพื่อศึกษาและทำความเข้าใจหลักการทำงานของ CPU Scheduling ในระบบปฏิบัติการ
•	เพื่อพัฒนาโปรแกรมจำลองการจัดตารางการทำงานของ CPU
เพื่อศึกษาความแตกต่างของอัลกอริทึม FCFS, SJF และ Round Robin
•	เพื่อฝึกการคำนวณค่า Waiting Time และ Turnaround Time
เพื่อแสดงผลการทำงานของแต่ละอัลกอริทึมผ่าน Gantt Chart
เพื่อเปรียบเทียบประสิทธิภาพของอัลกอริทึมผ่านค่าเฉลี่ย Waiting Time และ Turnaround Time

3.Program Features โปรแกรมมีความสามารถดังต่อไปนี้
1.	กำหนดจำนวน Process ที่ต้องการทดสอบได้
2.	กำหนด Burst Time (BT) ของแต่ละ Process ได้ด้วยตนเอง
สามารถสุ่มค่า Burst Time สำหรับการทดสอบได้
3.	กำหนด Arrival Time (AT) เท่ากับ 0 สำหรับทุก Process ตามเงื่อนไขของโปรแกรม
4.	รองรับอัลกอริทึม FCFS, SJF และ Round Robin
5.	กำหนดค่า Time Quantum สำหรับ Round Robin ได้
6.	แสดงลำดับการทำงานของ Process ผ่าน Gantt Chart
7.	แสดงตารางรายละเอียดของแต่ละ Process
8.	คำนวณค่า Start Time (ST), Completion Time (CT), Turnaround Time (TAT) และ Waiting Time (WT)
9.	คำนวณค่าเฉลี่ย AVG WT และ AVG TAT
10.	สามารถเปลี่ยนอัลกอริทึมเพื่อเปรียบเทียบผลลัพธ์ได้

4.CPU Scheduling Algorithms
โปรแกรมรองรับอัลกอริทึมการจัดตาราง CPU จำนวน 3 รูปแบบ

4.1.FCFS (First-Come, First-Served)
เป็นอัลกอริทึมที่ให้ Process ทำงานตามลำดับการเข้ามา โดย Process ที่มาก่อนจะได้รับสิทธิ์ใช้ CPU ก่อน และทำงานจนเสร็จสิ้นก่อนส่งต่อให้ Process ถัดไป

4.2.SJF (Shortest Job First – Non-preemptive)
เป็นอัลกอริทึมที่เลือก Process ที่มี Burst Time น้อยที่สุดก่อน โดยเมื่อ Process เริ่มทำงานแล้วจะทำงานต่อเนื่องจนเสร็จสิ้น จึงจะเลือก Process ถัดไป

4.3.RR (Round Robin)
เป็นอัลกอริทึมที่แบ่งเวลาให้แต่ละ Process ทำงานตามช่วงเวลาที่กำหนด เรียกว่า Time Quantum หาก Process ยังทำงานไม่เสร็จ จะถูกนำกลับไปต่อท้ายคิวเพื่อรอทำงานในรอบถัดไป

5.Technologies Used เทคโนโลยีและเครื่องมือที่ใช้ในการพัฒนาโปรแกรม
Technology	Purpose
HTML	ใช้สร้างโครงสร้างหน้าเว็บไซต์
CSS	ใช้ตกแต่งและจัดรูปแบบหน้าจอโปรแกรม
JavaScript	ใช้พัฒนาการคำนวณและการทำงานของอัลกอริทึม
Web Browser	ใช้เปิดและทดสอบโปรแกรม
Visual Studio Code	ใช้เขียนและแก้ไข Source Code
GitLab / GitHub	ใช้จัดเก็บหรือจัดการ Source Code (หากมีการใช้งานจริง)

6.Project Structure โครงสร้างไฟล์ของโปรเจกต์
โครงสร้างไฟล์ของโปรเจกต์ CPU Scheduling Simulator แบ่งออกเป็น 2 ส่วนหลัก ได้แก่ Website และ Documentation ดังนี้

327F_Slurpee_CPU-Scheduling.zip
│
└── 327F_Slurpee_CPU-Scheduling/
   │
   ├── Documentation/
   │   ├── README.md
   │   ├── Manual_Calculation.pdf
   │   └── Test_Data.pdf
   │   └── Test_Results.pdf
   │
   └── Website/
       ├── index.html
       ├── scheduler.js
       └── style.css

รายละเอียดไฟล์
Documentation
README.md – เอกสารแนะนำโปรเจกต์และวิธีใช้งาน
Test_Data.pdf – เอกสารตัวอย่างข้อมูลสำหรับทดสอบโปรแกรม
Test_Results.pdf – เอกสารผลการทดสอบโปรแกรมอย่างน้อย 3 กรณี
Manual_Calculation.pdf – เอกสารการคำนวณและตรวจสอบผลลัพธ์ด้วยตนเอง
Website
index.html – ไฟล์หลักสำหรับแสดงหน้าเว็บไซต์และโครงสร้างของโปรแกรม
scheduler.js – ไฟล์ JavaScript สำหรับคำนวณและประมวลผลอัลกอริทึม CPU Scheduling
style.css – ไฟล์ CSS สำหรับตกแต่งหน้าตาและจัดรูปแบบเว็บไซต์
 
7. System Requirements
ความต้องการขั้นต่ำสำหรับการใช้งานโปรแกรม
•	Operating System: Windows 10 หรือ Windows 11
•	Web Browser: Microsoft Edge หรือ Google Chrome
•	Internet Connection: ไม่จำเป็นสำหรับการเปิดใช้งานไฟล์โปรแกรมในเครื่อง หากไม่มีการเรียกใช้ทรัพยากรภายนอก
•	Hardware: คอมพิวเตอร์หรือโน้ตบุ๊กที่สามารถใช้งาน Web Browser ได้

8. Installation and Execution
วิธีเปิดใช้งานโปรแกรมผ่านเครื่องคอมพิวเตอร์
1.	ดาวน์โหลดหรือแตกไฟล์ ZIP ของโปรเจกต์
2.	เปิดโฟลเดอร์ CPU-Scheduling
3.	ค้นหาไฟล์ index.html
4.	ดับเบิลคลิกไฟล์ index.html
5.	โปรแกรมจะเปิดขึ้นผ่าน Web Browser
6.	สามารถเริ่มใช้งานโปรแกรมได้ทันที
โปรแกรมเป็น Web Application ที่สามารถเปิดผ่าน Web Browser ได้ โดยไม่จำเป็นต้องติดตั้งโปรแกรมเพิ่มเติม หากไฟล์และทรัพยากรที่จำเป็นอยู่ครบถ้วน

9.How to Use ขั้นตอนการใช้งานโปรแกรม
1.	เปิดโปรแกรม CPU Scheduling Simulator
2.	กำหนดจำนวน Process ที่ต้องการทดสอบ กำหนดค่า Time Quantum
3.	กำหนด Burst Time ของแต่ละ Process หรือเลือกใช้การสุ่มข้อมูล
4.	ตรวจสอบข้อมูล Process ที่แสดงบนหน้าจอ
5.	กดปุ่ม Calculate เพื่อเริ่มคำนวณ
6.	เลือกอัลกอริทึมที่ต้องการดูผลลัพธ์ ได้แก่ FCFS, SJF หรือ Round Robin
7.	ตรวจสอบ Gantt Chart ที่แสดงลำดับการทำงานของ Process
8.	ตรวจสอบตาราง Process Details และค่าเฉลี่ย AVG WT และ AVG TAT
9.	สามารถเปลี่ยนอัลกอริทึมเพื่อเปรียบเทียบผลลัพธ์ได้


10. Calculation Formulas สูตรที่ใช้ในการคำนวณภายในโปรแกรม
Abbreviation	Full Name	Formula
AT	Arrival Time	เวลาที่ Process เข้ามา
BT	Burst Time	เวลาที่ Process ใช้ CPU
ST	Start Time	เวลาที่เริ่มทำงาน
CT	Completion Time	ST + เวลาทำงานที่เหลือจนเสร็จ
TAT	Turnaround Time	CT – AT
WT	Waiting Time	TAT - BT

สูตรค่าเฉลี่ย
Average Waiting Time
AVG WT = ผลรวมของ WT ของทุก Process / จำนวน Process
Average Turnaround Time
AVG TAT = ผลรวมของ TAT ของทุก Process / จำนวน Process
หมายเหตุ: สำหรับ Round Robin ค่า ST หมายถึงเวลาเริ่มทำงานครั้งแรกของ Process ส่วน CT คือเวลาที่ Process ทำงานเสร็จทั้งหมด

11. Testing Information
โปรแกรมได้รับการเตรียมทดสอบด้วยชุดข้อมูลทั้งหมด 3 กรณี ได้แก่
•	Test Case 1: ข้อมูลที่กำหนดค่า Burst Time ด้วยตนเอง จำนวน 3 Process
•	Test Case 2: ข้อมูลที่กำหนดค่า Burst Time ด้วยตนเอง จำนวน 5 Process
•	Test Case 3: ข้อมูลที่ได้จากการสุ่ม จำนวน 5 Process

การทดสอบครอบคลุมอัลกอริทึม FCFS, SJF และ Round Robin โดยกำหนด Arrival Time เท่ากับ 0 ทุก Process และกำหนด Time Quantum เท่ากับ 2 สำหรับ Round Robin

ผลการทดสอบประกอบด้วย Gantt Chart ตาราง Process Details ค่าเฉลี่ย Waiting Time และ Turnaround Time ซึ่งสามารถตรวจสอบรายละเอียดเพิ่มเติมได้จากเอกสาร Test Results และ Manual Calculation ที่แนบมาพร้อมโปรเจกต์

12. AI Usage
ในการพัฒนาโปรเจกต์ กลุ่มได้ใช้ AI เป็นเครื่องมือช่วยสนับสนุนการทำงานในบางส่วน เช่น
•	ช่วยวางแนวทางและโครงสร้างของโปรแกรม
•	ช่วยอธิบายหลักการทำงานของอัลกอริทึม CPU Scheduling
•	ช่วยตรวจสอบแนวคิดและสูตรการคำนวณ
•	ช่วยวิเคราะห์ปัญหาที่อาจเกิดขึ้นในการทำงานของโปรแกรม
•	ช่วยเสนอแนวทางในการทดสอบและตรวจสอบผลลัพธ์

เครื่องมือ AI ที่ใช้ ได้แก่ ChatGPT และ Claude
สมาชิกกลุ่มมีหน้าที่พัฒนาและปรับปรุงโปรแกรม ตรวจสอบความถูกต้องของผลลัพธ์ และทดสอบการทำงานของโปรแกรมด้วยตนเอง โดยใช้ AI เป็นเครื่องมือช่วยสนับสนุนการพัฒนา




13.Team Members รายชื่อสมาชิกในกลุ่ม
— ออกแบบและพัฒนาอัลกอริทึม FCFS, SJF และ Round Robin
1.นายสุรเชษฏ์ ลุยะพันธุ์ 1680707427 (327F)
— ออกแบบ User Interface และส่วนรับข้อมูลและแสดงผล
2.นายณัฐวิทย์ เกศดายุรัตน์ 1670703360 (327F)
3.นางสาววรรณิษา นุชพงษ์ 1660706977 (327C)
— ทดสอบความถูกต้องของผลลัพธ์ จัดทำ README และจัดเตรียมวิดีโอนำเสนอ
4.นางสาวกันต์ปันนี บุญเลิศสิริ 1670703097 (327F)
5.นายปกป้อง ยิ้มปรีดา 1670701174 (327E)
