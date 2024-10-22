---
title: เพิ่มปุ่มตัวเลือกลงในเวิร์กชีตใน Excel
linktitle: เพิ่มปุ่มตัวเลือกลงในเวิร์กชีตใน Excel
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีการเพิ่มปุ่มตัวเลือกลงในเวิร์กชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET ด้วยคู่มือทีละขั้นตอนง่ายๆ นี้ เหมาะอย่างยิ่งสำหรับการสร้างแบบฟอร์ม Excel แบบโต้ตอบ
type: docs
weight: 19
url: /th/net/excel-shapes-controls/add-radio-button-to-worksheet-excel/
---
## การแนะนำ
คุณเคยสงสัยไหมว่าจะเพิ่มสีสันให้กับแผ่นงาน Excel ของคุณด้วยองค์ประกอบแบบโต้ตอบ เช่น ปุ่มตัวเลือกได้อย่างไร ไม่ว่าคุณจะกำลังสร้างแบบสำรวจ แบบฟอร์ม หรือเครื่องมือวิเคราะห์ การเพิ่มปุ่มตัวเลือกสามารถปรับปรุงการโต้ตอบของผู้ใช้ได้อย่างแท้จริง ในบทช่วยสอนนี้ เราจะแนะนำคุณเกี่ยวกับกระบวนการเพิ่มปุ่มตัวเลือกลงในแผ่นงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET เราจะแบ่งทุกอย่างออกเป็นขั้นตอนที่ทำตามได้ง่าย รับรองว่าคุณจะเป็นมืออาชีพเมื่ออ่านบทความนี้จบ พร้อมเริ่มกันเลยหรือยัง มาเริ่มกันเลย!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเข้าสู่ขั้นตอนสนุกๆ ของการเพิ่มปุ่มตัวเลือก เราต้องตรวจสอบให้แน่ใจก่อนว่าคุณได้ตั้งค่าทุกอย่างเพื่อเริ่มต้นใช้งานแล้ว
1.  Aspose.Cells สำหรับ .NET: ก่อนอื่น ตรวจสอบให้แน่ใจว่าคุณได้ดาวน์โหลดและติดตั้งแล้ว[Aspose.Cells สำหรับ .NET](https://releases.aspose.com/cells/net/) ไลบรารี คุณสามารถดาวน์โหลดผ่าน NuGet ใน Visual Studio หรือจากหน้าดาวน์โหลด
2. IDE (Integrated Development Environment): คุณจะต้องมี IDE เช่น Visual Studio เพื่อเขียนและดำเนินการโค้ด C# ของคุณ
3. .NET Framework: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง .NET Framework 4.0 ขึ้นไปบนเครื่องของคุณแล้ว Aspose.Cells ต้องการให้สิ่งนี้ทำงานได้
4. ความเข้าใจพื้นฐานเกี่ยวกับ C#: ความคุ้นเคยกับรูปแบบ C# และการเขียนโปรแกรม .NET จะทำให้สิ่งต่าง ๆ ง่ายขึ้นเมื่อคุณทำตาม
เมื่อคุณเตรียมทุกอย่างลงตัวแล้ว เราก็พร้อมที่จะเริ่มงาน!
## แพ็คเกจนำเข้า
ก่อนที่จะทำการเข้ารหัส จำเป็นต้องนำเข้าเนมสเปซที่จำเป็นเพื่อหลีกเลี่ยงข้อผิดพลาดในภายหลัง เพิ่มสิ่งต่อไปนี้ลงในโค้ดของคุณ:
```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
using Aspose.Cells.Drawing;
```
การนำเข้าเหล่านี้มีความจำเป็นสำหรับการเข้าถึงฟังก์ชันการทำงานของเวิร์กบุ๊ก การเพิ่มปุ่มตัวเลือก และการจัดการการดำเนินการไฟล์
## ขั้นตอนที่ 1: การตั้งค่าเวิร์กบุ๊ก
ขั้นแรกเราต้องสร้างเวิร์กบุ๊ก Excel ใหม่ก่อน
 ในการเริ่มต้น คุณจะต้องสร้างอินสแตนซ์ใหม่`Workbook` วัตถุ นี่จะแสดงไฟล์ Excel ของคุณในโค้ด
```csharp
// สร้างเวิร์กบุ๊กใหม่
Workbook excelbook = new Workbook();
```
ในขั้นตอนนี้ คุณกำลังสร้างเวิร์กบุ๊กเปล่า ลองนึกภาพว่าเวิร์กบุ๊กเปล่าเป็นพื้นที่ที่คุณจะเพิ่มปุ่มตัวเลือกในขั้นตอนต่อไป
## ขั้นตอนที่ 2: การเพิ่มและจัดรูปแบบค่าเซลล์
ต่อไปเรามาเพิ่มชื่อเรื่องให้กับเวิร์กชีตกัน เราจะเพิ่มข้อความลงในเซลล์`C2` และจัดรูปแบบให้เป็นตัวหนา ขั้นตอนนี้จะเพิ่มบริบทให้กับปุ่มตัวเลือกของคุณ
### แทรกข้อความลงในเซลล์
```csharp
// แทรกค่าในเซลล์ C2
excelbook.Worksheets[0].Cells["C2"].PutValue("Age Groups");
```
### ทำให้ข้อความเป็นตัวหนา
```csharp
// ตั้งค่าข้อความแบบอักษรในเซลล์ C2 เป็นตัวหนา
excelbook.Worksheets[0].Cells["C2"].GetStyle().Font.IsBold = true;
```
 ที่นี่เราได้เพิ่มชื่อเรื่องง่ายๆ ว่า "กลุ่มอายุ" ในเซลล์`C2`และทำให้มันหนาเพื่อให้โดดเด่น ง่ายใช่ไหม?
## ขั้นตอนที่ 3: การเพิ่มปุ่มตัวเลือกแรก
ตอนนี้มาถึงส่วนที่น่าตื่นเต้น: การเพิ่มปุ่มตัวเลือกแรกของคุณลงในเวิร์กชีต!
### เพิ่มปุ่มตัวเลือก
```csharp
// เพิ่มปุ่มตัวเลือกลงในแผ่นงานแรก
Aspose.Cells.Drawing.RadioButton radio1 = excelbook.Worksheets[0].Shapes.AddRadioButton(3, 0, 2, 0, 30, 110);
```
บรรทัดนี้จะเพิ่มปุ่มตัวเลือกไปยังตำแหน่งเฉพาะบนเวิร์กชีตของคุณ ตัวเลขแสดงตำแหน่งและขนาดของปุ่ม ลองนึกถึงการตั้งค่าพิกัด X และ Y ของปุ่มดูสิ
### ตั้งค่าข้อความปุ่มตัวเลือก
```csharp
// ตั้งค่าสตริงข้อความของมัน
radio1.Text = "20-29";
```
ที่นี่ เราได้ใส่ป้ายชื่อให้กับปุ่มตัวเลือกว่า “20-29” ซึ่งแสดงถึงกลุ่มอายุ
### เชื่อมโยงปุ่มตัวเลือกกับเซลล์
```csharp
// ตั้งค่าเซลล์ A1 เป็นเซลล์ที่เชื่อมโยงสำหรับปุ่มตัวเลือก
radio1.LinkedCell = "A1";
```
 การเชื่อมโยงปุ่มตัวเลือกกับเซลล์`A1`หมายความว่าผลลัพธ์ของการเลือกปุ่มจะถูกเก็บไว้ในเซลล์นั้น
### เพิ่มเอฟเฟค 3D
```csharp
// ทำปุ่มตัวเลือกให้เป็นแบบ 3 มิติ
radio1.Shadow = true;
```
เนื่องจากเราต้องการให้ปุ่มตัวเลือกนี้ปรากฏขึ้น เราจึงเพิ่มเอฟเฟ็กต์ 3 มิติ
### ปรับแต่งเส้นของปุ่มตัวเลือก
```csharp
// ตั้งค่าน้ำหนักของบรรทัดปุ่มตัวเลือก
radio1.Line.Weight = 4;
// ตั้งค่ารูปแบบเส้นประของเส้นปุ่มตัวเลือก
radio1.Line.DashStyle = MsoLineDashStyle.Solid;
```
บรรทัดโค้ดเหล่านี้ปรับความหนาและรูปแบบของเส้นประของขอบปุ่มตัวเลือกเพื่อให้ดูสวยงามยิ่งขึ้น
## ขั้นตอนที่ 4: การเพิ่มปุ่มตัวเลือกเพิ่มเติม
เรามาเพิ่มปุ่มตัวเลือกอีกสองปุ่มสำหรับกลุ่มอายุที่เหลือ: "30-39" และ "40-49" ขั้นตอนจะเหมือนกัน เพียงแต่มีการเปลี่ยนแปลงเล็กน้อยในพิกัดและป้ายกำกับ
### เพิ่มปุ่มตัวเลือกที่สอง
```csharp
// เพิ่มปุ่มตัวเลือกอีกปุ่มหนึ่งในแผ่นงานแรก
Aspose.Cells.Drawing.RadioButton radio2 = excelbook.Worksheets[0].Shapes.AddRadioButton(6, 0, 2, 0, 30, 110);
// ตั้งค่าสตริงข้อความของมัน
radio2.Text = "30-39";
// ตั้งค่าเซลล์ A1 เป็นเซลล์ที่เชื่อมโยงสำหรับปุ่มตัวเลือก
radio2.LinkedCell = "A1";
// ทำปุ่มตัวเลือกให้เป็นแบบ 3 มิติ
radio2.Shadow = true;
// ตั้งค่าน้ำหนักของปุ่มวิทยุ
radio2.Line.Weight = 4;
// ตั้งค่ารูปแบบเส้นประของปุ่มตัวเลือก
radio2.Line.DashStyle = MsoLineDashStyle.Solid;
```
### เพิ่มปุ่มตัวเลือกที่สาม
```csharp
// เพิ่มปุ่มตัวเลือกอีกปุ่มหนึ่งในแผ่นงานแรก
Aspose.Cells.Drawing.RadioButton radio3 = excelbook.Worksheets[0].Shapes.AddRadioButton(9, 0, 2, 0, 30, 110);
// ตั้งค่าสตริงข้อความของมัน
radio3.Text = "40-49";
// ตั้งค่าเซลล์ A1 เป็นเซลล์ที่เชื่อมโยงสำหรับปุ่มตัวเลือก
radio3.LinkedCell = "A1";
// ทำปุ่มตัวเลือกให้เป็นแบบ 3 มิติ
radio3.Shadow = true;
// ตั้งค่าน้ำหนักของปุ่มวิทยุ
radio3.Line.Weight = 4;
// ตั้งค่ารูปแบบเส้นประของปุ่มตัวเลือก
radio3.Line.DashStyle = MsoLineDashStyle.Solid;
```
## ขั้นตอนที่ 5: การบันทึกไฟล์ Excel
เมื่อคุณเพิ่มและจัดรูปแบบปุ่มตัวเลือกทั้งหมดแล้ว ก็ถึงเวลาบันทึกไฟล์
```csharp
// บันทึกไฟล์ Excel
string dataDir = "Your Document Directory";
excelbook.Save(dataDir + "book1.out.xls");
```
ในขั้นตอนนี้ เวิร์กบุ๊กจะถูกบันทึกลงในไดเร็กทอรีที่คุณระบุ ง่ายๆ เพียงเท่านี้ เวิร์กชีตแบบโต้ตอบของคุณก็พร้อมใช้งานแล้ว!
## บทสรุป
เท่านี้คุณก็ทำสำเร็จแล้ว! คุณเพิ่งเพิ่มปุ่มตัวเลือกลงในเวิร์กชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET บทช่วยสอนนี้ครอบคลุมทุกอย่างตั้งแต่การตั้งค่าเวิร์กบุ๊ก การแทรกและจัดรูปแบบค่า การเพิ่มปุ่มตัวเลือกหลายปุ่ม และการลิงก์ปุ่มเหล่านี้ไปยังเซลล์ ตอนนี้ คุณพร้อมที่จะสร้างชีต Excel แบบโต้ตอบที่ไม่เพียงแต่ดูดีเท่านั้น แต่ยังมอบประสบการณ์การใช้งานที่ดียิ่งขึ้นอีกด้วย สนุกกับการสำรวจความเป็นไปได้เพิ่มเติมด้วย Aspose.Cells!
## คำถามที่พบบ่อย
### ฉันสามารถเพิ่มปุ่มตัวเลือกเพิ่มเติมลงในชีตต่างๆ ได้หรือไม่  
แน่นอน! คุณสามารถทำซ้ำขั้นตอนนี้บนแผ่นงานใดๆ ภายในเวิร์กบุ๊กได้โดยระบุดัชนีเวิร์กชีตที่ถูกต้อง
### ฉันสามารถปรับแต่งลักษณะของปุ่มตัวเลือกเพิ่มเติมได้หรือไม่  
ใช่ Aspose.Cells มีตัวเลือกการปรับแต่งมากมาย รวมถึงการเปลี่ยนสี ขนาด และแอตทริบิวต์การจัดรูปแบบอื่นๆ
### ฉันจะตรวจจับปุ่มตัวเลือกใดที่ถูกเลือกได้อย่างไร  
เซลล์ที่เชื่อมโยง (เช่น A1) จะแสดงดัชนีของปุ่มตัวเลือกที่เลือก คุณสามารถตรวจสอบค่าของเซลล์ที่เชื่อมโยงเพื่อดูว่ามีการเลือกเซลล์ใด
### จำนวนปุ่มตัวเลือกที่สามารถเพิ่มได้มีขีดจำกัดหรือไม่  
ไม่ ไม่มีการจำกัดจำนวนปุ่มตัวเลือกที่คุณสามารถเพิ่มได้ อย่างไรก็ตาม การทำให้ส่วนต่อประสานเป็นมิตรต่อผู้ใช้ก็เป็นสิ่งที่ดี
### ฉันสามารถใช้ Aspose.Cells กับภาษาการเขียนโปรแกรมอื่นได้หรือไม่  
ใช่ Aspose.Cells รองรับภาษาการเขียนโปรแกรมหลายภาษา รวมถึง Java แต่บทช่วยสอนนี้มุ่งเน้นเฉพาะที่ .NET โดยเฉพาะ