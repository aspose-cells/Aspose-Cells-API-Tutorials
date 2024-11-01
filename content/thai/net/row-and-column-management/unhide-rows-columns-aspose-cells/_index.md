---
title: ยกเลิกการซ่อนแถวและคอลัมน์ใน Aspose.Cells .NET
linktitle: ยกเลิกการซ่อนแถวและคอลัมน์ใน Aspose.Cells .NET
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีแสดงแถวและคอลัมน์ใน Excel โดยใช้ Aspose.Cells สำหรับ .NET พร้อมคำแนะนำทีละขั้นตอนของเรา เหมาะอย่างยิ่งสำหรับการจัดการข้อมูล
type: docs
weight: 18
url: /th/net/row-and-column-management/unhide-rows-columns-aspose-cells/
---
## การแนะนำ
เมื่อทำงานกับไฟล์ Excel ด้วยโปรแกรม คุณอาจพบสถานการณ์ที่แถวหรือคอลัมน์บางแถวถูกซ่อนไว้ ซึ่งอาจเกิดจากตัวเลือกการจัดรูปแบบ การจัดระเบียบข้อมูล หรือเพียงเพื่อเพิ่มความสวยงามให้กับภาพ ในบทช่วยสอนนี้ เราจะมาสำรวจวิธีแสดงแถวและคอลัมน์ในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET คู่มือฉบับสมบูรณ์นี้จะแนะนำคุณตลอดกระบวนการ เพื่อให้คุณสามารถนำแนวคิดเหล่านี้ไปใช้ในโครงการของคุณเองได้อย่างมั่นใจ มาเริ่มกันเลย!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม โปรดตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:
1.  Aspose.Cells สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Cells แล้ว คุณสามารถรับได้จาก[เว็บไซต์อาโพส](https://releases.aspose.com/cells/net/).
2. Visual Studio: สภาพแวดล้อมการพัฒนาการทำงานที่คุณสามารถสร้างโปรเจ็กต์ C# ใหม่ได้
3. ความรู้พื้นฐานเกี่ยวกับ C#: ความคุ้นเคยกับแนวคิดการเขียนโปรแกรม C# จะเป็นประโยชน์ แต่ไม่ต้องกังวลหากคุณเป็นมือใหม่ เราจะอธิบายทุกอย่างในแง่ที่ง่าย
## แพ็คเกจนำเข้า
หากต้องการใช้ Aspose.Cells ในโปรเจ็กต์ของคุณ คุณจะต้องนำเข้าแพ็กเกจที่จำเป็น โดยคุณสามารถทำได้ดังนี้:
### สร้างโครงการใหม่
1. เปิด Visual Studio และสร้างโปรเจ็กต์ C# ใหม่
2. เลือกประเภทโครงการ (เช่น แอปพลิเคชันคอนโซล) และคลิกสร้าง
### เพิ่มการอ้างอิง Aspose.Cells
1. คลิกขวาที่โฟลเดอร์การอ้างอิงในโครงการของคุณ
2. เลือกจัดการแพ็คเกจ NuGet
3. ค้นหา Aspose.Cells และติดตั้ง ขั้นตอนนี้จะช่วยให้คุณใช้ประโยชน์จากฟังก์ชันที่ไลบรารี Aspose.Cells จัดเตรียมไว้ให้ได้
### นำเข้าเนมสเปซที่จำเป็น
ที่ด้านบนของไฟล์ C# ของคุณ เพิ่มคำสั่ง using ต่อไปนี้เพื่อนำเข้าเนมสเปซ Aspose.Cells:
```csharp
using System.IO;
using Aspose.Cells;
```
ตอนนี้เราได้ตั้งค่าสภาพแวดล้อมเรียบร้อยแล้ว มาดูคำแนะนำทีละขั้นตอนในการยกเลิกการซ่อนแถวและคอลัมน์ในไฟล์ Excel กัน
## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ
ก่อนที่คุณจะเริ่มทำงานกับไฟล์ Excel คุณต้องระบุเส้นทางไปยังไดเร็กทอรีที่เก็บเอกสารของคุณ นี่คือที่ที่คุณจะอ่านไฟล์ Excel และบันทึกเวอร์ชันที่แก้ไข วิธีตั้งค่ามีดังนี้:
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
```
 เคล็ดลับ: เปลี่ยน`"Your Document Directory"` ด้วยเส้นทางจริงที่ไฟล์ Excel ของคุณตั้งอยู่ ตัวอย่างเช่น`C:\Documents\`.
## ขั้นตอนที่ 2: สร้างสตรีมไฟล์
ขั้นต่อไป คุณจะสร้างสตรีมไฟล์เพื่อเข้าถึงไฟล์ Excel ของคุณ ซึ่งจะช่วยให้คุณสามารถเปิดและจัดการไฟล์ผ่านโปรแกรมได้
```csharp
// การสร้างสตรีมไฟล์ที่มีไฟล์ Excel ที่จะเปิด
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```
 ในขั้นตอนนี้ให้แทนที่`"book1.xls"` ด้วยชื่อไฟล์ Excel ของคุณ ซึ่งจะทำให้แอปพลิเคชันสามารถอ่านข้อมูลที่มีอยู่ในไฟล์นั้นได้
## ขั้นตอนที่ 3: สร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
 ตอนนี้ถึงเวลาสร้าง`Workbook` วัตถุที่จะแสดงไฟล์ Excel ของคุณในหน่วยความจำ ซึ่งถือเป็นสิ่งสำคัญสำหรับการดำเนินการใดๆ กับไฟล์
```csharp
// การสร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
// การเปิดไฟล์ Excel ผ่านทางสตรีมไฟล์
Workbook workbook = new Workbook(fstream);
```
 การ`Workbook` วัตถุเป็นเกตเวย์ของคุณสู่เนื้อหาของไฟล์ Excel ทำให้คุณปรับเปลี่ยนได้ตามต้องการ
## ขั้นตอนที่ 4: เข้าถึงแผ่นงาน
 เมื่อคุณมี`Workbook` วัตถุ คุณต้องเข้าถึงเวิร์กชีตเฉพาะที่คุณต้องการแก้ไข ในตัวอย่างนี้ เราจะทำงานกับเวิร์กชีตแรกในเวิร์กบุ๊ก
```csharp
// การเข้าถึงเวิร์กชีตแรกในไฟล์ Excel
Worksheet worksheet = workbook.Worksheets[0];
```
 ดัชนี`[0]`หมายถึงเวิร์กชีตแรก หากคุณต้องการเข้าถึงเวิร์กชีตอื่น เพียงเปลี่ยนดัชนีให้เหมาะสม
## ขั้นตอนที่ 5: ยกเลิกการซ่อนแถว
เมื่อเข้าถึงเวิร์กชีตได้แล้ว ตอนนี้คุณก็สามารถยกเลิกการซ่อนแถวที่ซ่อนไว้ได้แล้ว ต่อไปนี้เป็นวิธียกเลิกการซ่อนแถวที่สามและกำหนดความสูง:
```csharp
// การยกเลิกการซ่อนแถวที่ 3 และตั้งค่าความสูงเป็น 13.5
worksheet.Cells.UnhideRow(2, 13.5);
```
 ในโค้ดด้านบน`2` หมายถึงดัชนีของแถว (จำไว้ว่าเป็นฐานศูนย์) และ`13.5` กำหนดความสูงของแถวนั้น ปรับค่าเหล่านี้ตามความจำเป็นสำหรับกรณีเฉพาะของคุณ
## ขั้นตอนที่ 6: ยกเลิกการซ่อนคอลัมน์
ในทำนองเดียวกัน หากคุณต้องการยกเลิกการซ่อนคอลัมน์ คุณสามารถทำได้โดยทำตามวิธีนี้ ต่อไปนี้เป็นวิธียกเลิกการซ่อนคอลัมน์ที่สองและกำหนดความกว้าง:
```csharp
// การยกเลิกการซ่อนคอลัมน์ที่ 2 และตั้งค่าความกว้างเป็น 8.5
worksheet.Cells.UnhideColumn(1, 8.5);
```
 อีกครั้ง,`1` เป็นดัชนีฐานศูนย์สำหรับคอลัมน์และ`8.5` กำหนดความกว้างของคอลัมน์นั้น ปรับเปลี่ยนพารามิเตอร์เหล่านี้ตามความต้องการของคุณ
## ขั้นตอนที่ 7: บันทึกไฟล์ Excel ที่ปรับเปลี่ยนแล้ว
หลังจากทำการเปลี่ยนแปลงที่จำเป็นแล้ว คุณต้องบันทึกไฟล์ Excel ที่แก้ไขแล้ว วิธีนี้จะช่วยให้การยกเลิกการซ่อนแถวและคอลัมน์มีผล
```csharp
// การบันทึกไฟล์ Excel ที่แก้ไขแล้ว
workbook.Save(dataDir + "output.xls");
```
 ที่นี่,`output.xls` คือชื่อไฟล์ที่คุณต้องการบันทึกเนื้อหาที่แก้ไข คุณสามารถเลือกชื่อใดก็ได้ตามต้องการ แต่ต้องแน่ใจว่ามี`.xls` ส่วนขยาย.
## ขั้นตอนที่ 8: ปิดสตรีมไฟล์
สุดท้ายนี้ สิ่งสำคัญคือการปิดสตรีมไฟล์เพื่อปลดปล่อยทรัพยากรระบบ ซึ่งจะช่วยป้องกันการรั่วไหลของหน่วยความจำหรือการล็อกไฟล์ที่อาจเกิดขึ้นได้
```csharp
// การปิดสตรีมไฟล์เพื่อปลดปล่อยทรัพยากรทั้งหมด
fstream.Close();
```
เพียงเท่านี้ คุณก็ยกเลิกการซ่อนแถวและคอลัมน์ในไฟล์ Excel ได้สำเร็จแล้วโดยใช้ Aspose.Cells สำหรับ .NET
## บทสรุป
ในบทช่วยสอนนี้ เราได้อธิบายขั้นตอนในการยกเลิกการซ่อนแถวและคอลัมน์ในไฟล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET ไลบรารีนี้ทำให้การจัดการเอกสาร Excel ด้วยโปรแกรมเป็นเรื่องง่ายอย่างเหลือเชื่อ ช่วยเพิ่มความสามารถในการจัดการข้อมูลอย่างมีประสิทธิภาพ ไม่ว่าคุณจะกำลังอัปเดตสเปรดชีตสำหรับรายงานหรือรักษาความสมบูรณ์ของข้อมูล การทราบวิธีการยกเลิกการซ่อนแถวและคอลัมน์ก็มีประโยชน์อย่างยิ่ง
## คำถามที่พบบ่อย
### ฉันสามารถยกเลิกการซ่อนแถวและคอลัมน์หลายรายการพร้อมกันได้ไหม  
ใช่ คุณสามารถยกเลิกการซ่อนแถวและคอลัมน์หลายรายการได้โดยการวนซ้ำผ่านดัชนีและใช้`UnhideRow` และ`UnhideColumn` วิธีการตามนั้น.
### Aspose.Cells รองรับรูปแบบไฟล์อะไรบ้าง?  
Aspose.Cells รองรับรูปแบบต่างๆ เช่น XLS, XLSX, CSV และอื่นๆ อีกมากมาย คุณสามารถอ่านและเขียนรูปแบบเหล่านี้ได้อย่างราบรื่น
### มีรุ่นทดลองใช้งานฟรีสำหรับ Aspose.Cells หรือไม่  
 แน่นอน! คุณสามารถดาวน์โหลดเวอร์ชันทดลองใช้งานฟรีได้จาก[เว็บไซต์อาโพส](https://releases.aspose.com/).
### ฉันจะตั้งค่าความสูงที่แตกต่างกันสำหรับหลายแถวได้อย่างไร  
คุณสามารถยกเลิกการซ่อนแถวหลายแถวในลูปได้ โดยระบุความสูงที่แตกต่างกันตามต้องการ เพียงจำไว้ว่าต้องปรับดัชนีแถวในลูปของคุณ
### ฉันควรทำอย่างไรหากพบข้อผิดพลาดขณะทำงานกับไฟล์ Excel?  
หากคุณประสบปัญหา โปรดตรวจสอบข้อความแสดงข้อผิดพลาดเพื่อหาเบาะแส นอกจากนี้ คุณยังสามารถขอความช่วยเหลือจากฟอรัมสนับสนุน Aspose เพื่อแก้ไขปัญหาได้อีกด้วย